> 📌 *Guide compiled by* **Mboss** *(aka mbousebe)* *— C Piscine, C01* 🐧✨ *Pointers: unlocked.*

# 🏊 C Piscine — C01 Survival Guide

Welcome to Module 2 of the Piscine! If C00 taught you to *print things*, C01 teaches you to *reach into memory and change things* — the beginning of real pointer power. 🪄

> 📝 **Note:** This guide explains concepts and gives you strategies to reason through each exercise — it will **not** hand you final code. That's on purpose (see Chapter II of the subject). The struggle is the curriculum. 💪

> ⚠️ **Reminder from the subject:** Today's validation threshold is **50%**. You get to decide which exercises you tackle to hit it — but remember, easier exercises must work before harder ones count!

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

Same referee, new arena. Let's re-decode the essentials in plain English for C01.

| Term | What it actually means |
|---|---|
| **Moulinette** | The automated grading robot 🤖. Compiles your code, checks behavior. No appeals process. |
| **norminette** | The style-checker robot 🤖. If your code breaks 42's "Norm" formatting rules, Moulinette won't even look at whether it *works*. |
| **Turn-in directory** | Each exercise has its own dedicated folder (`ex00/`, `ex01/`, etc.) — put the *right* file in the *right* folder. |
| **Forbidden functions** | For C01, almost every exercise says **"Allowed functions: None"** — meaning no `write`, no standard library calls at all, just raw C. Only `ft_putstr` allows `write`. |
| **`-Wall -Wextra -Werror`** | Compiler flags Moulinette uses — all warnings become hard failures. Zero tolerance. |

### ✅ Norm-compliant vs ❌ Non-compliant (conceptual example)

Not a solution to any real exercise — just illustrating pointer-style formatting.

**✅ Norm-friendly shape:**
```c
void	ft_example(int *nbr)
{
	*nbr = 42;
}
```

**❌ Style violations (illustrative only):**
```c
void ft_example(int* nbr){
    *nbr=42;   // no spacing, star attached to wrong side, cramped brace, no tab indent
}
```

Key habits to lock in for C01 specifically:
- The `*` in a pointer type typically sits closer to the **variable name**, not the type (`int *nbr`, not `int* nbr`) — this is 42 Norm convention.
- Opening `{` for a function body goes on its **own line**.
- Tabs, not spaces.
- One declaration per line, no combined declare+assign.
- Since most C01 exercises forbid *all* functions, don't even instinctively reach for `write` unless the exercise explicitly allows it (only `ft_putstr` does here).

> ⚠️ **Tip:** Run `norminette -R CheckForbiddenSourceHeader` after every file. The 42 header comment block at the top of your `.c` files is mandatory and checked automatically.

---

## 2. 🧱 C Language Fundamentals (Pre-Coding Basics)

C01 is really "Intro to Pointers," so alongside the basics, we'll build up exactly the pointer vocabulary you'll need.

### 2.1 The semicolon `;`

Ends a statement — same rule as always. C reads your code statement by statement; `;` is how it knows where one ends.

```c
int x;
x = 5;
```

### 2.2 Curly braces `{}`

Group a block of statements — a function body, an `if`, a loop. Everything inside `{ }` is treated as one unit.

### 2.3 Indentation & tabs

Use **tabs** consistently to show nesting — it's both a readability habit and a norminette requirement.

### 2.4 Spacing conventions

- Space after commas: `ft_swap(int *a, int *b)`.
- No space between function name and `(`.
- Operators generally get spaces around them: `a + b`, `a / b`.

### 2.5 Variables & types (plus: pointers!)

You already know:

| Type | Stores | Example |
|---|---|---|
| `int` | Whole numbers | `-42`, `0`, `100000` |
| `char` | A single character (a small number under the hood) | `'a'`, `'Z'` |
| `void` | "Nothing" — no return value, or (in a pointer context) "a type not yet specified" | `void ft_ft(int *nbr)` |

Now, the star of C01: **pointers**.

A pointer is a variable that doesn't store a normal value — it stores a **memory address**, i.e. *directions to where another variable lives*. Think of a house 🏠 (your actual `int` variable) and a pointer as a **slip of paper with the house's address written on it**. You can hand that slip to someone else, and they can go to the house and even change what's inside — without ever being handed the house itself.

```c
int		nbr;     // a normal int — "the house"
int		*ptr;    // a pointer to an int — "the address slip"
```

Two operators you'll live and breathe in C01:

- `&` (**address-of**): "give me the address of this variable." `&nbr` means "the address where `nbr` lives."
- `*` (**dereference**, when used on an already-declared pointer): "go to the address this pointer holds, and give/set the value there." `*ptr = 42;` means "go to the address `ptr` points to, and put `42` there."

> 🎉 **Fun fact:** The `*` symbol does double duty in C. In a **declaration** (`int *ptr;`), it means "this variable is a pointer." In an **expression** (`*ptr = 42;`), it means "dereference — go to that address." Same symbol, different job depending on context. Confusing at first, totally normal to trip over it!

### 2.6 What a function signature/prototype means

Same idea as before, now often involving pointer types:

```c
void ft_swap(int *a, int *b);
```
Read this as: *"`ft_swap` takes two addresses of `int`s, named `a` and `b`, and returns nothing."*

### 2.7 Declaration vs. Definition

- **Declaration**: the promise/shape (a prototype line).
- **Definition**: the actual body of logic.

```c
void ft_ft(int *nbr);   // declaration

void ft_ft(int *nbr)    // definition
{
	*nbr = 42;
}
```

### 2.8 `return` — what it does and when you need it

`return` sends a value back to the caller and ends the function immediately at that point.

- `void` functions (which is *all* of C01's exercises!) don't return a value — they do their work by **modifying the memory a pointer points to**, instead of handing back a result. This is actually the core lesson of this whole module: pointers let a function change something in the *caller's* world, even though C normally passes everything "by value" (as a copy).
- Functions with a real return type (like `int ft_strlen`) must `return` something matching that type.

```c
int ft_double(int n)
{
	return (n * 2);
}
```

> 📝 **Note:** Why do `ft_ft`, `ft_swap`, `ft_div_mod`, etc. all use pointers instead of just `return`-ing a value? Because a function can only `return` **one** value. `ft_div_mod` needs to hand back *two* results (a quotient and a remainder) — pointers are how you get multiple "outputs" out of a single function call.

### 2.9 Basic control structures

You'll need these for looping through arrays (ex07, ex08):

**`if` — conditional branching:**
```c
if (a > b)
{
	// do something
}
```

**`for` — great for a known number of repeats (like looping through an array of known `size`):**
```c
for (i = 0; i < size; i++)
{
	// runs once per array element
}
```

**`while` — good when the number of repeats depends on a condition, not a fixed count:**
```c
while (i < size)
{
	i++;
}
```

### 2.10 42 Norm quick-hits relevant to C01

- One instruction per line, one declaration per line.
- No combined declare + assign (`int i = 0;` ❌ → declare `int i;`, then `i = 0;` ✅).
- Functions: max ~25 lines, max 4 parameters.
- Pointer `*` conventionally placed next to the variable name in declarations.
- Keep loop logic simple — one clear counter variable per loop.

---

## 3. 📦 Understanding `#include`

### What does it do?

`#include` copies the contents of a header file into yours *before* compilation, so the compiler knows about types/functions declared elsewhere.

### `<...>` vs `"..."`

```c
#include <unistd.h>    // system/standard library headers
#include "myheader.h"   // your own project headers
```

### How do I know which header a function needs?

Use `man`:

```bash
man write
man 2 write
```

The **SYNOPSIS** section tells you exactly which `#include` line(s) you need.

### What is `unistd.h` and why does `write` need it?

`unistd.h` declares low-level Unix system calls, including `write`. Since almost every C01 exercise forbids all functions (including `write`), you likely **won't** need `unistd.h` at all except for `ft_putstr` (ex05), which explicitly allows `write`.

> ⚠️ **Tip:** For exercises marked "Allowed functions: None" (which is most of C01!), you shouldn't need *any* `#include` beyond what's necessary for your own function prototypes — resist the urge to import things out of habit.

---

## 4. 🔤 ASCII & Character Basics

Less central to C01 than C00, but still relevant for `ft_strlen` (which walks through a string's characters) and `ft_putstr` (which prints them).

### Quick refresher

- Every `char` is secretly a small integer (its ASCII code). `'a'` is `97`, `'A'` is `65`, digits `'0'`–`'9'` are `48`–`57`.
- Strings in C are just arrays of `char`, ending with a special "null terminator" character written `'\0'` (ASCII value `0`) — this is how C knows where a string *ends*, since there's no built-in length tracking.

> 🎉 **Fun fact:** This `'\0'` sentinel is *exactly* the trick `ft_strlen` relies on — you keep walking through the array counting characters until you bump into that null terminator, and stop.

---

## 5. 📚 Per-Exercise Lessons

For each exercise: the concept, the problem in plain words, ways to think about it, a conceptual walkthrough, common pitfalls, and how to test it.

---

### 🟢 Exercise 00 — `ft_ft`

**Skill this builds:** Your very first pointer dereference — "reach through the address, change the value."

**The problem, plainly:** You're handed the *address* of an `int`. Make the actual `int` at that address equal `42`.

**Ways to think about it:**
- You're not creating a new `42` and handing it back (there's no `return` here — it's `void`). You're going to the address you were given and overwriting what's stored there.
- Picture it as: you're given a treasure map (`nbr`, the address). You don't draw a new map — you walk to the spot and put the treasure there yourself.

**Conceptual walkthrough:**
1. Function receives `nbr`, a pointer to an `int`.
2. Dereference `nbr` (go to the address it holds).
3. Assign `42` to that location.
4. Function ends — nothing to return.

**Common pitfalls:**
- Trying to do `nbr = 42;` instead of `*nbr = 42;` — this would overwrite the *address itself* rather than the value stored there, which is a type mismatch and won't compile cleanly anyway.
- Forgetting the 42 header comment block.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_ft.c -o test
```
Since you can't use `write` or `printf` here (no allowed functions!), write a tiny **temporary** local test file (not turned in) that declares an `int`, calls `ft_ft(&that_int)`, and then — just for your own local debugging — you could temporarily use `printf` in *that separate test file only* to confirm the value changed, then delete/don't submit it.

---

### 🟢 Exercise 01 — `ft_ultimate_ft`

**Skill this builds:** Multiple levels of indirection — pointers to pointers to pointers... nine layers deep!

**The problem, plainly:** Same mission as ex00 (set an `int` to `42`), but now you're handed a pointer... to a pointer... to a pointer (nine stars' worth!) instead of a direct pointer to the `int`.

**Ways to think about it:**
- Each `*` is one more "layer" of indirection — one more address slip pointing to another address slip, eventually leading to the actual `int` "house."
- To get to the real value, you need to dereference **once for each star** in the parameter type. If the parameter is `int *********nbr` (nine stars), you need nine dereferences total to finally reach the `int` itself.
- Analogy: imagine nine sealed envelopes, each containing directions to the next envelope, and the ninth envelope contains directions to the actual treasure chest. You open envelope 1, follow to envelope 2, follow to envelope 3... all the way to the treasure.

**Conceptual walkthrough:**
1. Function receives `nbr` (9 stars deep).
2. Dereference once → get an 8-star pointer.
3. Dereference again → 7-star pointer.
4. ...continue this chain...
5. After the 9th dereference, you've reached the actual `int` — assign `42` there.

**Common pitfalls:**
- Losing count of how many `*` you've applied (miscounting stars is the #1 bug here).
- Trying to write this as one giant line with nine stars stacked — it compiles, but it's much easier (and more debuggable) to unwrap gradually.
- Forgetting this is still just `void`, no return value needed.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_ultimate_ft.c -o test
```
Build a temporary local test: declare an `int`, then manually build up the nine layers of pointers (a pointer to it, a pointer to that pointer, and so on), pass the final 9-star pointer into `ft_ultimate_ft`, and verify the original `int` became `42`.

> ⚠️ **Tip:** Building the nine layers of pointers in your test file is itself great pointer practice — take your time with it.

---

### 🟢 Exercise 02 — `ft_swap`

**Skill this builds:** Using pointers to modify **two** caller-side variables — the classic "swap" problem that's impossible without pointers.

**The problem, plainly:** Given the addresses of two integers, swap their values (whatever was in `a` is now in `b`, and vice versa).

**Ways to think about it:**
- Why can't you just do `a = b; b = a;` directly on the values? Because that overwrites `a`'s original value before you've saved it anywhere — you'd end up with both variables holding the same value.
- This is the classic "you need a temporary holding spot" problem — same logic as swapping the contents of two cups: you need a **third, empty cup** to pour into temporarily.
- Since you were given *addresses*, all your reads/writes need a `*` to actually reach the values.

**Conceptual walkthrough:**
1. Declare a temporary local `int` to act as your "empty third cup."
2. Copy the value at `a`'s address into that temporary variable.
3. Copy the value at `b`'s address into `a`'s address.
4. Copy the temporary (originally `a`'s value) into `b`'s address.

**Common pitfalls:**
- Forgetting to dereference (`*a`, `*b`) and accidentally trying to swap the *addresses themselves* rather than the values at those addresses (which wouldn't affect anything back in the caller anyway).
- Overwriting `a`'s value before you've safely stashed it in your temporary variable, losing data.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_swap.c -o test
```
Local test: declare two `int`s with different values, call `ft_swap(&x, &y)`, confirm they're flipped afterward.

---

### 🟡 Exercise 03 — `ft_div_mod`

**Skill this builds:** Returning **two** results from one function call — the real "why pointers matter" moment.

**The problem, plainly:** Given `a` and `b`, compute `a / b` (integer division) and `a % b` (remainder), and store each result through the given pointers (`div` and `mod`) rather than returning them.

**Ways to think about it:**
- A function can only `return` one value — but this problem needs *two* outputs. Pointers solve that: the caller hands you two "mailboxes" (`div` and `mod`), and you drop a result into each.
- You'll want to recall (or look up) how integer division and the modulo operator behave in C — dividing two `int`s with `/` truncates toward zero, and `%` gives you the leftover remainder.

**Conceptual walkthrough:**
1. Compute `a / b` and store it at the address `div` points to.
2. Compute `a % b` and store it at the address `mod` points to.
3. No return needed — everything is communicated through the pointers.

**Common pitfalls:**
- Forgetting to dereference `div`/`mod` when assigning (`div = a / b;` sets the *address*, not the value — you want `*div = a / b;`).
- Not considering what happens with negative numbers or `b = 0` — think through (and test!) these edge cases even though the subject doesn't dictate specific behavior for them.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_div_mod.c -o test
```
Local test: declare `div` and `mod` as regular `int`s, call `ft_div_mod(17, 5, &div, &mod)`, confirm you get the expected quotient/remainder pair.

---

### 🟡 Exercise 04 — `ft_ultimate_div_mod`

**Skill this builds:** Reusing pointer *inputs* as pointer *outputs* — reading and overwriting through the same pointers.

**The problem, plainly:** This time, `a` and `b` themselves arrive as pointers (not plain `int`s). You divide the value at `a` by the value at `b`, then **overwrite `a`'s value** with the quotient and **overwrite `b`'s value** with the remainder.

**Ways to think about it:**
- The tricky part: you need the *original* values of both `a` and `b` to compute *both* the quotient and remainder — but if you overwrite `a` first, you lose the original value you still need for the remainder calculation (and vice versa)!
- This is very similar to the "swap" ordering problem from ex02: think about what you need to **read first and store safely** before you start **overwriting**.

**Conceptual walkthrough:**
1. Read (dereference) the original values at `a` and `b`, and think about whether you need to stash a copy of either before your first overwrite.
2. Compute the quotient using the original values.
3. Compute the remainder using the original values (not a version you've already overwritten!).
4. Write the quotient into `a`'s address, and the remainder into `b`'s address — in the order that keeps your original values intact for the whole calculation.

**Common pitfalls:**
- Overwriting `*a` with the quotient *before* computing the remainder (which needs the original `*a`) — this is the exact same "lost original value" bug as an incorrect swap.
- Same dereferencing mistake as before (forgetting `*` when reading or assigning).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_ultimate_div_mod.c -o test
```
Local test: declare `a` and `b` as `int`s with test values, call `ft_ultimate_div_mod(&a, &b)`, and check that `a` now holds the quotient and `b` now holds the remainder.

---

### 🟢 Exercise 05 — `ft_putstr`

**Skill this builds:** Walking through a string via a pointer, one character at a time, until you hit the end.

**The problem, plainly:** Print out a string of characters, given as a `char *`.

**Ways to think about it:**
- Remember from Section 4: strings end with `'\0'`. You don't know the length up front — you find out by walking forward until you *hit* that terminator.
- You can treat `str` almost like an array (`str[i]`) or walk it purely with pointer movement (`*str`, then advance `str` itself) — both are valid mental models; pick whichever clicks for you.
- This exercise *is* allowed to use `write` (check the allowed functions table!) — so you're back to the ex00-of-C00 style call, just now inside a loop.

**Conceptual walkthrough:**
1. Start at the beginning of `str`.
2. While the current character isn't the null terminator `'\0'`, print that character (via `write`, one byte at a time), then move to the next character.
3. Stop once you reach `'\0'` — don't print the terminator itself, it's not a visible character.

**Common pitfalls:**
- Printing the null terminator itself, or looping one step too far/short (classic off-by-one).
- Forgetting `#include <unistd.h>` since `write` is used here.
- Infinite loop if you forget to advance your position each iteration.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_putstr.c -o test
./test | cat -e
```
Local test: call `ft_putstr("Hello, 42!")` and confirm the output matches, with `cat -e` to double-check no stray/missing newline weirdness.

---

### 🟡 Exercise 06 — `ft_strlen`

**Skill this builds:** Counting by walking a string — the counting cousin of `ft_putstr`, and your first `int`-returning function in this module.

**The problem, plainly:** Given a string, return how many characters it contains (not counting the terminator).

**Ways to think about it:**
- Nearly identical walking pattern to `ft_putstr`, except instead of printing each character, you're just tallying them with a counter.
- This function *returns* a value (`int`), unlike most of this module — a good moment to contrast "communicate via pointer" (most of C01) vs. "communicate via return" (this one, and C00's exercises).

**Conceptual walkthrough:**
1. Start a counter at `0`.
2. Walk through the string from the beginning.
3. For each character that isn't `'\0'`, increment the counter and move forward.
4. Once you reach `'\0'`, stop and `return` the counter.

**Common pitfalls:**
- Counting the null terminator itself (off-by-one, resulting in a length that's one too many).
- Forgetting the `return` statement entirely (easy to forget after a module full of `void` functions!).
- Allowed functions is `None` here — don't reach for a standard library `strlen`-like helper, not even for testing logic on the side (build your own loop).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_strlen.c -o test
```
Local test: call `ft_strlen("Hello, 42!")` and check it matches the string's actual length (11 in the sample above, if the exclamation mark is included).

---

### 🟠 Exercise 07 — `ft_rev_int_tab`

**Skill this builds:** Working with arrays through pointers, and the "two ends moving inward" pattern — your first real algorithm on a data structure.

**The problem, plainly:** Given an array of `int`s and its size, reverse the array in place (first becomes last, second becomes second-to-last, etc.) — no returning a new array, you modify the original.

**Ways to think about it:**
- Classic approach: use two indices, one starting at the front (`0`) and one at the back (`size - 1`). Swap the elements at those two positions, then move the front index forward and the back index backward. Stop when they meet or cross in the middle.
- This is essentially `ft_swap`'s logic (ex02), just applied repeatedly to pairs of array elements instead of two standalone variables!
- Think through: what happens with an *odd*-length array? Does the middle element need to be touched at all?

**Conceptual walkthrough:**
1. Set up a "front" index at `0` and a "back" index at `size - 1`.
2. While front is still less than back:
   - Swap `tab[front]` and `tab[back]` (using the same temporary-variable trick as ex02).
   - Move front forward by one, back backward by one.
3. Loop ends naturally once front meets or passes back — for odd-length arrays, the middle element never needs swapping (it swaps with itself, or you simply stop before reaching it).

**Common pitfalls:**
- Looping all the way through the whole array instead of stopping at the midpoint — this would reverse it and then reverse it back to the original by the time you finish!
- Off-by-one on the back index (using `size` instead of `size - 1`, which reads outside the array's bounds — a classic and dangerous bug).
- Forgetting the temporary variable during the swap step and losing data (same trap as ex02).

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_rev_int_tab.c -o test
```
Local test: build an array like `{1, 2, 3, 4, 5}`, call `ft_rev_int_tab(tab, 5)`, and print/inspect the array afterward — it should read `{5, 4, 3, 2, 1}`. Test with both an even-length and odd-length array to be thorough.

---

### 🔴 Exercise 08 — `ft_sort_int_tab`

**Skill this builds:** Your first real sorting algorithm — combining loops, comparisons, and swaps into something genuinely useful.

**The problem, plainly:** Given an array of `int`s and its size, sort the array in ascending order, in place.

**Ways to think about it:**
- You don't need a fancy algorithm here — a simple, beginner-friendly approach like **bubble sort** or **selection sort** is completely fine (and a great learning exercise in itself):
  - **Bubble sort idea:** repeatedly walk through the array comparing *neighboring* pairs, swapping them if they're in the wrong order, and repeat this pass multiple times until nothing needs swapping anymore.
  - **Selection sort idea:** repeatedly find the *smallest* remaining unsorted element and swap it into its correct position, one slot at a time, moving left to right through the array.
- Either way, you'll lean heavily on: nested loops (one to control your "pass" or "position," one to scan/compare), and the swap logic you already built muscle memory for in ex02/ex07.

**Conceptual walkthrough (bubble-sort flavored, just one way to think about it):**
1. Repeat the following pass across the whole array, multiple times:
   - Walk through neighboring pairs of elements.
   - If a pair is out of order (left one bigger than right one), swap them.
2. Keep repeating full passes until you complete an entire pass with **no swaps** — that's your signal the array is fully sorted.
3. (Optional optimization once it works: each pass can safely ignore the last few elements that are now guaranteed to be in their final position, shrinking the "unsorted zone" each time.)

**Common pitfalls:**
- Off-by-one errors in your inner loop's boundary (comparing `tab[i]` and `tab[i + 1]` — make sure `i + 1` never runs off the end of the array).
- Forgetting to actually detect "no swaps happened" if you're using that early-exit optimization, leading to unnecessary extra passes (not wrong, just less efficient — fine for now!).
- Same swap-logic slip as always: forgetting the temporary variable and losing a value mid-swap.
- Testing only with already-sorted or tiny arrays — always test with a properly scrambled array, plus edge cases like a 1-element or 0-element array.

**How to test it:**
```bash
cc -Wall -Wextra -Werror ft_sort_int_tab.c -o test
```
Local test: build a deliberately scrambled array like `{5, 3, 4, 1, 2}`, call `ft_sort_int_tab(tab, 5)`, and confirm the array reads `{1, 2, 3, 4, 5}` afterward. Also try an already-sorted array and a reverse-sorted array to stress-test your logic.

---

## 6. 🧩 Function Types Reference

### `void` vs. returning functions

- **`void` functions** (almost all of C01!) do their work by **modifying memory through pointers**, rather than handing a computed value back. This is the entire theme of this module: learning to communicate results "sideways," through addresses, instead of only through `return`.
- **Returning functions** (like `ft_strlen`, which returns `int`) compute a value and hand it directly back to the caller — simpler when you only need *one* result and don't need to touch the caller's original variables.

### Iterative vs. recursive

- **Iterative** (loops): used throughout C01 — walking strings (`ft_strlen`, `ft_putstr`), walking/swapping array elements (`ft_rev_int_tab`, `ft_sort_int_tab`).
- **Recursive**: not really needed for C01's exercises, but worth remembering as a tool for later — especially once problems involve "process a smaller version of the same problem" patterns, like you may have seen in C00's combination exercises.

### How to decide which to use here

- Need to change a value that lives in the **caller's** scope, and it's just *one* value? → A single pointer parameter, dereferenced and assigned (`ft_ft`, `ft_swap`'s components).
- Need to hand back **more than one** result? → Multiple pointer parameters (`ft_div_mod`).
- Need to process **every element** of a string or array? → A loop, walking forward (and sometimes also backward, like ex07's two-pointer approach).
- Need to reorder or repeatedly compare elements? → Nested loops, usually paired with the swap pattern (ex07, ex08).

---

## 7. 🎉 Final Pep Talk

Pointers are famously the moment where a lot of new C programmers hit their first real wall — and also the moment where things start feeling genuinely powerful. You're not just printing anymore; you're reaching into memory and changing the world outside your function. That's a big deal. 🔓

Some parting reminders straight from the subject itself:
- 🤝 Stuck on the "why does this even work" feeling with pointers? Talk it through out loud with a peer — pointers are notoriously easier to grasp by explaining/drawing them than by silently staring at code.
- 🧪 Draw it out! Sketch boxes-and-arrows diagrams of variables and the pointers pointing at them — this single habit demystifies 90% of pointer confusion.
- 🧹 Run `norminette -R CheckForbiddenSourceHeader` early and often.
- 🎯 Remember: 50% threshold today. Get the earlier exercises rock-solid before chasing every optional one.

Good luck — and welcome to the pointer club. 🏊‍♀️🔗

---

> 📌 *Guide compiled by* **Mboss** *(aka mbousebe)* *— C Piscine, C01. May your pointers never dangle.* 🐧🎯
