# The Complete GCC & C Compilation Handbook
### For 1337 / 42 Network Piscine Preparation

This handbook covers every stage of turning C source code into a running program: the compilation pipeline, GCC itself, every flag category you'll actually use, multi-file projects, libraries, Makefiles, and how to debug when things break. Each section ends with a short drill so you can check you actually absorbed it, not just read it.

---

## Table of Contents

1. What Happens When You Compile C
2. Installing & Checking Your Toolchain
3. GCC Basics — `gcc`, `cc`, `-o`, `-c`
4. The Preprocessor — `#include`, `#define`, Macros
5. Warning Flags — `-Wall`, `-Wextra`, `-Werror`
6. C Language Standards — `-std=`
7. Debugging — `-g`, `gdb`, `valgrind`, sanitizers
8. Optimization Flags — `-O0` to `-O3`, `-Og`, `-Os`
9. Multi-File Projects & the Linker
10. Header Files & Include Guards
11. Libraries — `-I`, `-L`, `-l`, static vs. shared, building `libft.a`
12. Storage Classes — `static`, `extern`, `const`
13. Build Automation with `make`
14. Reading Compiler & Linker Errors
15. The Norm & 1337-Specific Habits
16. Full Quick-Reference Cheat Sheet

---

## 1. What Happens When You Compile C

A computer's CPU only executes machine code — raw binary instructions. C source code is human-readable text. GCC's job is translating one into the other, in four distinct stages:

```
file.c
   │
   ▼
┌─────────────────┐
│  Preprocessor    │   expands #include, #define, macros, strips comments
└─────────────────┘
   │  → file.i (expanded C source)
   ▼
┌─────────────────┐
│  Compiler proper │   translates C → assembly language
└─────────────────┘
   │  → file.s (assembly)
   ▼
┌─────────────────┐
│  Assembler       │   translates assembly → machine code
└─────────────────┘
   │  → file.o (object file)
   ▼
┌─────────────────┐
│  Linker          │   resolves symbols, merges object files + libraries
└─────────────────┘
   │
   ▼
executable (a.out / program)
```

Running `gcc file.c` does all four stages silently and deletes the intermediate files. You can stop at any stage to inspect what's happening:

```bash
gcc -E file.c -o file.i     # stop after preprocessing — see expanded source
gcc -S file.c -o file.s     # stop after compiling — see generated assembly
gcc -c file.c -o file.o     # stop after assembling — object file, not linked
gcc file.o -o program       # linking only
```

**Critical distinction:** the compiler *translates*, it never *executes*. Your program only runs when the operating system loads the finished executable into RAM and hands control to the CPU. A `.c` file, a `.i` file, a `.s` file, and a `.o` file are all non-executable — only the final linked output can run.

### Drill
Take any C file and run all four commands above in order. Open `file.i` in a text editor — find where your `#include <stdio.h>` line went. It should be replaced by hundreds of lines of declarations pulled straight from the header.

---

## 2. Installing & Checking Your Toolchain

On the Piscine machines this is already set up, but know how to verify it:

```bash
gcc --version      # confirm GCC is installed and which version
which gcc           # confirm which binary is being called
man gcc             # full manual — genuinely useful when a flag confuses you
```

---

## 3. GCC Basics

### `gcc` vs `cc`

```bash
gcc file.c -o program
cc  file.c -o program
```

`gcc` is a specific compiler. `cc` is a symlink to whatever the system's *default* C compiler is — on most Linux systems that's GCC, but it isn't guaranteed (macOS points `cc` to Clang). Many school Makefiles write `CC = cc` for portability. If your Norm/evaluation explicitly requires GCC, don't rely on `cc` unless you've confirmed what it resolves to.

### `-o <name>` — name the output

```bash
gcc file.c -o hello
```

Without `-o`, GCC names the executable `a.out` by default — a historical name from early Unix ("assembler output") that stuck.

### `-c` — compile only, don't link

```bash
gcc -c file.c -o file.o
```

Produces an object file. Doesn't produce anything runnable. This is the building block for multi-file projects (Section 9).

### Compiling multiple files in one shot

```bash
gcc main.c utils.c math.c -o program
```

This compiles all three, then links them, in one command. Fine for small projects; doesn't scale once you have dozens of files, because every file gets recompiled every time even if only one changed — this is exactly the problem `make` solves (Section 13).

### Drill
Write a two-line "hello world" `.c` file. Compile it three different ways: no flags, with `-o`, with `-c`. Run `ls` after each and confirm you understand what file was produced and whether it's runnable.

---

## 4. The Preprocessor

Before any real compilation happens, the preprocessor does pure text substitution.

### `#include`

```c
#include <stdio.h>   // angle brackets: search system include paths only
#include "myheader.h" // quotes: search current directory first, then system paths
```

### `#define` — macros

```c
#define MAX_SIZE 100
#define SQUARE(x) ((x) * (x))
```

Macros are textual substitution, not function calls — no type checking, no scoping. `SQUARE(x)` expanding to `((x) * (x))`, with parentheses around `x` and the whole expression, isn't decoration — omit them and `SQUARE(a + b)` expands to `a + b * a + b`, which is wrong. This is a classic C bug and a classic Piscine gotcha.

### Conditional compilation

```c
#ifndef MATH_H
# define MATH_H
// ... declarations
#endif
```

This pattern (an "include guard") is covered fully in Section 10 — it's what stops a header from being processed twice in the same file.

### Drill
Write `#define BAD_SQUARE(x) x * x` and call it as `BAD_SQUARE(1 + 2)`. Predict the output before compiling, then check with `gcc -E`.

---

## 5. Warning Flags

| Flag | Meaning |
|---|---|
| `-Wall` | Enables the commonly-used set of warnings. **Not literally "all" warnings** despite the name — this is the single most common misunderstanding of this flag. It catches things like unused variables, implicit function declarations, mismatched `printf` format specifiers. |
| `-Wextra` | Enables additional warnings not covered by `-Wall`: unused function parameters, signed/unsigned comparisons, missing struct field initializers. |
| `-Werror` | Turns every enabled warning into a hard compilation error. If any warning fires, no executable is produced. |

The near-universal 1337/42 compile line:

```bash
gcc -Wall -Wextra -Werror main.c -o main
```

A program that compiles cleanly *without* these flags can still be full of real bugs `-Wall`/`-Wextra` would have caught — always compile with them on, even outside of graded submissions.

### Drill
Write a function with an unused parameter and a variable declared but never used. Compile with no flags (clean), then with `-Wall -Wextra` (warnings appear), then with `-Wall -Wextra -Werror` (compilation fails). Confirm you understand why each stage behaves differently.

---

## 6. C Language Standards

```bash
gcc -std=c99 file.c -o program
```

| Standard | Year | What it changed |
|---|---|---|
| `c89`/`c90` | 1989 | Original ANSI C. No `//` comments, variables must be declared at the top of a block, no `long long`. |
| `c99` | 1999 | `//` comments, variable declarations anywhere in a block, `long long`, `stdbool.h`, variable-length arrays. **This is what 1337/42 requires by default — check your Norm.** |
| `c11` | 2011 | Anonymous structs/unions, `_Static_assert`, threading support. |
| `c17` | 2018 | Bugfix-only revision of C11. No new features. |
| `c23` | 2024 | Newest — adds `nullptr`, `constexpr`, native `bool` without `stdbool.h`. Not Piscine-relevant, but you'll see it referenced elsewhere. |

If a Norm document specifies a standard, use exactly that one for graded work — a program that only compiles under a newer standard than required will fail the grader even if the code itself is fine.

### Drill
Write a `for` loop that declares its counter inline (`for (int i = 0; ...)`). Compile with `-std=c89` and read the error. Recompile with `-std=c99` and confirm it now works.

---

## 7. Debugging

### `-g` — embed debug information

```bash
gcc -g file.c -o file
```

Adds symbol tables and source-line mappings to the binary so a debugger can show you real variable names and line numbers instead of raw memory addresses. Doesn't affect runtime behavior; increases binary size somewhat.

### `gdb` — interactive debugger

```bash
gdb ./program
```

| Command | Effect |
|---|---|
| `run` / `r` | Start execution |
| `break <loc>` / `b` | Set a breakpoint at a line or function |
| `next` / `n` | Execute the next line, stepping *over* function calls |
| `step` / `s` | Execute the next line, stepping *into* function calls |
| `continue` / `c` | Resume until the next breakpoint or crash |
| `print <var>` / `p` | Show a variable's current value |
| `backtrace` / `bt` | Show the full call stack — **the first thing to run after any crash** |
| `quit` / `q` | Exit |

Requires `-g` to be genuinely useful — otherwise you'll be reading raw addresses.

### `valgrind` — memory error detector

```bash
valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./program
```

Detects: memory leaks, use-after-free, double-free, invalid free, reading uninitialized memory, out-of-bounds heap access. Nearly every Piscine C project is graded partly on producing zero Valgrind errors — a program with correct output can still fail if it leaks.

Valgrind does **not** reliably catch stack buffer overflows or all undefined behavior. For that:

### AddressSanitizer — `-fsanitize=address`

```bash
gcc -Wall -Wextra -g -fsanitize=address file.c -o file
./file
```

Catches stack and heap overflows, use-after-free, and more, with much more readable error output than Valgrind — at the cost of a slower binary and needing a recompile (Valgrind works on any existing binary, no recompile required). Good for local development; confirm whether your evaluation environment allows extra flags before relying on it for graded runs.

### Drill
Deliberately write a program that calls `malloc` and never `free`s it. Run it under Valgrind and read the leak report line by line until you understand every field it reports (bytes leaked, where the allocation happened).

---

## 8. Optimization Flags

| Flag | Behavior |
|---|---|
| `-O0` | No optimization. Default. Best for debugging — code maps predictably to source. |
| `-O1` | Light optimization, fast compile time. |
| `-O2` | Standard "production" optimization level. |
| `-O3` | Maximum optimization, aggressive inlining/vectorization — not always actually faster; can bloat binaries. Benchmark, don't assume. |
| `-Og` | Optimizes without breaking debuggability — the right choice if you want some optimization while still using GDB. |
| `-Os` | Optimizes for smallest binary size rather than speed. |

You will almost never touch these during the Piscine — correctness and Norm compliance are graded, not runtime speed.

---

## 9. Multi-File Projects & the Linker

### Object files

```bash
gcc -c main.c    # → main.o
gcc -c utils.c   # → utils.o
```

Each object file contains machine code plus a symbol table: a list of what it *defines* (functions/globals available to others) and what it *needs* (functions/globals used but defined elsewhere).

### Linking

```bash
gcc main.o utils.o -o program
```

The linker walks every object file, matches every "needs X" against some file's "defines X," and merges everything into one executable. If a needed symbol is never found anywhere, you get:

```
undefined reference to `function_name'
```

This is a **linker** error, distinct from a compiler error — the code compiled fine syntactically, the linker just couldn't find where the symbol lives (forgot to link that `.o`, forgot a library, or typo'd the function name).

### Drill
Split a two-function program into two `.c` files where `main.c` calls a function defined in `utils.c`. Compile `main.c` alone with `gcc -c main.c -o program` (skip linking `utils.o`) and read the "undefined reference" error. Then fix it by linking both object files.

---

## 10. Header Files & Include Guards

A header declares what a source file provides, so other files can use it without seeing the implementation:

```c
// math_utils.h
#ifndef MATH_UTILS_H
# define MATH_UTILS_H

int add(int a, int b);
int subtract(int a, int b);

#endif
```

```c
// math_utils.c
#include "math_utils.h"

int add(int a, int b) { return a + b; }
int subtract(int a, int b) { return a - b; }
```

```c
// main.c
#include "math_utils.h"
#include <stdio.h>

int main(void)
{
    printf("%d\n", add(2, 3));
    return 0;
}
```

### Why the include guard matters

If `math_utils.h` is `#include`d from two different `.c` files that both get compiled into the same program, without the guard the declarations get processed twice within a build, which can trigger "redefinition" errors — especially painful in larger multi-file projects where headers include other headers. `#ifndef`/`#define`/`#endif` makes the second inclusion within the same compilation a no-op. The alternative, `#pragma once`, does the same thing but isn't part of the official C standard (though virtually every compiler supports it) — the Piscine convention is the portable `#ifndef` guard.

### Drill
Remove the include guard from a header and `#include` it twice in the same `.c` file (directly, not through separate files). Compile and read the redefinition error. Put the guard back and confirm it compiles clean.

---

## 11. Libraries — `-I`, `-L`, `-l`

### `-I` — extra include search path

```bash
gcc -Iinclude main.c -o program
```

Tells the *preprocessor* where else to look for headers included with `"quotes"`. Needed when headers live in a subdirectory like `include/`.

### `-L` — extra library search path

```bash
gcc main.o -L. -lft -o program
```

Tells the *linker* an extra directory to search for library files.

### `-l<name>` — link a specific library

```bash
gcc main.o -lm -o program     # links libm (the math library) — needed for sqrt(), pow(), etc.
gcc main.o -L. -lft -o program # links ./libft.a
```

`-l<name>` makes the linker search for `lib<name>.a` (static) or `lib<name>.so` (shared). `-lm` → `libm`, `-lft` → `libft`.

### Order matters

GCC's linker resolves symbols left to right in a single pass. Put libraries *after* the object files that depend on them:

```bash
gcc main.o -L. -lft -o program     # correct
gcc -lft main.o -L. -o program     # can fail with undefined reference
```

### Static vs. shared libraries

| | Static (`.a`) | Shared (`.so`) |
|---|---|---|
| When linked | Compile time — copied fully into the executable | Runtime — loaded from disk when the program starts |
| Executable size | Larger | Smaller |
| Portability | Self-contained, no runtime dependency | Needs the `.so` present on whatever machine runs it |
| Updating | Requires recompiling your program | Swap the `.so` file, program picks it up automatically |
| Piscine relevance | **This is what you'll build** — `libft.a` | Rare in Piscine-scale projects |

### Building `libft.a`

```bash
gcc -Wall -Wextra -Werror -c ft_strlen.c ft_strcpy.c ft_atoi.c
ar rcs libft.a ft_strlen.o ft_strcpy.o ft_atoi.o
```

`ar` flags: `r` = insert/replace files in the archive, `c` = create the archive if it doesn't already exist, `s` = write a symbol index into the archive so the linker can find symbols fast (equivalent to running `ranlib` separately).

```bash
gcc main.c -L. -lft -o program
```

### Drill
Write two tiny functions, compile them to `.o` files, archive them into `libtest.a` with `ar`, then link a `main.c` against it using `-L.` and `-ltest`. Confirm it runs.

---

## 12. Storage Classes — `static`, `extern`, `const`

These matter enormously once you go multi-file, and are usually glossed over.

### `static` on a function/global

```c
static int helper(int x) { return x * 2; }
```

Restricts visibility to the current `.c` file only — other files can't call it even with a matching prototype in a shared header. Useful for internal helper functions you don't want to leak into your library's public interface, and it avoids `-lname`-linking "multiple definition" clashes if two files happen to define same-named helpers.

### `extern`

```c
// in a header
extern int global_counter;

// in exactly one .c file
int global_counter = 0;
```

Declares that a global variable exists somewhere else, without defining storage for it here. Putting the actual definition (`int global_counter = 0;`) directly in a header that's included by multiple `.c` files causes a "multiple definition" linker error — one file must define it, others just declare it `extern`.

### `const`

```c
const int MAX_USERS = 100;
```

Read-only after initialization. Attempting to modify it is a compile error, not just a style suggestion.

### Drill
Put `int global = 0;` (without `extern`) directly in a header, include that header from two `.c` files, and link them together. Read the "multiple definition" error. Fix it using the `extern`-in-header / definition-in-one-`.c` pattern.

---

## 13. Build Automation with `make`

### The problem it solves

Recompiling every file by hand on every change doesn't scale. `make` reads a file named `Makefile` and rebuilds only what's stale, based on file modification timestamps.

### Rule syntax

```makefile
target: prerequisites
	command
```

**The command line must begin with an actual TAB character, not spaces.** This is the single most common Makefile failure (`Makefile:2: *** missing separator. Stop.`) — invisible in most editors, so if you hit that error, check for stray spaces.

### Minimal working example

```makefile
program: main.o utils.o
	gcc main.o utils.o -o program

main.o: main.c
	gcc -c main.c

utils.o: utils.c
	gcc -c utils.c
```

Running `make` builds the first target listed (`program` here). It checks whether `program` is older than either `.o`, and whether each `.o` is older than its `.c` — rebuilding only what's actually stale.

### Variables and pattern rules — a real project Makefile

```makefile
NAME    = program
CC      = gcc
CFLAGS  = -Wall -Wextra -Werror
SRC     = main.c utils.c math.c
OBJ     = $(SRC:.c=.o)

all: $(NAME)

$(NAME): $(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(NAME)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ)

fclean: clean
	rm -f $(NAME)

re: fclean all

.PHONY: all clean fclean re
```

### Automatic variables

| Variable | Meaning |
|---|---|
| `$@` | The current target's name |
| `$<` | The first prerequisite |
| `$^` | All prerequisites, space-separated |

### The `%.o: %.c` pattern rule

Reads as "to build any `X.o`, find `X.c` and run this command" — one rule replaces writing a separate recipe per source file.

### `$(SRC:.c=.o)`

A substitution reference: takes the `SRC` list and swaps every `.c` suffix for `.o`, generating the object list automatically instead of typing it twice.

### The standard target set (1337/42 convention)

| Target | Job |
|---|---|
| `all` | Default build target |
| `clean` | Delete object files only |
| `fclean` | `clean` + delete the final executable |
| `re` | `fclean` then rebuild everything |
| `.PHONY` | Declares these aren't real filenames — without it, if a file literally named `clean` ever exists in the folder, `make clean` sees it as "already up to date" and silently does nothing |

```bash
make          # build
make clean    # remove .o files
make fclean   # remove .o files + binary
make re       # full rebuild
```

### Why the grader cares

Moulinette/graders clone your repo fresh and run your Makefile cold. Common failure points: missing `.PHONY` (silent no-ops on `re`/`clean`), hardcoded absolute paths, a Makefile that isn't idempotent (running `make` twice back to back should do nothing the second time, not rebuild), or `all` not being the first/default target.

### Drill
Build the example Makefile above with 3 tiny source files. Run `make`, then `make` again immediately — confirm the second run does nothing (`make: 'program' is up to date`). Touch one `.c` file (`touch main.c`) and run `make` again — confirm only that one file recompiles.

---

## 14. Reading Compiler & Linker Errors

| Message | What it actually means |
|---|---|
| `undefined reference to 'X'` | Linker error: `X` is called/used somewhere but its definition was never linked in — missing `.o`, missing library, or typo'd name. |
| `implicit declaration of function 'X'` | You called a function before its prototype was visible — missing `#include` or missing header declaration. Warning under `-Wall`, fatal under `-Werror`. |
| `multiple definition of 'X'` | The same non-`static` symbol is fully defined in more than one file, or a variable (not just `extern` declaration) sits in a header included by multiple `.c` files. |
| `redefinition of 'X'` | Missing or broken include guard — a header got processed twice in the same translation unit. |
| `Makefile:N: *** missing separator. Stop.` | A recipe line uses spaces instead of a tab. |
| `Segmentation fault (core dumped)` | The program accessed memory it doesn't own — null dereference, buffer overrun, use-after-free, or stack overflow from runaway recursion. Get a `backtrace` in `gdb` or check with Valgrind. |

---

## 15. The Norm & 1337-Specific Habits

Beyond compilation mechanics, a few habits the grading process specifically rewards:

- **Compile with `-Wall -Wextra -Werror` from day one**, not just before submitting — catching warnings early is much cheaper than debugging them later.
- **Run Valgrind after every function you finish**, not just at the end of a project — it's far easier to localize a leak to the function you just wrote than to hunt through the whole codebase later.
- **Keep your Makefile idempotent and correct with `.PHONY`** — a broken Makefile can zero out an otherwise-correct project during evaluation.
- **Match the required `-std=` exactly** if your Norm specifies one — don't assume "newer is safer."
- **Don't define global mutable state carelessly** — `static`/`extern` discipline (Section 12) avoids a category of linker errors that otherwise eat evaluation time.

---

## 16. Full Quick-Reference Cheat Sheet

```bash
# Standard compile line
gcc -Wall -Wextra -Werror -std=c99 file.c -o program

# Inspect each pipeline stage
gcc -E file.c -o file.i    # preprocessed source
gcc -S file.c -o file.s    # assembly
gcc -c file.c -o file.o    # object file (no link)

# Multi-file build
gcc -c main.c utils.c
gcc main.o utils.o -o program

# With a static library
gcc main.c -Iinclude -L. -lft -o program

# Build a static library
gcc -Wall -Wextra -Werror -c a.c b.c c.c
ar rcs libname.a a.o b.o c.o

# Debug build
gcc -Wall -Wextra -Werror -g -fsanitize=address file.c -o file

# Memory check
valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./program

# Step debugger
gdb ./program
  run / break <loc> / next / step / continue / print <var> / backtrace / quit
```

```makefile
NAME    = program
CC      = gcc
CFLAGS  = -Wall -Wextra -Werror
SRC     = main.c utils.c
OBJ     = $(SRC:.c=.o)

all: $(NAME)

$(NAME): $(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(NAME)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ)

fclean: clean
	rm -f $(NAME)

re: fclean all

.PHONY: all clean fclean re
```
