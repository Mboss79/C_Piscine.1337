> 📌 *Guide compiled by* **mbousebe** *— C Piscine, C00* 🐧

# 🏊 C Piscine — C00 Survival Guide

Welcome to your very first C project at 42! This guide is here to walk you through everything you need to understand *before* and *while* you tackle each exercise — without ever handing you the final code. Think of this as your friendly dive buddy 🤿, not a life raft that does the swimming for you.

> 📝 **Note:** This guide won't give you copy-pasteable solutions. The goal is for *you* to build the reasoning muscle. That's literally the whole point of the Piscine (see Chapter II of the subject — "the learning journey is more important than the result" 🎯).

---

## Table of Contents

1. [Introduction / Instructions Recap](#1--introduction--instructions-recap)
2. [C Language Fundamentals](#2--c-language-fundamentals-pre-coding-basics)
3. [Understanding `#include`](#3--understanding-include)
4. [ASCII & Character Basics](#4--ascii--character-basics)
5. [Per-Exercise Lessons (ex00 → ex08)](#5--per-exercise-lessons)
6. [Function Types Reference](#6--function-types-reference)
7. [Final Pep Talk](#7--final-pep-talk-)

---

## 1. 🚦 Introduction / Instructions Recap

Let's decode the jargon from the subject page in plain English.

| Term | What it actually means |
|---|---|
| **Moulinette** | An automated robot grader 🤖. It compiles your code and checks the output. No feelings, no mercy, no negotiating. |
| **norminette** | A separate robot 🤖 that checks your *code style* against 42's "Norm" (formatting rules). If this fails, Moulinette won't even bother grading your logic. |
| **Turn-in directory** | The exact folder your file must live in (e.g. `ex00/`). Wrong folder = not found = 0. |
| **Forbidden functions** | Functions you're not allowed to use (here: only `write` is allowed). Using anything else, even `printf`, is an instant **-42** ☠️. |
| **`-Wall -Wextra -Werror`** | Compiler flags Moulinette uses. They mean "show all warnings, show extra warnings, and treat every warning as a hard error." One tiny warning = compilation failure = **0**. |

### ✅ Norm-compliant vs ❌ Non-compliant (conceptual example)

This isn't a solution to any exercise — just a style illustration.

**✅ Norm-friendly shape:**
```c
int	ft_add(int a, int b)
{
	int	result;

	result = a + b;
	return (result);
}
```

**❌ Style violations (illustrative only):**
```c
int ft_add(int a,int b) {
    int result = a + b;   // declaration + assignment combined = forbidden by Norm
    if(result>0){return result;}  // no space, no parentheses convention, cramped braces
}
```

Key norm habits to build immediately:
- Opening curly brace `{` goes on its **own line** for functions.
- **Tabs**, not spaces, for indentation.
- You generally can't declare **and** initialize a variable on the same line (`int result = a + b;` ❌ → declare first, assign after ✅).
- Max ~25 lines per function (excluding braces).
- Max 4 parameters per function.
- No more than one variable declaration per line.

> ⚠️ **Tip:** Get `norminette` running locally from day one (with the `-R CheckForbiddenSourceHeader` flag, per the subject!) and run it after *every* file you touch. Don't wait until the end — surprises are no fun.

---

## 2. 🧱 C Language Fundamentals (Pre-Coding Basics)

Before you write a single exercise, let's make sure the raw syntax makes sense.

### 2.1 The semicolon `;`

In C, `;` marks the **end of a statement** — like a period ending a sentence. Forget it, and the compiler gets confused about where one instruction ends and the next begins.

```c
int x;
x = 5;
```

### 2.2 Curly braces `{}`

Braces group statements into a **block** — the body of a function, an `if`, a loop, etc. Everything between `{` and `}` belongs together.

```c
void	example(void)
{
	// everything in here is "inside" the function
}
```

### 2.3 Indentation & tabs

Not just cosmetic! Indentation shows *nesting* — what's "inside" what. At 42, use **tabs** consistently. A well-indented file is dramatically easier to debug (and norminette cares about this too).

### 2.4 Spacing conventions

- Space after commas in parameter lists: `ft_putchar(char c)` not `ft_putchar(char  c)`.
- No space between function name and its parentheses: `write(1, &c, 1)` not `write (1, &c, 1)`.
- Operators are usually surrounded by spaces: `a + b`, `i < 10`.

### 2.5 Variables & types

A variable is a labeled box that stores a value. You must tell C what *type* of value it holds:

| Type | Stores | Example |
|---|---|---|
| `int` | Whole numbers | `-42`, `0`, `100000` |
| `char` | A single character (internally, a small number — see ASCII below) | `'a'`, `'Z'`, `'9'` |
| `void` | "Nothing" — used when a function returns nothing, or takes no parameters | `void ft_putchar(char c)` |

```c
int		age;
char	letter;
```

> 📝 **Note:** In C, you generally declare all the variables you'll use for a block near the top of that block (Norm convention), *then* use them below.

### 2.6 Function signatures / prototypes

A **function signature** (or prototype) tells the compiler three things:
1. What the function **returns** (`void`, `int`, etc.)
2. What it's **called**
3. What **parameters** (inputs) it expects, and their types

```c
void ft_putchar(char c);
```
Read this as: *"There exists a function named `ft_putchar`. It takes one `char` argument named `c`. It gives nothing back (`void`)."*

### 2.7 Declaration vs. Definition

- **Declaration**: "This function/variable exists, here's its shape." (like the prototype line above)
- **Definition**: "Here's the actual body/behavior."

```c
void ft_putchar(char c);   // declaration (a promise)

void ft_putchar(char c)    // definition (the actual work)
{
	write(1, &c, 1);
}
```

Think of a declaration as a movie trailer 🎬 and the definition as the full movie.

### 2.8 `return` — what it does and when you need it

`return` hands a value back to whoever called the function, **and** immediately stops the function's execution at that point.

- If a function's return type is `void`, you don't return a value (you can use a bare `return;` to exit early, but it's optional).
- If the return type is `int`, `char`, etc., you **must** send a value back with `return something;`.

```c
int ft_double(int n)
{
	return (n * 2);   // hands the doubled value back, function ends here
}
```

> ⚠️ **Tip:** All the C00 exercises use `void` — so you won't be returning values, just performing actions (writing to the screen). But you'll need `return` logic understanding for later exercises (`ft_is_negative` uses conditional logic, not return values, but the *thinking pattern* is the same).

### 2.9 Basic control structures

You'll lean on these heavily for the alphabet, numbers, and combination exercises.

**`if` — do something only when a condition is true:**
```c
if (n < 0)
{
	// runs only if n is negative
}
```

**`for` — repeat a fixed number of times (perfect for "count from a to z"):**
```c
for (i = 0; i < 10; i++)
{
	// runs 10 times, i goes 0,1,2...9
}
```
Break it down: `(start; condition to keep going; what happens each lap)`.

**`while` — repeat as long as a condition holds (good when the number of repeats isn't fixed in advance):**
```c
while (i < 10)
{
	// keep going while true
	i++;
}
```

> 🎉 **Fun fact:** `for` and `while` are interchangeable in almost every case — `for` is just a `while` with the setup/increment baked into one line. Pick whichever reads clearer for the problem.

### 2.10 42 Norm quick-hits relevant to C00

- One instruction per line.
- No more than one variable declared per line, and never combined with an assignment (`int i; i = 0;` not `int i = 0;`).
- Functions: max ~25 lines, max 4 parameters.
- No `for` loops with multiple variables/conditions crammed in (keep it simple — one counter).
- No `switch`/ternary weirdness needed at this stage — keep it dead simple with `if`/`for`/`while`.

---

## 3. 📦 Understanding `#include`

### What does it do?

`#include` is a **preprocessor directive** — before your code even compiles, the preprocessor literally copy-pastes the contents of another file (a "header file") into yours. Headers contain *declarations* of functions/types you want to use, so the compiler knows they exist and how to call them correctly.

### `<...>` vs `"..."`

```c
#include <unistd.h>   // angle brackets: look in the system's standard library folders
#include "myheader.h"  // quotes: look in your own project folder first
```

- **`<...>`**: for standard/system libraries (things that ship with C or your OS).
- **`"..."`**: for headers *you* wrote and placed in your project.

### How do I know which header a function needs?

Use the **man pages** (manual) in your terminal:

```bash
man write
man 2 write
```

Scroll to the **SYNOPSIS** section — it literally lists the `#include` lines you need, right above the function signature. This is your go-to detective tool for the rest of your C journey. 🕵️

### What is `unistd.h` and why does `write` need it?

`unistd.h` ("Unix Standard") declares low-level system-call functions for Unix-like operating systems — things that talk directly to the OS, like `write`, `read`, and `close`. Since `write` is a system call (not a regular library function), its declaration lives there. Without including it, the compiler doesn't know `write` exists — and with `-Wextra -Werror`, an implicit/undeclared function usage will blow up your compilation.

> ⚠️ **Tip:** Every `.c` file that calls `write` needs `#include <unistd.h>` at the top.

---

## 4. 🔤 ASCII & Character Basics

### What is ASCII?

ASCII is a table that maps characters to numbers. Computers only understand numbers, so every character your keyboard produces (`'a'`, `'Z'`, `'5'`, `'!'`, space, newline...) is secretly stored as an integer under the hood.

A few landmarks worth memorizing:
- `'a'` = 97, and lowercase letters run consecutively up to `'z'` = 122.
- `'A'` = 65, uppercase letters run up to `'Z'` = 90.
- `'0'` = 48, digits run up to `'9'` = 57.
- Space = 32, newline `'\n'` = 10.

### `char` *is* a small number

Because of this, a `char` variable in C is really just a tiny integer (usually 1 byte) that gets *displayed* as its corresponding character. This means...

### Char arithmetic works!

```c
char c;

c = 'a' + 1;   // this is 'b'! Because 'a' is 97, +1 = 98, which IS 'b'
```

You can also compare characters directly (`'a' < 'z'` is true, because 97 < 122), and loop through the alphabet by incrementing a `char` variable.

> 🎉 **Fun fact:** This is *exactly* why `ft_print_alphabet` and `ft_print_reverse_alphabet` are solvable with a simple loop and `+`/`-` arithmetic on a `char` — no lookup table needed!

---

## 5. 📚 Per-Exercise Lessons

For each exercise: the concept, the problem in plain words, ways to think about it, a conceptual walkthrough, common pitfalls, and how to test it. No final code — just the map, you drive. 🗺️

---

### 🟢 Exercise 00 — `ft_putchar`

**Skill this builds:** The absolute foundation — calling `write` correctly, understanding pointers-as-addresses at a surface level, and function definitions.

**The problem, plainly:** You get a single character. Print it. That's it.

**Ways to think about it:**
- `write` needs three things: *where to write* (1 = standard output, your terminal), *what to write* (a memory address pointing to the data), and *how many bytes*.
- You already have `c`, a `char`. `write` wants an **address**, so you give it `&c` — "the address of c" — and tell it to write exactly `1` byte.

**Conceptual walkthrough:**
1. Function receives `c`.
2. Call `write` with target `1`, address `&c`, length `1`.
3. Function ends (nothing to return, it's `void`).

**Common pitfalls:**
- Forgetting `#include <unistd.h>` → compiler doesn't recognize `write`.
- Passing `c` instead of `&c` (type mismatch — `write` wants a pointer/address, not the raw character value).
- Missing the 42 header comment block at the top of the file (norminette checks for it!).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_putchar.c -o test   # you'll need a small main() temporarily, not turned in
./test
```
Since you won't submit a `main()`, you can write a temporary throwaway test file locally (outside your turn-in folder) that calls `ft_putchar('A')` and confirms `A` appears.

---

### 🟢 Exercise 01 — `ft_print_alphabet`

**Skill this builds:** Loops + reusing the `char` arithmetic you just learned.

**The problem, plainly:** Print `a` through `z`, all in one line, no spaces or newline needed unless the exercise implies one line ends cleanly.

**Ways to think about it:**
- Approach A: A `for` loop with a `char` counter starting at `'a'`, looping *while* it's `<= 'z'`, printing then incrementing.
- Approach B: A `while` loop doing the same thing, just with the increment inside the loop body instead of the `for` header.
- You can even reuse a `write`-style call directly, or think about how you might structure a helper like the one from ex00 conceptually (though you can't call across files here — each `.c` is self-contained per exercise).

**Conceptual walkthrough:**
1. Start a counter at `'a'`.
2. Loop: while counter `<= 'z'`, output the counter, then bump it up by one.
3. Loop ends naturally once you pass `'z'`.

**Common pitfalls:**
- Off-by-one errors: looping `< 'z'` instead of `<= 'z'` will cut off the last letter.
- Infinite loop if you forget to increment the counter.
- Declaring your loop counter as `int` and forgetting to cast/convert when writing it (mixing `int` and `char` sloppily can trigger warnings).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_print_alphabet.c -o test
./test | cat -e
```
`cat -e` shows hidden characters (like `$` at line ends for newlines) — great for confirming you don't have a stray/missing newline.

---

### 🟢 Exercise 02 — `ft_print_reverse_alphabet`

**Skill this builds:** Loops running *backwards* — decrementing instead of incrementing.

**The problem, plainly:** Same as ex01, but start at `'z'` and count down to `'a'`.

**Ways to think about it:**
- Mirror image of ex01: start high, condition checks `>= 'a'`, and you subtract instead of add each lap.
- Ask yourself: what breaks if you use `char` vs `int` as your loop variable here near the boundary (`'a' - 1` — is that safe)? It's fine for `char`, but it's good to *reason through* why.

**Conceptual walkthrough:**
1. Start counter at `'z'`.
2. While counter `>= 'a'`, print it, then decrement.
3. Stop once you'd go below `'a'`.

**Common pitfalls:**
- Reversing the condition incorrectly (using `<=` instead of `>=`, which would never run).
- Forgetting that decrementing past `'a'` isn't dangerous for `char` here since we stop the loop before that, but it's a good habit to double check loop boundaries every time.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_print_reverse_alphabet.c -o test
./test | cat -e
```
Expect to see `zyxwvuts...ba` with no gaps.

---

### 🟢 Exercise 03 — `ft_print_numbers`

**Skill this builds:** Applying the same loop pattern to digits (`'0'`–`'9'`), reinforcing that digits are characters too.

**The problem, plainly:** Print `0123456789` on one line.

**Ways to think about it:**
- Identical structure to ex01, just swap the character range to `'0'` through `'9'`.
- Alternative: loop with an `int` from `0` to `9`, and convert each number to its character form using the ASCII offset you learned (`'0' + i`).

**Conceptual walkthrough:**
1. Either loop a `char` from `'0'` to `'9'`, or loop an `int` from `0` to `9` and convert with `'0' + i`.
2. Print each digit.
3. Loop naturally ends after `9`.

**Common pitfalls:**
- Forgetting the `'0' +` conversion if you loop with `int`, and accidentally trying to `write` the raw integer (which would write a weird non-printable byte, not the digit's text form).
- Mixing signed/unsigned comparisons that trigger `-Wextra` warnings.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_print_numbers.c -o test
./test | cat -e
```

---

### 🟡 Exercise 04 — `ft_is_negative`

**Skill this builds:** Your first real `if`/`else` decision-making based on function *input* (a parameter), not a loop.

**The problem, plainly:** Given an integer, print `'N'` if it's negative, `'P'` if it's zero or positive.

**Ways to think about it:**
- Approach A: simple `if (n < 0) { ... } else { ... }`.
- Approach B: think about it as "is `n` strictly less than 0?" — that single boolean question decides everything. No loop needed at all.
- Consider: what does "positive or zero" tell you about which comparison operator to use, and on which branch?

**Conceptual walkthrough:**
1. Check whether `n` is less than zero.
2. If true, output `'N'`.
3. Otherwise (zero or positive), output `'P'`.

**Common pitfalls:**
- Off-by-one logic errors: treating `0` as negative (it explicitly isn't, per the subject).
- Using `<=` vs `<` incorrectly and shifting the boundary.
- Forgetting this function is `void` — you're printing directly, not returning a value.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_is_negative.c -o test
./test    # test with a temporary main() calling ft_is_negative(-1), ft_is_negative(0), ft_is_negative(5)
```
Try boundary values especially: `0`, `-1`, `1`, and the extremes like `INT_MIN`/`INT_MAX` conceptually (do they behave as expected?).

---

### 🟠 Exercise 05 — `ft_print_comb`

**Skill this builds:** **Nested loops** — loops inside loops — plus formatting output with separators.

**The problem, plainly:** Print every 3-digit combination like `012`, `013`, ... `789`, where digits are strictly increasing within each combination (`123` yes, `321` no, `112` no — repeats aren't allowed), separated by `, `, with no trailing comma at the very end.

**Ways to think about it:**
- Think of it as 3 nested loops: an outer loop for the first digit, a middle loop for the second, an inner loop for the third.
- The trick is each inner loop's *starting point* depends on the outer loop's current value — this is what guarantees ascending order and prevents repeats. Ask yourself: if digit 1 is `a`, where should digit 2's loop *start* to guarantee `digit2 > digit1`?
- Separately, think about the comma-formatting problem: how do you print `, ` *between* combinations but not after the very last one? A common trick is to print the separator *before* each combination except the first, rather than after each one except the last.

**Conceptual walkthrough:**
1. Outer loop: first digit from `0` to `7` (since you need two more digits after it, up to `9`).
2. Middle loop: second digit starts *just after* the first digit's current value, up to `8`.
3. Inner loop: third digit starts *just after* the second digit's current value, up to `9`.
4. Print the three digits together as a combination.
5. Handle the separator logic so you don't get a trailing `, ` at the end.

**Common pitfalls:**
- Starting inner loops at `0` instead of "one more than the previous digit" — this creates duplicates/wrong order.
- Getting the upper bounds wrong (off-by-one at the loop boundaries) so you either miss `789` or print things beyond it.
- Trailing separator after the last combination — norminette/Moulinette *and* your own eyes will catch this immediately with `cat -e`.
- Forgetting these are `char` digits when printing (convert with the ASCII offset trick from Section 4!).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_print_comb.c -o test
./test | cat -e
```
Compare your first few and last few outputs directly against the subject's expected output.

---

### 🟠 Exercise 06 — `ft_print_comb2`

**Skill this builds:** Nested loops again, but now working with **two-digit numbers** (00–99) instead of single digits — meaning you'll likely need a helper concept for printing multi-digit numbers with leading zeros.

**The problem, plainly:** Print every pair of distinct two-digit numbers from `00` to `99`, first number always smaller than the second, formatted like `00 01, 00 02, ..., 98 99`.

**Ways to think about it:**
- Two nested loops: outer for the first number (0 to 98), inner starting *one above* the outer's value (guaranteeing ascending, no repeats), up to 99.
- The new challenge: printing a number 0–99 as *two* characters, even when it's a single digit (e.g., `5` must show as `05`, not `5`). Think about how you'd split a two-digit number into its "tens" and "units" digit using division and modulo (`/` and `%`), then convert each to a character.
- Same separator logic as ex05 applies for the `, ` between pairs.

**Conceptual walkthrough:**
1. Outer loop: first number from `0` to `98`.
2. Inner loop: second number from `outer + 1` to `99`.
3. For each number, extract tens digit (`n / 10`) and units digit (`n % 10`), convert both to characters, print them together.
4. Print a space between the two numbers in a pair, and `, ` between pairs (careful with the trailing separator again).

**Common pitfalls:**
- Forgetting the leading zero for single-digit numbers (`5` → should print `05`).
- Confusing `/` (integer division, drops the remainder) with `%` (modulo, gives *only* the remainder) — you need both.
- Loop boundary mistakes again (starting inner loop at `0` instead of `outer + 1`).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_print_comb2.c -o test
./test | cat -e
```

---

### 🟡 Exercise 07 — `ft_putnbr`

**Skill this builds:** Handling **any** `int` value, including negative numbers and the tricky extremes (`INT_MIN`), using recursion or iteration to print multi-digit numbers.

**The problem, plainly:** Print an integer exactly as a human would read it — sign included if negative, all digits in the right order.

**Ways to think about it:**
- Numbers don't come apart digit-by-digit in the order you want to print them (dividing by 10 repeatedly gives you digits from *last* to *first*). Two classic strategies:
  - **Recursion**: print the number-divided-by-10 first (a smaller version of the same problem), *then* print the last digit — this naturally reverses the reversal.
  - **Iterative with a buffer/array**: collect digits into some structure and print them backwards after.
- The genuinely tricky part: `INT_MIN` (around -2147483648) cannot be simply negated to make it positive — its positive counterpart overflows a 32-bit signed `int`. Think about how you might handle its sign and first digit *before* trying to treat it like a normal negative number, or work with a wider type in your calculations if you have one available in this exercise's constraints.

**Conceptual walkthrough (recursive angle):**
1. If the number is negative, print a `-` sign first, then think about how to handle the *value* from here on (careful with `INT_MIN`!).
2. If the number has more than one digit, recursively handle everything except the last digit first.
3. Print the last digit (using the ASCII offset trick).
4. Base case: when you're down to a single digit, just print it — this is what stops the recursion.

**Common pitfalls:**
- Forgetting to handle `0` (should just print `0`, not nothing).
- The infamous `INT_MIN` overflow trap — negating it doesn't give a valid positive `int`.
- Infinite recursion if your base case condition is wrong.
- Printing digits in reverse order by not thinking through the recursion direction carefully.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_putnbr.c -o test
./test    # try ft_putnbr(0), ft_putnbr(42), ft_putnbr(-42), ft_putnbr(-2147483648), ft_putnbr(2147483647)
```
> ⚠️ **Tip:** Always test the extreme edge cases (`INT_MIN`, `INT_MAX`, `0`, `-1`) — these are exactly what Moulinette will hammer you with.

---

### 🔴 Exercise 08 — `ft_print_combn`

**Skill this builds:** **Recursion done properly** — generalizing ex05's fixed 3-digit nested loops into an arbitrary `n`-digit version. This is the "boss level" of C00.

**The problem, plainly:** Same idea as `ft_print_comb`, but instead of always 3 digits, the caller passes in `n` (how many digits per combination), and you must generate all ascending, non-repeating combinations of `n` distinct digits (0–9).

**Ways to think about it:**
- Nested loops worked for a *fixed* depth of 3 (three loops, hardcoded). But you can't hardcode `n` loops when `n` is a variable at runtime! This screams **recursion**: a function that calls a smaller version of itself once per "level" of digit needed.
- Think of it like ex05's three loops, but instead of writing them out three times, you write *one* loop that calls itself again for the next digit position, keeping track of "which digit position am I filling" and "what's the smallest next digit allowed" (to preserve ascending order and no repeats).
- You'll likely need to track a growing sequence of chosen digits so far (e.g., in a small array) so you can print the whole combination once you've picked `n` digits.
- Base case: when you've picked `n` digits already, print what you've collected and stop recursing deeper.
- Separator logic (`, ` between combinations, none trailing) is the same challenge as ex05/ex06, just now needs to work generically regardless of `n`.

**Conceptual walkthrough:**
1. Write a recursive helper that receives: how many digits still needed, the smallest digit allowed to start from next, and the digits chosen so far.
2. At each call: loop through allowed digits (from "smallest allowed" up to `9`, leaving enough room for however many digits still remain to be picked).
3. For each candidate digit: add it to the "chosen so far" collection, then recursively call for the *next* digit position, with "smallest allowed" bumped up by one.
4. Base case: when digits needed reaches `0`, print the fully chosen combination (with separator logic) and return back up.
5. `ft_print_combn` itself becomes a thin wrapper that kicks off this recursive process with the initial parameters.

**Common pitfalls:**
- Not leaving enough "room" for remaining digits — e.g., trying to start too close to `9` when you still need several more digits (this causes missing combos or crashes if not bounded correctly).
- Getting confused about what state needs to be *passed along* in the recursive calls (which digits chosen, how many remain, where to resume from).
- Trailing separator bug at the very end of the entire output (not just per combination) — test carefully with `cat -e`.
- Forgetting edge cases: what should happen with `n = 1`? Does your recursion still work cleanly when it barely recurses at all?

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_print_combn.c -o test
./test    # test with n = 1, n = 2 (compare against subject's expected output!), and n = 9
```
> ⚠️ **Tip:** Start by manually testing `n = 2` against the exact expected output in the subject — it's given to you as a sanity check!

---

## 6. 🧩 Function Types Reference

A quick mental model for the kinds of functions you'll meet (and eventually write) in C:

### `void` vs. returning functions
- **`void` functions** *do* something (an action/side-effect, like printing) but hand nothing back to the caller. All of C00's exercises are `void` because they print directly.
- **Returning functions** (`int`, `char`, etc.) *compute* something and hand the result back, letting the caller decide what to do with it (print it, use it in more math, compare it...). You'll meet these constantly starting in later projects.

### Iterative vs. recursive
- **Iterative**: uses loops (`for`/`while`) to repeat work. Usually easier to read for simple, fixed-depth repetition (great for ex01–ex03, ex05, ex06).
- **Recursive**: a function that calls *itself* with a smaller/simpler version of the problem, until it hits a "base case" that stops the chain. Ideal when the depth of repetition isn't fixed in advance (perfect for ex07's digit-by-digit number printing, and essential for ex08's variable-length combinations).

**How to decide which to use:**
- Is the number of repetitions **known and fixed** ahead of time (like exactly 26 letters, or exactly 3 digits)? → Loops are usually simpler.
- Does the problem's "size" **change based on input** (like `n` digits, or peeling off one digit of a number at a time)? → Recursion often fits more naturally.
- Recursion always needs: a **base case** (when to stop) and a way the problem gets **smaller** with each call — otherwise, hello infinite recursion and a crash. 💥

---

## 7. 🎉 Final Pep Talk

You've now got the map — ASCII, loops, recursion, the Norm, and a level-by-level breakdown of every exercise. The actual code is yours to write, and yours to be proud of. 💪

Some parting reminders straight from the subject itself:
- 🤝 Talk to your peers — genuinely explaining your ideas out loud is one of the fastest ways to find bugs in your own thinking.
- 🧪 Test constantly, especially edge cases (`0`, negative numbers, boundaries).
- 🧹 Run `norminette -R CheckForbiddenSourceHeader` early and often.
- 🐢 It's okay to be slow here — struggling *is* the curriculum working as intended.

Good luck, and happy diving into the Piscine! 🏊‍♂️🌊

---

> 📌 *Guide compiled by* **mbousebe** *— keep this file, keep grinding, keep swimming.* 🐧
