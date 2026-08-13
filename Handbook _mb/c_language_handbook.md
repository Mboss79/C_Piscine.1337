# 📘 C Language Handbook

> A complete guide to the C programming language for the 1337 Piscine.
>
> Every chapter is designed to support my journey through the 1337 Piscine.
> The handbook serves as both a learning guide and a long-term reference.

---

# 📖 Table of Contents

# Part I — Foundations

## 🧠 Chapter 1 — Introduction to C

- What is C?
- Why Learn C?
- History of C
- Why 42/1337 Uses C
- Advantages & Limitations
- Compilation Overview
- Writing Your First Program
- Program Execution Flow

---

## 🧠 Chapter 2 — Program Structure

- Source Files
- Header Files
- main()
- Statements
- Blocks
- Comments
- Preprocessor Directives
- Header Guards

---

# Part II — Computer Memory

## 🧠 Chapter 3 — Data Representation

- Bits
- Bytes
- Binary
- Decimal
- Hexadecimal
- ASCII
- Unicode
- Endianness

---

## 🧠 Chapter 4 — Memory

- RAM
- Variables in Memory
- Memory Addresses
- Stack
- Heap
- Code Segment
- Data Segment
- Memory Layout

---

# Part III — Variables & Types

## 📦 Chapter 5 — Variables

- Variables
- Identifiers
- Naming Rules
- Declaration
- Definition
- Initialization
- Assignment
- Constants

---

## 🔠 Chapter 6 — Data Types

- char
- int
- short
- long
- float
- double
- signed
- unsigned
- sizeof
- Type Conversion
- Overflow

---

# Part IV — Expressions

## ➕ Chapter 7 — Operators

- Arithmetic
- Assignment
- Comparison
- Logical
- Increment
- Decrement
- Bitwise
- Ternary
- sizeof

---

## 🔀 Chapter 8 — Control Flow

- if
- else
- switch
- while
- do while
- for
- break
- continue
- goto (theory only)

---

# Part V — Functions

## 🔧 Chapter 9 — Functions

- Function Declaration
- Definition
- Prototype
- Parameters
- Return Values
- Scope
- Storage Duration
- Recursion

---

# Part VI — Arrays & Strings

## 📚 Chapter 10 — Arrays

- One-dimensional Arrays
- Multi-dimensional Arrays
- Memory Layout
- Array Traversal

---

## 🔤 Chapter 11 — Strings

- Character Arrays
- String Literals
- Null Terminator
- Common Mistakes
- String Manipulation

---

# Part VII — Pointers

## 👉 Chapter 12 — Pointers

- Memory Addresses
- Pointer Variables
- Dereferencing
- Pointer Arithmetic
- NULL
- Pointer to Pointer
- Arrays & Pointers
- Function Pointers (Introduction)

---

# Part VIII — User Defined Types

## 🏗️ Chapter 13 — Structures

- struct
- typedef
- Nested Structures
- Passing Structures
- Arrays of Structures

---

## 📚 Chapter 14 — Enumerations

- enum
- Practical Uses

---

# Part IX — Dynamic Memory

## 🧠 Chapter 15 — Dynamic Memory

- malloc
- calloc
- realloc
- free
- Memory Leaks
- Dangling Pointers

---

# Part X — File Handling

## 📂 Chapter 16 — File I/O

- fopen
- fclose
- fread
- fwrite
- fprintf
- fscanf
- fgets
- fputs

---

# Part XI — Debugging

## 🐞 Chapter 17 — Common Errors

- Syntax Errors
- Compiler Errors
- Linker Errors
- Runtime Errors
- Segmentation Fault
- Undefined Behavior
- Buffer Overflow
- Memory Leaks

---

# Part XII — Professional Programming

## 🏆 Chapter 18 — Best Practices

- Readable Code
- Naming Conventions
- Code Organization
- Defensive Programming
- Code Review
- 42 Norm

---

# 📋 Final Appendix

- C Cheat Sheet
- ASCII Table
- Data Type Sizes
- Operator Precedence
- Common GCC Commands
- Useful Terminal Commands
- Glossary

# 📖 Part I — Foundations

Programming is much easier when you understand **how the computer thinks**.

Many beginners memorize syntax without understanding what actually happens inside the computer.

This handbook follows a different approach.

Instead of asking:

> "How do I write C code?"

we first ask:

> "How does the computer execute C code?"

Understanding the *why* before the *how* makes every future topic easier.

Throughout this handbook we will progressively build our knowledge from the smallest unit of information (a single bit) to complete software projects.

Every chapter builds on the previous one.

Do not skip chapters.

---

# 🧠 Chapter 1 — Introduction to C

> "Before writing code, understand the language you are about to learn."

---

## What is C?

C is a **general-purpose programming language** created to write software efficiently and with high performance.

Unlike many modern languages, C gives the programmer direct control over memory and the computer's hardware.

Because of this, C is often described as a middle-level programming language.

It combines:

- High-level programming features
- Low-level hardware control
It combines:

- High-level programming features
- Low-level hardware control

This balance makes C one of the most influential programming languages ever created.

---

## Why Learn C?

Learning C teaches much more than syntax.

It teaches how computers actually work.

While modern languages often hide many details,

C exposes concepts such as:

- Memory
- Variables
- CPU operations
- Data representation
- Pointers
- File management

Once you understand C,

learning languages like C++, Java, Rust, Go or Python becomes much easier.

---

## History of C

The C programming language was created by Dennis Ritchie at Bell Labs in 1972.

It was originally developed to rewrite the UNIX operating system.

It was originally developed to rewrite the UNIX operating system.

Before C,

operating systems were mostly written in Assembly.

C allowed software to become:

- Faster to develop
- Easier to maintain
- Portable across different hardware

Today,

billions of devices still rely on software written in C.

---

## Why Does 42 / 1337 Teach C?

42 does not teach C because it is the newest language.

It teaches C because it builds strong programming fundamentals.

By learning C first,

students understand concepts that many programmers never fully learn, including:

- Memory management
- Program execution
- Compilation
- Pointers
- Performance
- Manual resource management

Once these concepts become natural,

other programming languages become significantly easier.

---

## Advantages of C

✔ Extremely fast

✔ Portable

✔ Small runtime

✔ Predictable performance

✔ Direct memory access

✔ Used in operating systems

✔ Used in embedded systems

✔ Used in game engines

✔ Excellent for learning computer science

---

## Limitations of C

✘ No automatic memory management

✘ No built-in classes

✘ No garbage collector

✘ Easier to introduce memory bugs

✘ Requires careful programming

These limitations are intentional.

They force programmers to understand what the computer is actually doing.

---

## Where is C Used?

Even today,

C is everywhere.

Examples include:

- Operating Systems
- Operating System Kernels
- Device Drivers
- Embedded Systems
- Networking Software
- Databases
- Compilers
- Game Engines
- Robotics
- Microcontrollers
- High-performance Applications

---

## What You Will Learn

By the end of this handbook,

you will understand:

- How data is stored
- How memory works
- How variables exist in RAM
- How functions execute
- How arrays are organized
- How pointers really work
- How files are managed
- How software communicates with the operating system

More importantly,

you will understand **why** these things work.

---

## Coach Philosophy

This handbook does not aim to teach you how to memorize C.

It aims to teach you how to think like a programmer.

Understanding always comes before memorization.

Every concept will be explained visually,

step by step,

from the computer's point of view.

---

# 🧠 Chapter 2 — Program Structure

> "Every C program follows a structure. Understanding this structure is more important than memorizing syntax."

---

## Introduction

Every C program, whether it contains 10 lines or 10 million lines, is built from the same fundamental components.

Understanding these components allows you to read unfamiliar programs and organize your own code professionally.

Throughout your journey, the complexity of your programs will increase, but the basic structure will remain the same.

---

# Source Files

## What is a Source File?

A source file is a text file containing C source code.

Its extension is:

```text
.c
```

Examples:

```text
hello.c

main.c

utils.c

parser.c
```

A source file contains instructions written by the programmer.

The CPU **cannot execute** a source file directly.

It must first be compiled into machine code.

---

## Characteristics

✔ Human-readable

✔ Editable with any text editor

✔ Contains C instructions

✔ Must be compiled

---

## Mental Model

```
Programmer

↓

hello.c

↓

GCC

↓

Executable
```

---

# Header Files

## What is a Header File?

A header file contains declarations that can be shared between multiple source files.

Its extension is:

```text
.h
```

Examples:

```text
stdio.h

stdlib.h

unistd.h

math.h

libft.h
```

Header files usually contain:

- Function declarations
- Constants
- Macros
- Structures
- Type definitions

---

## File Extensions

| Extension | Purpose |
|-----------|---------|
| `.h` | Contains declarations (functions, macros, types, constants) shared between source files. |
| `.c` | Contains implementations (function definitions and executable code). |

---

### Remember

```text
.h

↓

Declarations
```

```text
.c

↓

Implementations
```

A common rule:

```
Declare in .h

Define in .c
```


## Why Use Header Files?

Without headers,

every source file would have to redefine everything manually.

Headers allow code reuse.

---

## Mental Model

Think of a header file as the **table of contents** of a book.

It tells you what exists,

without showing every implementation.

---

# The main() Function

Every C program starts execution inside:

```c
int main(void)
{
    return (0);
}
```

The operating system calls `main()` when the executable starts.

No matter how many functions your program contains,

execution always begins here.

---

## Why is it Called main?

Because it is the program's entry point.

Without `main()`, a normal C program cannot start.

---

## Mental Model

```
Operating System

↓

main()

↓

Rest of the Program
```

---

# Statements

A statement is a single instruction executed by the computer.

Examples:

```c
printf("Hello\n");
```

```c
x = 5;
```

```c
return (0);
```

Each statement usually ends with:

```text
;
```

The semicolon tells the compiler:

> "This instruction is complete."

---

## Common Mistake

Forgetting the semicolon.

Example:

```c
printf("Hello")
```

This produces a compilation error.

---

# Blocks

A block is a group of statements enclosed by braces.

Example:

```c
{
    int x = 5;
    printf("%d\n", x);
}
```

Blocks organize code and define scope.

Almost every control structure in C uses blocks.

Examples include:

- Functions
- if
- while
- for

---

## Mental Model

Think of a block as a room.

Variables created inside the room usually belong only to that room.

---

# Comments

Comments are ignored by the compiler.

They exist only for humans.

---

## Single-line Comment

```c
// This is a comment
```

---

## Multi-line Comment

```c
/*
    This is
    a multi-line
    comment.
*/
```

---

## Why Write Comments?

Comments explain:

- Why code exists
- Complex algorithms
- Important decisions

They should not explain obvious code.

Bad example:

```c
x++;


// Increase x
```

Good comments explain intent,

not syntax.

---

# Preprocessor Directives

Lines beginning with:

```text
#
```

are processed before compilation.

Example:

```c
#include <stdio.h>
```

The preprocessor copies the contents of the requested header before compilation begins.

Other examples:

```c
#define

#ifdef

#ifndef
```

These will be studied later.

---

## Mental Model

```
Source File

↓

Preprocessor

↓

Compiler
```

The preprocessor prepares the source code.

It does not compile it.

---

# Header Guards

Header guards prevent the same header from being included multiple times.

Example:

```c
#ifndef LIBFT_H
#define LIBFT_H

/* declarations */

#endif
```

Without header guards,

the compiler may encounter duplicate declarations.

---

## Mental Model

Imagine a security guard checking tickets.

If you've already entered,

you're not allowed inside again.

Header guards do the same thing for header files.

---

# Complete Program Structure

```c
#include <stdio.h>

int main(void)
{
    printf("Hello, World!\n");
    return (0);
}
```

Let's identify each part:

```
#include <stdio.h>

↓

Preprocessor Directive

------------------------

int main(void)

↓

Program Entry Point

------------------------

{

↓

Block

------------------------

printf("Hello\n");

↓

Statement

------------------------

return (0);

↓

Statement

------------------------

}

↓

End of Block
```

---

## 📚 Summary

A C program is built from several components.

Source files contain code.

Header files share declarations.

Execution begins in `main()`.

Statements perform individual actions.

Blocks group statements together.

Comments help humans.

The preprocessor prepares code before compilation.

Header guards prevent duplicate inclusions.

---

## 🧠 Key Concepts

- Source File
- Header File
- main()
- Statement
- Block
- Comment
- Preprocessor
- Header Guard

---

## ⚠ Common Mistakes

- Forgetting the semicolon.
- Forgetting `main()`.
- Confusing `.c` and `.h`.
- Thinking comments affect execution.
- Forgetting braces.

---

## 💡 Coach Tips

✔ Learn the structure before writing complex programs.

✔ Every large project is built from these same components.

✔ Read code by identifying its structure first.

✔ Good organization is as important as correct syntax.

---

## 🚀 Mastery Checklist

- [ ] I know the purpose of a source file.
- [ ] I know the purpose of a header file.
- [ ] I understand why `main()` exists.
- [ ] I can identify statements.
- [ ] I understand what blocks are.
- [ ] I know the purpose of comments.
- [ ] I understand what the preprocessor does.
- [ ] I know why header guards exist.

---

# 📖 Part II — Computer Memory

Computers do not understand words, numbers, variables, or functions.

Everything inside a computer is ultimately represented as electrical signals.

From these signals, the computer builds bits.

Bits build bytes.

Bytes build memory.

Memory stores data.

Data becomes variables.

Variables become programs.

Understanding this chain is one of the biggest differences between someone who simply writes C code and someone who truly understands C.

In this part of the handbook, we begin exploring how information is represented inside a computer.

---

# 🧠 Chapter 3 — Data Representation

> "Every image, every song, every video, every number, and every program is ultimately stored as bits."

---

## Introduction

When we look at a computer, we see:

- Text
- Pictures
- Videos
- Games
- Websites
- Applications

To us, these appear completely different.

To the computer...

they are all exactly the same.

Everything is just numbers.

More specifically,

everything is just **binary digits**.

Understanding how computers represent information is the first step toward understanding memory, variables, pointers, and every advanced C concept.

---

## Why Learn Data Representation?

Many beginners think variables "store numbers."

That is only partially true.

Variables actually store **binary patterns** inside memory.

For example,

the number:

```text
25
```

is not stored as the characters:

```text
2
5
```

Instead,

it is stored internally as binary.

Likewise,

the letter:

```text
A
```

is not stored as a letter.

It is stored as a binary value according to the ASCII table.

Even colors, sounds, and videos are ultimately represented using binary.

Understanding this concept changes the way you think about programming.

---

## Learning Roadmap

In this chapter we will learn:

```
Electric Signals
        ↓
Bit
        ↓
Byte
        ↓
Binary Numbers
        ↓
Decimal Numbers
        ↓
Hexadecimal Numbers
        ↓
ASCII
        ↓
Unicode
        ↓
Endianness
```

Each concept builds directly on the previous one.

Do not skip sections.

---

# What is Data?

Data is any information that a computer can store or process.

Examples include:

- Numbers
- Characters
- Images
- Audio
- Video
- Programs
- Files

Although these appear different,

they are all stored in the same way:

Binary.

---

## Real-World Examples

When you save:

```
photo.jpg
```

the computer stores binary.

When you save:

```
music.mp3
```

the computer stores binary.

When you write:

```c
int age = 25;
```

the computer stores binary.

Everything eventually becomes bits.

---

## Mental Model

```
Your Program

↓

Variables

↓

Memory

↓

Bytes

↓

Bits

↓

Electrical Signals
```

The programmer thinks about variables.

The computer thinks about bits.

---

## Key Question

Throughout this chapter, keep asking yourself:

> "How would the computer represent this using only zeros and ones?"

That single question will help you understand almost every future topic in C.

---

## 📚 Summary

Computers do not understand text, images, or variables directly.

Everything is represented using binary.

This chapter explains how information is transformed from human-readable data into patterns of bits stored in memory.

Understanding data representation is essential before learning variables, memory, pointers, or dynamic allocation.

---

## 🧠 Key Concepts

- Data
- Representation
- Binary
- Memory
- Bits
- Bytes

---

## ⚠ Common Mistakes

- Thinking computers store letters directly.
- Thinking numbers are stored exactly as we write them.
- Confusing data with its representation.
- Ignoring that every data type ultimately becomes binary.

---

## 💡 Coach Tips

✔ Don't memorize binary yet.

✔ Focus on understanding the overall idea.

✔ Every future chapter builds on this one.

✔ Think like the computer, not like the programmer.

---

## 🚀 Mastery Checklist

- [ ] I understand what data is.
- [ ] I know that computers store everything in binary.
- [ ] I understand why data representation matters.
- [ ] I know the learning roadmap for this chapter.
- [ ] I am ready to learn what a bit is.

---
# What is a Bit?

> "The bit is the smallest unit of information a computer can store."

---

## Introduction

The word **Bit** comes from:

```
Binary Digit
```

A bit can store **only one of two possible values**:

```
0

or

1
```

Nothing else.

A bit **cannot** store:

```
2

5

A

Hello

3.14
```

Only:

```
0

or

1
```

---

## Why Only Two Values?

Computers are built from billions of tiny electronic switches called **transistors**.

A transistor has only two stable states:

```
OFF

ON
```

These physical states are represented digitally as:

```
OFF → 0

ON → 1
```

Therefore,

the computer naturally stores information using only zeros and ones.

---

## Visual Representation

Imagine a light switch.

```
OFF

↓

0
```

```
ON

↓

1
```

Every transistor inside your CPU behaves similarly.

Modern processors contain **billions of these switches**.

---

## Real Example

One bit can answer a Yes/No question.

```
Is the light on?

0 → No

1 → Yes
```

```
Is the door open?

0 → Closed

1 → Open
```

```
Is the player alive?

0 → No

1 → Yes
```

One bit is perfect for storing information with only two possibilities.

---

## Limitation of a Single Bit

A single bit is extremely limited.

It can represent only:

```
0

1
```

Suppose we want to represent:

```
0

1

2

3
```

One bit is no longer enough.

We need multiple bits working together.

This leads us to the next concept:

**Bytes.**

---

## Mental Model

Think of a bit as a single light bulb.

```
💡 OFF

↓

0
```

```
💡 ON

↓

1
```

One light bulb cannot display much information.

A room filled with thousands of light bulbs can create complex images.

Computers work in a very similar way.

---

## Where Are Bits Used?

Bits are everywhere.

They represent:

- Numbers
- Letters
- Images
- Videos
- Music
- Programs
- Memory
- CPU Instructions

Everything eventually becomes combinations of bits.

---

## Fun Fact

Your computer does **not** think in:

- English
- Arabic
- French

It does **not** understand:

```
Hello
```

Nor does it understand:

```
42
```

Internally,

it only understands long sequences like:

```
010011010110010101...
```

The operating system and programs translate these binary patterns into forms humans can understand.

---

## 📚 Summary

A bit is the smallest unit of digital information.

It can store only:

```
0

or

1
```

Bits correspond to the physical ON/OFF states of electronic transistors.

Although a single bit stores very little information, combining many bits allows computers to represent every kind of data.

---

## 🧠 Key Concepts

- Bit
- Binary Digit
- ON
- OFF
- 0
- 1
- Transistor

---

## ⚠ Common Mistakes

- Thinking a bit can store any number.
- Confusing a bit with a byte.
- Believing computers naturally understand text.
- Forgetting that everything starts as bits.

---

## 💡 Coach Tips

✔ Never memorize before understanding.

✔ Imagine a light switch whenever you hear "bit."

✔ Every future topic in C depends on understanding bits.

✔ One bit stores only two possibilities.

---

## 🚀 Mastery Checklist

- [ ] I know what a bit is.
- [ ] I know why computers use bits.
- [ ] I understand the relationship between transistors and bits.
- [ ] I know that a bit stores only 0 or 1.
- [ ] I understand why one bit is not enough to represent most information.

---
# What is a Byte?

> "A byte is a group of eight bits."

---

## Introduction

A single bit can only represent:

```
0

or

1
```

That is not enough to represent useful information.

To solve this problem,

computers combine multiple bits together.

The most common group is called a **Byte**.

```
1 Byte = 8 Bits
```

Every modern computer uses bytes as the basic unit for storing data.

---

## Visual Representation

One bit:

```
1
```

Eight bits:

```
10110010
```

This entire sequence is called **one byte**.

Notice that:

```
10110010
```

is **not** eight separate numbers.

It is **one byte** made of eight bits.

---

## Why Eight Bits?

Early computers used different byte sizes.

Some computers used:

```
6 Bits

7 Bits

8 Bits

9 Bits
```

Eventually,

**8 bits** became the worldwide standard.

Today,

almost every computer uses:

```
1 Byte = 8 Bits
```

---

## How Many Values Can One Byte Store?

Each bit has two possible values.

```
0

or

1
```

If we have:

```
8 Bits
```

the total number of possible combinations is:

```
2 × 2 × 2 × 2 × 2 × 2 × 2 × 2

=

2⁸

=

256
```

Therefore,

one byte can represent:

```
256 different values
```

---

## Range of Values

For unsigned values:

```
0

↓

255
```

There are exactly:

```
256 values
```

Later,

we will learn why signed numbers have a different range.

---

## Examples of Bytes

One byte can store:

```
01000001
```

which represents the letter:

```
A
```

Another byte:

```
00110001
```

represents:

```
1
```

Another byte:

```
11111111
```

represents:

```
255
```

(or -1 depending on the data type.)

---

## Bytes in Memory

Imagine RAM as a long row of boxes.

Each box stores exactly one byte.

```
+--------+
|10101011|
+--------+

+--------+
|00110010|
+--------+

+--------+
|11110000|
+--------+
```

Each box contains:

```
8 Bits
```

Programs are stored using millions (or billions) of these boxes.

---

## Memory Sizes

Bytes are combined to create larger units.

```
8 Bits

↓

1 Byte
```

```
1024 Bytes

↓

1 KB
```

```
1024 KB

↓

1 MB
```

```
1024 MB

↓

1 GB
```

```
1024 GB

↓

1 TB
```

Modern computers usually have:

```
8 GB

16 GB

32 GB

64 GB
```

of RAM.

---

## Real-World Examples

A character:

```
'A'
```

usually occupies:

```
1 Byte
```

A file containing:

```
1000 characters
```

occupies approximately:

```
1000 Bytes
```

A picture may require:

```
Millions of Bytes.
```

A video may require:

```
Billions of Bytes.
```

---

## Mental Model

Think of a bit as a LEGO block.

```
🧱
```

One block cannot build much.

Now imagine eight LEGO blocks connected together.

```
🧱🧱🧱🧱🧱🧱🧱🧱
```

That group is a **Byte**.

Thousands or millions of bytes together create files, images, videos, and programs.

---

## Relationship Between Bits and Bytes

```
Electrical Signal

↓

Bit

↓

Byte

↓

Memory

↓

Variables

↓

Programs
```

Everything inside a computer follows this chain.

---

## 📚 Summary

A byte is a group of eight bits.

Modern computers use bytes as the basic unit for storing information.

One byte contains:

```
8 Bits
```

and can represent:

```
256 different values.
```

Bytes combine together to create larger memory units such as kilobytes, megabytes, gigabytes, and terabytes.

---

## 🧠 Key Concepts

- Byte
- 8 Bits
- 256 Values
- Memory
- KB
- MB
- GB
- TB

---

## ⚠ Common Mistakes

- Confusing bits with bytes.
- Thinking one byte stores only one bit.
- Confusing MB with Mb.
- Believing a byte can store unlimited values.

---

## 💡 Coach Tips

✔ Remember:

```
bit
```

uses a lowercase **b**.

```
Byte
```

uses an uppercase **B**.

For example:

```
Mbps ≠ MB/s
```

These are completely different units.

✔ Most variables occupy one or more bytes.

✔ Every address in memory points to a byte.

---

## 🧩 Think Like the Computer

If:

```
1 Bit = 2 possibilities
```

How many possibilities can:

- 2 Bits represent?
- 4 Bits represent?
- 16 Bits represent?

Try to calculate the answers before continuing.

---

## 🚀 Mastery Checklist

- [ ] I know what a byte is.
- [ ] I know that one byte contains eight bits.
- [ ] I understand why computers use bytes.
- [ ] I know that one byte represents 256 values.
- [ ] I understand the relationship between bits, bytes, and memory.
- [ ] I can distinguish between b and B.

---

# Binary Number System

> "Humans naturally count using ten digits. Computers count using only two."

---

## Introduction

Every day, we use the **Decimal Number System**.

For example:

```
0
1
2
3
4
5
6
7
8
9
10
11
12
...
```

This system is called **Decimal** because it is based on:

```
10 digits
```

```
0 1 2 3 4 5 6 7 8 9
```

Humans use decimal because we naturally count using our ten fingers.

Computers, however, do not have fingers.

They use electronic switches that can only be:

```
OFF

or

ON
```

Therefore, computers use the **Binary Number System**.

---

## What is Binary?

Binary is a numbering system that uses only:

```
0

1
```

Instead of ten digits,

binary has only two.

```
Decimal

↓

0 1 2 3 4 5 6 7 8 9

----------------------------

Binary

↓

0 1
```

Every number inside a computer is represented using combinations of these two digits.

---

## Why Do Computers Use Binary?

Imagine trying to build a computer using light switches.

Each switch has only two states.

```
OFF

↓

0
```

```
ON

↓

1
```

Since billions of transistors behave exactly like switches,

the computer naturally represents information using binary.

Using ten different electrical states would be much slower,

much more expensive,

and much less reliable.

Binary is simple,

fast,

and extremely dependable.

---

## Counting in Binary

Humans count like this:

```
0
1
2
3
4
5
6
7
8
9
10
11
12
```

Computers count differently.

```
Decimal      Binary

0            0

1            1

2            10

3            11

4            100

5            101

6            110

7            111

8            1000

9            1001

10           1010
```

Notice something interesting.

Binary numbers become longer much faster because only two digits are available.

---

## Binary is NOT Random

Many beginners see this:

```
10110101
```

and think:

> "That's just random zeros and ones."

It isn't.

Binary follows strict mathematical rules,

just like decimal.

Once you understand those rules,

binary becomes just another way of writing numbers.

---

## Binary Place Values

In decimal,

each position represents a power of ten.

```
583

↓

5 × 100

8 × 10

3 × 1
```

Binary works exactly the same way,

except each position represents a power of two.

```
128

64

32

16

8

4

2

1
```

Example:

```
10110010
```

can be viewed as:

```
128   64   32   16   8   4   2   1

 1     0    1    1   0   0   1   0
```

We'll learn how to convert this shortly.

---

## Binary in Memory

Imagine eight switches.

```
OFF OFF OFF OFF OFF OFF OFF OFF
```

becomes

```
00000000
```

Turn on only the last switch.

```
00000001
```

Turn on the last two.

```
00000011
```

Turn on different switches.

```
10100110
```

Every combination represents a different value.

---

## Mental Model

Imagine a row of eight lamps.

```
💡 💡 💡 💡 💡 💡 💡 💡
```

Each lamp can be:

```
OFF

or

ON
```

Different ON/OFF combinations create different binary numbers.

Computers use this exact idea billions of times every second.

---

## Why Should C Programmers Learn Binary?

Because C works very close to hardware.

Understanding binary helps explain:

- Variables
- Memory
- Characters
- Integers
- Bitwise Operators
- Pointers
- File Formats

Without binary,

many advanced C topics seem mysterious.

With binary,

they become logical.

---

## 📚 Summary

Binary is the numbering system used by computers.

It contains only two digits:

```
0

1
```

Binary exists because computer hardware naturally has two stable electrical states.

Every number,

every character,

every image,

every instruction,

is ultimately represented as binary.

---

## 🧠 Key Concepts

- Binary
- Base 2
- Bits
- Powers of Two
- ON
- OFF

---

## ⚠ Common Mistakes

- Thinking binary is a different kind of number.
- Believing binary is random.
- Forgetting that binary follows mathematical rules.
- Confusing binary digits with decimal digits.

---

## 💡 Coach Tips

✔ Binary is simply another way of writing numbers.

✔ Never memorize binary tables.

✔ Understand the pattern instead.

✔ Decimal and binary represent the same values using different symbols.

---

## 🧩 Think Like the Computer

Without calculating,

predict:

Which number is larger?

```
1010

or

1001
```

How do you know?

We'll learn the exact method in the next section.

---

## 🚀 Mastery Checklist

- [ ] I know what binary is.
- [ ] I know why computers use binary.
- [ ] I understand why binary uses only 0 and 1.
- [ ] I know that binary is a numbering system.
- [ ] I understand that binary follows mathematical rules.

---

# Decimal Number System

> "Decimal is the numbering system humans use every day."

---

## Introduction

The **Decimal Number System** is the most familiar numbering system in the world.

Every number you normally read or write is written in decimal.

Examples:

```
7

25

1337

2026

1000000
```

All of these are decimal numbers.

---

## Why is it Called Decimal?

The word **Decimal** comes from the Latin word:

```
Decem
```

which means:

```
Ten
```

This numbering system uses exactly **10 different digits**.

```
0

1

2

3

4

5

6

7

8

9
```

Once we reach:

```
9
```

there are no more digits.

Instead,

we create a new position.

```
9

↓

10
```

The cycle starts again.

---

## Place Values

The position of each digit determines its value.

Example:

```
583
```

This does **not** mean:

```
5

8

3
```

Instead it means:

```
5 × 100

+

8 × 10

+

3 × 1
```

Or:

```
5 × 10²

+

8 × 10¹

+

3 × 10⁰
```

Notice the powers of ten.

```
10²

10¹

10⁰
```

This is why the system is called **Base 10**.

---

## Decimal Place Value Table

```
1000 | 100 | 10 | 1

10³  |10² |10¹|10⁰
```

Example:

```
2745
```

becomes:

```
2 × 1000

+

7 × 100

+

4 × 10

+

5 × 1
```

---

## Counting in Decimal

Decimal counting follows a simple pattern.

```
0

1

2

3

4

5

6

7

8

9

10

11

12

13

...
```

Every time the last position reaches:

```
9
```

it resets to:

```
0
```

while the digit to its left increases by one.

---

## Decimal vs Binary

Humans count using:

```
10 digits
```

Computers count using:

```
2 digits
```

Comparison:

```
Decimal

0

1

2

3

4

5

6

7

8

9

10

-------------------------

Binary

0

1

10

11

100

101

110

111

1000

1001

1010
```

Although the symbols look different,

they represent the **same quantities**.

---

## Why Programmers Need Decimal

Programmers constantly move between:

- Decimal
- Binary
- Hexadecimal

Users usually think in decimal.

Computers work in binary.

Programmers act as translators between both worlds.

Understanding decimal place values makes binary much easier to learn.

---

## Mental Model

Imagine an odometer in a car.

```
000009
```

After:

```
9
```

comes:

```
10
```

The last wheel returns to:

```
0
```

while the previous wheel increases.

Binary behaves exactly the same way,

except each wheel only has:

```
0

1
```

instead of ten digits.

---

## Real-World Examples

Money

```
25 DH
```

Age

```
26 Years
```

Temperature

```
34°C
```

Phone Numbers

```
0612345678
```

Years

```
2026
```

All of these are written in decimal.

---

## 📚 Summary

Decimal is the numbering system used by humans.

It contains ten digits.

Each position represents a power of ten.

Understanding decimal makes learning binary much easier because both systems follow the same mathematical principles.

---

## 🧠 Key Concepts

- Decimal
- Base 10
- Digits
- Place Value
- Powers of Ten

---

## ⚠ Common Mistakes

- Thinking decimal is the only numbering system.
- Forgetting that digit position changes value.
- Confusing a digit with the value it represents.

---

## 💡 Coach Tips

✔ Binary is not "hard."

✔ Binary is simply decimal with a different base.

✔ Master place values before learning conversions.

✔ Every numbering system follows the same logic.

---

## 🧩 Think Like the Computer

Why does this happen?

```
9

↓

10
```

instead of

```
10

↓

11
```

Think about the role of **place values** before moving to the next section.

---

## 🚀 Mastery Checklist

- [ ] I know why decimal is called Base 10.
- [ ] I know the ten decimal digits.
- [ ] I understand place values.
- [ ] I understand powers of ten.
- [ ] I know how decimal differs from binary.

---

# 🔄 Decimal ↔ Binary Conversion

> "Decimal and binary represent the same values using different numbering systems."

---

## Introduction

Humans naturally understand decimal numbers.

Computers naturally understand binary numbers.

Programmers often need to convert between both systems.

Fortunately,

the conversion follows simple mathematical rules.

---

# Converting Binary → Decimal

## Step 1

Write the powers of two.

Example:

```
Binary Number

10110110
```

Write the place values above each bit.

```
128   64   32   16   8   4   2   1

 1     0    1    1   0   1   1   0
```

---

## Step 2

Multiply each bit by its value.

```
1 × 128 = 128

0 × 64  = 0

1 × 32  = 32

1 × 16  = 16

0 × 8   = 0

1 × 4   = 4

1 × 2   = 2

0 × 1   = 0
```

---

## Step 3

Add everything together.

```
128

+

32

+

16

+

4

+

2

=

182
```

Therefore,

```
10110110₂

=

182₁₀
```

---

## Another Example

```
Binary

00101010
```

```
128 64 32 16 8 4 2 1

0   0  1  0 1 0 1 0
```

```
32

+

8

+

2

=

42
```

```
00101010₂

=

42₁₀
```

---

# Converting Decimal → Binary

This conversion uses repeated division.

---

## Example

Convert:

```
25
```

to binary.

---

### Divide by 2

```
25 ÷ 2

=

12

Remainder:

1
```

---

```
12 ÷ 2

=

6

Remainder:

0
```

---

```
6 ÷ 2

=

3

Remainder:

0
```

---

```
3 ÷ 2

=

1

Remainder:

1
```

---

```
1 ÷ 2

=

0

Remainder:

1
```

---

## Read the Remainders

Read them **from bottom to top**.

```
11001
```

Therefore,

```
25₁₀

=

11001₂
```

---

## Another Example

Convert:

```
13
```

```
13 ÷ 2

=

6

Remainder:

1
```

```
6 ÷ 2

=

3

Remainder:

0
```

```
3 ÷ 2

=

1

Remainder:

1
```

```
1 ÷ 2

=

0

Remainder:

1
```

Read upward.

```
1101
```

Therefore,

```
13₁₀

=

1101₂
```

---

# Quick Reference

```
Decimal     Binary

0           0

1           1

2           10

3           11

4           100

5           101

6           110

7           111

8           1000

9           1001

10          1010

11          1011

12          1100

13          1101

14          1110

15          1111

16          10000
```

---

# Mental Model

Imagine translating between two spoken languages.

```
English

↓

Arabic
```

The meaning stays the same.

Only the representation changes.

Binary and decimal work exactly the same way.

```
25

↓

11001
```

Same value.

Different representation.

---

# 📚 Summary

Binary and decimal represent the same numbers.

To convert:

Binary → Decimal

Multiply each bit by its power of two.

Decimal → Binary

Repeatedly divide by two and read the remainders upward.

---

## 🧠 Key Concepts

- Base 2
- Base 10
- Powers of Two
- Division by Two
- Place Values

---

## ⚠ Common Mistakes

- Reading remainders from top to bottom.
- Forgetting powers of two.
- Mixing decimal place values with binary place values.
- Thinking the value changes after conversion.

---

## 💡 Coach Tips

✔ Binary is simply another representation of the same value.

✔ Always write the powers of two first.

✔ Practice with small numbers before larger ones.

✔ Conversion becomes automatic with repetition.

---

## 🧩 Think Like the Computer

Without calculating,

what is:

```
11111111₂
```

in decimal?

How many different values can:

```
8 bits
```

represent?

---

## 🚀 Mastery Checklist

- [ ] I can convert binary to decimal.
- [ ] I can convert decimal to binary.
- [ ] I know the powers of two.
- [ ] I understand that conversions do not change the value.
- [ ] I can solve simple conversion problems without help.

---

# Hexadecimal Number System

> "Hexadecimal is a compact and human-friendly way to represent binary numbers."

---

## Introduction

Binary is perfect for computers.

Humans, however, find long binary numbers difficult to read.

For example:

```
1111000010101100
```

Although correct,

it is difficult to read,

easy to mistype,

and hard to remember.

To solve this problem,

computer scientists introduced another numbering system:

**Hexadecimal**.

Hexadecimal is simply a shorter way of writing binary numbers.

---

## What is Hexadecimal?

Hexadecimal is a numbering system based on:

```
16 symbols
```

Unlike decimal,

which has ten digits,

hexadecimal uses sixteen symbols.

```
0
1
2
3
4
5
6
7
8
9
A
B
C
D
E
F
```

---

## What Do the Letters Mean?

The letters represent decimal values.

```
Hex      Decimal

A         10

B         11

C         12

D         13

E         14

F         15
```

Therefore,

```
F

=

15
```

---

## Why Base 16?

Binary becomes very long.

Example:

```
11111111
```

Decimal:

```
255
```

Hexadecimal:

```
FF
```

Much shorter.

Much easier to read.

---

## Relationship Between Binary and Hexadecimal

One hexadecimal digit represents exactly:

```
4 Bits
```

Example:

```
Binary

1010

↓

Hex

A
```

Another example:

```
1111

↓

F
```

Another example:

```
0000

↓

0
```

---

## Binary ↔ Hex Table

```
Binary     Hex

0000        0

0001        1

0010        2

0011        3

0100        4

0101        5

0110        6

0111        7

1000        8

1001        9

1010        A

1011        B

1100        C

1101        D

1110        E

1111        F
```

This table is one of the most useful tables in Computer Science.

---

## Example

Convert:

```
10101111
```

Split into groups of four.

```
1010

1111
```

Convert each group.

```
1010

↓

A
```

```
1111

↓

F
```

Result:

```
AF
```

Therefore,

```
10101111₂

=

AF₁₆
```

---

## Another Example

Convert:

```
11001010
```

Split:

```
1100

1010
```

Convert.

```
1100

↓

C
```

```
1010

↓

A
```

Final answer.

```
CA
```

---

## Hexadecimal Prefix

In programming,

hexadecimal numbers are usually written with:

```
0x
```

Examples:

```c
0x2A

0xFF

0x7F

0x100
```

The prefix tells both the programmer and the compiler:

"This number is hexadecimal."

---

## Why Programmers Love Hexadecimal

Suppose we want to inspect memory.

Binary:

```
1111000010101100
```

Hexadecimal:

```
F0AC
```

Much easier to read.

Memory addresses,

machine instructions,

colors,

network packets,

and debuggers all use hexadecimal extensively.

---

## Real-World Examples

Color:

```
#FFFFFF
```

White

```
#000000
```

Black

Memory Address:

```
0x7FFE12A0
```

Machine Code

```
0x90
```

These values are hexadecimal.

---

## Mental Model

Think of hexadecimal as an abbreviation.

Instead of writing:

```
11111111
```

you simply write:

```
FF
```

Both represent the same value.

---

## Decimal vs Binary vs Hexadecimal

```
Decimal     Binary        Hex

10          1010          A

15          1111          F

16          10000         10

31          11111         1F

42          101010        2A

255         11111111      FF
```

Notice that

the value never changes.

Only its representation changes.

---

## 📚 Summary

Hexadecimal is a numbering system based on sixteen symbols.

It is widely used because it provides a compact representation of binary numbers.

Every hexadecimal digit represents exactly four bits.

Programmers use hexadecimal extensively when working with memory, debugging, and low-level programming.

---

## 🧠 Key Concepts

- Base 16
- Hexadecimal
- 0x Prefix
- Binary Groups
- Four Bits

---

## ⚠ Common Mistakes

- Forgetting that A represents 10.
- Thinking hexadecimal is different from binary.
- Forgetting the `0x` prefix in C code.
- Mixing decimal digits with hexadecimal digits.

---

## 💡 Coach Tips

✔ Learn the Binary ↔ Hex table by practice, not memorization.

✔ Every hexadecimal digit always represents four bits.

✔ Hexadecimal is designed for humans.

✔ Binary is designed for computers.

---

## 🧩 Think Like the Computer

Without calculating,

what is:

```
FFFF
```

written in binary?

How many bits does it contain?

Hint:

```
1 Hex Digit = 4 Bits
```

---

## 🏋️ Practice Exercises

Convert to hexadecimal.

```
10101010
```

---

Convert to hexadecimal.

```
11110000
```

---

Convert to binary.

```
2F
```

---

Convert to binary.

```
A9
```

---

Write the hexadecimal representation of:

```
255
```

---

## 🚀 Mastery Checklist

- [ ] I know what hexadecimal is.
- [ ] I know why programmers use hexadecimal.
- [ ] I know that one hexadecimal digit represents four bits.
- [ ] I can convert binary to hexadecimal.
- [ ] I can convert hexadecimal to binary.
- [ ] I know what the `0x` prefix means.

---

# ASCII (American Standard Code for Information Interchange)

> "ASCII is a standard that assigns a unique number to every character."

---

## Introduction

Computers do not understand letters.

They only understand numbers.

Suppose you write:

```c
printf("Hello");
```

The CPU does **not** see:

```
H

e

l

l

o
```

Instead,

it sees:

```
72

101

108

108

111
```

These numbers are defined by the **ASCII Standard**.

---

## What is ASCII?

ASCII stands for:

```
American Standard Code for Information Interchange
```

It is a standard table that assigns a numeric value to characters.

For example,

```
'A'
```

has a number.

```
65
```

```
'B'
```

has another number.

```
66
```

Every printable character has its own numeric value.

---

## Why Was ASCII Created?

Imagine two computers.

Computer A decides that:

```
A = 15
```

Computer B decides:

```
A = 93
```

They could never communicate correctly.

ASCII solved this problem by defining one common table used by every computer.

---

## ASCII Table (Partial)

```
Character      Decimal

A              65

B              66

C              67

D              68

E              69

...

Z              90

a              97

b              98

c              99

...

z              122

0              48

1              49

2              50

...

9              57

Space          32

!              33

?              63

New Line       10
```

---

## Example

When you write

```c
char letter = 'A';
```

The computer stores

```
65
```

inside memory.

When you write

```c
char number = '7';
```

The computer stores

```
55
```

Notice:

```
7

≠

'7'
```

These are completely different.

```
7

↓

Number
```

```
'7'

↓

ASCII Character
```

---

## Strings

Suppose we write

```c
"ABC"
```

Memory actually stores

```
65

66

67
```

Later,

we'll learn that another value is also stored.

```
0
```

called the **Null Terminator**.

---

## ASCII in Memory

Imagine RAM.

```
Address

1000

↓

65
```

```
1001

↓

66
```

```
1002

↓

67
```

The operating system later displays these values as:

```
ABC
```

---

## Real-World Examples

Keyboard

↓

ASCII

↓

Memory

↓

CPU

↓

Screen

Every time you press a key,

ASCII is involved.

---

## Why C Programmers Must Learn ASCII

ASCII explains many things.

Examples:

Why does this work?

```c
printf("%d\n", 'A');
```

Output

```
65
```

Why?

Because characters are numbers.

---

Another example.

```c
printf("%c\n", 66);
```

Output

```
B
```

Because

```
66

↓

B
```

according to ASCII.

---

## Mental Model

Imagine a dictionary.

```
A

↓

65
```

```
B

↓

66
```

```
!

↓

33
```

ASCII is simply a dictionary between characters and numbers.

---

## Limitations of ASCII

ASCII contains only:

```
128 Characters
```

This works well for English.

But what about:

```
العربية

日本語

中文

Русский

😀
```

ASCII cannot represent these characters.

A larger standard was needed.

This led to:

```
Unicode
```

---

## 📚 Summary

ASCII is a standard that assigns numeric values to characters.

Computers store those numbers,

not the characters themselves.

ASCII made communication between computers consistent and reliable.

Although still widely used,

ASCII is limited to a small set of characters.

---

## 🧠 Key Concepts

- ASCII
- Character Encoding
- Decimal Value
- Characters
- Numbers

---

## ⚠ Common Mistakes

- Thinking characters are stored directly.
- Confusing:

```
7

and

'7'
```

- Forgetting that characters are actually numbers.

---

## 💡 Coach Tips

✔ Memorize a few important ASCII values.

```
A = 65

a = 97

0 = 48
```

You don't need to memorize the entire table.

✔ Every character occupies one byte in standard ASCII.

✔ Understanding ASCII makes strings much easier later.

---

## 🧩 Think Like the Computer

Without searching,

predict the output.

```c
printf("%d\n", 'B');
```

What number will be printed?

Now predict.

```c
printf("%c\n", 67);
```

---

## 🏋️ Practice Exercises

Find the ASCII values of:

```
Z

a

9

?
```

---

Convert these numbers into characters.

```
72

73

74

75
```

---

Explain the difference between:

```
5

and

'5'
```

---

## 🚀 Mastery Checklist

- [ ] I know what ASCII is.
- [ ] I know why ASCII exists.
- [ ] I understand that characters are stored as numbers.
- [ ] I know the difference between `7` and `'7'`.
- [ ] I can use ASCII values in C.

---

# Unicode

> "Unicode is a universal standard that allows computers to represent characters from every language."

---

## Introduction

ASCII was a revolutionary standard.

However,

it had one major limitation.

ASCII contains only:

```
128 Characters
```

This is enough for:

- English letters
- Numbers
- Basic punctuation
- Control characters

But what about:

```
العربية

Français

Deutsch

日本語

中文

Русский

한국어

😀😂❤️🚀
```

ASCII cannot represent any of these.

To solve this problem,

Unicode was created.

---

## What is Unicode?

Unicode is a universal character encoding standard.

Its goal is simple:

> Every character in every language should have a unique number.

Unlike ASCII,

Unicode is not limited to English.

It supports almost every writing system used today.

---

## Why Was Unicode Created?

Imagine a document written in Arabic.

A computer using only ASCII would not know how to display:

```
مرحبا
```

Instead,

you might see strange symbols like:

```
Ù…Ø±Ø­Ø¨Ø§
```

or

```
?????
```

Unicode solves this problem by assigning a unique code to every character.

---

## Unicode Examples

```
Character        Unicode

A                U+0041

a                U+0061

0                U+0030

م                U+0645

ر                U+0631

ح                U+062D

😀               U+1F600

❤️               U+2764
```

Notice that every character has its own code.

---

## Unicode Code Points

Every Unicode character is identified by a unique value called a **Code Point**.

Examples:

```
A

↓

U+0041
```

```
م

↓

U+0645
```

```
😀

↓

U+1F600
```

The prefix:

```
U+
```

means:

```
Unicode Code Point
```

---

## Unicode vs ASCII

ASCII is actually part of Unicode.

The first 128 Unicode characters are exactly the ASCII table.

Example:

```
Character

A

ASCII

65

Unicode

U+0041
```

Therefore,

every ASCII character is also a Unicode character.

---

## Unicode is NOT UTF-8

Many beginners think:

```
Unicode

=

UTF-8
```

This is incorrect.

Unicode defines **which number belongs to each character**.

UTF-8 defines **how those numbers are stored in memory**.

Think of it like this:

Unicode

↓

Dictionary

UTF-8

↓

Storage Method

---

## UTF-8

UTF-8 is the most popular Unicode encoding today.

Advantages:

✔ Compatible with ASCII

✔ Efficient

✔ Supports every language

✔ Used on websites

✔ Used by Linux

✔ Used by modern programming languages

Most files you create today are encoded using UTF-8.

---

## Why C Programmers Should Know Unicode

Although many beginner C programs use ASCII,

real software often handles:

- Arabic
- French
- Chinese
- Emojis
- International filenames
- User input from different countries

Understanding Unicode helps explain why text processing becomes more complex.

---

## Real-World Example

Suppose you write:

```c
printf("مرحبا");
```

Your compiler stores Unicode characters,

not ASCII.

Modern terminals display those characters correctly because they understand UTF-8.

---

## Mental Model

Imagine the world's largest dictionary.

Every character ever created has its own page.

```
A

↓

Page 65
```

```
م

↓

Page U+0645
```

```
😀

↓

Page U+1F600
```

Unicode is that dictionary.

UTF-8 is the method used to store the pages efficiently.

---

## ASCII vs Unicode

| Feature | ASCII | Unicode |
|---------|-------|----------|
| Characters | 128 | Over 1 million possible code points |
| English | ✅ | ✅ |
| Arabic | ❌ | ✅ |
| Chinese | ❌ | ✅ |
| Emojis | ❌ | ✅ |
| Modern Software | Limited | Standard |

---

## 📚 Summary

Unicode is the universal standard for representing characters.

Unlike ASCII,

it supports nearly every language and symbol used today.

UTF-8 is the most common way of storing Unicode characters in memory.

Modern operating systems,

websites,

and programming languages rely heavily on Unicode.

---

## 🧠 Key Concepts

- Unicode
- Character Encoding
- Code Point
- UTF-8
- Internationalization

---

## ⚠ Common Mistakes

- Thinking Unicode and UTF-8 are the same.
- Believing ASCII supports every language.
- Assuming every character occupies one byte.
- Confusing code points with memory representation.

---

## 💡 Coach Tips

✔ Remember:

```
Unicode

↓

Character Standard
```

```
UTF-8

↓

Encoding Method
```

✔ ASCII is included inside Unicode.

✔ Most modern C projects use UTF-8 encoded source files.

---

## 🧩 Think Like the Computer

Suppose your program prints:

```c
printf("Hello مرحبا 😀");
```

How many writing systems are present?

Why can't ASCII represent this string correctly?

---

## 🏋️ Practice Exercises

1. Explain the difference between ASCII and Unicode.

2. Explain the difference between Unicode and UTF-8.

3. Why was Unicode created?

4. Give three examples of characters that ASCII cannot represent.

---

## 🚀 Mastery Checklist

- [ ] I know what Unicode is.
- [ ] I know why Unicode was created.
- [ ] I understand what a Unicode code point is.
- [ ] I understand the difference between Unicode and UTF-8.
- [ ] I know why modern software uses Unicode.

---

# Endianness

> "Endianness defines the order in which bytes are stored in memory."

---

## Introduction

By now we know:

```
8 Bits

↓

1 Byte
```

Some data types occupy more than one byte.

For example:

```
short

↓

2 Bytes
```

```
int

↓

4 Bytes
```

```
long long

↓

8 Bytes
```

The question is:

> When a value occupies multiple bytes,

which byte should be stored first?

This is exactly what **Endianness** answers.

---

## What is Endianness?

Endianness is the rule that determines the order in which bytes are stored in memory.

There are two main types:

- Little Endian
- Big Endian

The value itself never changes.

Only the order of the bytes in memory changes.

---

# Big Endian

Big Endian stores the **Most Significant Byte (MSB)** first.

Imagine the hexadecimal number:

```
0x12345678
```

Split into bytes:

```
12

34

56

78
```

Memory looks like this:

```
Address      Value

1000         12

1001         34

1002         56

1003         78
```

The biggest byte comes first.

---

# Little Endian

Little Endian stores the **Least Significant Byte (LSB)** first.

Using the same value:

```
0x12345678
```

Memory becomes:

```
Address      Value

1000         78

1001         56

1002         34

1003         12
```

Same number.

Different byte order.

---

## Visual Comparison

```
Value

0x12345678
```

Big Endian

```
12

34

56

78
```

Little Endian

```
78

56

34

12
```

Notice:

Nothing changed except the storage order.

---

## Why Does Endianness Exist?

Different CPU architectures were designed differently.

Some processors naturally work better with:

```
Big Endian
```

Others with:

```
Little Endian
```

Modern Intel and AMD processors use:

```
Little Endian
```

Most Linux PCs,

Windows PCs,

and Macs (Apple Silicon also operates in little-endian mode for normal memory access)

store data using Little Endian.

---

## Does the Programmer Usually Care?

Most of the time,

No.

The compiler handles everything automatically.

However,

Endianness becomes important when working with:

- Networking
- File Formats
- Operating Systems
- Embedded Systems
- Binary Files
- Reverse Engineering

---

## Example in C

Suppose:

```c
int number = 0x12345678;
```

Memory on a Little Endian machine:

```
Address      Byte

1000         78

1001         56

1002         34

1003         12
```

The variable still equals:

```
0x12345678
```

Only its bytes are stored differently.

---

## Real-World Example

Imagine writing a four-digit number on paper.

```
1234
```

Big Endian:

Read from left to right.

```
1

2

3

4
```

Little Endian:

Store starting with the last digit.

```
4

3

2

1
```

The number remains:

```
1234
```

Only the storage order changes.

---

## Network Byte Order

Computer networks use a standard byte order called:

```
Network Byte Order
```

This is:

```
Big Endian
```

Therefore,

programs often convert values before sending them over the network.

Functions such as:

```c
htonl()

htons()

ntohl()

ntohs()
```

perform these conversions.

You will encounter them later when studying network programming.

---

## Mental Model

Imagine four books.

```
Book 1

Book 2

Book 3

Book 4
```

Big Endian stores them in order.

Little Endian stores them in reverse order on the shelf.

The books themselves never change.

Only their positions do.

---

## 📚 Summary

Endianness determines how multi-byte values are arranged in memory.

There are two common formats:

- Big Endian
- Little Endian

Modern desktop computers typically use Little Endian.

The numeric value remains the same regardless of the storage order.

---

## 🧠 Key Concepts

- Endianness
- Byte Order
- Big Endian
- Little Endian
- MSB
- LSB

---

## ⚠ Common Mistakes

- Thinking Endianness changes the value.
- Confusing bits with bytes.
- Assuming all computers use the same byte order.
- Forgetting that Endianness matters only for values occupying multiple bytes.

---

## 💡 Coach Tips

✔ Endianness only affects data larger than one byte.

✔ A single byte has no byte order.

✔ Most modern computers use Little Endian.

✔ Networking usually uses Big Endian.

---

## 🧩 Think Like the Computer

Suppose:

```
0xAABBCCDD
```

How would it appear in memory on:

- Big Endian?
- Little Endian?

Try to draw both layouts before checking the answer.

---

## 🏋️ Practice Exercises

1. Explain the difference between Big Endian and Little Endian.

2. Why does Endianness not affect one-byte values?

3. Draw the memory layout of:

```
0x11223344
```

for both byte orders.

4. Why do network protocols use a standard byte order?

---

## 🚀 Mastery Checklist

- [ ] I know what Endianness is.
- [ ] I know the difference between Big Endian and Little Endian.
- [ ] I understand that the value does not change.
- [ ] I know that Endianness affects only multi-byte values.
- [ ] I know that most modern PCs use Little Endian.

---

# 🎉 End of Chapter 3 — Data Representation

Congratulations!

You have completed one of the most fundamental chapters in Computer Science.

Everything you learn from this point onward—memory, variables, pointers, arrays, strings, structures, files, and networking—will build upon the concepts introduced in this chapter.

Take your time to review it carefully before moving to Chapter 4.
# 🧠 Chapter 4 — Memory

> "Memory is where programs come to life."

🟢 Beginner

⏱ Estimated Study Time: ~3 Hours

---

## Introduction

Imagine writing this program.

```c
int age = 25;
```

Where is the value **25** stored?

Inside the source code?

Inside the CPU?

Inside Linux?

The answer is:

```
RAM (Random Access Memory)
```

Every variable your program creates occupies a location in memory.

Understanding memory is one of the biggest steps toward becoming a real C programmer.

---

## What is Memory?

Computer memory is the place where programs temporarily store data while they are running.

Think of memory as the computer's workspace.

While your program is executing,

every variable,

every function,

every string,

and every calculation exists somewhere inside memory.

Without memory,

programs could not run.

---

## Why Does a Computer Need Memory?

Imagine trying to solve a math problem without writing anything on paper.

You would have to remember every number in your head.

A computer faces the same problem.

The CPU can perform calculations,

but it needs a place to store:

- Numbers
- Variables
- Characters
- Arrays
- Function calls
- Program instructions

That place is memory.

---

## RAM (Random Access Memory)

The main memory used while programs run is called:

```
RAM
```

RAM stands for:

```
Random Access Memory
```

It is called "Random Access" because the CPU can access any memory location directly,

without reading every location before it.

---

## Characteristics of RAM

✔ Very fast

✔ Temporary

✔ Readable

✔ Writable

✔ Used only while programs are running

---

## Temporary Storage

RAM is **volatile memory**.

This means:

When the computer loses power,

everything stored inside RAM disappears.

Example:

You open a text editor.

Write a document.

Do **not** save it.

Turn off the computer.

The document is gone.

Why?

Because it existed only in RAM.

---

## RAM vs Storage

Many beginners confuse RAM with storage.

They are different.

| RAM | Storage (SSD / HDD) |
|------|---------------------|
| Temporary | Permanent |
| Very Fast | Slower |
| Used while programs run | Used to save files |
| Cleared when power is lost | Data remains after shutdown |

Example:

```
hello.c
```

is stored permanently on your SSD.

When you compile and run it,

Linux loads the executable into RAM.

The CPU then executes it from memory.

---

## How a Program Uses Memory

Suppose we write:

```c
int age = 25;
```

The execution flow looks like this.

```
Source Code

↓

Compiler

↓

Executable File

↓

Operating System

↓

RAM

↓

CPU Executes
```

Notice:

The variable exists in RAM,

not inside the source file.

---

## Memory is Organized

Memory is not one giant block.

It is divided into many tiny locations.

Each location stores:

```
1 Byte
```

Example:

```
Address      Value

1000         25

1001         00

1002         00

1003         00
```

Each row represents one byte of memory.

---

## Memory Addresses

Every byte in memory has its own unique address.

Think of addresses like house numbers.

```
House

↓

Address
```

Memory works the same way.

```
Byte

↓

Address
```

Later,

Pointers will allow us to work directly with these addresses.

---

## Why Addresses Matter

Suppose memory looked like this.

```
Address      Value

1000         25

1001         31

1002         48

1003         90
```

If we ask for the value stored at:

```
1002
```

the computer immediately knows where to look.

Addresses make memory organized and efficient.

---

## Memory During Program Execution

Every time a program starts,

the operating system reserves memory for it.

When the program ends,

that memory is released and becomes available for other programs.

This process happens automatically.

---

## Mental Model

Imagine a hotel.

```
Hotel

↓

Memory
```

```
Room Number

↓

Memory Address
```

```
Guest

↓

Variable
```

When a guest checks out,

the room becomes available again.

Memory behaves in a similar way.

---

## Real-World Example

Suppose you open:

- Google Chrome
- VS Code
- Spotify

Each program receives its own portion of RAM.

When you close Spotify,

its memory is released.

The operating system can then give that memory to another program.

---

## 📚 Summary

Memory is the workspace used by running programs.

Variables,

functions,

and program data all exist inside RAM while the program executes.

Each byte of memory has a unique address.

Understanding memory is essential before learning variables,

pointers,

and dynamic allocation.

---

## 🧠 Key Concepts

- Memory
- RAM
- Storage
- Address
- Byte
- Variable

---

## ⚠ Common Mistakes

- Confusing RAM with SSD or HDD.
- Thinking variables are stored inside the source code.
- Believing memory keeps its contents after shutdown.
- Forgetting that every byte has an address.

---

## 💡 Coach Tips

✔ Think of RAM as your program's workspace.

✔ Variables live in memory.

✔ The CPU executes instructions using data loaded into RAM.

✔ Every pointer you learn later will simply be an address in memory.

---

## 🧩 Think Like the Computer

Suppose your program creates:

```c
int age = 25;
```

Ask yourself:

- Where is the value stored?
- Who placed it there?
- Does it remain after the program ends?

---

## 🏋️ Practice Exercises

1. Explain the difference between RAM and SSD.

2. Why is RAM called volatile memory?

3. Why does every byte have an address?

4. Explain the journey of a program from `hello.c` to execution.

---

## 🚀 Mastery Checklist

- [ ] I know what memory is.
- [ ] I know what RAM is.
- [ ] I understand the difference between RAM and storage.
- [ ] I know that every byte has an address.
- [ ] I understand where variables live while a program runs.

---

# Variables in Memory

> "A variable is not just a name. It is a reserved location inside memory."

---

## Introduction

When beginners write:

```c
int age = 25;
```

they often think:

> "I created a variable."

This is true.

But something much more important also happened.

The operating system reserved memory for that variable.

The compiler generated machine instructions.

The CPU executed those instructions.

Finally,

the value was stored inside RAM.

The variable is therefore much more than a name.

It is an actual location inside the computer's memory.

---

## What Happens When You Declare a Variable?

Consider this program.

```c
int age = 25;
```

Several things happen.

### Step 1

The compiler understands that:

```
age
```

is an integer variable.

---

### Step 2

The compiler knows that an `int` usually requires:

```
4 Bytes
```

of memory.

---

### Step 3

When the program starts,

the operating system reserves four bytes inside RAM.

Example:

```
Address

1000

1001

1002

1003
```

---

### Step 4

The value

```
25
```

is converted into binary.

```
00000000
00000000
00000000
00011001
```

(or stored in little-endian order depending on the system.)

---

### Step 5

Those bytes are written into memory.

The variable now exists.

---

## Visual Representation

Source Code

```c
int age = 25;
```

↓

Compiler

↓

Executable

↓

Operating System

↓

RAM

```
Address      Value

1000         ...

1001         ...

1002         ...

1003         ...
```

↓

CPU Uses It

---

## Variables Are Labels

The variable name:

```
age
```

does **not** exist inside RAM.

Memory stores only:

- Bits
- Bytes
- Values

The name:

```
age
```

exists only for the programmer and the compiler.

Once the program is compiled,

the CPU does not know the variable is called:

```
age
```

It only knows memory addresses.

---

## Example

You write:

```c
int score = 100;
```

The computer does **not** store:

```
score
```

inside RAM.

Instead,

it stores only:

```
100
```

at some memory address.

The compiler remembers that

```
score
```

refers to that location.

---

## Multiple Variables

Example:

```c
int age = 25;
int score = 100;
char grade = 'A';
```

Memory might look like:

```
Address      Variable      Value

1000         age           25

1004         score         100

1008         grade         'A'
```

The exact addresses are determined by the compiler and operating system.

---

## Variables Can Change

Memory is writable.

Example:

```c
age = 30;
```

The variable keeps the same memory location.

Only its value changes.

Before:

```
Address      Value

1000         25
```

After:

```
Address      Value

1000         30
```

Notice:

The address did **not** change.

Only the stored value changed.

---

## Memory Lifetime

Variables exist only for a certain period.

Some variables disappear when a function finishes.

Others remain for the entire program.

Later,

we'll study:

- Scope
- Lifetime
- Storage Duration

---

## Mental Model

Imagine a locker at school.

```
Locker Number

↓

Memory Address
```

```
Student Name

↓

Variable Name
```

```
Books Inside

↓

Stored Value
```

The locker number never changes.

The books inside can change.

The same is true for variables.

---

## Real Example

Suppose:

```c
int lives = 3;
```

Later:

```c
lives--;
```

Memory changes.

Before:

```
3
```

After:

```
2
```

The variable is still stored in the same place.

Only the contents changed.

---

## 📚 Summary

Variables occupy memory.

The compiler reserves enough space for the variable's data type.

The variable name exists only during compilation.

The CPU ultimately works with memory addresses,

not variable names.

Changing a variable changes the stored value,

not its location.

---

## 🧠 Key Concepts

- Variable
- Memory
- Address
- Value
- Compiler
- RAM

---

## ⚠ Common Mistakes

- Thinking variables are stored inside the source code.
- Believing the variable name exists in RAM.
- Confusing the variable with its value.
- Thinking changing a variable creates new memory.

---

## 💡 Coach Tips

✔ A variable is simply a named location in memory.

✔ The name is for humans.

✔ The address is for the computer.

✔ The value is what changes during execution.

---

## 🧩 Think Like the Computer

Suppose:

```c
int x = 10;

x = 20;
```

Ask yourself:

- Did the address change?
- Did the variable change?
- What actually changed inside RAM?

---

## 🏋️ Practice Exercises

1. Explain what happens when a variable is declared.

2. Does the variable name exist inside RAM?

3. What changes after executing:

```c
x = 50;
```

4. Draw a memory diagram for:

```c
int age = 25;
char grade = 'A';
```

---

## 🚀 Mastery Checklist

- [ ] I understand where variables are stored.
- [ ] I know that variables occupy memory.
- [ ] I understand that the variable name is not stored in RAM.
- [ ] I know the difference between a variable, its address, and its value.
- [ ] I can explain what happens when a variable changes.

---

# Memory Addresses

> "Every byte in memory has its own unique address."

---

## Introduction

Imagine a city.

Every house has an address.

```
House

↓

221B Baker Street
```

Without addresses,

the mail carrier would never know where to deliver letters.

Computer memory works exactly the same way.

Every byte inside RAM has its own unique address.

The CPU uses these addresses to find data quickly.

---

## What is a Memory Address?

A memory address is a unique number that identifies one specific byte in RAM.

Think of it as the "home address" of a piece of data.

Example:

```
Address

1000

1001

1002

1003
```

Each address represents exactly one byte.

---

## Memory is a Long Sequence of Bytes

Imagine memory as a long street.

```
+---------+---------+---------+---------+
| Address | Address | Address | Address |
| 1000    | 1001    | 1002    | 1003    |
+---------+---------+---------+---------+
```

Every box stores one byte.

Millions (or billions) of these boxes together form RAM.

---

## Example

Suppose we write:

```c
int age = 25;
```

If an `int` occupies four bytes,

memory could look like:

```
Address      Value

1000         25

1001         0

1002         0

1003         0
```

The exact representation depends on the computer's architecture and endianness,

but the important idea is that the variable occupies multiple consecutive memory addresses.

---

## Addresses are Numbers

Memory addresses are simply numbers.

In C,

they are usually displayed in hexadecimal.

Example:

```
0x7FFE1234

0x7FFE1238

0x7FFE123C
```

The prefix:

```
0x
```

means the number is written in hexadecimal.

---

## Why Hexadecimal?

Imagine writing this address.

```
111111101010101100001001
```

Very difficult.

Now compare it to:

```
0xFEAB09
```

Much shorter.

Much easier to read.

That is why programmers use hexadecimal for addresses.

---

## Every Variable Has an Address

Suppose we write:

```c
int age = 25;
char grade = 'A';
```

Memory could look like:

```
Address      Variable

0x1000       age

0x1004       grade
```

Each variable has its own location in memory.

---

## Finding an Address in C

The address-of operator is:

```c
&
```

Example:

```c
int age = 25;

printf("%p\n", &age);
```

Possible output:

```
0x7ffeefbff56c
```

This is the address where the variable is stored.

We will study this operator in detail when learning pointers.

---

## Variables vs Addresses

It is important to distinguish between:

The variable

```c
age
```

The value

```
25
```

The address

```
0x7ffeefbff56c
```

These are three completely different things.

---

## Memory Diagram

```
Variable

age

↓

Address

0x1000

↓

Stored Value

25
```

Think of it like this.

```
Name

↓

Location

↓

Content
```

The name is for the programmer.

The location is for the computer.

The content is the actual data.

---

## Consecutive Addresses

Memory addresses increase one byte at a time.

```
0x1000

↓

0x1001

↓

0x1002

↓

0x1003
```

Notice that addresses increase by one,

because each address refers to one byte.

---

## Why Addresses Matter

Without addresses,

the CPU would have no idea where variables are stored.

Addresses allow:

- Reading values
- Writing values
- Passing data between functions
- Dynamic memory allocation
- Using pointers

Almost every advanced C concept depends on memory addresses.

---

## Mental Model

Imagine a library.

Each book has:

```
Shelf Number

↓

Memory Address
```

The book itself contains information.

The shelf number tells you where to find it.

Memory addresses work exactly the same way.

---

## Real Example

Suppose we have:

```c
char letter = 'A';
```

Memory:

```
Address

0x2000

↓

65
```

The address tells the CPU where to find the value.

The value tells the CPU what is stored there.

---

## 📚 Summary

Every byte in memory has its own unique address.

Variables occupy one or more consecutive bytes.

Addresses are usually displayed in hexadecimal because they are easier to read.

Understanding memory addresses is essential before learning pointers.

---

## 🧠 Key Concepts

- Memory Address
- Byte
- Hexadecimal
- Address-of Operator
- Consecutive Memory

---

## ⚠ Common Mistakes

- Confusing a variable with its address.
- Thinking addresses are random numbers.
- Forgetting that each address represents one byte.
- Assuming addresses are always the same every time a program runs.

---

## 💡 Coach Tips

✔ The value answers:

> "What is stored?"

✔ The address answers:

> "Where is it stored?"

✔ Learn to distinguish between the name, the value, and the address.

✔ Pointers are simply variables that store addresses.

---

## 🧩 Think Like the Computer

Suppose:

```c
int age = 25;
```

Answer these questions.

- What is the variable name?
- What is the stored value?
- What is the memory address?
- Which one does the CPU actually use?

---

## 🏋️ Practice Exercises

1. Explain what a memory address is.

2. Why are addresses usually written in hexadecimal?

3. Draw a memory diagram for:

```c
int score = 100;
```

4. Explain the difference between:

- Variable
- Address
- Value

---

## 🚀 Mastery Checklist

- [ ] I know what a memory address is.
- [ ] I know why every byte has an address.
- [ ] I understand the difference between a variable, its value, and its address.
- [ ] I know why hexadecimal is used for addresses.
- [ ] I understand why pointers depend on memory addresses.

---

# Stack Memory

> "The stack is the memory area used for function calls and local variables."

---

## Introduction

Every time a C program starts,

the operating system divides the program's memory into several sections.

One of the most important sections is called the **Stack**.

The stack stores information that is needed **temporarily** while the program is running.

Examples include:

- Local variables
- Function parameters
- Return addresses
- Function call information

Almost every C program uses the stack.

---

## What is the Stack?

The Stack is a special region of RAM managed automatically by the operating system and the compiler.

Whenever a function is called,

space is automatically reserved on the stack.

When the function finishes,

that space is automatically released.

The programmer does not need to manage it manually.

---

## Why is it Called a Stack?

Imagine a stack of books.

```
+---------+
| Book 3  |
+---------+

| Book 2  |
+---------+

| Book 1  |
+---------+
```

You always place a new book **on top**.

You always remove the **top** book first.

The Stack works exactly the same way.

This behavior is called:

```
LIFO

Last In

First Out
```

---

## Stack Growth

Suppose our program starts.

Memory looks like this.

```
Stack

↓

(empty)
```

Now the program enters:

```c
int main(void)
{
    int age = 25;
}
```

Memory becomes:

```
+-------------------+
| age = 25          |
+-------------------+

Stack Top
```

---

## Calling Another Function

Suppose:

```c
int main(void)
{
    int age = 25;

    foo();
}
```

Inside:

```c
void foo(void)
{
    int x = 10;
}
```

The Stack becomes:

```
+-------------------+
| x = 10            |
+-------------------+

| age = 25          |
+-------------------+

Stack Top
```

Notice that

the newest function is always placed on top.

---

## Returning from a Function

When:

```c
foo();
```

finishes,

its stack frame disappears.

```
Before

+-------------------+
| x = 10            |
+-------------------+

| age = 25          |
+-------------------+
```

After:

```
+-------------------+
| age = 25          |
+-------------------+
```

Everything belonging to `foo()` is removed automatically.

---

## Stack Frame

Every function creates its own area on the stack.

This area is called a:

```
Stack Frame
```

A stack frame usually contains:

- Local Variables
- Parameters
- Return Address
- Saved Registers

When the function ends,

the entire frame disappears.

---

## Example

```c
void foo(void)
{
    int x = 10;
    int y = 20;
}
```

Stack:

```
+----------------------+
| y = 20               |
+----------------------+

| x = 10               |
+----------------------+
```

After returning,

both variables disappear automatically.

---

## Lifetime of Stack Variables

Variables declared inside a function exist only while that function is executing.

Example:

```c
void foo(void)
{
    int number = 42;
}
```

After:

```
foo();
```

returns,

```
number
```

no longer exists.

Its memory is released automatically.

---

## Advantages of the Stack

✔ Extremely fast

✔ Automatically managed

✔ No manual allocation

✔ No manual freeing

✔ Perfect for temporary data

---

## Limitations of the Stack

✘ Limited size

✘ Cannot store very large data

✘ Variables disappear when functions return

✘ Can overflow if too much memory is used

---

## Stack Overflow

Suppose a function keeps calling itself forever.

```c
void foo(void)
{
    foo();
}
```

Every call creates another stack frame.

Eventually,

the stack becomes full.

Result:

```
Stack Overflow
```

The program usually crashes.

---

## Mental Model

Imagine a stack of dinner plates.

```
New Plate

↓

Top
```

Remove plates.

↓

Always from the top.

You never remove a plate from the middle.

The Stack behaves exactly the same way.

---

## Real Example

```c
int square(int n)
{
    int result;

    result = n * n;

    return (result);
}
```

While this function executes,

its variables exist on the Stack.

After it returns,

those variables disappear automatically.

---

## 📚 Summary

The Stack is a memory region used for temporary data.

Each function creates a new stack frame.

When the function finishes,

its stack frame is automatically removed.

The Stack follows the Last In, First Out (LIFO) principle.

---

## 🧠 Key Concepts

- Stack
- Stack Frame
- Local Variables
- Function Call
- Return Address
- LIFO

---

## ⚠ Common Mistakes

- Thinking stack variables exist forever.
- Returning pointers to local variables.
- Confusing Stack with Heap.
- Believing the programmer manually frees stack memory.

---

## 💡 Coach Tips

✔ Local variables usually live on the Stack.

✔ The Stack is managed automatically.

✔ Every function call creates a new Stack Frame.

✔ Every function return destroys that Stack Frame.

---

## 🧩 Think Like the Computer

Suppose:

```c
main()

↓

foo()

↓

bar()
```

Draw the Stack.

Which function is on top?

Which function disappears first?

---

## 🏋️ Practice Exercises

1. Explain why the Stack uses LIFO.

2. What is a Stack Frame?

3. Why do local variables disappear?

4. What causes a Stack Overflow?

---

## 🚀 Mastery Checklist

- [ ] I know what the Stack is.
- [ ] I understand Stack Frames.
- [ ] I know why local variables disappear.
- [ ] I understand LIFO.
- [ ] I know what causes Stack Overflow.

---

# Heap Memory

> "The Heap is a memory region used for dynamically allocated memory."

---

## Introduction

In the previous section, we learned that local variables are stored on the **Stack**.

The Stack is:

- Fast
- Automatic
- Temporary

However,

what happens if we need memory that:

- survives after a function returns?
- has a size known only while the program is running?
- is much larger than the Stack can safely hold?

For these situations,

C provides another memory region called the **Heap**.

---

## What is the Heap?

The Heap is a region of memory used for **dynamic memory allocation**.

Unlike the Stack,

memory on the Heap is **not managed automatically**.

The programmer is responsible for:

- Requesting memory
- Using memory
- Releasing memory

---

## Stack vs Heap

| Stack | Heap |
|--------|------|
| Automatic | Manual |
| Very Fast | Slower |
| Small | Much Larger |
| Temporary | Flexible Lifetime |
| Freed Automatically | Must Be Freed Manually |

---

## Why Do We Need the Heap?

Imagine asking the user:

```text
How many students are there?
```

The user answers:

```
5000
```

When writing the program,

you could not have known that number.

Therefore,

the amount of memory must be decided **while the program is running**.

The Heap makes this possible.

---

## Dynamic Allocation

Instead of reserving memory during compilation,

the program requests memory during execution.

Example:

```c
int *numbers;

numbers = malloc(100 * sizeof(int));
```

Here,

memory is allocated only when the program reaches this instruction.

Later,

we'll study `malloc()` in detail.

---

## Heap Lifetime

Memory allocated on the Heap remains allocated until one of two things happens:

- The programmer releases it using:

```c
free();
```

- The program terminates.

Unlike Stack variables,

Heap memory does **not** disappear when a function returns.

---

## Example

```c
void example(void)
{
    int *x;

    x = malloc(sizeof(int));

    *x = 42;
}
```

After this function returns,

the pointer:

```
x
```

disappears,

but the allocated memory still exists.

This creates a:

```
Memory Leak
```

unless `free()` is called.

---

## Memory Leak

A memory leak occurs when allocated Heap memory is no longer accessible.

Example:

```c
int *x;

x = malloc(sizeof(int));

x = NULL;
```

The original allocated memory still exists,

but nothing points to it anymore.

It cannot be freed.

That memory is permanently lost until the program exits.

---

## Heap Diagram

Before allocation:

```
Heap

(empty)
```

After:

```c
malloc(16);
```

```
Heap

+----------------------+
| Reserved Memory      |
+----------------------+
```

After:

```c
free(ptr);
```

```
Heap

(empty)
```

---

## Advantages of the Heap

✔ Flexible size

✔ Large allocations

✔ Data can outlive function calls

✔ Essential for dynamic data structures

---

## Limitations of the Heap

✘ Slower than the Stack

✘ Programmer must manage memory

✘ Can leak memory

✘ Can become fragmented

---

## Heap Fragmentation

Imagine a parking lot.

Cars leave randomly.

```
🚗

Empty

🚗

Empty

🚗
```

Although free spaces exist,

they are scattered.

The Heap can suffer from the same problem,

called:

```
Memory Fragmentation
```

---

## Stack vs Heap Visualization

```
Program Memory

+---------------------------+
| Code Segment              |
+---------------------------+

| Data Segment              |
+---------------------------+

| Heap                      |
| ↑ grows upward            |
+---------------------------+

|                           |
| Free Memory               |
|                           |
+---------------------------+

| Stack                     |
| ↓ grows downward          |
+---------------------------+
```

Eventually,

the Stack and Heap could collide if memory is exhausted.

---

## Real-World Uses

The Heap is commonly used for:

- Dynamic Arrays
- Linked Lists
- Trees
- Graphs
- Buffers
- Game Objects
- Images
- Databases

Almost every large application relies heavily on Heap memory.

---

## Mental Model

Imagine renting a warehouse.

The Stack is like a hotel room.

You check in.

You leave.

The room is cleaned automatically.

The Heap is like renting a warehouse.

You must:

- Rent it
- Use it
- Return it

If you forget to return it,

you continue paying for it.

---

## 📚 Summary

The Heap is used for dynamic memory allocation.

Unlike the Stack,

Heap memory is managed manually by the programmer.

Allocated memory remains available until it is explicitly released using `free()`.

Improper Heap management leads to memory leaks and other bugs.

---

## 🧠 Key Concepts

- Heap
- Dynamic Memory
- malloc()
- free()
- Memory Leak
- Fragmentation

---

## ⚠ Common Mistakes

- Forgetting to call `free()`.
- Accessing memory after it has been freed.
- Losing the pointer returned by `malloc()`.
- Confusing Heap memory with Stack memory.

---

## 💡 Coach Tips

✔ Every successful `malloc()` should eventually have a matching `free()`.

✔ Heap memory is powerful but requires responsibility.

✔ Most memory bugs in C involve incorrect Heap usage.

✔ Always think about who owns allocated memory.

---

## 🧩 Think Like the Computer

Suppose:

```c
int *ptr;

ptr = malloc(sizeof(int));

*ptr = 42;

free(ptr);
```

Ask yourself:

- Where is the pointer stored?
- Where is the integer stored?
- Which memory disappears automatically?
- Which memory must be released manually?

---

## 🏋️ Practice Exercises

1. Explain the difference between the Stack and the Heap.

2. Why does the Heap exist?

3. What is a memory leak?

4. Why is `free()` necessary?

5. Give three examples where Heap memory is required.

---

## 🚀 Mastery Checklist

- [ ] I know what the Heap is.
- [ ] I understand why dynamic memory exists.
- [ ] I know the difference between Stack and Heap.
- [ ] I understand what a memory leak is.
- [ ] I know why `malloc()` and `free()` always go together.

---

# Code Segment

> "The Code Segment stores the executable instructions of your program."

---

## Introduction

When you compile a C program,

the source code itself is **not** loaded into memory.

Instead,

the compiler translates it into machine code.

That machine code is stored inside a special region of memory called the **Code Segment**.

The CPU executes instructions directly from this segment.

---

## What is Stored in the Code Segment?

The Code Segment contains:

- Machine Instructions
- Compiled Functions
- Program Entry Point (`main()`)
- Read-only executable code

It does **not** contain variables.

---

## Example

Source code:

```c
int main(void)
{
    printf("Hello\n");
    return (0);
}
```

After compilation,

instructions similar to the following exist inside the Code Segment.

```
Load instruction

↓

Call printf()

↓

Return
```

The CPU reads these instructions one by one.

---

## Characteristics

✔ Contains executable instructions

✔ Read-only

✔ Loaded when the program starts

✔ Executed directly by the CPU

---

## Mental Model

Think of the Code Segment as the script of a movie.

The actors (CPU) simply follow the script.

The script itself never changes while the movie is playing.

---

## 📚 Summary

The Code Segment stores the executable instructions generated by the compiler.

The CPU fetches instructions from this segment during program execution.

Variables are **not** stored here.

---

# Data Segment

> "The Data Segment stores global and static variables."

---

## Introduction

Not every variable lives on the Stack.

Some variables exist before `main()` starts.

Others remain alive until the program ends.

These variables are stored inside the **Data Segment**.

---

## What is Stored in the Data Segment?

Examples include:

- Global Variables
- Static Variables
- Initialized Global Variables
- Uninitialized Global Variables

---

## Example

```c
int score = 100;
```

If `score` is declared outside every function,

it is stored in the Data Segment.

---

## Initialized Data

Example:

```c
int score = 100;
```

The value

```
100
```

already exists before the program starts.

---

## Uninitialized Data (BSS)

Example:

```c
int counter;
```

This variable is automatically initialized to:

```
0
```

It belongs to a special part of the Data Segment called:

```
BSS
```

(BSS = Block Started by Symbol)

---

## Lifetime

Unlike Stack variables,

Data Segment variables exist:

```
Program Starts

↓

Program Ends
```

They are never destroyed when functions return.

---

## Characteristics

✔ Global

✔ Static

✔ Exists for the entire execution

✔ Automatically managed

---

## Mental Model

Imagine a company's permanent archive.

The documents remain there all day.

Employees come and go,

but the archive remains.

---

## 📚 Summary

The Data Segment stores global and static variables.

These variables exist during the entire lifetime of the program.

They are different from Stack variables,

which disappear when functions return.

---

# Complete Memory Layout

> "Every running C program is divided into several memory regions."

---

## Complete Layout

```
High Memory
+--------------------------------------+
|               Stack                  |
|      Local Variables                 |
|      Function Calls                  |
|      Return Addresses                |
|                                      |
|        (Grows Downward ↓)            |
+--------------------------------------+
|                                      |
|          Free Memory                 |
|                                      |
+--------------------------------------+
|                                      |
|               Heap                   |
|     malloc(), calloc(), realloc()    |
|                                      |
|         (Grows Upward ↑)             |
+--------------------------------------+
|                                      |
|           BSS Segment                |
|  Uninitialized Global Variables      |
+--------------------------------------+
|                                      |
|           Data Segment               |
|   Initialized Global Variables       |
+--------------------------------------+
|                                      |
|           Code Segment               |
|  Machine Instructions                |
|  Compiled Functions                  |
+--------------------------------------+
Low Memory
```

---

## Memory Region Overview

| Region | Stores |
|---------|--------|
| Code Segment | Executable instructions |
| Data Segment | Initialized global/static variables |
| BSS Segment | Uninitialized global/static variables |
| Heap | Dynamically allocated memory |
| Free Memory | Available memory |
| Stack | Local variables and function calls |

---

## Example

Consider this program.

```c
int global = 10;

int main(void)
{
    int local = 20;

    int *ptr = malloc(sizeof(int));

    *ptr = 30;

    free(ptr);

    return (0);
}
```

Memory usage:

```
Code Segment

↓

main()

↓

Data Segment

↓

global

↓

Stack

↓

local

↓

Heap

↓

malloc()
```

Each piece of data lives in a different memory region.

---

## Why is Memory Divided?

Different types of data have different lifetimes.

For example:

```
Temporary Variables

↓

Stack
```

```
Dynamic Objects

↓

Heap
```

```
Program Instructions

↓

Code Segment
```

Keeping them separate makes programs faster,

more organized,

and easier for the operating system to manage.

---

## Mental Model

Think of a company building.

```
Ground Floor

↓

Reception

(Code)
```

```
Second Floor

↓

Archives

(Data)
```

```
Third Floor

↓

Temporary Offices

(Stack)
```

```
Warehouse

↓

Storage

(Heap)
```

Every department has a different responsibility.

Memory works in exactly the same way.

---

## 📚 Chapter 4 Summary

Memory is divided into specialized regions.

Each region has a specific purpose.

The Stack stores temporary function data.

The Heap stores dynamically allocated memory.

The Data Segment stores global and static variables.

The Code Segment stores executable instructions.

Understanding this layout makes advanced C topics much easier.

---

## 🧠 Key Concepts

- RAM
- Memory Layout
- Code Segment
- Data Segment
- BSS
- Heap
- Stack
- Memory Address

---

## ⚠ Common Mistakes

- Thinking all variables are stored in the Stack.
- Confusing Heap memory with Stack memory.
- Forgetting to free Heap memory.
- Believing source code is stored in RAM during execution.
- Confusing the Code Segment with the source file.

---

## 💡 Coach Tips

✔ Learn the complete memory layout before studying pointers.

✔ Always ask yourself:

> "Where does this variable live?"

✔ Understanding memory layout makes debugging much easier.

✔ Every C programmer should be able to draw the memory layout from memory.

---

## 🏋️ Practice Exercises

1. Draw the complete memory layout of a C program.

2. Explain the purpose of each memory region.

3. Where does a local variable live?

4. Where does a global variable live?

5. Where does `malloc()` allocate memory?

6. Why do the Stack and Heap grow toward each other?

---

## 🚀 Mastery Checklist

- [ ] I know the purpose of every memory region.
- [ ] I understand the difference between Stack and Heap.
- [ ] I know where global variables are stored.
- [ ] I know where local variables are stored.
- [ ] I understand where executable instructions are stored.
- [ ] I can draw the complete memory layout of a C program.

---

# 🎉 End of Chapter 4 — Memory

Congratulations!

You now understand one of the most important concepts in C programming.

From this point onward, variables, pointers, arrays, function calls, dynamic memory allocation, and debugging will all build upon this memory model.

Take time to master this chapter before moving to Chapter 5.

# 📦 Chapter 5 — Variables

> "Variables are the bridge between the programmer and the computer's memory."

🟢 Beginner

⏱ Estimated Study Time: ~3 Hours

---

## Introduction

Every program stores information.

For example,

- A player's score
- A person's age
- A student's grade
- The temperature
- The result of a calculation

If we could not store information,

programs would be useless.

This is where **variables** become essential.

Variables allow a program to remember information while it is running.

---

## What is a Variable?

A variable is a **named location in memory** used to store data.

Think of a variable as a container.

```
+-------------+
|     age     |
+-------------+
|     25      |
+-------------+
```

The label:

```
age
```

helps the programmer identify the stored value.

The computer,

however,

only cares about the memory address where the value is stored.

---

## Why Do We Need Variables?

Imagine writing this.

```c
printf("25");
```

Now suppose the age changes to:

```
26
```

You would have to modify the source code.

Instead,

we write:

```c
int age = 25;
```

Later,

changing the value becomes simple.

```c
age = 26;
```

The program becomes flexible.

---

## Variables Store Values

A variable always stores a value.

Examples:

```c
int age = 25;
```

```
Variable

↓

age
```

```
Value

↓

25
```

---

```c
char grade = 'A';
```

```
Variable

↓

grade
```

```
Value

↓

'A'
```

---

```c
float price = 19.99;
```

```
Variable

↓

price
```

```
Value

↓

19.99
```

---

## Variables Live in Memory

When a variable is created,

the operating system reserves memory for it.

Example:

```c
int age = 25;
```

Memory might look like:

```
Address      Variable      Value

1000         age           25
```

The exact address is chosen automatically.

---

## Variables Can Change

Unlike constants,

variables may receive new values.

Example:

```c
int score = 10;
```

Later,

```c
score = 15;
```

Only the stored value changes.

The variable itself still exists.

---

## Variables Have Three Important Properties

Every variable has:

### 1. A Name

Example:

```c
age
```

---

### 2. A Data Type

Example:

```c
int
```

The type determines:

- What kind of data can be stored
- How much memory is required

---

### 3. A Value

Example:

```
25
```

The value may change while the program runs.

---

## Example

```c
int age = 25;
```

Breakdown:

```
int

↓

Data Type
```

```
age

↓

Variable Name
```

```
25

↓

Initial Value
```

---

## Variables and Memory

```
Source Code

↓

Variable

↓

Memory Address

↓

Stored Value
```

This relationship is one of the most important concepts in C.

---

## Real-World Examples

A game stores:

```
Health

↓

100
```

A bank stores:

```
Balance

↓

2500
```

A GPS stores:

```
Current Position
```

Every one of these is represented by variables.

---

## Mental Model

Imagine a mailbox.

```
Mailbox Label

↓

Variable Name
```

```
Mailbox Location

↓

Memory Address
```

```
Letters Inside

↓

Stored Value
```

The label identifies the mailbox.

The address locates it.

The letters are the stored data.

Variables behave in exactly the same way.

---

## 📚 Summary

Variables are named memory locations.

They allow programs to store and modify information.

Every variable has:

- A name
- A data type
- A value

Variables exist in memory,

not inside the source code.

---

## 🧠 Key Concepts

- Variable
- Name
- Value
- Memory
- Data Type

---

## ⚠ Common Mistakes

- Thinking variables exist only in source code.
- Confusing the variable name with its value.
- Thinking the memory address changes every time the value changes.
- Forgetting that variables occupy memory.

---

## 💡 Coach Tips

✔ A variable is simply a name given to a memory location.

✔ The compiler understands names.

✔ The CPU works with addresses.

✔ Always think:

```
Name

↓

Address

↓

Value
```

---

## 🧩 Think Like the Computer

Suppose:

```c
int age = 25;

age = 30;
```

Ask yourself:

- What changed?
- What stayed the same?
- Did the memory address change?

---

## 🏋️ Practice Exercises

1. Define the term "variable."

2. Explain why variables are necessary.

3. Identify the name, type, and value in:

```c
int score = 100;
```

4. Explain what happens in memory when executing:

```c
score = 200;
```

---

## 🚀 Mastery Checklist

- [ ] I know what a variable is.
- [ ] I understand why variables exist.
- [ ] I know the three properties of every variable.
- [ ] I understand that variables occupy memory.
- [ ] I can explain the relationship between a variable and memory.

---

# Identifiers

> "An identifier is the name used to identify program elements."

---

## Introduction

When writing a C program,

we constantly create names.

For example:

```c
int age;

int score;

float price;

char grade;
```

The names:

```
age

score

price

grade
```

are called **Identifiers**.

Identifiers allow programmers to refer to variables,

functions,

arrays,

structures,

and many other program elements.

Without identifiers,

programs would be almost impossible to read.

---

## What is an Identifier?

An identifier is a user-defined name used to identify something inside a program.

Examples include:

- Variables
- Functions
- Arrays
- Structures
- Typedefs
- Enumerations

Examples:

```c
int age;

float temperature;

char grade;

int max_value(void);
```

Every highlighted word below is an identifier.

```
age

temperature

grade

max_value
```

---

## Why Do We Need Identifiers?

Imagine writing a program without names.

Instead of writing:

```c
age = 25;
```

you would somehow have to remember a memory address like:

```
0x7FFE1234
```

This would be almost impossible.

Identifiers make programs readable.

The compiler later replaces those names with memory addresses.

---

## Identifier vs Variable

Many beginners think:

```
Identifier

=

Variable
```

This is **not** correct.

A variable is an object stored in memory.

An identifier is simply its name.

Example:

```c
int age = 25;
```

```
Identifier

↓

age
```

```
Variable

↓

Memory Location
```

```
Value

↓

25
```

---

## Good Examples

```c
int age;

float salary;

char grade;

int total_students;
```

These names immediately describe their purpose.

---

## Bad Examples

```c
int x;

int a;

float temp1;

char q;
```

Although these compile,

they provide very little information.

Someone reading the code has to guess their meaning.

---

## Self-Documenting Code

Good identifiers reduce the need for comments.

Compare these examples.

Poor:

```c
int x;

x = 25;
```

Better:

```c
int age;

age = 25;
```

The second version explains itself.

This is called:

```
Self-documenting Code
```

---

## Real-World Examples

Imagine developing a hospital management system.

Good identifiers:

```c
patient_age

blood_pressure

heart_rate

doctor_name
```

Poor identifiers:

```c
a

b

x

tmp
```

Which program would you rather maintain?

---

## Mental Model

Imagine a school.

Every student has:

- A name
- An ID number

The teacher remembers the student by name.

The school database remembers the student by ID.

Programming works the same way.

```
Identifier

↓

Programmer
```

```
Memory Address

↓

Computer
```

---

## 📚 Summary

Identifiers are names chosen by programmers.

They help humans understand code.

The compiler uses identifiers to keep track of program elements before converting them into machine code.

Choosing good identifiers greatly improves code readability.

---

## 🧠 Key Concepts

- Identifier
- Variable
- Readability
- Naming
- Self-documenting Code

---

## ⚠ Common Mistakes

- Thinking identifiers exist in RAM.
- Using meaningless names.
- Confusing identifiers with variables.
- Making names too short.

---

## 💡 Coach Tips

✔ Choose names that describe purpose.

✔ Imagine someone else reading your code.

✔ Good names reduce bugs.

✔ Readability is more important than short names.

---

## 🧩 Think Like the Computer

Suppose you write:

```c
int age = 25;
```

Ask yourself:

- What is the identifier?
- Where does the value live?
- Does the CPU know the name "age"?

---

## 🏋️ Practice Exercises

Choose better identifiers for:

```c
int x;
```

```c
float a;
```

```c
char b;
```

Explain why your new names are better.

---

## 🚀 Mastery Checklist

- [ ] I know what an identifier is.
- [ ] I understand the difference between an identifier and a variable.
- [ ] I know why identifiers improve readability.
- [ ] I can choose meaningful names.
- [ ] I understand that identifiers are for programmers, not the CPU.

---

# Naming Rules

> "An identifier must follow the rules of the C language before it can follow good programming style."

---

## Introduction

Not every word can be used as an identifier.

The C language defines strict rules for naming variables,

functions,

arrays,

and other program elements.

If a name violates these rules,

the compiler will generate an error.

Understanding these rules is essential before writing larger programs.

---

# Rule 1 — An Identifier Must Begin with a Letter or an Underscore

The first character must be:

- A letter (`A-Z` or `a-z`)
- An underscore (`_`)

Examples:

```c
age

score

_student

counter
```

Valid.

---

These are invalid:

```c
1age

9score

7number
```

Why?

Because identifiers cannot begin with a digit.

---

# Rule 2 — Remaining Characters

After the first character,

an identifier may contain:

- Letters
- Digits
- Underscores

Examples:

```c
player1

student_age

score2026

max_value
```

All are valid.

---

# Rule 3 — No Spaces

Spaces are never allowed.

Incorrect:

```c
student age
```

Correct:

```c
student_age
```

or

```c
studentAge
```

---

# Rule 4 — No Special Characters

The following characters are illegal inside identifiers.

```
+

-

*

/

%

@

#

$

!

?

.

,

(
)

[
]

{
}
```

Incorrect:

```c
student-age

price$

total#

my.value
```

Correct:

```c
student_age

price

total

my_value
```

---

# Rule 5 — Case Sensitive

C distinguishes between uppercase and lowercase letters.

Example:

```c
age

Age

AGE
```

These are **three completely different identifiers**.

Example:

```c
int age = 20;
int Age = 30;
```

This program is valid,

although using similar names is discouraged.

---

# Rule 6 — Reserved Keywords Cannot Be Used

The C language already uses certain words.

Examples:

```c
int

char

return

if

while

for

switch
```

These are called:

```
Keywords
```

You cannot create variables with these names.

Incorrect:

```c
int int;

char return;
```

The compiler will report an error.

---

# Rule 7 — Choose Meaningful Names

Although this is not required by the compiler,

it is one of the most important programming practices.

Poor:

```c
int x;

int a;

int n;
```

Better:

```c
int student_age;

int total_score;

int player_health;
```

The second version is much easier to understand.

---

# Rule 8 — Keep Names Consistent

Choose one naming style and use it throughout the project.

Example:

```c
student_age

total_score

player_health
```

Not:

```c
studentAge

player_health

TotalScore
```

Consistency makes code easier to read and maintain.

---

# Common Naming Styles

## snake_case

```c
student_age

total_score

max_value
```

Uses underscores between words.

This is the style required by the **42 Norm**.

---

## camelCase

```c
studentAge

totalScore

maxValue
```

Common in Java and JavaScript,

but **not preferred in the 42 Piscine**.

---

## PascalCase

```c
StudentAge

TotalScore
```

Often used for classes in C++ and C#.

Rarely used in C variables.

---

## UPPER_CASE

```c
MAX_SIZE

BUFFER_LENGTH

PI
```

Usually reserved for:

- Constants
- Macros

---

# Valid vs Invalid Examples

| Identifier | Valid? | Reason |
|------------|--------|--------|
| `age` | ✅ | Starts with a letter |
| `_count` | ✅ | Starts with `_` |
| `player1` | ✅ | Digits allowed after first character |
| `1player` | ❌ | Starts with a digit |
| `student age` | ❌ | Contains a space |
| `price$` | ❌ | Contains `$` |
| `return` | ❌ | Reserved keyword |

---

# Mental Model

Think of identifiers as names on official documents.

Every person must have a valid name.

You cannot register someone with:

```
123John

Hello!

Student Name

return
```

Programming follows similar rules.

---

## 📚 Summary

Identifiers must follow the syntax rules defined by the C language.

A valid identifier:

- Starts with a letter or underscore
- Contains only letters, digits, and underscores
- Has no spaces
- Has no special characters
- Is not a reserved keyword

Choosing meaningful and consistent names improves code quality.

---

## 🧠 Key Concepts

- Identifier
- Naming Rules
- Keywords
- Case Sensitive
- snake_case

---

## ⚠ Common Mistakes

- Starting identifiers with numbers.
- Using spaces.
- Using special characters.
- Using reserved keywords.
- Mixing multiple naming styles.

---

## 💡 Coach Tips

✔ Prefer descriptive names.

✔ Use `snake_case` in 42 projects.

✔ Avoid one-letter variable names unless the context is obvious (such as loop counters).

✔ Readability is one of the most valuable programming skills.

---

## 🧩 Think Like the Computer

Which of the following identifiers are valid?

```c
player1

1player

_player

student_age

student-age

return

MAX_SIZE

my value
```

Explain **why** each one is valid or invalid.

---

## 🏋️ Practice Exercises

1. Write five valid identifiers.

2. Write five invalid identifiers and explain why they are invalid.

3. Convert the following into valid `snake_case` names:

```
Student Age

Player Health

Total Score

Maximum Speed
```

4. Why does the C language forbid using keywords as identifiers?

---

## 🚀 Mastery Checklist

- [ ] I know the rules for valid identifiers.
- [ ] I understand why identifiers cannot start with digits.
- [ ] I know that C is case-sensitive.
- [ ] I know the difference between valid and invalid identifiers.
- [ ] I understand why `snake_case` is preferred in the 42 Piscine.

---

# Declaration

> "A declaration tells the compiler that a variable exists and specifies its type."

---

## Introduction

Before a variable can be used,

the compiler must know two things:

- Its name
- Its data type

Providing this information is called a **Declaration**.

Think of a declaration as introducing a new variable to the compiler.

---

## What is a Declaration?

A declaration tells the compiler:

> "I want to create a variable with this name and this data type."

Example:

```c
int age;
```

This statement declares a variable named:

```
age
```

whose type is:

```
int
```

At this point,

no value has been assigned.

---

## Basic Syntax

```c
data_type variable_name;
```

Example:

```c
int age;

char grade;

float price;

double salary;
```

Each line declares one variable.

---

## Multiple Declarations

Several variables of the same type may be declared together.

Example:

```c
int x, y, z;
```

This is equivalent to:

```c
int x;
int y;
int z;
```

Although valid,

many programmers prefer one declaration per line because it is easier to read.

Preferred:

```c
int x;
int y;
int z;
```

---

## Declaration Without Initialization

Example:

```c
int score;
```

The variable now exists.

However,

its value is **not initialized**.

Reading it before assigning a value results in **undefined behavior**.

---

## Memory Perspective

Suppose we write:

```c
int age;
```

The compiler reserves enough memory for an `int`.

Conceptually:

```
Variable

↓

age

↓

Memory

+---------+
|    ?    |
+---------+
```

The memory exists,

but its contents are unspecified until a value is assigned.

---

## Why Declare Variables?

Declaring variables allows the compiler to:

- Reserve memory
- Check data types
- Detect errors
- Generate correct machine code

Without declarations,

the compiler would not know how much memory to reserve.

---

## Real Examples

```c
char letter;

int count;

float average;

double temperature;
```

Each declaration introduces a new variable.

---

## Common Beginner Mistake

Many beginners think:

```c
int age;
```

means:

```
age = 0;
```

This is **incorrect**.

A declaration alone does **not** assign a value.

(We will learn initialization in the next section.)

---

## Mental Model

Imagine registering for university.

You provide:

- Your name
- Your major

The university now knows you exist.

However,

you have not attended any classes yet.

A declaration works the same way.

The compiler knows the variable exists,

but it has not yet received a value.

---

## Declaration vs Initialization

These are **not** the same.

Declaration:

```c
int age;
```

Declaration + Initialization:

```c
int age = 25;
```

The second statement performs two actions.

---

## 📚 Summary

A declaration introduces a variable to the compiler.

It specifies the variable's name and data type.

A declaration alone does not assign a value.

Variables should normally be initialized before being used.

---

## 🧠 Key Concepts

- Declaration
- Variable
- Data Type
- Compiler
- Memory Reservation

---

## ⚠ Common Mistakes

- Thinking declaration automatically assigns zero.
- Using a variable before initializing it.
- Confusing declaration with initialization.
- Declaring many unrelated variables on one line.

---

## 💡 Coach Tips

✔ Think:

```
Declaration

↓

"This variable exists."
```

✔ Initialization comes later.

✔ The compiler needs declarations before it can generate machine code.

✔ Prefer one declaration per line for readability.

---

## 🧩 Think Like the Computer

Suppose you write:

```c
int score;
```

Ask yourself:

- Does the compiler know the variable?
- Has memory been reserved?
- Does the variable already contain a useful value?

---

## 🏋️ Practice Exercises

1. Declare variables for:

- Age
- Height
- Grade
- Price

2. Rewrite this declaration using one variable per line.

```c
int x, y, z;
```

3. Explain why this is dangerous.

```c
int number;

printf("%d\n", number);
```

---

## 🎯 42 Piscine Notes

- ✅ Declare variables as close as possible to where they are used.
- ✅ Prefer one declaration per line.
- ✅ Never assume a local variable contains `0`.
- ✅ Always initialize variables before reading them.

---

## 🚀 Mastery Checklist

- [ ] I know what a declaration is.
- [ ] I understand what information a declaration provides.
- [ ] I know that declaration does not assign a value.
- [ ] I understand why the compiler needs declarations.
- [ ] I can distinguish declaration from initialization.

---

# Initialization

> "Initialization gives a variable its first value at the moment it is created."

---

## Introduction

In the previous section, we learned that declaring a variable tells the compiler:

- The variable's name
- The variable's data type

However,

a declaration alone does **not** provide a value.

To give a variable its **first value**, we use **Initialization**.

---

## What is Initialization?

Initialization is the process of assigning the **initial value** to a variable **at the moment it is declared**.

Example:

```c
int age = 25;
```

This single statement performs **two operations**.

1. Declares the variable.
2. Initializes it with the value `25`.

---

## Basic Syntax

```c
data_type variable_name = value;
```

Examples:

```c
int age = 25;

char grade = 'A';

float price = 19.99;

double pi = 3.1415926535;
```

Each variable receives its first value immediately after being created.

---

## Why Initialize Variables?

Suppose we write:

```c
int score;
```

The variable exists,

but its value is unknown.

Now compare it with:

```c
int score = 0;
```

Immediately after creation,

the variable already contains a valid value.

Initialization helps prevent bugs caused by reading uninitialized memory.

---

## Declaration vs Initialization

Declaration only:

```c
int age;
```

Declaration + Initialization:

```c
int age = 25;
```

Comparison:

| Statement | Declares Variable | Gives Initial Value |
|-----------|------------------|---------------------|
| `int age;` | ✅ | ❌ |
| `int age = 25;` | ✅ | ✅ |

---

## Initialization Happens Only Once

Consider this code.

```c
int age = 25;
```

The value:

```
25
```

is the **initial value**.

Later,

we write:

```c
age = 30;
```

This is **not** initialization.

It is called:

```
Assignment
```

Initialization happens only once,

when the variable is first created.

---

## Memory Perspective

Before initialization:

```c
int age;
```

Conceptually:

```
+---------+
|    ?    |
+---------+
```

After initialization:

```c
int age = 25;
```

Memory becomes:

```
+---------+
|   25    |
+---------+
```

Now the variable contains a known value.

---

## Examples

Example 1

```c
int lives = 3;
```

Initial value:

```
3
```

---

Example 2

```c
char letter = 'M';
```

Initial value:

```
'M'
```

---

Example 3

```c
float temperature = 23.5;
```

Initial value:

```
23.5
```

---

## Multiple Initializations

You may initialize several variables.

```c
int x = 1;
int y = 2;
int z = 3;
```

Although this is valid:

```c
int x = 1, y = 2, z = 3;
```

Most programmers prefer one declaration per line.

It is easier to read and debug.

---

## Initialization is Good Practice

Professional programmers try to initialize variables whenever possible.

Instead of:

```c
int count;
```

Prefer:

```c
int count = 0;
```

Even if the value changes later,

starting with a known value makes programs safer.

---

## Real-World Example

Suppose you're writing a game.

```c
int player_health = 100;
```

The player begins the game with:

```
100 Health
```

As the game continues,

the value changes,

but the initialization happened only once.

---

## Mental Model

Imagine buying a notebook.

Declaration:

You buy the notebook.

Initialization:

You write your first note inside it.

Later,

you can erase or replace the notes,

but the first note was the initialization.

---

## 📚 Summary

Initialization assigns the first value to a variable.

It happens when the variable is declared.

Initialization occurs only once.

Any later modification is called assignment.

Initializing variables helps prevent undefined behavior and improves program reliability.

---

## 🧠 Key Concepts

- Initialization
- Initial Value
- Declaration
- Variable
- Memory

---

## ⚠ Common Mistakes

- Confusing initialization with assignment.
- Believing initialization can happen multiple times.
- Forgetting to initialize variables before using them.
- Assuming declaration automatically initializes local variables.

---

## 💡 Coach Tips

✔ Initialize variables whenever possible.

✔ Initialization happens once.

✔ Everything after that is assignment.

✔ Reading an uninitialized variable leads to undefined behavior.

---

## 🧩 Think Like the Computer

Which statements perform initialization?

```c
int age;

age = 25;

int score = 100;

score = 200;
```

Identify:

- Declaration
- Initialization
- Assignment

---

## 🏋️ Practice Exercises

1. Write declarations with initialization for:

- Age
- Height
- Grade
- Balance

2. Explain why this is safer.

```c
int total = 0;
```

instead of

```c
int total;
```

3. Which of the following are initialized?

```c
int a;

int b = 5;

char c = 'A';

float d;
```

---

## 🎯 42 Piscine Notes

- ✅ Initialize variables whenever possible.
- ✅ One declaration per line improves readability.
- ✅ Never rely on uninitialized local variables.
- ✅ Clear initialization makes debugging easier.

---

## 🚀 Mastery Checklist

- [ ] I know what initialization is.
- [ ] I understand that initialization happens only once.
- [ ] I know the difference between declaration and initialization.
- [ ] I understand why initialization improves program safety.
- [ ] I can identify initialized and uninitialized variables.

---

# Assignment

> "Assignment changes the value stored inside an existing variable."

---

## Introduction

Once a variable has been created,

its value can change many times during the execution of the program.

Changing the value of an existing variable is called:

```
Assignment
```

Unlike initialization,

assignment can happen **as many times as needed**.

---

## What is Assignment?

Assignment is the process of storing a new value into an existing variable.

Example:

```c
int age = 25;

age = 30;
```

The first line:

- Declares the variable
- Initializes the variable

The second line:

- Assigns a new value

---

## Assignment Operator

The assignment operator is:

```c
=
```

Example:

```c
score = 100;
```

Read it as:

> "Store the value 100 inside the variable `score`."

Notice:

It does **not** mean:

```
score equals 100
```

It means:

```
Put 100 into score.
```

---

## Basic Syntax

```c
variable = value;
```

Examples:

```c
age = 26;

grade = 'A';

price = 29.99;

is_alive = 1;
```

---

## Assignment Changes Memory

Suppose we write:

```c
int score = 10;
```

Memory:

```
+---------+
|   10    |
+---------+
```

Later:

```c
score = 50;
```

Memory becomes:

```
+---------+
|   50    |
+---------+
```

Notice:

The **memory address stays the same**.

Only the stored value changes.

---

## Assignment Multiple Times

A variable may receive many assignments.

```c
int x = 0;

x = 5;

x = 20;

x = -3;

x = 100;
```

The variable is initialized only once,

but assigned many times.

---

## Assignment from Another Variable

The assigned value does not have to be a constant.

Example:

```c
int a = 10;

int b = 0;

b = a;
```

Result:

```
a = 10

b = 10
```

The value stored in `a` is copied into `b`.

The variables remain independent.

---

## Assignment Using Expressions

The right side may contain an expression.

Example:

```c
int age = 20;

age = age + 5;
```

Execution:

```
20 + 5

↓

25
```

The final value stored becomes:

```
25
```

---

Another example:

```c
int x = 10;

x = x * 2;
```

Result:

```
20
```

---

## Common Beginner Mistake

Many beginners think:

```c
x = x + 1;
```

is impossible.

In mathematics,

this is incorrect.

```
x = x + 1

❌
```

But in C,

it means:

```
Take the current value of x.

↓

Add 1.

↓

Store the result back into x.
```

The left side is the destination.

The right side is evaluated first.

---

## Assignment vs Equality

Very important.

Assignment:

```c
=
```

Comparison:

```c
==
```

These are completely different.

Assignment:

```c
score = 100;
```

Stores a value.

Comparison:

```c
score == 100
```

Checks whether two values are equal.

We'll study comparisons in the Operators chapter.

---

## Mental Model

Imagine a whiteboard.

Initialization:

You write the first number.

```
25
```

Assignment:

You erase it and write:

```
30
```

The whiteboard is the same.

Only its contents changed.

---

## Real Example

Bank account.

```c
int balance = 1000;
```

Customer deposits money.

```c
balance = 1500;
```

Customer withdraws money.

```c
balance = 1200;
```

The account remains the same.

Only the stored value changes.

---

## 📚 Summary

Assignment changes the value stored inside an existing variable.

It uses the assignment operator:

```c
=
```

Unlike initialization,

assignment may happen many times during program execution.

The variable's memory address remains the same.

Only the stored value changes.

---

## 🧠 Key Concepts

- Assignment
- Assignment Operator
- Value
- Expression
- Variable

---

## ⚠ Common Mistakes

- Confusing `=` with `==`.
- Thinking assignment creates a new variable.
- Believing `x = x + 1` is invalid.
- Forgetting that the right side is evaluated first.

---

## 💡 Coach Tips

✔ Read:

```c
x = 5;
```

as:

> "Store 5 in x."

✔ Never read it as:

> "x equals 5."

✔ Assignment changes values,

not addresses.

✔ A variable can be assigned infinitely many times.

---

## 🧩 Think Like the Computer

Consider:

```c
int x = 5;

x = x + 2;

x = x * 3;
```

Answer:

- What is the initial value?
- What is the final value?
- How many assignments occurred?
- Did the memory address ever change?

---

## 🏋️ Practice Exercises

1. Predict the final value.

```c
int x = 10;

x = 20;

x = x + 5;
```

---

2. Explain why this is valid.

```c
x = x + 1;
```

---

3. Which lines are assignments?

```c
int a = 5;

a = 8;

int b;

b = a;
```

---

4. Explain the difference between:

```c
=
```

and

```c
==
```

---

## 🎯 42 Piscine Notes

- ✅ Assignment changes an existing variable.
- ✅ Initialization happens only once.
- ✅ Use meaningful variable names when assigning values.
- ✅ Never confuse `=` with `==`.

---

## 🚀 Mastery Checklist

- [ ] I know what assignment is.
- [ ] I understand the assignment operator.
- [ ] I know the difference between assignment and initialization.
- [ ] I know the difference between `=` and `==`.
- [ ] I understand that assignment changes the value, not the address.

---

# Declaration vs Initialization vs Assignment

> "These three concepts are closely related, but they are not the same."

---

# Introduction

One of the most common mistakes among beginner C programmers is confusing:

- Declaration
- Initialization
- Assignment

Although these operations often appear together,

they have different meanings.

Understanding the difference is essential before moving to more advanced topics.

---

# Declaration

A declaration introduces a variable to the compiler.

It tells the compiler:

- The variable's name
- The variable's data type

Example:

```c
int age;
```

This statement declares a variable named:

```
age
```

No value has been assigned yet.

---

# Initialization

Initialization gives the variable its **first value**.

Example:

```c
int age = 25;
```

This statement performs two actions.

```
Declaration

+

Initialization
```

The variable is created,

then immediately receives its first value.

Initialization happens only once.

---

# Assignment

Assignment changes the value of an already existing variable.

Example:

```c
age = 30;
```

The variable already exists.

Only its stored value changes.

Assignment may occur many times.

---

# Visual Timeline

```
Declaration

↓

Initialization

↓

Assignment

↓

Assignment

↓

Assignment

↓

...
```

Declaration happens once.

Initialization happens once.

Assignment can happen forever.

---

# Example

```c
int age;
```

↓

Declaration

---

```c
age = 25;
```

↓

Assignment

---

Now compare with:

```c
int age = 25;
```

↓

Declaration

+

Initialization

---

Later:

```c
age = 30;
```

↓

Assignment

---

Later:

```c
age = 35;
```

↓

Assignment

---

# Memory Perspective

Declaration

```
Variable Exists

↓

Memory Reserved

↓

Unknown Value
```

Initialization

```
Variable Exists

↓

Memory Reserved

↓

First Value Stored
```

Assignment

```
Variable Exists

↓

Memory Address Stays The Same

↓

Stored Value Changes
```

---

# Side-by-Side Comparison

| Feature | Declaration | Initialization | Assignment |
|---------|-------------|----------------|------------|
| Creates Variable | ✅ | ❌ *(requires a declaration)* | ❌ |
| Gives First Value | ❌ | ✅ | ❌ |
| Changes Existing Value | ❌ | ❌ | ✅ |
| Happens Once | ✅ | ✅ | ❌ |
| Can Repeat | ❌ | ❌ | ✅ |

---

# Complete Example

```c
int score;

score = 50;

score = 75;

score = 100;
```

Analysis.

```
int score;

↓

Declaration
```

```
score = 50;

↓

Assignment
```

```
score = 75;

↓

Assignment
```

```
score = 100;

↓

Assignment
```

Notice:

There was **no initialization**.

---

Now compare.

```c
int score = 50;

score = 75;

score = 100;
```

Analysis.

```
int score = 50;

↓

Declaration

+

Initialization
```

```
score = 75;

↓

Assignment
```

```
score = 100;

↓

Assignment
```

---

# Common Beginner Mistakes

Incorrect thinking.

```
int age;

↓

Initialization
```

❌

Correct.

```
Declaration
```

---

Incorrect thinking.

```
age = 25;

↓

Initialization
```

❌

Correct.

```
Assignment
```

---

Incorrect thinking.

```
int age = 25;

↓

Assignment
```

❌

Correct.

```
Declaration

+

Initialization
```

---

# Mental Model

Imagine renting an apartment.

Declaration

↓

You sign the rental contract.

The apartment now belongs to you.

Initialization

↓

You move your furniture inside for the first time.

Assignment

↓

You rearrange or replace the furniture later.

The apartment stays the same.

Only its contents change.

---

## 📚 Summary

Declaration introduces a variable.

Initialization gives it its first value.

Assignment changes its value later.

Understanding the difference between these three operations is fundamental to writing correct C programs.

---

## 🧠 Key Concepts

- Declaration
- Initialization
- Assignment
- Variable
- Memory
- First Value

---

## ⚠ Common Mistakes

- Thinking declaration automatically initializes a variable.
- Thinking assignment is initialization.
- Believing initialization can happen multiple times.
- Confusing `=` with declaration.

---

## 💡 Coach Tips

✔ Ask yourself one question.

> "Does the variable already exist?"

If the answer is:

```
No

↓

Declaration
```

If it also receives its first value:

```
Initialization
```

If it already exists:

```
Assignment
```

This simple question removes almost all confusion.

---

## 🧩 Think Like the Computer

Identify each operation.

```c
int x;

x = 10;

int y = 20;

y = 30;
```

For every line,

write:

- Declaration
- Initialization
- Assignment

---

## 🏋️ Practice Exercises

Classify every line.

```c
int age;

age = 25;

int score = 100;

score = score + 50;

char grade;

grade = 'A';
```

Explain why each line belongs to its category.

---

## 🎯 42 Piscine Notes

- ✅ Know these three concepts perfectly.
- ✅ Many Piscine exercises assume you already understand the difference.
- ✅ Initialize variables whenever possible.
- ✅ Assignment modifies existing variables.
- ✅ Declaration introduces variables to the compiler.

---

## 🚀 Mastery Checklist

- [ ] I know what declaration is.
- [ ] I know what initialization is.
- [ ] I know what assignment is.
- [ ] I can distinguish all three in real code.
- [ ] I can explain the difference without looking at notes.

---

# Constants

> "A constant is a value that does not change during the execution of a program."

🟢 Beginner

⏱ Estimated Study Time: ~30 Minutes

---

## Introduction

So far,

we have learned that variables can change.

Example:

```c
int score = 100;

score = 150;

score = 200;
```

The value stored inside the variable changes over time.

But what if we have a value that should **never change**?

Examples:

- The number of days in a week
- The value of π (Pi)
- The speed of light
- The maximum number of players
- The size of a buffer

These values are called **Constants**.

---

## What is a Constant?

A constant is a value that remains the same during program execution.

Unlike variables,

constants are **not intended to be modified**.

---

## Literal Constants

Sometimes we write values directly.

Example:

```c
int age = 25;
```

The number:

```
25
```

is called an **Integer Literal**.

Other examples:

```c
'A'

3.14

100

0

-15
```

These are all literal constants.

---

## Named Constants

Instead of writing the same value many times,

we usually give it a meaningful name.

Example:

```c
#define MAX_PLAYERS 4
```

Instead of writing:

```c
if (players > 4)
```

we write:

```c
if (players > MAX_PLAYERS)
```

The second version is much easier to understand.

---

## Why Use Constants?

Imagine this program.

```c
if (score > 100)
```

Later,

you discover that the maximum score should be:

```
150
```

Now you must search the entire project.

Instead,

use:

```c
#define MAX_SCORE 150
```

Now changing the value requires modifying only one line.

---

## Constants Improve Readability

Compare.

Poor:

```c
if (speed > 120)
```

Better:

```c
if (speed > MAX_SPEED)
```

The second version explains the meaning immediately.

---

## Constants Prevent Mistakes

Suppose:

```c
#define BUFFER_SIZE 1024
```

Every part of the program now uses the same value.

Without constants,

one programmer might write:

```c
1024
```

Another:

```c
1000
```

Another:

```c
2048
```

Bugs quickly appear.

Constants eliminate this problem.

---

## Different Ways to Create Constants

In C,

there are several methods.

### Literal Constants

```c
42

'A'

3.14
```

---

### Macro Constants

```c
#define PI 3.1415926535

#define MAX_SIZE 1024
```

---

### const Variables

Later in the handbook,

we'll study:

```c
const int max_age = 120;
```

For now,

just know that this is another way to create values that should not be modified.

---

## Real-World Examples

Game:

```c
#define MAX_LEVEL 100
```

Network:

```c
#define PORT 8080
```

Graphics:

```c
#define SCREEN_WIDTH 1920

#define SCREEN_HEIGHT 1080
```

These values rarely change,

making constants the ideal choice.

---

## Mental Model

Imagine printing a road sign.

```
Speed Limit

120
```

You do not erase the number every few minutes.

It stays fixed.

Variables are like a whiteboard.

Constants are like a printed road sign.

---

## 📚 Summary

A constant is a value that does not change during program execution.

Constants improve readability,

reduce mistakes,

and make programs easier to maintain.

C provides several ways to define constants,

including literals,

macros,

and `const` variables.

---

## 🧠 Key Concepts

- Constant
- Literal
- Macro
- `#define`
- `const`

---

## ⚠ Common Mistakes

- Using magic numbers throughout the code.
- Giving constants unclear names.
- Assuming every value should be a variable.
- Confusing literal constants with named constants.

---

## 💡 Coach Tips

✔ Replace repeated numbers with named constants.

✔ Use descriptive names.

✔ Write macro constants in:

```text
UPPER_CASE
```

✔ Avoid "magic numbers."

---

## What is a Magic Number?

A **magic number** is a numeric value written directly into the code without explaining its meaning.

Example:

```c
if (score > 150)
```

Where did:

```
150
```

come from?

Nobody knows.

Better:

```c
#define MAX_SCORE 150

if (score > MAX_SCORE)
```

Now the meaning is obvious.

Professional programmers avoid magic numbers whenever possible.

---

## 🧩 Think Like the Computer

Which version is easier to maintain?

Version 1

```c
if (speed > 120)
```

Version 2

```c
#define MAX_SPEED 120

if (speed > MAX_SPEED)
```

Why?

---

## 🏋️ Practice Exercises

1. Identify the constants.

```c
int age = 25;

#define MAX_SIZE 1024;

const int DAYS = 7;
```

---

2. Replace the magic numbers.

```c
if (temperature > 40)

if (players == 4)

if (score >= 100)
```

---

3. Give meaningful names for:

- 60 (seconds in a minute)
- 24 (hours in a day)
- 365 (days in a year)

---

## 🎯 42 Piscine Notes

- ✅ Avoid magic numbers.
- ✅ Prefer meaningful names.
- ✅ Use `UPPER_CASE` for macro constants.
- ✅ Do not overuse constants for values that truly change.

---

## 🚀 Mastery Checklist

- [ ] I know what a constant is.
- [ ] I know the difference between variables and constants.
- [ ] I understand what a magic number is.
- [ ] I know why constants improve readability.
- [ ] I know the common ways to define constants in C.

---

# 🎉 End of Chapter 5 — Variables

Congratulations!

You now understand how programmers store, name, initialize, modify, and protect data using variables and constants.

You are ready to move to the next major chapter:

# 🔠 Chapter 6 — Data Types

> "A data type tells the compiler what kind of data a variable can store, how much memory it needs, and how that data should be interpreted."

🟢 Beginner

⏱ Estimated Study Time: ~4–5 Hours

---

## Introduction

Imagine you have three different containers.

```
🥤 Glass

📦 Box

🛢️ Tank
```

Could you store the same amount of water in each one?

Of course not.

Each container has a different size and a different purpose.

Variables work exactly the same way.

Every variable has a **Data Type**.

The data type tells the computer:

- What kind of data the variable stores.
- How much memory it occupies.
- What operations can be performed on it.
- What range of values it can hold.

Without data types,

the computer would not know how to interpret the bits stored in memory.

---

## What is a Data Type?

A data type is a rule that describes how a value is stored and interpreted in memory.

For example,

consider these variables.

```c
char letter = 'A';

int age = 25;

float price = 19.99;
```

Although all of them are stored as binary,

the computer interprets each one differently.

```
'A'

↓

Character
```

```
25

↓

Integer
```

```
19.99

↓

Floating-Point Number
```

The stored bits may look completely different,

but the data type tells the CPU how to interpret them.

---

## Why Do Data Types Exist?

Suppose the computer stores:

```
01000001
```

What does it represent?

Could it be:

```
65
```

or

```
'A'
```

The answer depends entirely on the data type.

Example:

```c
char c = 'A';
```

The computer interprets the bits as a character.

Now:

```c
unsigned char n = 65;
```

The same bits are interpreted as a number.

The bits did not change.

Only their interpretation changed.

---

## Data Types Define Memory Size

Different data types require different amounts of memory.

Typical sizes on modern systems are:

| Data Type | Typical Size |
|-----------|-------------:|
| `char` | 1 Byte |
| `short` | 2 Bytes |
| `int` | 4 Bytes |
| `long` | 8 Bytes* |
| `float` | 4 Bytes |
| `double` | 8 Bytes |

> **Note:** The exact size of some types (especially `int` and `long`) depends on the compiler and operating system. Use `sizeof` to determine the actual size on your system.

---

## Why Not Use One Data Type for Everything?

Suppose every variable occupied:

```
8 Bytes
```

even if it only stored:

```c
char letter = 'A';
```

Millions of small variables would waste enormous amounts of memory.

On the other hand,

suppose every variable occupied only:

```
1 Byte
```

Large numbers would no longer fit.

Different data types provide a balance between:

- Memory usage
- Performance
- Range of values

---

## Choosing the Right Data Type

Think about the information you want to store.

Age

```c
int age;
```

Letter

```c
char grade;
```

Temperature

```c
float temperature;
```

Bank Balance

```c
double balance;
```

The programmer chooses the type that best represents the data.

---

## Data Types Affect Operations

Different data types support different kinds of operations.

Example:

```c
int a = 10;
int b = 5;
```

Arithmetic:

```c
a + b
```

works perfectly.

Now:

```c
char c = 'A';
```

Although `char` is stored as a number internally,

its primary purpose is to represent characters.

Understanding the intended use of each type leads to cleaner code.

---

## Mental Model

Imagine labels on storage boxes.

```
Fruit

↓

🍎 Apples
```

```
Books

↓

📚 Books
```

```
Clothes

↓

👕 Clothes
```

The label tells everyone what belongs inside.

A data type works the same way.

It tells the compiler how the stored bits should be interpreted.

---

## Roadmap of This Chapter

In this chapter we will study:

```
char
    ↓
short
    ↓
int
    ↓
long
    ↓
float
    ↓
double
    ↓
signed
    ↓
unsigned
    ↓
sizeof
    ↓
Type Conversion
    ↓
Overflow
```

Each topic builds directly on the previous one.

---

## 📚 Summary

A data type defines:

- The kind of data stored.
- The amount of memory required.
- The valid range of values.
- How the CPU interprets the stored bits.

Choosing the correct data type is essential for writing efficient and reliable C programs.

---

## 🧠 Key Concepts

- Data Type
- Memory Size
- Interpretation
- Range
- Storage

---

## ⚠ Common Mistakes

- Thinking data types only change memory size.
- Assuming all computers use the same sizes.
- Using larger data types than necessary.
- Believing the stored bits determine the meaning by themselves.

---

## 💡 Coach Tips

✔ A data type is a description, not the data itself.

✔ The same binary value can represent different things depending on its type.

✔ Learn **why** each type exists before memorizing sizes.

✔ Always use `sizeof` when you need the exact size on your platform.

---

## 🧩 Think Like the Computer

Suppose memory contains:

```
01000001
```

Could it represent:

- The number `65`?
- The character `'A'`?

The answer is:

**Yes.**

What determines the correct interpretation?

---

## 🏋️ Practice Exercises

1. Define "Data Type" in your own words.

2. Explain why C has multiple data types.

3. Why doesn't every variable simply use 8 bytes?

4. Which data type would you choose for:

- A person's age
- A letter grade
- A product price
- The number of students in a class

Explain your choices.

---

## 🎯 42 Piscine Notes

- ✅ Choose the smallest appropriate type that correctly represents your data.
- ✅ Don't memorize sizes—verify them with `sizeof`.
- ✅ Understand the purpose of each type before learning its limits.
- ✅ Data types affect both correctness and memory usage.

---

## 🚀 Mastery Checklist

- [ ] I know what a data type is.
- [ ] I know why data types exist.
- [ ] I understand that data types determine memory size and interpretation.
- [ ] I know why different data types are necessary.
- [ ] I am ready to study each built-in C data type individually.

---

# char

> "A `char` stores a single character, but internally it is just a small integer."

🟢 Beginner

⏱ Estimated Study Time: ~45 Minutes

---

## Introduction

One of the first data types every C programmer learns is:

```c
char
```

Many beginners believe that `char` stores letters.

That is only partially true.

Internally,

a `char` stores a **small integer**.

Because of ASCII (and later Unicode),

that integer represents a character.

Understanding this idea is essential before learning strings.

---

## What is char?

The keyword:

```c
char
```

stands for:

```
Character
```

A `char` is used to store a **single character**.

Examples:

```c
char letter = 'A';

char grade = 'B';

char digit = '7';

char symbol = '#';
```

Each variable stores exactly one character.

---

## Memory Size

A `char` always occupies:

```
1 Byte

=

8 Bits
```

Unlike other data types,

the C standard guarantees that:

```
sizeof(char)

==

1
```

on every C implementation.

---

## ⚠️ Important: char's Signedness is Implementation-Defined

The C standard does NOT specify whether a plain `char` is signed or unsigned by default — this depends on the compiler and platform.

```c
char c = -1;
// On some systems: c stays negative (char behaves like signed char)
// On other systems: c becomes 255 (char behaves like unsigned char)
```

This matters when:

- Comparing `char` values against negative numbers
- Passing `char` to functions expecting `int` (like `ctype.h` functions: `isalpha()`, `isdigit()`, etc.)
- Working with raw bytes in libft-style projects

**Best practice:** when signedness matters, be explicit.

```c
signed char c = -1;

unsigned char c = 255;
```

Or cast explicitly:

```c
(unsigned char)str[i]
```

---

## Why One Byte?

Earlier,

we learned that one byte can represent:

```
256 different values
```

This is enough to store:

- English letters
- Digits
- Punctuation
- Control characters

through the ASCII table.

---

## Characters are Numbers

Consider:

```c
char letter = 'A';
```

Internally,

the computer stores:

```
65
```

because:

```
'A'

↓

ASCII

↓

65
```

Another example:

```c
char digit = '7';
```

Internally:

```
55
```

because:

```
'7'

↓

ASCII

↓

55
```

The computer stores numbers.

The compiler and terminal display them as characters.

---

## Character Literals

Characters are written using:

```
Single Quotes
```

Example:

```c
'A'

'B'

'7'

'?'
```

Notice:

Single quotes represent one character.

---

## Strings are Different

This is a character.

```c
'A'
```

This is a string.

```c
"A"
```

Although they look similar,

they are completely different.

```
'A'

↓

One Character
```

```
"A"

↓

A String
```

We'll study strings in a later chapter.

---

## Printing Characters

Use:

```c
%c
```

Example:

```c
char letter = 'A';

printf("%c\n", letter);
```

Output:

```
A
```

---

## Printing ASCII Values

Because a `char` is stored as a number,

we can print it as an integer.

```c
char letter = 'A';

printf("%d\n", letter);
```

Output:

```
65
```

Now reverse it.

```c
printf("%c\n", 66);
```

Output:

```
B
```

The same data can be interpreted differently depending on the format specifier.

---

## Common Escape Characters

Some characters cannot be typed directly.

C provides escape sequences.

| Escape | Meaning |
|---------|---------|
| `'\n'` | New Line |
| `'\t'` | Tab |
| `'\\'` | Backslash |
| `'\''` | Single Quote |
| `'\"'` | Double Quote |
| `'\0'` | Null Character |

Example:

```c
printf("Hello\nWorld\n");
```

Output:

```
Hello
World
```

---

## Real-World Examples

Store a grade.

```c
char grade = 'A';
```

Store a menu option.

```c
char choice = 'Y';
```

Store a chess piece.

```c
char piece = 'K';
```

Store a digit.

```c
char digit = '5';
```

---

## Mental Model

Imagine a mailbox.

It has room for only **one letter**.

```
+-----+
|  A  |
+-----+
```

If you need to store:

```
Hello
```

one mailbox is not enough.

You need several mailboxes.

That idea leads directly to **strings**.

---

## 📚 Summary

The `char` data type stores a single character.

Internally,

characters are represented as integer values,

usually according to the ASCII table.

A `char` always occupies one byte.

Single quotes are used for character literals,

while double quotes create strings.

---

## 🧠 Key Concepts

- char
- Character
- ASCII
- Character Literal
- `%c`
- `%d`

---

## ⚠ Common Mistakes

- Confusing `'A'` with `"A"`.
- Forgetting to use single quotes.
- Thinking a `char` stores text.
- Confusing `'7'` with `7`.

---

## 💡 Coach Tips

✔ A `char` stores **one character**, not a word.

✔ Internally, every character is just a number.

✔ Remember:

```c
'A'
```

≠

```c
"A"
```

✔ Learn the important ASCII values:

```
'A' = 65

'a' = 97

'0' = 48
```

---

## 🧩 Think Like the Computer

Predict the output.

```c
char c = 'A';

printf("%c\n", c);

printf("%d\n", c);
```

Then predict:

```c
printf("%c\n", 90);
```

What character will be printed?

---

## 🏋️ Practice Exercises

1. Declare variables to store:

- The letter `M`
- The digit `8`
- The symbol `#`

---

2. Predict the output.

```c
char letter = 'C';

printf("%d\n", letter);
```

---

3. Explain the difference between:

```c
'A'
```

and

```c
"A"
```

---

4. Why does a `char` always occupy exactly one byte?

---

## 🎯 42 Piscine Notes

- ✅ Use `char` for a single character.
- ✅ Use `%c` to print characters.
- ✅ Remember that `char` is an integer type in C.
- ✅ Don't confuse character literals with strings.

---

## 🚀 Mastery Checklist

- [ ] I know what `char` is.
- [ ] I know that `char` occupies one byte.
- [ ] I understand that characters are stored as numbers.
- [ ] I know the difference between `'A'` and `"A"`.
- [ ] I can print characters using `%c` and their numeric values using `%d`.

---

# short

> "A `short` stores integer values using less memory than a typical `int`."

🟢 Beginner

⏱ Estimated Study Time: ~30 Minutes

---

## Introduction

In the previous section,

we learned about:

```c
char
```

which occupies:

```
1 Byte
```

Now we move to another integer type:

```c
short
```

Unlike `char`,

which is mainly used for characters,

`short` is designed to store **small integer values**.

It uses less memory than a typical `int`.

---

## What is short?

The keyword:

```c
short
```

is an abbreviation for:

```c
short int
```

Both declarations are identical.

```c
short age;

short int age;
```

Most programmers simply write:

```c
short
```

---

## Memory Size

On almost all modern computers,

a `short` occupies:

```
2 Bytes

=

16 Bits
```

Unlike `char`,

the C standard guarantees only that:

```
sizeof(short)

<=

sizeof(int)
```

On almost every modern system:

```
sizeof(short)

=

2
```

---

## Range of Values

A signed `short` typically stores:

```
-32,768

↓

32,767
```

An unsigned `short` typically stores:

```
0

↓

65,535
```

We'll study `signed` and `unsigned` later in this chapter.

---

## Declaring a short

Example:

```c
short age = 25;

short temperature = -10;

short score = 1500;
```

Each variable stores an integer value.

---

## Printing a short

Use the `%hd` format specifier.

Example:

```c
short age = 25;

printf("%hd\n", age);
```

Output:

```
25
```

> **Note:** Because of C's integer promotions, `%d` often appears to work with a `short` in `printf`, but `%hd` is the correct format specifier and is the best habit to learn.

---

## ⚠️ Critical: scanf() vs printf()

With `printf()`, using `%d` instead of `%hd` for a `short` often still "works" because of integer promotion — it's a bad habit, not a bug.

With `scanf()`, the difference is critical:

```c
short age;

scanf("%d", &age);   // ❌ UNDEFINED BEHAVIOR
```

`scanf()` writes 4 bytes (the size of `int`) into a variable that only has 2 bytes (the size of `short`) reserved. This corrupts adjacent memory and can crash your program or cause silent bugs elsewhere.

Always use `%hd` with `scanf()` for `short`:

```c
short age;

scanf("%hd", &age);  // ✅ Correct
```

---

## Why Does short Exist?

Imagine storing:

```
Age

↓

26
```

Would using:

```
8 Bytes
```

be efficient?

Not really.

If you have millions of values,

using a smaller data type can reduce memory usage significantly.

---

## Memory Comparison

```
char

↓

1 Byte
```

```
short

↓

2 Bytes
```

```
int

↓

Usually 4 Bytes
```

As the type becomes larger,

it can represent larger numbers.

---

## Real-World Examples

Store a person's age.

```c
short age = 26;
```

Store the year.

```c
short year = 2026;
```

Store the temperature.

```c
short temperature = -15;
```

Store the number of students.

```c
short students = 500;
```

All of these fit comfortably inside a `short`.

---

## Overflow Example

Suppose we write:

```c
short number = 32767;
```

Now imagine adding one.

```c
number = number + 1;
```

The result cannot be represented by a signed `short`.

This causes:

```
Overflow
```

We'll study overflow in detail later in this chapter.

---

## short vs int

Many beginners ask:

> Why not always use `int`?

The answer depends on the application.

If memory usage is important,

smaller types can be useful.

However,

on modern CPUs,

`int` is often the preferred default integer type because it usually matches the processor's natural word size and is generally the most efficient choice.

Choose the type that best matches both your data and your application's requirements.

---

## Mental Model

Imagine three boxes.

```
Small Box

↓

char
```

```
Medium Box

↓

short
```

```
Large Box

↓

int
```

Each box can hold different amounts of data.

Choosing the right box avoids wasting space while still fitting the contents.

---

## 📚 Summary

The `short` data type stores integer values.

It typically occupies:

```
2 Bytes
```

and is used when the range of an `int` is unnecessary.

Using the appropriate integer type helps balance memory usage and program efficiency.

---

## 🧠 Key Concepts

- short
- short int
- Integer
- Range
- Overflow

---

## ⚠ Common Mistakes

- Thinking `short` always occupies exactly 2 bytes because the standard requires it.
- Confusing `short` with `char`.
- Using `short` without considering the required range.
- Ignoring overflow.

---

## 💡 Coach Tips

✔ `short` is simply a smaller integer type.

✔ Don't choose a type based only on size.

✔ Choose a type that safely stores every possible value.

✔ Use `sizeof()` whenever you want to verify the actual size on your platform.

---

## 🧩 Think Like the Computer

Suppose:

```c
short age = 25;
```

Ask yourself:

- How many bytes are reserved?
- What happens if you try to store:

```
100000
```

inside a `short`?

Why?

---

## 🏋️ Practice Exercises

1. Declare a `short` variable for:

- Age
- Temperature
- Year
- Number of students

---

2. Explain why this value cannot fit inside a signed `short`.

```
50000
```

---

3. Compare:

```
char

short

int
```

Which one occupies more memory?

---

4. Why doesn't every program simply use `short`?

---

## 🎯 42 Piscine Notes

- ✅ `short` is another integer type.
- ✅ Prefer `int` unless you have a specific reason to use `short`.
- ✅ Learn the typical ranges, but remember that `sizeof()` is the authoritative way to check your platform.
- ✅ Understand overflow before relying on integer limits.

---

## 📊 Data Type Summary

| Property | `short` |
|----------|----------|
| Category | Integer |
| Typical Size | 2 Bytes |
| Typical Signed Range | -32,768 → 32,767 |
| Typical Unsigned Range | 0 → 65,535 |
| Stores | Small Integer Values |
| Format Specifier | `%hd` |
| Common Uses | Age, Year, Counters, Small Numbers |

---

## 🚀 Mastery Checklist

- [ ] I know what `short` is.
- [ ] I know its typical memory size.
- [ ] I understand why `short` exists.
- [ ] I know its typical range.
- [ ] I understand the concept of integer overflow.

---

# int

> "An `int` is the standard integer data type in C and is the most commonly used type for storing whole numbers."

🟢 Beginner

⏱ Estimated Study Time: ~45 Minutes

---

## Introduction

In the previous section,

we learned about:

```c
short
```

Now we arrive at the most commonly used integer type:

```c
int
```

Whenever programmers need to store whole numbers,

their first choice is usually:

```c
int
```

Throughout the 1337 Piscine,

you will use `int` more than any other data type.

---

## What is int?

The keyword:

```c
int
```

stands for:

```
Integer
```

An integer is a whole number.

Examples:

```
-100

-5

0

12

2026

50000
```

Unlike floating-point numbers,

integers do **not** contain a decimal point.

---

## Memory Size

On most modern systems,

an `int` occupies:

```
4 Bytes

=

32 Bits
```

However,

the C standard does **not** require an `int` to be exactly 4 bytes.

It only guarantees that:

```
sizeof(short)

<=

sizeof(int)

<=

sizeof(long)
```

Use:

```c
sizeof(int)
```

to determine the exact size on your system.

---

## Typical Range

A signed `int` usually stores:

```
-2,147,483,648

↓

2,147,483,647
```

An unsigned `int` usually stores:

```
0

↓

4,294,967,295
```

---

## Declaring an int

Examples:

```c
int age = 25;

int score = 100;

int temperature = -15;

int population = 500000;
```

---

## Printing an int

Use:

```c
%d
```

Example:

```c
int age = 25;

printf("%d\n", age);
```

Output:

```
25
```

---

## Why is int the Default Integer Type?

Modern processors are optimized for handling integers that match their natural word size.

Because of this,

operations using `int` are usually very efficient.

For most programs,

there is no advantage in replacing every `int` with `short`.

This is why experienced C programmers usually choose `int` unless another type is clearly more appropriate.

---

## Common Uses

Store age.

```c
int age = 26;
```

Store score.

```c
int score = 500;
```

Store number of students.

```c
int students = 120;
```

Store loop counters.

```c
int i;
```

Store arithmetic results.

```c
int total = a + b;
```

These are among the most common uses of `int`.

---

## Integer Arithmetic

Example:

```c
int a = 20;

int b = 5;
```

Addition

```c
a + b
```

↓

```
25
```

Subtraction

```c
a - b
```

↓

```
15
```

Multiplication

```c
a * b
```

↓

```
100
```

Division

```c
a / b
```

↓

```
4
```

---

## Integer Division

One of the most common beginner mistakes.

Example:

```c
int a = 7;

int b = 2;

printf("%d\n", a / b);
```

Output:

```
3
```

Not:

```
3.5
```

Why?

Because both operands are integers.

The fractional part is discarded.

We'll study type conversion later in this chapter.

---

## Overflow

Suppose:

```c
int number = 2147483647;
```

Now:

```c
number = number + 1;
```

The value exceeds the maximum range.

Result:

```
Overflow
```

The exact result depends on the implementation and signed overflow in C is **undefined behavior**.

For unsigned integers,

overflow wraps around according to the C standard.

We'll study overflow in detail later.

---

## int vs short

Comparison:

```
short

↓

Smaller range

↓

Typically 2 Bytes
```

```
int

↓

Larger range

↓

Typically 4 Bytes
```

For most everyday programming,

`int` is the preferred integer type.

---

## Mental Model

Imagine containers.

```
Cup

↓

char
```

```
Bucket

↓

short
```

```
Barrel

↓

int
```

The barrel stores much more than the bucket.

Choosing the correct container prevents wasted memory while providing enough space.

---

## 📚 Summary

`int` is the standard integer type in C.

It stores whole numbers,

typically occupies four bytes,

and is the preferred choice for most integer calculations.

Because of its balance between size and performance,

it is one of the most frequently used data types in C programming.

---

## 🧠 Key Concepts

- int
- Integer
- Whole Numbers
- Integer Arithmetic
- Integer Division
- Overflow

---

## ⚠ Common Mistakes

- Expecting integer division to produce decimal values.
- Assuming `int` is always 4 bytes on every system.
- Ignoring integer overflow.
- Using `float` when only whole numbers are required.

---

## 💡 Coach Tips

✔ If you're storing whole numbers,

`int` is usually the correct choice.

✔ Remember:

```c
7 / 2

↓

3
```

not

```
3.5
```

✔ Learn integer division early.

It appears constantly in Piscine exercises.

✔ Verify sizes with `sizeof()` rather than assuming.

---

## 🧩 Think Like the Computer

Predict the output.

```c
int a = 9;

int b = 4;

printf("%d\n", a / b);
```

Now predict:

```c
printf("%d\n", a * b);
```

Explain each result.

---

## 🏋️ Practice Exercises

1. Declare variables to store:

- Age
- Score
- Number of books
- Population

---

2. Predict the output.

```c
int x = 15;

int y = 4;

printf("%d\n", x + y);

printf("%d\n", x - y);

printf("%d\n", x * y);

printf("%d\n", x / y);
```

---

3. Explain why:

```c
7 / 2
```

does not produce:

```
3.5
```

---

4. Compare:

```
char

short

int
```

Which one would you normally choose for arithmetic?

Why?

---

## 🎯 42 Piscine Notes

- ✅ `int` is the default integer type.
- ✅ Most Piscine exercises use `int`.
- ✅ Learn integer division thoroughly.
- ✅ Never assume the exact size of an `int`; use `sizeof()` when it matters.

---

## 📊 Data Type Summary

| Property | `int` |
|----------|-------|
| Category | Integer |
| Typical Size | 4 Bytes |
| Typical Signed Range | -2,147,483,648 → 2,147,483,647 |
| Typical Unsigned Range | 0 → 4,294,967,295 |
| Stores | Whole Numbers |
| Format Specifier | `%d` |
| Common Uses | Arithmetic, Counters, Scores, Ages, Loop Variables |

---

## 🚀 Mastery Checklist

- [ ] I know what `int` is.
- [ ] I understand that `int` stores whole numbers.
- [ ] I know its typical memory size.
- [ ] I understand integer division.
- [ ] I know why `int` is the default integer type in C.

---

# long

> "A `long` stores larger integer values than a typical `int`."

🟢 Beginner

⏱ Estimated Study Time: ~30 Minutes

---

## Introduction

So far, we have studied:

```
char

↓

1 Byte
```

```
short

↓

Typically 2 Bytes
```

```
int

↓

Typically 4 Bytes
```

Now we move to:

```c
long
```

A `long` is another integer type,

designed to store **larger whole numbers**.

---

## What is long?

The keyword:

```c
long
```

is an abbreviation for:

```c
long int
```

These are identical.

```c
long number;

long int number;
```

Most programmers simply write:

```c
long
```

---

## Memory Size

Unlike `char`,

the C standard does **not** define an exact size for `long`.

It only guarantees:

```text
sizeof(long)

>=

sizeof(int)
```

Typical sizes:

| System | Typical Size |
|---------|--------------|
| 32-bit | 4 Bytes |
| 64-bit Linux/macOS | 8 Bytes |
| 64-bit Windows | 4 Bytes |

Always verify with:

```c
sizeof(long)
```

---

## Typical Range

When `long` occupies 8 bytes,

its typical signed range is:

```
-9,223,372,036,854,775,808

↓

9,223,372,036,854,775,807
```

Unsigned:

```
0

↓

18,446,744,073,709,551,615
```

If `long` is 4 bytes,

its range is similar to a typical `int`.

---

## Declaring a long

Examples:

```c
long distance = 5000000;

long population = 38000000;

long balance = 1000000000;
```

---

## Printing a long

Use:

```c
%ld
```

Example:

```c
long population = 38000000;

printf("%ld\n", population);
```

Output:

```
38000000
```

---

## Why Does long Exist?

Imagine storing:

```
World Population

↓

8,000,000,000
```

A typical signed 32-bit `int` cannot represent this value.

Using `long` (when it is 64-bit) solves this problem.

---

## Real-World Examples

Population

```c
long population = 38000000;
```

Distance

```c
long distance = 384400000;
```

Large Counter

```c
long files_processed = 5000000000;
```

Timestamp

```c
long timestamp = 1783894000;
```

---

## long vs int

Comparison:

```
int

↓

Usually 4 Bytes

↓

Smaller Range
```

```
long

↓

4 or 8 Bytes

↓

Larger or Equal Range
```

Remember:

The exact size depends on your platform.

---

## Integer Overflow

Suppose:

```c
long number = 9223372036854775807;
```

Now:

```c
number++;
```

The value exceeds the maximum representable range.

Result:

```
Overflow
```

For signed integers,

this is undefined behavior in C.

---

## Mental Model

Imagine containers.

```
Cup

↓

char
```

```
Bucket

↓

short
```

```
Barrel

↓

int
```

```
Storage Tank

↓

long
```

The storage tank holds much more than the barrel.

---

## 📚 Summary

`long` is an integer type used to store larger whole numbers.

Its size depends on the system,

but it is guaranteed to be at least as large as an `int`.

Whenever your program must safely store larger integer values,

`long` is an appropriate choice.

---

## 🧠 Key Concepts

- long
- long int
- Integer
- Range
- Overflow

---

## ⚠ Common Mistakes

- Assuming `long` is always 8 bytes.
- Assuming `long` is always larger than `int`.
- Using `%d` instead of `%ld`.
- Ignoring platform differences.

---

## 💡 Coach Tips

✔ Never assume the size of `long`.

✔ Verify sizes using:

```c
sizeof(long)
```

✔ Use `long` only when larger integer ranges are actually needed.

✔ Remember that different operating systems may represent `long` differently.

---

## 🧩 Think Like the Computer

Suppose:

```c
long distance = 384400000;
```

Ask yourself:

- Why might `int` not always be the best choice?
- What format specifier should be used?
- How many bytes does `long` occupy on your system?

---

## 🏋️ Practice Exercises

1. Declare `long` variables for:

- Population
- Distance
- Timestamp
- National Debt

---

2. Which format specifier prints a `long`?

---

3. Explain why:

```c
sizeof(long)
```

is better than memorizing its size.

---

4. Compare:

```
short

int

long
```

Which one has the largest typical range?

---

## 🎯 42 Piscine Notes

- ✅ `long` stores larger integer values.
- ✅ Don't assume its size—check with `sizeof()`.
- ✅ Use `%ld` with `printf()`.
- ✅ Most Piscine exercises primarily use `int`, but understanding `long` is important.

---

## 📊 Data Type Summary

| Property | `long` |
|----------|--------|
| Category | Integer |
| Typical Size | 4 or 8 Bytes |
| Typical Signed Range | Platform Dependent |
| Typical Unsigned Range | Platform Dependent |
| Stores | Large Whole Numbers |
| Format Specifier | `%ld` |
| Common Uses | Population, Distance, Timestamps, Large Counters |

---

## 🚀 Mastery Checklist

- [ ] I know what `long` is.
- [ ] I understand that its size depends on the platform.
- [ ] I know when to use `long` instead of `int`.
- [ ] I know the correct format specifier.
- [ ] I understand why `sizeof(long)` is more reliable than memorizing its size.

---

# long long

> "A `long long` stores the largest standard integer values available in the C language."

🟢 Beginner

⏱ Estimated Study Time: ~25 Minutes

---

## Introduction

Sometimes,

even a `long` is not large enough.

For applications that require extremely large integer values,

C provides:

```c
long long
```

It is the largest standard signed integer type available in the C language.

---

## What is long long?

The keyword:

```c
long long
```

is an abbreviation for:

```c
long long int
```

These declarations are identical.

```c
long long distance;

long long int distance;
```

Most programmers simply write:

```c
long long
```

---

## Memory Size

The C standard guarantees:

```
sizeof(long long)

>=

sizeof(long)
```

On almost every modern compiler,

a `long long` occupies:

```
8 Bytes

=

64 Bits
```

Always verify with:

```c
sizeof(long long)
```

---

## Typical Range

Signed:

```
-9,223,372,036,854,775,808

↓

9,223,372,036,854,775,807
```

Unsigned:

```
0

↓

18,446,744,073,709,551,615
```

These are the largest standard integer ranges available in C.

---

## Declaring a long long

Examples:

```c
long long population = 8000000000LL;

long long stars = 1000000000000LL;

long long bytes = 9876543210123LL;
```

Notice the suffix:

```c
LL
```

It tells the compiler that the literal is a `long long`.

---

## Printing a long long

Use:

```c
%lld
```

Example:

```c
long long population = 8000000000LL;

printf("%lld\n", population);
```

Output:

```
8000000000
```

---

## Why Does long long Exist?

Imagine storing:

```
World Population

↓

8,000,000,000
```

A typical signed 32-bit `int` cannot hold this value.

A `long long` easily can.

Another example:

```
Nanoseconds

↓

1,000,000,000,000
```

Again,

`long long` is appropriate.

---

## Real-World Examples

Large File Size

```c
long long bytes;
```

Database ID

```c
long long user_id;
```

Nanoseconds

```c
long long time_ns;
```

Astronomical Distances

```c
long long distance;
```

---

## long vs long long

```
long

↓

Usually

4 or 8 Bytes
```

```
long long

↓

Usually

8 Bytes
```

Remember:

Only the minimum relationships are guaranteed by the C standard.

---

## Integer Literals

Large integer literals may require the suffix:

```c
LL
```

Example:

```c
9000000000LL
```

Unsigned version:

```c
9000000000ULL
```

Using the correct suffix helps the compiler interpret the literal correctly.

---

## Overflow

Even `long long` has limits.

Suppose:

```c
long long x = 9223372036854775807LL;
```

Now:

```c
x++;
```

The value exceeds the maximum representable signed value.

Result:

```
Signed Integer Overflow

↓

Undefined Behavior
```

---

## Mental Model

Imagine containers.

```
Cup

↓

char
```

```
Bucket

↓

short
```

```
Barrel

↓

int
```

```
Storage Tank

↓

long
```

```
Shipping Container

↓

long long
```

Each step increases the amount of data that can be stored.

---

## 📚 Summary

`long long` is the largest standard integer type in C.

It typically occupies 8 bytes and is used for very large integer values.

When normal integer types are insufficient,

`long long` provides a much larger range.

---

## 🧠 Key Concepts

- long long
- 64-bit Integer
- Large Numbers
- Integer Literals
- `%lld`

---

## ⚠ Common Mistakes

- Assuming every large integer fits inside an `int`.
- Forgetting the `LL` suffix for large literals.
- Using `%d` instead of `%lld`.
- Assuming `long` and `long long` are always the same size.

---

## 💡 Coach Tips

✔ Use `long long` only when the required range exceeds `int` or `long`.

✔ Use:

```c
%lld
```

for printing.

✔ Verify the size using:

```c
sizeof(long long)
```

✔ Bigger data types are not always better.

Choose the smallest type that safely stores your data.

---

## 🧩 Think Like the Computer

Suppose:

```c
long long stars = 1000000000000LL;
```

Ask yourself:

- Why can't an `int` store this value?
- Why is the `LL` suffix used?
- Which format specifier prints this variable?

---

## 🏋️ Practice Exercises

1. Declare `long long` variables for:

- World Population
- Number of Nanoseconds
- Distance Between Stars
- File Size

---

2. Which format specifier prints a `long long`?

---

3. Why is:

```c
5000000000
```

often unsafe as an `int` literal?

---

4. Compare:

```
int

long

long long
```

Which one provides the largest typical range?

---

## 🎯 42 Piscine Notes

- ✅ `long long` is available in modern C (C99 and later).
- ✅ Use `%lld` with `printf()`.
- ✅ Use the `LL` suffix for large integer literals when appropriate.
- ✅ Don't choose `long long` unless your data actually requires it.

---

## 📊 Data Type Summary

| Property | `long long` |
|----------|-------------|
| Category | Integer |
| Typical Size | 8 Bytes |
| Typical Signed Range | -9.22×10¹⁸ → 9.22×10¹⁸ |
| Typical Unsigned Range | 0 → 1.84×10¹⁹ |
| Stores | Very Large Whole Numbers |
| Format Specifier | `%lld` |
| Common Uses | File Sizes, IDs, Timestamps, Scientific Calculations |

---

## 🚀 Mastery Checklist

- [ ] I know what `long long` is.
- [ ] I know its typical size.
- [ ] I know when to use it.
- [ ] I know the correct format specifier.
- [ ] I understand why larger integer types exist.

---

# signed & unsigned

> "`signed` and `unsigned` determine whether an integer type can store negative values."

🟡 Intermediate

⏱ Estimated Study Time: ~1 Hour

---

# Introduction

So far, we've learned several integer types.

```
char

short

int

long

long long
```

But there is another concept that affects all of them.

It is called:

```
signed

unsigned
```

These keywords do **not** create new data types.

Instead,

they modify how integer values are interpreted.

---

# What Does signed Mean?

A signed integer can store:

- Negative numbers
- Zero
- Positive numbers

Example:

```c
signed int temperature = -15;
```

Possible values:

```
-3

-2

-1

0

1

2

3
```

A signed type uses one bit to represent the sign of the number.

---

# What Does unsigned Mean?

An unsigned integer stores:

- Zero
- Positive numbers only

Example:

```c
unsigned int age = 25;
```

Possible values:

```
0

1

2

3

...

100
```

Negative numbers are **not allowed**.

---

# Why Does unsigned Exist?

Imagine you need to store:

```
Number of Students
```

Can the number of students ever be:

```
-25 ?
```

Of course not.

So allowing negative numbers wastes part of the available range.

Using:

```c
unsigned int
```

gives the entire range to positive values.

---

# Memory Does Not Change

Suppose:

```c
int
```

occupies:

```
4 Bytes
```

Now:

```c
unsigned int
```

still occupies:

```
4 Bytes
```

Nothing changes in memory size.

Only the interpretation of the bits changes.

---

# Example

Signed:

```
32 Bits

↓

Positive

+

Negative
```

Unsigned:

```
32 Bits

↓

Positive Only
```

Because negative numbers are removed,

the maximum positive value becomes much larger.

---

# Typical Ranges

| Type | Typical Signed Range | Typical Unsigned Range |
|------|----------------------|-------------------------|
| char | -128 → 127 | 0 → 255 |
| short | -32,768 → 32,767 | 0 → 65,535 |
| int | -2,147,483,648 → 2,147,483,647 | 0 → 4,294,967,295 |
| long long | -9.22×10¹⁸ → 9.22×10¹⁸ | 0 → 1.84×10¹⁹ |

---

# Declaring signed Variables

Examples:

```c
signed int temperature = -20;

signed short score = -50;

signed char value = -10;
```

---

# Declaring unsigned Variables

Examples:

```c
unsigned int age = 25;

unsigned short players = 16;

unsigned char level = 255;
```

---

# What Happens If You Store a Negative Number?

Example:

```c
unsigned int age = -5;
```

This compiles,

but the result is **not** what beginners expect.

The negative value is converted according to the rules of unsigned arithmetic,

producing a very large positive number.

This is almost always a bug.

---

# Overflow Example

Suppose:

```c
unsigned char x = 255;
```

Now:

```c
x++;
```

Result:

```
0
```

Unlike signed integers,

overflow for unsigned integers is **well-defined** in C.

It wraps around modulo the maximum value plus one.

---

# signed vs unsigned

```
signed

↓

Negative

↓

Zero

↓

Positive
```

```
unsigned

↓

Zero

↓

Positive Only
```

Same memory.

Different interpretation.

---

# Real-World Examples

Temperature

```c
signed int temperature;
```

Population

```c
unsigned long population;
```

Age

```c
unsigned int age;
```

Bank Account Balance (if debt isn't allowed)

```c
unsigned long long balance;
```

---

# Mental Model

Imagine a road.

Signed road:

```
← Negative

0

Positive →
```

Unsigned road:

```
0

Positive →
```

The road no longer extends into negative numbers.

Instead,

all available space is used for positive values.

---

## 📚 Summary

`signed` allows both positive and negative values.

`unsigned` allows only zero and positive values.

Neither keyword changes the amount of memory used.

They only change how the stored bits are interpreted.

Choosing the correct modifier depends on the meaning of the data.

---

## 🧠 Key Concepts

- signed
- unsigned
- Integer Modifier
- Range
- Overflow

---

## ⚠ Common Mistakes

- Thinking `unsigned` uses more memory.
- Assuming `unsigned` prevents overflow.
- Assigning negative values to unsigned variables.
- Forgetting that unsigned arithmetic behaves differently.

---

## 💡 Coach Tips

✔ Use `signed` when negative values are meaningful.

✔ Use `unsigned` only when negative values are impossible.

✔ Don't choose `unsigned` just because it has a larger maximum value.

✔ Understand the meaning of your data before choosing the type.

---

## 🧩 Think Like the Computer

Which is more appropriate?

```c
Temperature
```

```
signed

or

unsigned ?
```

---

```c
Age
```

```
signed

or

unsigned ?
```

---

```c
Player Score
```

```
signed

or

unsigned ?
```

Explain your choices.

---

## 🏋️ Practice Exercises

1. Declare variables for:

- Temperature
- Age
- Population
- Number of Files

Choose `signed` or `unsigned` appropriately.

---

2. Explain why this is dangerous.

```c
unsigned int x = -10;
```

---

3. Compare:

```
signed int

unsigned int
```

What changes?

What stays the same?

---

4. Why does `unsigned` provide a larger positive range?

---

## 🎯 42 Piscine Notes

- ✅ `signed` and `unsigned` modify integer types.
- ✅ They do **not** change memory size.
- ✅ They change the range of representable values.
- ✅ Avoid using `unsigned` unless it truly matches the problem.

---

## 📊 Modifier Summary

| Property | `signed` | `unsigned` |
|----------|----------|------------|
| Negative Values | ✅ Yes | ❌ No |
| Positive Values | ✅ Yes | ✅ Yes |
| Zero | ✅ Yes | ✅ Yes |
| Memory Size | Same | Same |
| Typical Use | Temperatures, Offsets | Sizes, Counts, Ages |

---

## 🚀 Mastery Checklist

- [ ] I know what `signed` means.
- [ ] I know what `unsigned` means.
- [ ] I understand that they modify integer types.
- [ ] I know that they do not change memory size.
- [ ] I know when to choose `signed` or `unsigned`.

---

# 📊 Integer Types Comparison

> "Choosing the correct integer type is about selecting the right balance between memory usage and the range of values."

🟢 Beginner

⏱ Estimated Study Time: ~20 Minutes

---

# Introduction

The C language provides several integer data types.

Although they all store whole numbers,

they differ in:

- Memory size
- Range of values
- Typical use cases

Choosing the appropriate type improves both program correctness and efficiency.

---

# Integer Family

```
char

↓

short

↓

int

↓

long

↓

long long
```

Each step generally provides a larger range of values.

---

# Typical Sizes

| Data Type | Typical Size |
|-----------|-------------:|
| `char` | 1 Byte |
| `short` | 2 Bytes |
| `int` | 4 Bytes |
| `long` | 4 or 8 Bytes |
| `long long` | 8 Bytes |

> Always remember:
>
> The C standard does **not** guarantee these exact sizes (except that `char` is always 1 byte).
>
> Use:
>
> ```c
> sizeof(type)
> ```
>
> to determine the actual size on your system.

---

# Typical Signed Ranges

| Type | Typical Range |
|------|---------------|
| `char` | -128 → 127 |
| `short` | -32,768 → 32,767 |
| `int` | -2,147,483,648 → 2,147,483,647 |
| `long` | Platform Dependent |
| `long long` | ±9.22 × 10¹⁸ |

---

# Typical Unsigned Ranges

| Type | Typical Range |
|------|---------------|
| `unsigned char` | 0 → 255 |
| `unsigned short` | 0 → 65,535 |
| `unsigned int` | 0 → 4,294,967,295 |
| `unsigned long` | Platform Dependent |
| `unsigned long long` | 0 → 1.84 × 10¹⁹ |

---

# printf() Format Specifiers

| Type | Format Specifier |
|------|------------------|
| `char` | `%c` (character), `%d` (numeric value) |
| `short` | `%hd` |
| `int` | `%d` |
| `long` | `%ld` |
| `long long` | `%lld` |

---

# scanf() Format Specifiers

| Type | Format Specifier |
|------|------------------|
| `char` | `%c` |
| `short` | `%hd` |
| `int` | `%d` |
| `long` | `%ld` |
| `long long` | `%lld` |

---

# When Should I Use Each Type?

### char

Use for:

- Letters
- Digits
- Symbols
- Individual characters

Example:

```c
char grade = 'A';
```

---

### short

Use for:

- Small integer values
- Memory-sensitive applications

Example:

```c
short year = 2026;
```

---

### int

The default choice.

Use for:

- Arithmetic
- Loop counters
- Scores
- Ages
- Most whole numbers

Example:

```c
int score = 100;
```

---

### long

Use when integers may exceed the range of a typical `int`.

Example:

```c
long population;
```

---

### long long

Use for extremely large integer values.

Example:

```c
long long file_size;
```

---

# signed vs unsigned

| signed | unsigned |
|---------|-----------|
| Negative ✔ | Negative ✘ |
| Positive ✔ | Positive ✔ |
| Zero ✔ | Zero ✔ |
| Same Memory | Same Memory |

Use `unsigned` only when negative values are impossible.

---

# Visual Comparison

```
char

↓

Very Small Numbers

↓

1 Byte
```

```
short

↓

Small Numbers

↓

2 Bytes
```

```
int

↓

General Purpose

↓

Typically 4 Bytes
```

```
long

↓

Large Numbers

↓

4 or 8 Bytes
```

```
long long

↓

Very Large Numbers

↓

Typically 8 Bytes
```

---

# Which Type Should I Choose?

Ask yourself these questions.

### Is it a character?

↓

Use

```c
char
```

---

### Is it a normal whole number?

↓

Use

```c
int
```

---

### Is the value extremely large?

↓

Use

```c
long

or

long long
```

---

### Can it never be negative?

↓

Consider

```c
unsigned
```

---

# Common Beginner Mistakes

❌ Using `long long` for every variable.

❌ Assuming larger types are always better.

❌ Forgetting the correct `printf()` format specifier.

❌ Assuming all computers use the same type sizes.

❌ Choosing `unsigned` only because it has a larger maximum value.

---

## 📚 Summary

The C language provides several integer data types.

Each one balances:

- Memory usage
- Range
- Performance

Choosing the correct type is an important programming skill.

For most programs,

```c
int
```

is the best default choice.

---

## 🎯 42 Piscine Notes

- ✅ Use `int` unless another type is clearly needed.
- ✅ Learn the format specifiers by heart.
- ✅ Never assume the size of `long`.
- ✅ Use `sizeof()` whenever the exact size matters.
- ✅ Understand the purpose of a type before choosing it.

---

## 🚀 Mastery Checklist

- [ ] I know every integer type.
- [ ] I know the typical size of each type.
- [ ] I know the common format specifiers.
- [ ] I know when to choose each type.
- [ ] I understand the role of `signed` and `unsigned`.

---

# 🎉 End of Integer Types

You have completed the entire Integer Family in C.

Next, we move to a completely different family of data types:

```
Floating-Point Types

↓

float

↓

double
```

These types allow programs to store numbers with decimal fractions, opening the door to scientific calculations, measurements, graphics, and many other applications.

# float

> "A `float` stores real numbers that contain a fractional (decimal) part."

🟢 Beginner

⏱ Estimated Study Time: ~45 Minutes

---

## Introduction

Until now,

every number we stored was an integer.

Examples:

```c
25

100

-15

0
```

These are called:

```
Whole Numbers
```

But what about numbers like:

```
3.14

19.99

-7.5

0.125
```

These are called:

```
Floating-Point Numbers
```

To store them,

C provides the data type:

```c
float
```

---

# What is float?

A `float` is a data type used to store numbers with a decimal part.

Example:

```c
float price = 19.99;

float pi = 3.14;

float temperature = -7.5;
```

Unlike `int`,

a `float` can represent fractional values.

---

# Why is it Called "Floating-Point"?

Consider these numbers.

```
15.0

1.5

0.15

0.015
```

Notice how the decimal point appears to "move."

In reality,

computers store these values using a scientific notation format where the decimal point effectively "floats."

That is why they are called:

```
Floating-Point Numbers
```

---

# Memory Size

A `float` typically occupies:

```
4 Bytes

=

32 Bits
```

Use:

```c
sizeof(float)
```

to verify the size on your system.

---

# Declaring float Variables

Examples:

```c
float price = 19.99;

float weight = 75.5;

float speed = 120.25;

float pi = 3.14159;
```

---

# Printing a float

Use:

```c
%f
```

Example:

```c
float price = 19.99;

printf("%f\n", price);
```

Output:

```
19.990000
```

---

# Why So Many Zeros?

Many beginners expect:

```
19.99
```

Instead they see:

```
19.990000
```

This is normal.

By default,

`printf()` displays six digits after the decimal point.

---

# Controlling Decimal Places

Two decimal places:

```c
printf("%.2f\n", price);
```

Output:

```
19.99
```

Three decimal places:

```c
printf("%.3f\n", price);
```

Output:

```
19.990
```

One decimal place:

```c
printf("%.1f\n", price);
```

Output:

```
20.0
```

Notice that the displayed value is rounded.

---

# Integer vs Float

Compare:

```c
int x = 7;

int y = 2;

printf("%d\n", x / y);
```

Output:

```
3
```

Now:

```c
float x = 7.0;

float y = 2.0;

printf("%f\n", x / y);
```

Output:

```
3.500000
```

The difference is that floating-point numbers preserve the fractional part.

---

# Precision

Although `float` stores decimal numbers,

it cannot represent every decimal value exactly.

Example:

```c
float x = 0.1;
```

Internally,

the stored value is only an approximation.

This is because decimal fractions are stored in binary.

We'll study this in more detail later.

---

# Common Uses

Store a price.

```c
float price = 29.99;
```

Store temperature.

```c
float temperature = 36.7;
```

Store weight.

```c
float weight = 72.5;
```

Store speed.

```c
float speed = 120.8;
```

---

# Memory Comparison

```
char

↓

1 Byte
```

```
short

↓

2 Bytes
```

```
int

↓

Typically 4 Bytes
```

```
float

↓

Typically 4 Bytes
```

Notice:

`int` and `float` usually occupy the same amount of memory,

but they store completely different kinds of values.

---

# Mental Model

Imagine two notebooks.

Notebook 1:

```
Whole Numbers Only
```

Notebook 2:

```
Whole Numbers

+

Decimals
```

`int` uses the first notebook.

`float` uses the second.

---

## 📚 Summary

A `float` stores real numbers with fractional parts.

It typically occupies four bytes.

Unlike integers,

floating-point numbers preserve decimal values,

making them useful for measurements,

prices,

scientific calculations,

and many real-world applications.

---

## 🧠 Key Concepts

- float
- Floating-Point Number
- Decimal
- Fraction
- Precision
- `%f`

---

## ⚠ Common Mistakes

- Using `%d` instead of `%f`.
- Expecting exact decimal precision.
- Confusing `7` with `7.0`.
- Forgetting that `printf()` prints six decimal places by default.

---

## 💡 Coach Tips

✔ Use `float` only when decimal values are required.

✔ Don't compare floating-point values for exact equality unless you understand precision issues.

✔ Learn the difference between integer division and floating-point division.

✔ Use formatting like:

```c
%.2f
```

to control displayed precision.

---

## 🧩 Think Like the Computer

Predict the output.

```c
float x = 5.5;

printf("%f\n", x);

printf("%.2f\n", x);

printf("%.1f\n", x);
```

Explain why each line prints a different result.

---

## 🏋️ Practice Exercises

1. Declare `float` variables for:

- Price
- Temperature
- Height
- Speed

---

2. Predict the output.

```c
float a = 10.5;

float b = 2.0;

printf("%f\n", a / b);
```

---

3. Explain the difference between:

```c
7 / 2
```

and

```c
7.0 / 2.0
```

---

4. Why does:

```c
printf("%f\n", price);
```

print six decimal places?

---

## 🎯 42 Piscine Notes

- ✅ Use `float` when decimal values are needed.
- ✅ Use `%f` with `printf()`.
- ✅ Control precision with formats like `%.2f`.
- ✅ Remember that floating-point values are approximations.

---

## 📊 Data Type Summary

| Property | `float` |
|----------|---------|
| Category | Floating-Point |
| Typical Size | 4 Bytes |
| Stores | Decimal Numbers |
| Precision | ~6–7 Decimal Digits |
| Format Specifier | `%f` |
| Common Uses | Prices, Temperatures, Measurements, Speeds |

---

## 🚀 Mastery Checklist

- [ ] I know what `float` is.
- [ ] I know when to use `float` instead of `int`.
- [ ] I know the correct format specifier.
- [ ] I understand why `printf()` prints six decimal places.
- [ ] I understand that floating-point numbers are approximations.

---

# double

> "A `double` stores decimal numbers with much higher precision than a `float`."

🟢 Beginner

⏱ Estimated Study Time: ~40 Minutes

---

## Introduction

In the previous section,

we learned about:

```c
float
```

A `float` stores decimal numbers,

but it has limited precision.

Suppose we need to perform:

- Scientific calculations
- Financial calculations
- Engineering simulations
- Physics calculations

Small rounding errors can become important.

For these situations,

C provides:

```c
double
```

---

# What is double?

A `double` is a floating-point data type that stores decimal numbers with higher precision than a `float`.

Example:

```c
double pi = 3.141592653589793;

double price = 19.99;

double gravity = 9.80665;
```

Just like `float`,

`double` stores decimal values.

The difference is **how accurately they are stored**.

---

# Why is it Called "double"?

Historically,

a `double` provided approximately **twice the precision** of a `float`.

Today,

the exact implementation depends on the platform,

but on most modern systems:

```
float

↓

32 Bits
```

```
double

↓

64 Bits
```

---

# Memory Size

A `double` typically occupies:

```
8 Bytes

=

64 Bits
```

Use:

```c
sizeof(double)
```

to verify the size on your system.

---

# Declaring double Variables

Examples:

```c
double pi = 3.141592653589793;

double balance = 12345.67;

double gravity = 9.80665;
```

---

# Printing a double

Use:

```c
%f
```

Example:

```c
double pi = 3.141592653589793;

printf("%f\n", pi);
```

Output:

```
3.141593
```

Notice:

`printf()` uses `%f` for both `float` and `double`.

---

# Showing More Precision

Example:

```c
printf("%.15f\n", pi);
```

Output:

```
3.141592653589793
```

You can choose how many decimal places to display.

---

# float vs double

Suppose:

```c
float pi = 3.141592653589793;

double PI = 3.141592653589793;
```

The `float` loses part of the precision.

The `double` preserves much more of it.

This is why scientific software usually uses `double`.

---

# Precision Comparison

Typical precision:

```
float

↓

About 6–7 Decimal Digits
```

```
double

↓

About 15–16 Decimal Digits
```

Notice:

Precision refers to the number of significant decimal digits,

not the number of digits after the decimal point.

---

# Common Uses

Scientific calculations

```c
double distance;
```

Financial calculations

```c
double balance;
```

Physics

```c
double velocity;
```

Engineering

```c
double voltage;
```

---

# Memory Comparison

```
int

↓

Typically 4 Bytes
```

```
float

↓

Typically 4 Bytes
```

```
double

↓

Typically 8 Bytes
```

A `double` occupies more memory,

but stores values with much greater precision.

---

# Precision Example

Consider:

```c
float a = 1.123456789;

double b = 1.123456789;
```

Printing both values may produce:

```
float

↓

1.123457
```

```
double

↓

1.123456789000000
```

The exact output depends on the implementation,

but `double` generally preserves more digits.

---

# Mental Model

Imagine two rulers.

Small ruler:

```
Measures

↓

Nearest Millimeter
```

Large ruler:

```
Measures

↓

Nearest Micrometer
```

Both measure distance.

One simply measures much more accurately.

---

## 📚 Summary

A `double` stores decimal numbers with higher precision than a `float`.

It typically occupies:

```
8 Bytes
```

It is commonly used when calculations require greater accuracy.

---

## 🧠 Key Concepts

- double
- Floating-Point
- Precision
- Decimal
- `%f`

---

## ⚠ Common Mistakes

- Thinking `double` stores larger numbers only.
- Assuming `double` prints more decimal places automatically.
- Using `float` when higher precision is required.
- Believing floating-point numbers are always exact.

---

## 💡 Coach Tips

✔ Choose `double` when precision matters more than memory usage.

✔ Remember:

Higher precision

≠

Infinite precision.

✔ `double` still stores approximations.

✔ Use formatting such as:

```c
%.10f

%.15f
```

to display additional precision.

---

## 🧩 Think Like the Computer

Predict which variable stores more accurate information.

```c
float a = 3.1415926535;

double b = 3.1415926535;
```

Explain why.

---

## 🏋️ Practice Exercises

1. Declare `double` variables for:

- Pi
- Gravity
- Bank Balance
- Earth Radius

---

2. Compare:

```c
float pi;

double pi;
```

Which one preserves more precision?

---

3. Why does a `double` usually require more memory?

---

4. Which type would you choose?

- Temperature Sensor
- Scientific Calculator
- Bank Balance
- Game Character Health

Explain your choices.

---

## 🎯 42 Piscine Notes

- ✅ Use `double` when precision is important.
- ✅ `printf()` uses `%f` for both `float` and `double`.
- ✅ Don't assume more memory always means a better choice.
- ✅ Understand the trade-off between precision and memory.

---

## 📊 Data Type Summary

| Property | `double` |
|----------|----------|
| Category | Floating-Point |
| Typical Size | 8 Bytes |
| Stores | Decimal Numbers |
| Typical Precision | ~15–16 Decimal Digits |
| Format Specifier | `%f` |
| Common Uses | Scientific Computing, Finance, Engineering, Physics |

---

## 🚀 Mastery Checklist

- [ ] I know what `double` is.
- [ ] I understand the difference between `float` and `double`.
- [ ] I know the typical memory size of `double`.
- [ ] I know when to choose `double`.
- [ ] I understand that `double` still stores approximate values.

---

# sizeof

> "`sizeof` returns the number of bytes occupied by a data type or object."

🟢 Beginner

⏱ Estimated Study Time: ~40 Minutes

---

## Introduction

Earlier in this chapter,

we repeatedly said things like:

```
char

↓

1 Byte
```

```
int

↓

Typically 4 Bytes
```

```
double

↓

Typically 8 Bytes
```

But...

How does the programmer actually know these sizes?

Should we simply memorize them?

The answer is:

```
No.
```

C provides a built-in operator called:

```c
sizeof
```

that tells us the size directly.

---

# What is sizeof?

`sizeof` is a compile-time operator that returns the size, in **bytes**, of a data type or an object.

Example:

```c
sizeof(int)
```

Possible output:

```
4
```

Meaning:

An `int` occupies four bytes on this system.

---

# Basic Syntax

With a type:

```c
sizeof(type)
```

Examples:

```c
sizeof(char)

sizeof(int)

sizeof(float)

sizeof(double)
```

---

With a variable:

```c
int age = 25;

sizeof(age)
```

The result is exactly the same as:

```c
sizeof(int)
```

---

# Using sizeof()

Example:

```c
#include <stdio.h>

int main(void)
{
    printf("%zu\n", sizeof(char));
    printf("%zu\n", sizeof(short));
    printf("%zu\n", sizeof(int));
    printf("%zu\n", sizeof(long));
    printf("%zu\n", sizeof(long long));
    printf("%zu\n", sizeof(float));
    printf("%zu\n", sizeof(double));

    return (0);
}
```

Possible output on a 64-bit Linux system:

```
1

2

4

8

8

4

8
```

Remember:

These values may differ on another system.

---

# Why Use sizeof?

Suppose you write:

```c
char letter;
```

Instead of guessing,

you simply ask:

```c
sizeof(letter)
```

The compiler gives the correct answer.

No memorization required.

---

# sizeof Returns Bytes

Notice:

`sizeof` returns:

```
Bytes
```

Not:

```
Bits
```

Example:

```c
sizeof(int)

↓

4
```

means:

```
4 Bytes

=

32 Bits
```

---

# sizeof and Variables

Example:

```c
double price = 19.99;

printf("%zu\n", sizeof(price));
```

Output:

```
8
```

The operator examines the variable's type,

not its value.

---

# sizeof and Arrays

Suppose:

```c
int numbers[10];
```

Then:

```c
sizeof(numbers)
```

returns:

```
40
```

Why?

Because:

```
10 Integers

×

4 Bytes

=

40 Bytes
```

We'll study arrays in detail later.

---

# Why Use %zu?

The value returned by `sizeof` has the type:

```c
size_t
```

The correct format specifier is:

```c
%zu
```

Example:

```c
printf("%zu\n", sizeof(int));
```

Using `%zu` is the portable and recommended approach.

---

# sizeof Never Modifies Data

Example:

```c
int x = 50;

sizeof(x);
```

After executing,

```
x
```

is still:

```
50
```

`sizeof` only reports information.

It never changes memory.

---

# Real-World Uses

Dynamic Memory

```c
malloc(10 * sizeof(int));
```

Arrays

```c
sizeof(array)
```

Structures

```c
sizeof(struct Student)
```

Buffer Sizes

```c
char buffer[256];

sizeof(buffer)
```

You'll encounter `sizeof` frequently throughout the Piscine.

---

# Mental Model

Imagine asking:

```
How big is this box?
```

Instead of measuring it yourself,

someone instantly tells you:

```
4 Liters
```

`sizeof` works the same way.

It tells you how much memory something occupies.

---

## 📚 Summary

`sizeof` returns the size of a type or object in bytes.

It is a compile-time operator used to determine memory requirements.

Using `sizeof` makes programs more portable because sizes can vary between systems.

---

## 🧠 Key Concepts

- sizeof
- Bytes
- size_t
- Memory
- Portability

---

## ⚠ Common Mistakes

- Thinking `sizeof` returns bits.
- Using `%d` instead of `%zu`.
- Assuming every `int` occupies exactly four bytes.
- Memorizing sizes instead of checking them.

---

## 💡 Coach Tips

✔ Prefer:

```c
sizeof(type)
```

instead of hardcoding sizes.

✔ Always print `sizeof` using:

```c
%zu
```

✔ Remember:

Portable programs ask the compiler,

not the programmer.

✔ You'll use `sizeof` constantly with `malloc()` later.

---

## 🧩 Think Like the Computer

Predict the output.

```c
printf("%zu\n", sizeof(char));

printf("%zu\n", sizeof(double));
```

Now answer:

Why does:

```c
sizeof(numbers)
```

depend on the number of elements?

---

## 🏋️ Practice Exercises

1. Write a program that prints the size of:

- `char`
- `short`
- `int`
- `long`
- `long long`
- `float`
- `double`

---

2. What is the difference between:

```c
sizeof(int)
```

and

```c
sizeof(age)
```

---

3. If:

```c
int values[25];
```

and an `int` occupies 4 bytes,

what should:

```c
sizeof(values)
```

return?

Explain your reasoning.

---

4. Why is `sizeof` important when writing portable programs?

---

## 🎯 42 Piscine Notes

- ✅ Always prefer `sizeof(type)` over hardcoded numbers.
- ✅ Print `sizeof` using `%zu`.
- ✅ Don't assume data type sizes.
- ✅ `sizeof` becomes essential when using `malloc()` and arrays.

---

## 📊 sizeof Summary

| Expression | Meaning |
|------------|---------|
| `sizeof(char)` | Size of `char` |
| `sizeof(int)` | Size of `int` |
| `sizeof(variable)` | Size of the variable's type |
| `sizeof(array)` | Total size of the entire array |
| Return Type | `size_t` |
| Format Specifier | `%zu` |

---

## 🚀 Mastery Checklist

- [ ] I know what `sizeof` does.
- [ ] I know that it returns bytes.
- [ ] I know why `%zu` is used.
- [ ] I understand why `sizeof` improves portability.
- [ ] I know that `sizeof` does not modify variables.

---

# Type Conversion

> "Type conversion is the process of changing a value from one data type to another."

🟡 Intermediate

⏱ Estimated Study Time: ~1 Hour

---

# Introduction

Until now,

we've learned several data types.

```c
char

short

int

long

float

double
```

But what happens when different types are used together?

Example:

```c
int x = 7;

float y = 2.0;

printf("%f\n", x / y);
```

How can an `int` be divided by a `float`?

The answer is:

```
Type Conversion
```

The compiler converts one type into another so the operation can be performed correctly.

---

# What is Type Conversion?

Type conversion means changing a value from one data type into another.

Example:

```
Integer

↓

Floating Point
```

or

```
Character

↓

Integer
```

This happens constantly inside C programs.

Sometimes,

the compiler performs it automatically.

Sometimes,

the programmer must request it explicitly.

---

# Two Types of Conversion

There are two kinds.

```
Automatic

↓

Implicit Conversion
```

```
Manual

↓

Explicit Conversion

(Casting)
```

We'll study both.

---

# Implicit Conversion

Implicit conversion happens automatically.

The programmer does nothing.

Example:

```c
int x = 10;

float y = x;
```

What happens?

The compiler automatically converts:

```
10

↓

10.0
```

before storing it in `y`.

---

# Another Example

```c
char letter = 'A';

int number = letter;
```

Internally:

```
'A'

↓

65
```

The compiler performs the conversion automatically.

---

# Integer Promotion

Small integer types are often promoted automatically.

Example:

```c
char a = 5;

char b = 10;

char c = a + b;
```

The addition is **not** performed using `char`.

Instead,

both operands are first promoted to:

```c
int
```

Then the addition is performed.

This process is called:

```
Integer Promotion
```

It helps the CPU perform arithmetic efficiently.

---

# Explicit Conversion (Casting)

Sometimes,

automatic conversion is not enough.

The programmer must request it manually.

This is called:

```
Casting
```

Syntax:

```c
(type)value
```

Example:

```c
float result = (float)7;
```

The integer:

```
7
```

is converted into:

```
7.0
```

before being stored.

---

# Why Casting Matters

Consider:

```c
int x = 7;

int y = 2;

printf("%d\n", x / y);
```

Output:

```
3
```

Because both operands are integers.

Now:

```c
printf("%f\n", (float)x / y);
```

Output:

```
3.500000
```

The cast changes the entire calculation.

---

# Another Example

Without casting:

```c
5 / 2

↓

2
```

With casting:

```c
(float)5 / 2

↓

2.5
```

A single cast completely changes the result.

---

# Losing Information

Conversions are not always safe.

Example:

```c
float price = 19.99;

int x = price;
```

Result:

```
19
```

The decimal part is discarded.

It is **not rounded**.

---

Another example:

```c
double pi = 3.1415926535;

float x = pi;
```

Some precision is lost because a `float` stores fewer significant digits than a `double`.

---

# Character Conversion

Characters are simply numbers.

Example:

```c
char letter = 'A';

int x = letter;
```

Result:

```
65
```

Reverse:

```c
int number = 66;

char c = number;
```

Result:

```
'B'
```

The stored bits are interpreted differently depending on the data type.

---

# Real-World Example

Average Score.

Incorrect:

```c
int total = 15;

int students = 4;

float average = total / students;
```

Result:

```
3.0
```

Correct:

```c
float average = (float)total / students;
```

Result:

```
3.75
```

The cast prevents integer division.

---

# Mental Model

Imagine two measuring cups.

Cup A:

```
Whole Liters Only
```

Cup B:

```
Whole Liters

+

Milliliters
```

Pouring water from Cup A to Cup B adds precision.

Pouring from Cup B to Cup A loses the fractional part.

Type conversion works in a similar way.

---

## 📚 Summary

Type conversion changes a value from one data type to another.

Conversions may happen automatically (implicit conversion) or manually (explicit conversion using casting).

Understanding type conversion is essential for writing correct arithmetic expressions and avoiding unexpected results.

---

## 🧠 Key Concepts

- Type Conversion
- Implicit Conversion
- Explicit Conversion
- Casting
- Integer Promotion
- Precision Loss

---

## ⚠ Common Mistakes

- Forgetting that integer division removes the fractional part.
- Believing casting changes the original variable.
- Assuming all conversions preserve information.
- Confusing assignment with type conversion.

---

## 💡 Coach Tips

✔ When you need decimal division,

cast **before** the division.

Correct:

```c
(float)a / b
```

Not:

```c
(float)(a / b)
```

because by then the integer division has already happened.

✔ Remember that converting from a larger type to a smaller one may lose information.

✔ Casting creates a converted value.

It does **not** change the original variable.

---

## 🧩 Think Like the Computer

Predict the output.

```c
int a = 7;

int b = 2;

printf("%f\n", (float)a / b);
```

Now predict:

```c
printf("%f\n", (float)(a / b));
```

Why are the results different?

---

## 🏋️ Practice Exercises

1. Predict the output.

```c
int x = 10;

float y = x;

printf("%f\n", y);
```

---

2. Explain why this prints `2` instead of `2.5`.

```c
printf("%d\n", 5 / 2);
```

---

3. Rewrite the expression to produce `2.5`.

---

4. What value is stored?

```c
float price = 9.99;

int x = price;
```

Explain why.

---

## 🎯 42 Piscine Notes

- ✅ Integer division is one of the most common beginner mistakes.
- ✅ Cast before arithmetic when decimal precision is required.
- ✅ Understand implicit conversions before relying on them.
- ✅ Casting does not modify the original variable.

---

## 📊 Type Conversion Summary

| Conversion | Automatic? | Information Loss? |
|------------|------------|-------------------|
| `int → float` | ✅ Usually | ❌ |
| `float → int` | ❌ (assignment converts) | ✅ Decimal part discarded |
| `char → int` | ✅ | ❌ |
| `double → float` | ❌ (assignment converts) | ✅ Possible precision loss |
| `(float)a / b` | Manual Cast | ❌ Enables floating-point division |

---

## 🚀 Mastery Checklist

- [ ] I know what type conversion is.
- [ ] I understand implicit conversion.
- [ ] I understand explicit conversion (casting).
- [ ] I know why `7 / 2` equals `3`.
- [ ] I know why `(float)7 / 2` equals `3.5`.
- [ ] I understand that some conversions lose information.

---

# Overflow

> "Overflow occurs when a value exceeds the range that its data type can represent."

🟡 Intermediate

⏱ Estimated Study Time: ~50 Minutes

---

# Introduction

Every data type has a limited range.

For example,

a typical signed `int` can store approximately:

```
-2,147,483,648

↓

2,147,483,647
```

But what happens if we try to store:

```
3,000,000,000
```

The answer is:

```
Overflow
```

The value no longer fits inside the available memory.

---

# What is Overflow?

Overflow occurs when the result of a calculation is larger than the maximum value (or smaller than the minimum value) that a data type can represent.

Example:

```c
int number = 2147483647;

number = number + 1;
```

The result cannot be represented by a typical signed 32-bit `int`.

---

# Why Does Overflow Happen?

Memory is limited.

Suppose an integer occupies:

```
4 Bytes

=

32 Bits
```

With only 32 bits,

there is a maximum and minimum value that can be represented.

Once that limit is exceeded,

overflow occurs.

---

# Signed Overflow

Example:

```c
int x = 2147483647;

x++;
```

What happens?

Many beginners expect:

```
2147483648
```

But a signed `int` cannot represent this value.

According to the C standard,

this causes:

```
Undefined Behavior
```

The compiler is free to produce any result.

Some systems may appear to "wrap around,"

others may not.

**Never rely on signed overflow.**

---

# Unsigned Overflow

Now consider:

```c
unsigned int x = 4294967295U;

x++;
```

Result:

```
0
```

Unlike signed integers,

unsigned integers always wrap around.

This behavior is defined by the C standard.

---

# Underflow

Overflow happens when the value becomes too large.

The opposite also exists.

Example:

```c
int x = -2147483648;

x--;
```

The result becomes smaller than the minimum representable value.

This is also a form of overflow (often informally called **underflow** for integers).

For signed integers,

this is also undefined behavior.

---

# Overflow During Assignment

Suppose:

```c
char x = 300;
```

Can a `char` store:

```
300 ?
```

No.

The value does not fit inside one byte.

The compiler may produce a warning,

and the stored value will not be what the programmer expected.

Always pay attention to compiler warnings.

---

# Overflow in Arithmetic

Overflow doesn't only happen during assignment.

Example:

```c
int a = 2000000000;

int b = 2000000000;

int c = a + b;
```

Although both variables are valid,

their sum exceeds the range of `int`.

Result:

```
Overflow
```

---

# Floating-Point Overflow

Floating-point numbers can also overflow.

Example:

```c
float x = 3.4e38f;

x = x * 100.0f;
```

The result is too large to be represented by a `float`.

Depending on the implementation,

the result is often:

```
inf
```

meaning:

```
Infinity
```

---

# Detecting Overflow

The safest solution is:

Never allow calculations to exceed the range of the data type.

For critical programs,

check values before performing arithmetic.

Example:

```c
if (a > INT_MAX - b)
{
    /* Overflow would occur */
}
```

The constants like `INT_MAX` are defined in:

```c
#include <limits.h>
```

---

# Real-World Example

Suppose a game stores health using:

```c
unsigned char health = 255;
```

Now:

```c
health++;
```

Health becomes:

```
0
```

instead of:

```
256
```

A serious bug.

---

# Mental Model

Imagine a measuring cup that holds exactly:

```
1 Liter
```

You pour:

```
2 Liters
```

The extra water spills.

The container cannot hold more than its capacity.

Overflow works exactly the same way.

---

## 📚 Summary

Overflow occurs when a value exceeds the limits of its data type.

Signed integer overflow is undefined behavior.

Unsigned integer overflow wraps around according to the C standard.

Understanding overflow is essential for writing safe and reliable C programs.

---

## 🧠 Key Concepts

- Overflow
- Integer Limits
- Undefined Behavior
- Wrap Around
- Range

---

## ⚠ Common Mistakes

- Assuming larger numbers always fit.
- Relying on signed integer overflow.
- Ignoring compiler warnings.
- Forgetting that arithmetic can overflow even if individual variables are valid.

---

## 💡 Coach Tips

✔ Every data type has limits.

✔ Learn to think about the maximum possible value before performing calculations.

✔ Use `limits.h` when checking integer limits.

✔ Never rely on signed overflow.

---

## 🧩 Think Like the Computer

Predict the result.

```c
unsigned char x = 255;

x++;
```

Now predict:

```c
int x = 2147483647;

x++;
```

Why are these two cases different?

---

## 🏋️ Practice Exercises

1. Explain why this code is dangerous.

```c
int x = 2147483647;

x++;
```

---

2. Why does this produce `0`?

```c
unsigned char x = 255;

x++;
```

---

3. Which header provides:

```c
INT_MAX
```

and

```c
INT_MIN
```

---

4. Explain the difference between signed and unsigned overflow.

---

## 🎯 42 Piscine Notes

- ✅ Never rely on signed overflow.
- ✅ Unsigned overflow wraps around.
- ✅ Pay attention to compiler warnings.
- ✅ Use `limits.h` when checking integer limits.

---

## 📊 Overflow Summary

| Situation | Result |
|-----------|--------|
| Signed Integer Overflow | Undefined Behavior |
| Unsigned Integer Overflow | Wrap Around |
| Assignment Too Large | Truncation / Implementation-Defined Result (often with a warning) |
| Floating-Point Overflow | Often `inf` |

---

## 🚀 Mastery Checklist

- [ ] I know what overflow is.
- [ ] I know why overflow happens.
- [ ] I understand the difference between signed and unsigned overflow.
- [ ] I know why signed overflow is dangerous.
- [ ] I know how to reduce the risk of overflow.

---

# 📊 Floating-Point Types Comparison

> "Floating-point types store real numbers with fractional parts. Choosing between `float` and `double` depends on the balance between memory usage and precision."

🟢 Beginner

⏱ Estimated Study Time: ~15 Minutes

---

# Introduction

The C language provides two primary floating-point data types.

```
float

↓

double
```

Both store decimal numbers,

but they differ in:

- Memory size
- Precision
- Typical use cases

---

# Floating-Point Family

```
float

↓

double
```

Unlike integer types,

their purpose is to represent numbers with fractional (decimal) parts.

---

# Typical Sizes

| Data Type | Typical Size |
|-----------|-------------:|
| `float` | 4 Bytes |
| `double` | 8 Bytes |

> The C standard guarantees that:
>
> ```text
> sizeof(float)
> <=
> sizeof(double)
> ```
>
> Use:
>
> ```c
> sizeof(float)
> sizeof(double)
> ```
>
> to determine the exact sizes on your system.

---

# Typical Precision

| Type | Typical Precision |
|------|-------------------|
| `float` | About 6–7 significant decimal digits |
| `double` | About 15–16 significant decimal digits |

Remember:

Precision refers to **significant digits**,

not simply the number of digits after the decimal point.

---

# Typical Range

| Type | Approximate Range |
|------|--------------------|
| `float` | ±3.4 × 10³⁸ |
| `double` | ±1.7 × 10³⁰⁸ |

Notice:

`double` can represent both:

- Much larger numbers
- Much smaller numbers
- More precise numbers

---

# printf() Format Specifiers

| Type | Format Specifier |
|------|------------------|
| `float` | `%f` |
| `double` | `%f` |

Notice:

Although they are different types,

`printf()` uses:

```c
%f
```

for both.

This happens because `float` arguments are automatically promoted to `double` when passed to functions like `printf()`.

---

# scanf() Format Specifiers

Unlike `printf()`,

`scanf()` distinguishes between the two types.

| Type | Format Specifier |
|------|------------------|
| `float` | `%f` |
| `double` | `%lf` |

This difference is very important.

---

# Memory Comparison

```
float

↓

4 Bytes
```

```
double

↓

8 Bytes
```

A `double` requires approximately twice as much memory,

but provides much greater precision.

---

# Precision Comparison

Example:

```c
float pi = 3.141592653589793;

double PI = 3.141592653589793;
```

Typical result:

```
float

↓

3.141593
```

```
double

↓

3.141592653589793
```

The exact output depends on formatting,

but `double` preserves considerably more precision.

---

# When Should I Use float?

Choose `float` when:

- Memory is important.
- Moderate precision is sufficient.
- Large arrays of decimal values are stored.
- Embedded systems with limited memory.

Example:

```c
float temperature;
```

---

# When Should I Use double?

Choose `double` when:

- Precision is important.
- Scientific calculations.
- Financial software.
- Physics simulations.
- Engineering calculations.

Example:

```c
double pi;
```

---

# Common Beginner Mistakes

❌ Thinking `double` stores only larger numbers.

❌ Believing floating-point numbers are always exact.

❌ Using `%lf` with `printf()`.

❌ Expecting `float` to preserve every decimal digit.

---

# Visual Comparison

```
float

↓

Smaller

↓

Less Memory

↓

Less Precision
```

```
double

↓

Larger

↓

More Memory

↓

More Precision
```

---

## 📚 Summary

Both `float` and `double` store decimal numbers.

`float` uses less memory,

while `double` provides significantly greater precision.

The correct choice depends on the needs of your program.

---

## 🎯 42 Piscine Notes

- ✅ Use `float` for ordinary decimal values.
- ✅ Use `double` when higher precision is required.
- ✅ Remember `%f` for `printf()`.
- ✅ Remember `%lf` for `scanf()` with `double`.
- ✅ Floating-point numbers are approximations.

---

## 🚀 Mastery Checklist

- [ ] I know the difference between `float` and `double`.
- [ ] I know their typical sizes.
- [ ] I know their typical precision.
- [ ] I know the correct format specifiers.
- [ ] I know when to choose each type.

---

# 🎉 End of Floating-Point Types

You have now completed the entire Floating-Point Family in C.

Next comes the final page of this chapter:

# 🧾 Chapter 6 Cheat Sheet

> **Chapter 6 — Data Types**
>
> A quick reference for all built-in C data types covered in this chapter.

---

# 📦 Integer Types

| Type | Typical Size | Typical Signed Range | Format Specifier |
|------|-------------:|----------------------|------------------|
| `char` | 1 Byte | -128 → 127 | `%c` / `%d` |
| `short` | 2 Bytes | -32,768 → 32,767 | `%hd` |
| `int` | 4 Bytes | -2,147,483,648 → 2,147,483,647 | `%d` |
| `long` | 4 or 8 Bytes | Platform Dependent | `%ld` |
| `long long` | 8 Bytes | ±9.22 × 10¹⁸ | `%lld` |

> ⚠ Remember:
>
> Exact sizes depend on the platform.
>
> Always verify using:
>
> ```c
> sizeof(type)
> ```

---

# 🌊 Floating-Point Types

| Type | Typical Size | Precision | Format Specifier |
|------|-------------:|-----------|------------------|
| `float` | 4 Bytes | ~6–7 digits | `%f` |
| `double` | 8 Bytes | ~15–16 digits | `%f` (`printf`) / `%lf` (`scanf`) |

---

# 🔀 signed vs unsigned

| signed | unsigned |
|---------|-----------|
| ✔ Negative Values | ✘ Negative Values |
| ✔ Positive Values | ✔ Positive Values |
| ✔ Zero | ✔ Zero |
| Same Memory Size | Same Memory Size |

Remember:

```
signed

↓

Negative + Positive
```

```
unsigned

↓

Positive Only
```

---

# 📏 sizeof

```c
sizeof(type)

sizeof(variable)
```

Returns:

```
Size in Bytes
```

Correct format specifier:

```c
%zu
```

Example:

```c
printf("%zu\n", sizeof(int));
```

---

# 🔄 Type Conversion

Automatic:

```c
int x = 5;

float y = x;
```

↓

```
5

↓

5.0
```

---

Manual (Casting):

```c
(float)x
```

Example:

```c
(float)7 / 2

↓

3.5
```

Remember:

```c
(float)(7 / 2)

↓

3.0
```

because the integer division already happened.

---

# ⚠ Overflow

Signed:

```c
int x = INT_MAX;

x++;
```

↓

```
Undefined Behavior
```

---

Unsigned:

```c
unsigned int x = UINT_MAX;

x++;
```

↓

```
0
```

Wrap Around

---

# 📋 Format Specifiers

| Type | printf | scanf |
|------|---------|--------|
| `char` | `%c` | `%c` |
| `short` | `%hd` | `%hd` |
| `int` | `%d` | `%d` |
| `long` | `%ld` | `%ld` |
| `long long` | `%lld` | `%lld` |
| `float` | `%f` | `%f` |
| `double` | `%f` | `%lf` |

---

# 🎯 Choosing the Right Type

Need...

One character?

↓

```c
char
```

---

Whole number?

↓

```c
int
```

---

Very large integer?

↓

```c
long

or

long long
```

---

Decimal number?

↓

```c
float
```

---

High precision decimal?

↓

```c
double
```

---

Never negative?

↓

Consider

```c
unsigned
```

---

# 🚫 Common Beginner Mistakes

❌ Using:

```c
=
```

instead of

```c
==
```

---

❌ Forgetting initialization.

---

❌ Expecting:

```c
7 / 2

↓

3.5
```

---

❌ Assuming:

```c
int

=

4 Bytes
```

on every computer.

---

❌ Using:

```c
%d
```

for every data type.

---

❌ Confusing:

```c
'A'
```

with

```c
"A"
```

---

❌ Assuming floating-point numbers are exact.

---

❌ Ignoring compiler warnings about overflow.

---

# 💡 Professional Tips

✔ Use `int` unless another integer type is clearly needed.

✔ Use `double` when precision matters.

✔ Verify sizes using:

```c
sizeof()
```

✔ Avoid magic numbers.

✔ Initialize variables.

✔ Choose descriptive names.

✔ Read compiler warnings carefully.

✔ Write readable code before clever code.

---

# 🏆 Chapter 6 Mastery Checklist

## Data Types

- [ ] I know every integer type.
- [ ] I know every floating-point type.
- [ ] I know the difference between `float` and `double`.
- [ ] I know the difference between signed and unsigned integers.

---

## Memory

- [ ] I know how to use `sizeof`.
- [ ] I understand that sizes depend on the platform.

---

## Type Conversion

- [ ] I understand implicit conversion.
- [ ] I understand casting.
- [ ] I know why `7 / 2` equals `3`.
- [ ] I know why `(float)7 / 2` equals `3.5`.

---

## Overflow

- [ ] I know what overflow is.
- [ ] I know the difference between signed and unsigned overflow.
- [ ] I know why signed overflow is dangerous.

---

# 🎉 End of Chapter 6

Congratulations!

You have completed one of the most important chapters in the C Language Handbook.

You now understand:

- ✔ Variables
- ✔ Constants
- ✔ Integer Types
- ✔ Floating-Point Types
- ✔ `sizeof`
- ✔ Type Conversion
- ✔ Overflow

These concepts form the foundation of almost every C program you'll write.

---

# 🚀 What's Next?

The next chapter is:

# ➕ Chapter 7 — Operators

You will learn:

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- Logical Operators
- Increment & Decrement
- Bitwise Operators
- Ternary Operator
- `sizeof` Operator (advanced usage)

# ➕ Chapter 7 — Operators

> "Operators are symbols that tell the computer to perform operations on data."

🟢 Beginner

⏱ Estimated Study Time: ~5–6 Hours

---

# Introduction

So far,

we've learned:

- Variables
- Constants
- Data Types
- Memory

But knowing how to store data isn't enough.

Programs become useful only when they **operate** on data.

For example:

```c
age + 1

price * quantity

score >= 50

a && b
```

The symbols:

```
+

*

>=

&&
```

are called **Operators**.

They tell the compiler what operation should be performed.

---

# What is an Operator?

An operator is a special symbol that performs an operation on one or more values.

Example:

```c
5 + 3
```

The operator is:

```text
+
```

The values are called:

```
Operands
```

Visual representation:

```
5

+

3

↑

Operator
```

---

# What are Operands?

Operands are the values on which an operator works.

Example:

```c
10 - 4
```

Operator:

```text
-
```

Operands:

```
10

4
```

---

# Example

```c
int result = 10 + 5;
```

```
10

↓

Operand
```

```
+

↓

Operator
```

```
5

↓

Operand
```

Result:

```
15
```

---

# Categories of Operators

C provides many kinds of operators.

In this chapter we will study:

```
Arithmetic

↓

Assignment

↓

Comparison

↓

Logical

↓

Increment

↓

Decrement

↓

Bitwise

↓

Conditional (Ternary)

↓

sizeof
```

Each category solves a different problem.

---

# Unary, Binary and Ternary Operators

Operators are also classified by the number of operands they require.

---

## Unary Operators

Operate on **one operand**.

Example:

```c
++x

--x

sizeof(x)

!x
```

One operand only.

---

## Binary Operators

Operate on **two operands**.

Example:

```c
a + b

x * y

score >= 50
```

Most operators in C are binary operators.

---

## Ternary Operator

Operates on **three operands**.

Example:

```c
condition ? value1 : value2
```

This is the only ternary operator in C.

We'll study it later in this chapter.

---

# Why Operators Matter

Without operators,

programs couldn't perform calculations.

Example:

```c
salary = hours * wage;
```

Without:

```text
*
```

there would be no multiplication.

Operators are one of the fundamental building blocks of programming.

---

# Mental Model

Imagine a factory.

```
Input

↓

Machine

↓

Output
```

The machine is the operator.

The input values are the operands.

The output is the result.

Example:

```
7

↓

+

↓

5

↓

12
```

---

## 📚 Summary

Operators perform actions on data.

The values involved are called operands.

C provides several categories of operators,

each designed for a specific purpose.

Understanding operators is essential because almost every C program relies on them.

---

## 🧠 Key Concepts

- Operator
- Operand
- Unary
- Binary
- Ternary
- Expression

---

## ⚠ Common Mistakes

- Confusing operators with keywords.
- Thinking `=` means comparison.
- Forgetting that operators produce values.
- Ignoring operator precedence.

---

## 💡 Coach Tips

✔ Learn what each operator does before memorizing its symbol.

✔ Think of operators as actions performed on data.

✔ Every expression contains one or more operators.

✔ Understanding operators is more important than memorizing all of them.

---

## 🧩 Think Like the Computer

Identify the operator and operands.

```c
10 * 4
```

---

```c
score >= 50
```

---

```c
!finished
```

How many operands does each operator have?

---

## 🏋️ Practice Exercises

1. Define "Operator" in your own words.

---

2. Define "Operand."

---

3. Which category does each belong to?

```text
+

=

&&

>

++

sizeof
```

---

4. Explain the difference between:

- Unary Operator
- Binary Operator
- Ternary Operator

---

## 🎯 42 Piscine Notes

- ✅ Operators perform actions on data.
- ✅ Operands are the values involved.
- ✅ Most C expressions are combinations of operators and operands.
- ✅ Learn operator categories before individual operators.

---

## 🚀 Mastery Checklist

- [ ] I know what an operator is.
- [ ] I know what an operand is.
- [ ] I know the difference between unary, binary and ternary operators.
- [ ] I know the operator categories in C.
- [ ] I am ready to study each operator family.

---

# Arithmetic Operators

> "Arithmetic operators perform mathematical calculations on numeric values."

🟢 Beginner

⏱ Estimated Study Time: ~50 Minutes

---

# Introduction

One of the first things every programmer learns is how to make the computer perform calculations.

Examples:

```
10 + 5

20 - 8

7 * 9

100 / 5
```

The symbols:

```
+

-

*

/

%
```

are called:

```
Arithmetic Operators
```

They perform mathematical operations on numbers.

---

# The Arithmetic Operators

C provides five basic arithmetic operators.

| Operator | Name | Example |
|----------|------|----------|
| `+` | Addition | `5 + 3` |
| `-` | Subtraction | `8 - 2` |
| `*` | Multiplication | `4 * 6` |
| `/` | Division | `20 / 5` |
| `%` | Modulus (Remainder) | `7 % 3` |

These operators work with integer and floating-point values (except `%`, which works only with integer types).

---

# Addition (+)

The addition operator adds two values.

Example:

```c
int result = 10 + 5;

printf("%d\n", result);
```

Output:

```
15
```

---

Example:

```c
int apples = 7;

int oranges = 4;

int fruits = apples + oranges;
```

Result:

```
11
```

---

# Subtraction (-)

The subtraction operator subtracts one value from another.

Example:

```c
int result = 20 - 8;
```

Result:

```
12
```

---

Example:

```c
int lives = 5;

lives = lives - 1;
```

Result:

```
4
```

---

# Multiplication (*)

The multiplication operator multiplies two values.

Example:

```c
int result = 6 * 7;
```

Output:

```
42
```

---

Example:

```c
int rows = 5;

int columns = 10;

int cells = rows * columns;
```

Result:

```
50
```

---

# Division (/)

The division operator divides one value by another.

Example:

```c
20 / 4
```

↓

```
5
```

---

Example:

```c
float x = 7.0;

float y = 2.0;

printf("%f\n", x / y);
```

Output:

```
3.500000
```

---

## Integer Division

One of the most important rules in C.

If both operands are integers,

the result is also an integer.

Example:

```c
7 / 2
```

Result:

```
3
```

The fractional part is discarded.

---

Compare:

```c
7.0 / 2.0
```

Result:

```
3.5
```

This difference is one of the most common beginner mistakes.

---

# Modulus (%)

The modulus operator returns the remainder after integer division.

Example:

```c
7 % 3
```

Calculation:

```
7 ÷ 3

↓

2

Remainder

↓

1
```

Output:

```
1
```

---

Another example:

```c
20 % 6
```

Calculation:

```
20 ÷ 6

↓

3

Remainder

↓

2
```

Output:

```
2
```

---

# Why is Modulus Useful?

Check if a number is even.

```c
number % 2
```

If the remainder is:

```
0
```

The number is even.

Otherwise,

it is odd.

---

Cycle through values.

Example:

```
0

1

2

3

4

↓

0

1

2

...
```

This idea appears constantly in programming.

---

# Operator Precedence

Consider:

```c
2 + 3 * 4
```

Many beginners expect:

```
20
```

Actually:

```
3 * 4

↓

12
```

Then:

```
2 + 12

↓

14
```

Multiplication has higher precedence than addition.

---

Use parentheses when needed.

```c
(2 + 3) * 4
```

Result:

```
20
```

Parentheses make expressions easier to understand.

---

# Division by Zero

Never divide by zero.

Example:

```c
10 / 0
```

This causes:

```
Undefined Behavior
```

Always ensure the divisor is not zero before performing division.

---

# Real-World Examples

Shopping

```c
total = price * quantity;
```

Average

```c
average = total / count;
```

Remaining Lives

```c
lives = lives - 1;
```

Bonus

```c
score = score + bonus;
```

Even Number

```c
number % 2
```

---

# Mental Model

Imagine a calculator.

Every button is an operator.

```
+

-

*

/

%
```

The numbers are the operands.

The display shows the result.

---

## 📚 Summary

Arithmetic operators perform mathematical calculations.

C provides five arithmetic operators:

- Addition
- Subtraction
- Multiplication
- Division
- Modulus

Understanding integer division and the modulus operator is essential for solving many programming problems.

---

## 🧠 Key Concepts

- Addition
- Subtraction
- Multiplication
- Division
- Modulus
- Integer Division
- Operator Precedence

---

## ⚠ Common Mistakes

- Expecting `7 / 2` to equal `3.5`.
- Using `%` with floating-point values.
- Forgetting operator precedence.
- Dividing by zero.
- Assuming `%` returns the quotient instead of the remainder.

---

## 💡 Coach Tips

✔ Remember:

```
/

↓

Division
```

```
%

↓

Remainder
```

✔ Use parentheses to make expressions clear.

✔ Learn `%` well.

It appears in many Piscine exercises.

✔ Always check for division by zero.

---

## 🧩 Think Like the Computer

Predict the output.

```c
printf("%d\n", 10 + 5);

printf("%d\n", 20 - 8);

printf("%d\n", 6 * 7);

printf("%d\n", 9 / 2);

printf("%d\n", 9 % 2);
```

Explain every result.

---

## 🏋️ Practice Exercises

1. Predict the output.

```c
int a = 12;

int b = 5;

printf("%d\n", a + b);

printf("%d\n", a - b);

printf("%d\n", a * b);

printf("%d\n", a / b);

printf("%d\n", a % b);
```

---

2. Explain why:

```c
7 / 2
```

returns:

```
3
```

---

3. Explain why:

```c
7 % 2
```

returns:

```
1
```

---

4. Add parentheses so the result becomes:

```
20
```

```c
2 + 3 * 4
```

---

## 🎯 42 Piscine Notes

- ✅ Master integer division.
- ✅ Master the modulus operator.
- ✅ Use parentheses for readability.
- ✅ Never divide by zero.
- ✅ Remember operator precedence.

---

## 📊 Arithmetic Operators Summary

| Operator | Meaning | Example | Result |
|----------|---------|----------|--------|
| `+` | Addition | `5 + 2` | `7` |
| `-` | Subtraction | `5 - 2` | `3` |
| `*` | Multiplication | `5 * 2` | `10` |
| `/` | Division | `5 / 2` | `2` *(integer division)* |
| `%` | Remainder | `5 % 2` | `1` |

---

## 🚀 Mastery Checklist

- [ ] I know every arithmetic operator.
- [ ] I understand integer division.
- [ ] I know what the modulus operator does.
- [ ] I understand operator precedence.
- [ ] I know why division by zero is dangerous.

---

# 📝 Assignment Operators

> "Assignment operators store or update values inside variables."

🟢 Beginner

⏱ Estimated Study Time: ~45 Minutes

---

# Introduction

Earlier in the handbook,

we learned about:

```
Assignment
```

Example:

```c
int age = 25;

age = 30;
```

The symbol:

```text
=
```

is called the:

```
Assignment Operator
```

However,

C provides several assignment operators that make code shorter and easier to read.

---

# Basic Assignment (=)

The simplest assignment operator is:

```text
=
```

It stores a value inside a variable.

Example:

```c
int score;

score = 100;
```

After execution:

```
score

↓

100
```

---

Another example:

```c
int age = 20;

age = 25;
```

The previous value is replaced.

---

# Compound Assignment Operators

Instead of writing:

```c
x = x + 5;
```

C allows us to write:

```c
x += 5;
```

Both statements produce exactly the same result.

Compound assignment operators make programs shorter and often easier to read.

---

# Addition Assignment (+=)

General form:

```c
x += value;
```

Equivalent to:

```c
x = x + value;
```

Example:

```c
int score = 50;

score += 10;
```

Result:

```
60
```

---

# Subtraction Assignment (-=)

General form:

```c
x -= value;
```

Equivalent to:

```c
x = x - value;
```

Example:

```c
int lives = 5;

lives -= 1;
```

Result:

```
4
```

---

# Multiplication Assignment (*=)

General form:

```c
x *= value;
```

Equivalent to:

```c
x = x * value;
```

Example:

```c
int money = 20;

money *= 3;
```

Result:

```
60
```

---

# Division Assignment (/=)

General form:

```c
x /= value;
```

Equivalent to:

```c
x = x / value;
```

Example:

```c
int value = 20;

value /= 4;
```

Result:

```
5
```

Remember:

If both operands are integers,

integer division still applies.

---

# Modulus Assignment (%=)

General form:

```c
x %= value;
```

Equivalent to:

```c
x = x % value;
```

Example:

```c
int number = 17;

number %= 5;
```

Calculation:

```
17 % 5

↓

2
```

Result:

```
2
```

---

# Visual Comparison

Normal assignment:

```c
x = x + 10;
```

↓

```
Read x

↓

Add 10

↓

Store result
```

Shortcut:

```c
x += 10;
```

↓

Exactly the same operation.

---

# Common Examples

Increase score.

```c
score += 100;
```

Lose health.

```c
health -= 10;
```

Triple money.

```c
money *= 3;
```

Split equally.

```c
players /= 2;
```

Find remainder.

```c
number %= 2;
```

---

# Assignment Operators Return a Value

An assignment expression has a value.

Example:

```c
int a;
int b;

a = b = 5;
```

Execution:

```
b = 5

↓

Returns 5

↓

a = 5
```

Result:

```
a = 5

b = 5
```

Although valid,

writing assignments like this too often can reduce readability.

---

# Mental Model

Imagine updating a bank account.

Current balance:

```
100
```

Deposit:

```c
balance += 50;
```

New balance:

```
150
```

The account remains the same.

Only its value changes.

---

## 📚 Summary

Assignment operators modify the value of a variable.

Compound assignment operators provide shorter forms for common operations such as addition, subtraction, multiplication, division, and modulus.

They improve readability and reduce repetition.

---

## 🧠 Key Concepts

- Assignment
- Compound Assignment
- `=`
- `+=`
- `-=`
- `*=`
- `/=`
- `%=`

---

## ⚠ Common Mistakes

- Confusing:

```c
=
```

with:

```c
==
```

- Forgetting that:

```c
/=
```

still performs integer division when both operands are integers.

- Assuming compound operators are different operations.

They are simply shorthand.

---

## 💡 Coach Tips

✔ Learn compound assignment operators early.

✔ They appear constantly in real-world code.

✔ Prefer:

```c
count++;
```

over:

```c
count += 1;
```

when increasing by exactly one.

We'll study `++` next.

✔ Keep assignments simple and readable.

---

## 🧩 Think Like the Computer

Predict the final value.

```c
int x = 10;

x += 5;

x *= 2;

x -= 4;

x /= 2;
```

Now predict:

```c
int y = 17;

y %= 5;
```

---

## 🏋️ Practice Exercises

1. Rewrite using compound assignment.

```c
score = score + 20;
```

---

```c
health = health - 5;
```

---

```c
money = money * 4;
```

---

```c
points = points / 2;
```

---

```c
number = number % 3;
```

---

2. Predict the output.

```c
int x = 12;

x += 8;

x /= 4;

printf("%d\n", x);
```

---

3. Explain why:

```c
x += 5;
```

and

```c
x = x + 5;
```

produce the same result.

---

4. What are the final values?

```c
int a = 5;

int b = 10;

a = b = 20;
```

---

## 🎯 42 Piscine Notes

- ✅ Learn all compound assignment operators.
- ✅ Use them to improve readability.
- ✅ Don't confuse assignment with comparison.
- ✅ Keep assignment expressions simple.

---

## 📊 Assignment Operators Summary

| Operator | Equivalent Expression |
|----------|------------------------|
| `=` | Assign value |
| `+=` | `x = x + y` |
| `-=` | `x = x - y` |
| `*=` | `x = x * y` |
| `/=` | `x = x / y` |
| `%=` | `x = x % y` |

---

## 🚀 Mastery Checklist

- [ ] I know every assignment operator.
- [ ] I know what compound assignment is.
- [ ] I understand that compound operators are shorthand.
- [ ] I know that assignment changes a variable's value.
- [ ] I know the difference between `=` and `==`.

---

# ⚖️ Comparison Operators

> "Comparison operators compare two values and produce either true or false."

🟢 Beginner

⏱ Estimated Study Time: ~1 Hour

---

# Introduction

Programs often need to answer questions like:

- Is the user old enough?
- Did the player win?
- Are two numbers equal?
- Is one value larger than another?

These questions require **comparison**.

Example:

```c
age >= 18
```

The result is not a number.

The result is either:

```
True

or

False
```

---

# What is a Comparison Operator?

A comparison operator compares two values.

Example:

```c
10 > 5
```

Question:

```
Is 10 greater than 5?
```

Answer:

```
True
```

---

Another example:

```c
3 > 7
```

Answer:

```
False
```

---

# Boolean Results

Although C does not have a built-in `bool` type until C99 (`<stdbool.h>`),

comparison operators still produce logical results.

Internally:

```
False

↓

0
```

```
True

↓

1
```

Example:

```c
printf("%d\n", 10 > 5);
```

Output:

```
1
```

Example:

```c
printf("%d\n", 10 < 5);
```

Output:

```
0
```

---

# The Comparison Operators

| Operator | Meaning |
|----------|---------|
| `==` | Equal To |
| `!=` | Not Equal To |
| `>` | Greater Than |
| `<` | Less Than |
| `>=` | Greater Than or Equal To |
| `<=` | Less Than or Equal To |

---

# Equal To (==)

Checks whether two values are equal.

Example:

```c
10 == 10
```

↓

```
True
```

---

Example:

```c
7 == 5
```

↓

```
False
```

---

Real example:

```c
if (score == 100)
```

Meaning:

```
Did the player score exactly 100?
```

---

# Not Equal To (!=)

Checks whether two values are different.

Example:

```c
5 != 10
```

↓

```
True
```

---

Example:

```c
7 != 7
```

↓

```
False
```

---

# Greater Than (>)

Checks whether the left value is larger.

Example:

```c
20 > 15
```

↓

```
True
```

---

Example:

```c
5 > 20
```

↓

```
False
```

---

# Less Than (<)

Checks whether the left value is smaller.

Example:

```c
10 < 20
```

↓

```
True
```

---

Example:

```c
20 < 10
```

↓

```
False
```

---

# Greater Than or Equal (>=)

Example:

```c
18 >= 18
```

↓

```
True
```

---

Example:

```c
20 >= 18
```

↓

```
True
```

---

Example:

```c
15 >= 18
```

↓

```
False
```

---

# Less Than or Equal (<=)

Example:

```c
5 <= 5
```

↓

```
True
```

---

Example:

```c
3 <= 7
```

↓

```
True
```

---

Example:

```c
10 <= 7
```

↓

```
False
```

---

# Comparison Operators Return Values

Example:

```c
printf("%d\n", 5 > 3);
```

Output:

```
1
```

---

Example:

```c
printf("%d\n", 5 == 8);
```

Output:

```
0
```

Remember:

```
True

↓

1
```

```
False

↓

0
```

---

# The Biggest Beginner Mistake

Compare these:

Assignment:

```c
=
```

Comparison:

```c
==
```

These are **not** the same.

Assignment:

```c
score = 100;
```

Stores a value.

Comparison:

```c
score == 100;
```

Checks whether the value is 100.

---

Incorrect:

```c
if (score = 100)
```

Correct:

```c
if (score == 100)
```

This is one of the most common beginner mistakes.

---

# Real-World Examples

Voting

```c
age >= 18
```

Passing Exam

```c
score >= 50
```

Password Check

```c
password == saved_password
```

Temperature Alert

```c
temperature > 40
```

Game Over

```c
lives == 0
```

---

# Mental Model

Imagine a judge comparing two boxes.

```
Box A

?

Box B
```

The judge answers only:

```
YES

or

NO
```

Comparison operators work exactly like that.

---

## 📚 Summary

Comparison operators compare two values.

They always produce a logical result:

```
True

↓

1
```

or

```
False

↓

0
```

These operators are essential for decision-making in C programs.

---

## 🧠 Key Concepts

- Comparison
- Equality
- Relational Operator
- True
- False

---

## ⚠ Common Mistakes

- Confusing `=` with `==`.
- Expecting comparison operators to change values.
- Forgetting that comparisons produce `1` or `0`.
- Using assignment inside conditions by mistake.

---

## 💡 Coach Tips

✔ Read:

```c
==
```

as:

```
"Is equal to?"
```

✔ Read:

```c
=
```

as:

```
"Store this value."
```

✔ Remember:

Comparisons answer questions.

Assignments change values.

---

## 🧩 Think Like the Computer

Predict the output.

```c
printf("%d\n", 10 == 10);

printf("%d\n", 5 != 5);

printf("%d\n", 8 > 3);

printf("%d\n", 2 < 1);

printf("%d\n", 10 >= 10);

printf("%d\n", 5 <= 8);
```

Explain each result.

---

## 🏋️ Practice Exercises

1. Predict the result.

```c
8 == 8
```

---

```c
7 != 5
```

---

```c
12 > 30
```

---

```c
15 <= 20
```

---

2. Explain the difference between:

```c
=
```

and

```c
==
```

---

3. Which comparisons are true?

```c
5 < 10

20 >= 20

7 != 7

8 == 9
```

---

4. Write comparisons for:

- Age is at least 18.
- Score is exactly 100.
- Temperature is below 0.
- Lives are not zero.

---

## 🎯 42 Piscine Notes

- ✅ Master all six comparison operators.
- ✅ Never confuse `=` with `==`.
- ✅ Comparisons produce `1` or `0`.
- ✅ Every `if` statement depends on comparison operators.

---

## 📊 Comparison Operators Summary

| Operator | Meaning | Example | Result |
|----------|---------|----------|--------|
| `==` | Equal | `5 == 5` | `1` |
| `!=` | Not Equal | `5 != 3` | `1` |
| `>` | Greater Than | `7 > 2` | `1` |
| `<` | Less Than | `2 < 7` | `1` |
| `>=` | Greater Than or Equal | `5 >= 5` | `1` |
| `<=` | Less Than or Equal | `3 <= 8` | `1` |

---

## 🚀 Mastery Checklist

- [ ] I know every comparison operator.
- [ ] I understand the difference between `=` and `==`.
- [ ] I know that comparisons return `1` or `0`.
- [ ] I can predict comparison results.
- [ ] I understand why comparison operators are essential for `if` statements.

---

# 🔗 Logical Operators

> "Logical operators combine or modify logical expressions."

🟢 Beginner

⏱ Estimated Study Time: ~1 Hour

---

# Introduction

Suppose we want to answer this question.

```
Is the user:

Older than 18

AND

Has a valid ID?
```

One comparison isn't enough.

We need to combine multiple conditions.

C provides three logical operators.

```
&&

||

!
```

These operators allow programs to make intelligent decisions.

---

# What is a Logical Operator?

A logical operator works with logical values.

Remember:

Comparison operators produce:

```
True

↓

1
```

or

```
False

↓

0
```

Logical operators combine these results.

---

# The Logical Operators

| Operator | Name |
|----------|------|
| `&&` | Logical AND |
| `||` | Logical OR |
| `!` | Logical NOT |

---

# Logical AND (&&)

The AND operator requires **both conditions** to be true.

Syntax:

```c
condition1 && condition2
```

Example:

```c
age >= 18 && has_id
```

Meaning:

```
Age is at least 18

AND

Has an ID
```

Both conditions must be true.

---

Example:

```c
10 > 5 && 8 > 3
```

Result:

```
True

↓

1
```

---

Example:

```c
10 > 5 && 2 > 8
```

Result:

```
False

↓

0
```

---

# Truth Table — AND

| A | B | A && B |
|---|---|---------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

Remember:

```
AND

↓

Everything must be true.
```

---

# Logical OR (||)

The OR operator requires **at least one condition** to be true.

Syntax:

```c
condition1 || condition2
```

Example:

```c
has_ticket || has_pass
```

Meaning:

```
Has a ticket

OR

Has a pass
```

Either one is enough.

---

Example:

```c
10 > 5 || 2 > 8
```

Result:

```
True

↓

1
```

---

Example:

```c
2 > 5 || 1 > 8
```

Result:

```
False

↓

0
```

---

# Truth Table — OR

| A | B | A \|\| B |
|---|---|-----------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

Remember:

```
OR

↓

Only one condition is enough.
```

---

# Logical NOT (!)

The NOT operator reverses a logical value.

Syntax:

```c
!condition
```

Example:

```c
!(10 > 5)
```

Original:

```
True
```

After NOT:

```
False
```

---

Example:

```c
!(2 > 5)
```

Original:

```
False
```

After NOT:

```
True
```

---

# Truth Table — NOT

| A | !A |
|---|----|
| 0 | 1 |
| 1 | 0 |

NOT simply flips the result.

---

# Combining Logical Operators

Example:

```c
(age >= 18) && (score >= 50)
```

Meaning:

```
Adult

AND

Passed
```

---

Another example:

```c
(age < 18) || (has_permission)
```

Meaning:

```
Minor

OR

Has Permission
```

---

# Operator Precedence

Logical NOT has the highest precedence.

Then:

```
&&
```

Then:

```
||
```

To avoid confusion,

use parentheses.

Example:

```c
(age >= 18) && (score >= 50)
```

instead of:

```c
age >= 18 && score >= 50
```

Both are equivalent,

but parentheses improve readability.

---

# Short-Circuit Evaluation

Logical operators sometimes stop evaluating early.

Example:

```c
if (x != 0 && 10 / x > 2)
```

If:

```c
x == 0
```

The second condition is **never evaluated**.

Why?

Because the first condition is already false,

so the entire `&&` expression must be false.

This behavior is called:

```
Short-Circuit Evaluation
```

It prevents errors like division by zero.

Similarly,

with `||`:

```c
if (is_admin || has_permission)
```

If:

```c
is_admin
```

is already true,

the second condition is skipped.

---

# Real-World Examples

Login

```c
username_ok && password_ok
```

Voting

```c
age >= 18 && citizen
```

Access

```c
is_admin || is_owner
```

Game

```c
!game_over
```

---

# Mental Model

Imagine security guards.

AND

```
Guard 1

✔

AND

Guard 2

✔

↓

Access
```

One "No"

↓

No access.

---

OR

```
VIP Card

OR

Ticket

↓

Access
```

Either one is enough.

---

NOT

```
Door Locked

↓

NOT

↓

Door Unlocked
```

---

## 📚 Summary

Logical operators combine or modify logical expressions.

They always produce:

```
True

↓

1
```

or

```
False

↓

0
```

The three logical operators are:

- `&&`
- `||`
- `!`

These operators are fundamental for writing conditions in C.

---

## 🧠 Key Concepts

- Logical AND
- Logical OR
- Logical NOT
- Boolean Logic
- Short-Circuit Evaluation

---

## ⚠ Common Mistakes

- Confusing `&&` with `&`.
- Confusing `||` with `|`.
- Forgetting parentheses in complex expressions.
- Forgetting short-circuit behavior.
- Using `=` instead of `==` inside conditions.

---

## 💡 Coach Tips

✔ Read:

```c
&&
```

as:

```
AND
```

✔ Read:

```c
||
```

as:

```
OR
```

✔ Read:

```c
!
```

as:

```
NOT
```

✔ Use parentheses when combining conditions.

They make code much easier to understand.

---

## 🧩 Think Like the Computer

Predict the result.

```c
10 > 5 && 8 > 2
```

---

```c
10 > 5 || 2 > 8
```

---

```c
!(7 > 2)
```

---

```c
(5 < 2) || (10 > 3)
```

Explain each answer.

---

## 🏋️ Practice Exercises

1. Predict the result.

```c
5 > 2 && 7 > 4
```

---

```c
5 > 8 || 10 > 2
```

---

```c
!(8 == 8)
```

---

2. Write a condition that checks:

- Age is at least 18 **and** score is at least 50.

---

3. Write a condition that checks:

- The user is an administrator **or** a moderator.

---

4. Explain what short-circuit evaluation means.

---

## 🎯 42 Piscine Notes

- ✅ Learn all three logical operators.
- ✅ Use parentheses in complex conditions.
- ✅ Understand short-circuit evaluation.
- ✅ Logical operators are used constantly with `if`, `while`, and `for`.

---

## 📊 Logical Operators Summary

| Operator | Meaning | Example | Result |
|----------|---------|----------|--------|
| `&&` | AND | `5 > 2 && 8 > 3` | `1` |
| `||` | OR | `5 > 8 || 8 > 3` | `1` |
| `!` | NOT | `!(5 > 2)` | `0` |

---

## 🚀 Mastery Checklist

- [ ] I know all three logical operators.
- [ ] I understand AND, OR, and NOT.
- [ ] I can read logical expressions.
- [ ] I understand short-circuit evaluation.
- [ ] I can combine multiple conditions correctly.

---

# 🧩 Building Complex Conditions

> "Complex conditions combine multiple comparisons using logical operators to express real-world decisions."

🟡 Intermediate

⏱ Estimated Study Time: ~45 Minutes

---

# Introduction

A single comparison is often not enough.

For example,

this question:

```
Is the user at least 18 years old?
```

needs only one comparison.

```c
age >= 18
```

But real programs usually ask more complicated questions.

Example:

```
Is the user:

At least 18

AND

Has a driver's license?
```

Now we need multiple comparisons.

---

# A Simple Condition

Example:

```c
score >= 50
```

Question:

```
Did the student pass?
```

Possible answers:

```
True

or

False
```

Simple conditions contain only one comparison.

---

# Combining Conditions

Suppose:

```
Adult

AND

Has ID
```

C expression:

```c
(age >= 18) && (has_id)
```

Both conditions must be true.

---

Another example:

```
Has Ticket

OR

VIP
```

Expression:

```c
(has_ticket) || (is_vip)
```

Only one is required.

---

# Example 1 — Voting

Requirements:

- At least 18
- Citizen

Condition:

```c
(age >= 18) && (is_citizen)
```

Meaning:

```
Adult

AND

Citizen
```

---

# Example 2 — Passing a Course

Requirements:

- Score at least 50
- Attendance at least 75%

Condition:

```c
(score >= 50) && (attendance >= 75)
```

---

# Example 3 — Entering a Building

Requirements:

```
Employee

OR

Manager
```

Expression:

```c
(is_employee) || (is_manager)
```

---

# Example 4 — Playing Again

Requirement:

```
Game is NOT over
```

Expression:

```c
!game_over
```

---

# Mixing AND and OR

Suppose:

```
Student passed

OR

Teacher approved
```

AND

```
Paid Fees
```

Write:

```c
((score >= 50) || teacher_approved) && fees_paid
```

The parentheses clearly show the intended logic.

---

# Why Parentheses Matter

Compare:

```c
a || b && c
```

with:

```c
(a || b) && c
```

These expressions may produce different results.

Whenever an expression becomes complex,

use parentheses.

Even if the compiler doesn't need them,

humans do.

---

# Reading Conditions Like English

Example:

```c
(age >= 18) && (score >= 50)
```

Read it as:

```
Age is at least 18

AND

Score is at least 50
```

---

Example:

```c
(score < 50) || absent
```

Read it as:

```
Score is below 50

OR

Student was absent
```

Reading conditions aloud is an excellent debugging technique.

---

# Real-World Examples

Driving License

```c
(age >= 18) && passed_exam
```

---

Scholarship

```c
(score >= 90) && (attendance >= 95)
```

---

Discount

```c
(is_student) || (is_senior)
```

---

Login

```c
username_ok && password_ok
```

---

# Mental Model

Imagine a checklist.

```
✔ Adult

✔ Citizen

↓

Can Vote
```

Miss one requirement:

```
❌ Cannot Vote
```

Logical operators simply combine checklists.

---

## 📚 Summary

Complex conditions combine multiple comparisons using logical operators.

They allow programs to represent real-world rules clearly and accurately.

Parentheses improve readability and help prevent logical mistakes.

---

## 🧠 Key Concepts

- Simple Condition
- Compound Condition
- Parentheses
- AND
- OR
- NOT

---

## ⚠ Common Mistakes

- Writing long conditions without parentheses.
- Mixing `&&` and `||` carelessly.
- Forgetting that `!` reverses the result.
- Thinking the compiler interprets expressions the same way humans do.

---

## 💡 Coach Tips

✔ Every comparison asks one question.

✔ Logical operators combine those questions.

✔ Read every condition as if you were reading an English sentence.

✔ When in doubt,

add parentheses.

They improve readability even when not required.

---

## 🧩 Think Like the Computer

Read each condition aloud.

```c
(age >= 18) && has_license
```

---

```c
(score >= 50) || teacher_permission
```

---

```c
!(game_over)
```

---

```c
(age >= 18) && ((score >= 50) || special_permission)
```

What real-world rule does each condition represent?

---

## 🏋️ Practice Exercises

1. Write a condition for:

- The user is at least 18 **and** has a passport.

---

2. Write a condition for:

- The player has a key **or** knows the password.

---

3. Write a condition for:

- The student passed **or** has permission to retake the exam.

---

4. Add parentheses to improve readability.

```c
age >= 18 && score >= 50 || has_permission
```

---

5. Explain this condition in plain English.

```c
(age >= 18) && ((has_id) || (is_police))
```

---

## 🎯 42 Piscine Notes

- ✅ Real programs rarely use only one comparison.
- ✅ Parentheses make conditions easier to understand.
- ✅ Read complex conditions aloud.
- ✅ Build conditions one comparison at a time.

---

## 📊 Condition Building Checklist

Before writing a condition, ask yourself:

- What am I checking?
- How many comparisons do I need?
- Should they all be true (`&&`)?
- Is one enough (`||`)?
- Do I need to reverse a result (`!`)?
- Would parentheses improve readability?

---

## 🚀 Mastery Checklist

- [ ] I can write simple conditions.
- [ ] I can combine conditions with `&&`.
- [ ] I can combine conditions with `||`.
- [ ] I know when to use `!`.
- [ ] I use parentheses to improve readability.
- [ ] I can translate real-world rules into C conditions.

---

# 🔄 Increment & Decrement Operators

> "Increment and decrement operators increase or decrease a variable by one."

🟡 Intermediate

⏱ Estimated Study Time: ~1 Hour

---

# Introduction

Suppose you have:

```c
int score = 10;
```

After defeating an enemy,

the score should become:

```
11
```

You could write:

```c
score = score + 1;
```

or

```c
score += 1;
```

But C provides an even shorter notation:

```c
score++;
```

Likewise,

to decrease a value:

```c
score--;
```

These are called:

```
Increment

and

Decrement Operators
```

---

# Increment (++)

The increment operator increases a variable by exactly one.

Example:

```c
int x = 5;

x++;
```

Result:

```
6
```

Equivalent to:

```c
x = x + 1;
```

or

```c
x += 1;
```

---

# Decrement (--)

The decrement operator decreases a variable by exactly one.

Example:

```c
int x = 5;

x--;
```

Result:

```
4
```

Equivalent to:

```c
x = x - 1;
```

or

```c
x -= 1;
```

---

# Prefix Increment

General form:

```c
++x
```

Meaning:

```
Increase first

↓

Then use the value
```

Example:

```c
int x = 5;

int y = ++x;
```

Execution:

```
x

↓

6

↓

y

↓

6
```

Final values:

```
x = 6

y = 6
```

---

# Postfix Increment

General form:

```c
x++
```

Meaning:

```
Use the value first

↓

Then increase it
```

Example:

```c
int x = 5;

int y = x++;
```

Execution:

```
y

↓

5

↓

x

↓

6
```

Final values:

```
x = 6

y = 5
```

---

# Prefix vs Postfix

Prefix:

```c
++x
```

```
Increase

↓

Use
```

---

Postfix:

```c
x++
```

```
Use

↓

Increase
```

This difference matters only when the expression's value is used.

---

# Prefix Decrement

Example:

```c
int x = 5;

int y = --x;
```

Result:

```
x = 4

y = 4
```

---

# Postfix Decrement

Example:

```c
int x = 5;

int y = x--;
```

Result:

```
x = 4

y = 5
```

---

# When Used Alone

Compare:

```c
x++;
```

and

```c
++x;
```

Both produce:

```
x + 1
```

There is **no practical difference** when the result is ignored.

Example:

```c
int x = 10;

x++;

++x;
```

Final value:

```
12
```

---

# Visual Timeline

Prefix:

```
5

↓

Increment

↓

6

↓

Use 6
```

---

Postfix:

```
5

↓

Use 5

↓

Increment

↓

6
```

---

# Common Uses

Loop Counter

```c
i++;
```

---

Countdown

```c
seconds--;
```

---

Array Traversal

```c
index++;
```

---

Character Processing

```c
pointer++;
```

We'll see this again with pointers.

---

# Be Careful!

Avoid writing confusing expressions.

Example:

```c
x = x++;
```

or

```c
printf("%d %d\n", x++, x++);
```

These involve modifying the same variable multiple times without a clear sequencing rule.

The behavior is undefined or unspecified depending on the expression and the C standard.

**Do not write code like this.**

---

# Mental Model

Imagine taking a numbered ticket.

Postfix:

```
Receive Ticket #5

↓

Machine becomes #6
```

Prefix:

```
Machine becomes #6

↓

Receive Ticket #6
```

The only difference is:

```
When

the increment happens.
```

---

## 📚 Summary

The increment operator increases a variable by one.

The decrement operator decreases a variable by one.

Prefix modifies the variable before its value is used.

Postfix uses the current value before modifying it.

When used as standalone statements,

both forms produce the same final value.

---

## 🧠 Key Concepts

- Increment
- Decrement
- Prefix
- Postfix
- Expression Evaluation

---

## ⚠ Common Mistakes

- Thinking prefix and postfix are always identical.
- Using `x = x++;`.
- Modifying the same variable multiple times in one expression.
- Forgetting that postfix returns the old value.

---

## 💡 Coach Tips

✔ Use:

```c
i++
```

or

```c
++i
```

as standalone statements freely.

✔ Inside complex expressions,

be careful.

✔ Prefer writing clear code instead of clever code.

✔ In the Piscine,

readability is more valuable than tricks.

---

## 🧩 Think Like the Computer

Predict the final values.

Example 1:

```c
int x = 5;

int y = ++x;
```

---

Example 2:

```c
int x = 5;

int y = x++;
```

---

Example 3:

```c
int x = 10;

x++;

++x;
```

What is the final value of `x`?

---

## 🏋️ Practice Exercises

1. Predict the output.

```c
int x = 8;

printf("%d\n", ++x);
```

---

2. Predict the output.

```c
int x = 8;

printf("%d\n", x++);
```

What is the value of `x` afterward?

---

3. Explain the difference between:

```c
++x
```

and

```c
x++
```

---

4. Rewrite using increment operators.

```c
count = count + 1;
```

---

5. Rewrite using decrement operators.

```c
lives = lives - 1;
```

---

## 🎯 42 Piscine Notes

- ✅ Use `++` and `--` for adding or subtracting one.
- ✅ Learn the difference between prefix and postfix.
- ✅ Avoid tricky expressions involving multiple increments.
- ✅ Write clear, readable code.

---

## 📊 Increment & Decrement Summary

| Operator | Meaning |
|----------|---------|
| `++x` | Increment first, then use |
| `x++` | Use first, then increment |
| `--x` | Decrement first, then use |
| `x--` | Use first, then decrement |

---

## 🚀 Mastery Checklist

- [ ] I know what `++` does.
- [ ] I know what `--` does.
- [ ] I understand prefix increment.
- [ ] I understand postfix increment.
- [ ] I understand prefix decrement.
- [ ] I understand postfix decrement.
- [ ] I know when prefix and postfix behave differently.
- [ ] I avoid confusing expressions with multiple increments.

---

# ⚙️ Bitwise Operators

> "Bitwise operators manipulate individual bits of integer values."

🔴 Advanced Beginner

⏱ Estimated Study Time: ~1.5 Hours

---

# Introduction

Until now,

we have performed operations on entire numbers.

Example:

```c
5 + 3

10 > 2

x += 5
```

But computers do not truly think in decimal.

Internally,

everything is stored as bits.

Example:

```
5

↓

00000101
```

```
3

↓

00000011
```

Bitwise operators work directly on these binary digits.

---

# What is a Bit?

A bit is the smallest unit of data in a computer.

A bit can contain only:

```
0

or

1
```

Example:

```
13

↓

00001101
```

Each digit is one bit.

---

# Bitwise Operators

C provides six bitwise operators.

| Operator | Name |
|----------|------|
| `&` | Bitwise AND |
| `|` | Bitwise OR |
| `^` | Bitwise XOR |
| `~` | Bitwise NOT |
| `<<` | Left Shift |
| `>>` | Right Shift |

These operators work only on integer types.

---

# Bitwise AND (&)

Rule:

```
1 & 1

↓

1
```

Everything else becomes:

```
0
```

Truth Table:

| A | B | A & B |
|---|---|-------|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|

---

Example

```
5

↓

0101
```

```
3

↓

0011
```

Operation:

```
0101

0011

&

↓

0001
```

Result:

```
1
```

---

# Bitwise OR (|)

Rule:

If either bit is:

```
1
```

Result:

```
1
```

Truth Table:

| A | B | A \| B |
|---|---|---------|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

Example:

```
0101

0011

|

↓

0111
```

Result:

```
7
```

---

# Bitwise XOR (^)

Rule:

```
Different

↓

1
```

```
Same

↓

0
```

Truth Table:

| A | B | A ^ B |
|---|---|-------|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

Example:

```
0101

0011

^

↓

0110
```

Result:

```
6
```

---

# Bitwise NOT (~)

NOT flips every bit.

Example:

```
00001111
```

becomes

```
11110000
```

Example:

```c
~5
```

The exact decimal result depends on the integer representation (typically two's complement).

For beginners,

focus on understanding that every bit is inverted.

---

# Left Shift (<<)

Moves bits to the left.

Example:

```
00000101

↓

<<1

↓

00001010
```

Decimal:

```
5

↓

10
```

Each left shift by one position is often equivalent to multiplying by 2 (when overflow does not occur).

---

# Right Shift (>>)

Moves bits to the right.

Example:

```
00001010

↓

>>1

↓

00000101
```

Decimal:

```
10

↓

5
```

For positive integers,

each right shift by one position is often equivalent to dividing by 2 (discarding any remainder).

---

# Real-World Uses

Bit Flags

```c
permissions
```

Device Drivers

```c
hardware registers
```

Graphics Programming

```c
RGB colors
```

Networking

```c
protocol headers
```

Operating Systems

```c
CPU flags
```

Embedded Systems

```c
microcontrollers
```

---

# Bitwise vs Logical

These are completely different.

Logical AND:

```c
&&
```

Bitwise AND:

```c
&
```

Logical OR:

```c
||
```

Bitwise OR:

```c
|
```

Do not confuse them.

---

# Mental Model

Imagine eight light switches.

```
0

↓

OFF
```

```
1

↓

ON
```

Bitwise operators change individual switches,

not the whole room.

---

## 📚 Summary

Bitwise operators manipulate individual bits rather than whole numbers.

They are essential in systems programming,

embedded programming,

networking,

and operating systems.

Although they are less common in beginner programs,

understanding them provides a deeper understanding of how computers work.

---

## 🧠 Key Concepts

- Bit
- Binary
- Bitwise AND
- Bitwise OR
- XOR
- NOT
- Shift Operators

---

## ⚠ Common Mistakes

- Confusing `&` with `&&`.
- Confusing `|` with `||`.
- Assuming shifts always multiply or divide safely.
- Forgetting that bitwise operators work on bits, not decimal digits.

---

## 💡 Coach Tips

✔ Always convert small numbers to binary when learning bitwise operations.

✔ Draw the bits on paper.

✔ Learn the truth tables.

✔ Don't memorize examples—understand the rules.

---

## 🧩 Think Like the Computer

Convert to binary.

Then predict the result.

```c
5 & 3
```

---

```c
5 | 3
```

---

```c
5 ^ 3
```

---

```c
5 << 1
```

---

```c
10 >> 1
```

---

## 🏋️ Practice Exercises

1. Convert these numbers to binary.

```
3

5

8

12
```

---

2. Compute:

```c
5 & 1
```

---

```c
5 | 2
```

---

```c
5 ^ 1
```

---

3. Explain why:

```c
8 << 1
```

usually becomes:

```
16
```

---

4. Explain the difference between:

```c
&&

&
```

---

## 🎯 42 Piscine Notes

- ✅ Bitwise operators work only on integer types.
- ✅ Never confuse logical and bitwise operators.
- ✅ Learn binary first.
- ✅ Bitwise operations become very useful when studying memory, flags, and low-level programming.

---

## 📊 Bitwise Operators Summary

| Operator | Meaning |
|----------|---------|
| `&` | Bitwise AND |
| `|` | Bitwise OR |
| `^` | Bitwise XOR |
| `~` | Bitwise NOT |
| `<<` | Left Shift |
| `>>` | Right Shift |

---

## 🚀 Mastery Checklist

- [ ] I know every bitwise operator.
- [ ] I understand how AND, OR, XOR, and NOT work.
- [ ] I understand left and right shifts.
- [ ] I know the difference between logical and bitwise operators.
- [ ] I can solve simple binary operations by hand.

---

# ❓ Conditional (Ternary) Operator

> "The ternary operator chooses one of two values based on a condition."

🟡 Intermediate

⏱ Estimated Study Time: ~50 Minutes

---

# Introduction

Suppose we want to determine whether someone passed an exam.

Using `if` (which we'll study in Chapter 8), the idea would be:

```
If score is at least 50

↓

Passed

Otherwise

↓

Failed
```

C provides a shorter way to write simple decisions.

It is called the:

```
Conditional Operator

(Ternary Operator)
```

---

# Why is it Called "Ternary"?

Most operators use:

```
One Operand

or

Two Operands
```

Examples:

Unary

```c
++x
```

Binary

```c
x + y
```

The conditional operator uses:

```
Three Operands
```

That is why it is called:

```
Ternary
```

---

# Syntax

```c
condition ? value_if_true : value_if_false
```

General form:

```
Question ?

↓

Answer if True

↓

Answer if False
```

---

# First Example

```c
int age = 20;

char *result = (age >= 18) ? "Adult" : "Minor";
```

Meaning:

```
If

age >= 18

↓

Adult

Else

↓

Minor
```

---

# Another Example

```c
int max = (a > b) ? a : b;
```

Meaning:

```
If

a > b

↓

Choose a

Else

↓

Choose b
```

---

# Step-by-Step Execution

Example:

```c
int score = 80;

char *status = (score >= 50) ? "Pass" : "Fail";
```

Step 1

Evaluate:

```c
score >= 50
```

↓

```
True
```

Step 2

Choose:

```
"Pass"
```

Result:

```c
status

↓

"Pass"
```

---

# Comparison with if...else

Ternary:

```c
max = (a > b) ? a : b;
```

Equivalent `if` statement:

```c
if (a > b)
{
    max = a;
}
else
{
    max = b;
}
```

Both produce the same result.

The ternary operator is simply a shorter expression.

---

# Nested Ternary Operators

Example:

```c
result = (score >= 90)
    ? "Excellent"
    : (score >= 50)
        ? "Pass"
        : "Fail";
```

This is valid,

but it quickly becomes difficult to read.

---

# When Should You Use It?

Good use:

```c
max = (a > b) ? a : b;
```

Simple.

Easy to read.

---

Poor use:

```c
result =
(condition1)
? value1
: (condition2)
? value2
: (condition3)
? value3
: value4;
```

Although valid,

this is difficult to understand.

Prefer `if...else` for complex logic.

---

# Real-World Examples

Maximum Number

```c
max = (a > b) ? a : b;
```

Voting

```c
status = (age >= 18)
? "Allowed"
: "Not Allowed";
```

Discount

```c
price = is_student
? 50
: 100;
```

Temperature

```c
state =
(temp < 0)
? "Frozen"
: "Liquid";
```

---

# Mental Model

Imagine a fork in the road.

```
Condition

↓

True

↓

Left Road
```

```
Condition

↓

False

↓

Right Road
```

Only one road is chosen.

---

## 📚 Summary

The conditional operator evaluates a condition.

If the condition is true,

it returns one value.

Otherwise,

it returns another value.

It provides a compact alternative to simple `if...else` statements.

---

## 🧠 Key Concepts

- Conditional Operator
- Ternary Operator
- Condition
- True Expression
- False Expression

---

## ⚠ Common Mistakes

- Using the ternary operator for complicated logic.
- Forgetting that it returns a value.
- Omitting parentheses around complex conditions.
- Sacrificing readability to save a few lines.

---

## 💡 Coach Tips

✔ Use the ternary operator only for simple decisions.

✔ If an expression becomes difficult to read,

use `if...else` instead.

✔ Read it as a question:

```
Condition?

↓

Yes

↓

Value A

↓

No

↓

Value B
```

---

## 🧩 Think Like the Computer

Predict the result.

```c
int age = 16;

char *status =
(age >= 18)
? "Adult"
: "Minor";
```

---

Predict:

```c
int max =
(a > b)
? a
: b;
```

Which value is selected?

---

## 🏋️ Practice Exercises

1. Write a ternary operator that stores:

```
"Pass"

or

"Fail"
```

based on whether:

```c
score >= 50
```

---

2. Rewrite using the ternary operator.

```c
if (age >= 18)
{
    status = "Adult";
}
else
{
    status = "Minor";
}
```

---

3. Rewrite the following ternary operator using `if...else`.

```c
max = (a > b) ? a : b;
```

---

4. Explain why deeply nested ternary operators reduce readability.

---

## 🎯 42 Piscine Notes

- ✅ The ternary operator is the only ternary operator in C.
- ✅ It returns one of two values.
- ✅ Use it for simple decisions.
- ✅ Prefer `if...else` for complex logic.

---

## 📊 Conditional Operator Summary

| Syntax | Meaning |
|--------|---------|
| `condition ? A : B` | If condition is true, return A; otherwise return B |

---

## 🚀 Mastery Checklist

- [ ] I know the syntax of the ternary operator.
- [ ] I understand why it is called "ternary."
- [ ] I can rewrite a simple `if...else` using `?:`.
- [ ] I know when **not** to use the ternary operator.
- [ ] I understand that the ternary operator returns a value.

---

# 📊 Operator Precedence & Associativity

> "Operator precedence determines which operator is evaluated first. Associativity determines the evaluation direction when operators have the same precedence."

🟡 Intermediate

⏱ Estimated Study Time: ~45 Minutes

---

# Introduction

Suppose you write:

```c
2 + 3 * 4
```

Should the computer calculate:

```
2 + 3

↓

5

↓

5 × 4

↓

20
```

or:

```
3 × 4

↓

12

↓

2 + 12

↓

14
```

The answer is determined by:

```
Operator Precedence
```

---

# What is Operator Precedence?

Operator precedence determines which operator is evaluated first.

Different operators have different priorities.

Higher-precedence operators are evaluated before lower-precedence operators.

---

# Simple Example

```c
2 + 3 * 4
```

Evaluation:

```
3 * 4

↓

12

↓

2 + 12

↓

14
```

Multiplication has higher precedence than addition.

---

# Parentheses Have Highest Priority

Example:

```c
(2 + 3) * 4
```

Evaluation:

```
2 + 3

↓

5

↓

5 × 4

↓

20
```

Parentheses override the normal precedence rules.

---

# What is Associativity?

Sometimes two operators have the same precedence.

Example:

```c
20 - 5 - 3
```

Should the compiler evaluate:

```
20 - 5

↓

15

↓

15 - 3

↓

12
```

or:

```
5 - 3

↓

2

↓

20 - 2

↓

18
```

The answer depends on:

```
Associativity
```

---

# Left-to-Right Associativity

Most arithmetic operators are evaluated from left to right.

Example:

```c
20 - 5 - 3
```

Evaluation:

```
20 - 5

↓

15

↓

15 - 3

↓

12
```

---

Another example:

```c
100 / 5 / 2
```

Evaluation:

```
100 / 5

↓

20

↓

20 / 2

↓

10
```

---

# Right-to-Left Associativity

Assignment operators are evaluated from right to left.

Example:

```c
a = b = c = 5;
```

Evaluation:

```
c = 5

↓

Returns 5

↓

b = 5

↓

Returns 5

↓

a = 5
```

Final values:

```
a = 5

b = 5

c = 5
```

---

# Typical Operator Precedence

From highest to lowest:

| Level | Operators |
|-------:|-----------|
| 1 | `()` |
| 2 | `++` `--` (prefix), `!`, `~`, unary `+`, unary `-`, `(type)` |
| 3 | `*` `/` `%` |
| 4 | `+` `-` |
| 5 | `<<` `>>` |
| 6 | `<` `<=` `>` `>=` |
| 7 | `==` `!=` |
| 8 | `&` |
| 9 | `^` |
| 10 | `|` |
| 11 | `&&` |
| 12 | `||` |
| 13 | `?:` |
| 14 | `=` `+=` `-=` `*=` `/=` `%=` |

You do **not** need to memorize every level.

Learn the most common ones first.

---

# Most Important Rules

Remember these:

```
()

↓

Highest Priority
```

↓

```
Unary Operators

++, --, !
```

↓

```
* / %
```

↓

```
+ -
```

↓

```
Comparisons
```

↓

```
&&
```

↓

```
||
```

↓

```
Assignment
```

These are the operators you'll use most often.

---

# Real Examples

Example 1

```c
2 + 3 * 4
```

↓

```
14
```

---

Example 2

```c
(2 + 3) * 4
```

↓

```
20
```

---

Example 3

```c
5 > 2 && 8 > 3
```

Evaluation:

```
5 > 2

↓

1

8 > 3

↓

1

1 && 1

↓

1
```

---

Example 4

```c
5 > 8 || 10 > 2
```

Evaluation:

```
0 || 1

↓

1
```

---

# Should I Memorize Everything?

No.

Professional programmers rely on:

```
Parentheses
```

instead of memorizing every precedence level.

Example:

Instead of:

```c
a + b * c
```

write:

```c
a + (b * c)
```

Even if unnecessary,

it improves readability.

---

# Mental Model

Imagine a line of people waiting.

The VIPs go first.

```
()

↓

VIP
```

```
*

↓

Before
```

```
+

↓

After
```

Operator precedence simply decides who goes first.

---

## 📚 Summary

Operator precedence determines the order of evaluation.

Associativity determines the direction of evaluation when operators have equal precedence.

Parentheses are the safest way to make expressions clear.

---

## 🧠 Key Concepts

- Precedence
- Associativity
- Left-to-Right
- Right-to-Left
- Parentheses

---

## ⚠ Common Mistakes

- Ignoring operator precedence.
- Writing complex expressions without parentheses.
- Confusing precedence with associativity.
- Assuming expressions are always evaluated left to right.

---

## 💡 Coach Tips

✔ Learn the common precedence rules.

✔ Use parentheses whenever an expression may be confusing.

✔ Read expressions one operation at a time.

✔ Clear code is better than clever code.

---

## 🧩 Think Like the Computer

Predict the result.

```c
2 + 3 * 4
```

---

```c
(2 + 3) * 4
```

---

```c
10 > 5 && 3 < 2
```

---

```c
a = b = 7;
```

Explain the evaluation order.

---

## 🏋️ Practice Exercises

1. Predict the result.

```c
8 + 4 * 2
```

---

2. Rewrite using parentheses.

```c
a + b * c
```

---

3. Explain why:

```c
a = b = 5;
```

works.

---

4. What is the difference between:

```
Precedence

and

Associativity?
```

---

## 🎯 42 Piscine Notes

- ✅ Parentheses improve readability.
- ✅ Multiplication has higher precedence than addition.
- ✅ Assignment is evaluated right to left.
- ✅ Don't try to memorize the entire precedence table.

---

## 📊 Quick Reference

| Rule | Remember |
|------|----------|
| `()` | Highest Priority |
| `* / %` | Before `+ -` |
| Comparisons | Before `&&` |
| `&&` | Before `||` |
| Assignment | Last |

---

## 🚀 Mastery Checklist

- [ ] I know what operator precedence is.
- [ ] I know what associativity is.
- [ ] I understand left-to-right evaluation.
- [ ] I understand right-to-left assignment.
- [ ] I use parentheses to improve readability.

---

# 🧾 Chapter 7 Cheat Sheet

> **Chapter 7 — Operators**
>
> A quick reference for every operator covered in this chapter.

---

# ➕ Arithmetic Operators

| Operator | Meaning | Example | Result |
|----------|---------|----------|--------|
| `+` | Addition | `5 + 2` | `7` |
| `-` | Subtraction | `5 - 2` | `3` |
| `*` | Multiplication | `5 * 2` | `10` |
| `/` | Division | `5 / 2` | `2` *(integer division)* |
| `%` | Modulus (Remainder) | `5 % 2` | `1` |

Remember:

```
7 / 2

↓

3
```

```
7.0 / 2.0

↓

3.5
```

---

# 📝 Assignment Operators

| Operator | Equivalent |
|----------|------------|
| `=` | Assignment |
| `+=` | `x = x + y` |
| `-=` | `x = x - y` |
| `*=` | `x = x * y` |
| `/=` | `x = x / y` |
| `%=` | `x = x % y` |

Example:

```c
score += 10;
```

instead of

```c
score = score + 10;
```

---

# ⚖️ Comparison Operators

| Operator | Meaning |
|----------|---------|
| `==` | Equal |
| `!=` | Not Equal |
| `>` | Greater Than |
| `<` | Less Than |
| `>=` | Greater Than or Equal |
| `<=` | Less Than or Equal |

Remember:

```
True

↓

1
```

```
False

↓

0
```

---

# 🔗 Logical Operators

| Operator | Meaning |
|----------|---------|
| `&&` | AND |
| `\|\|` | OR |
| `!` | NOT |

Examples:

```c
age >= 18 && has_id
```

```c
is_admin || is_owner
```

```c
!game_over
```

---

# 🧩 Building Complex Conditions

Examples:

```c
(age >= 18) && has_license
```

```c
(score >= 50) || teacher_permission
```

```c
(age >= 18) && ((score >= 50) || special_permission)
```

✔ Prefer parentheses for readability.

# 🔄 Increment & Decrement

| Operator | Meaning |
|----------|---------|
| `++x` | Increment first, then use |
| `x++` | Use first, then increment |
| `--x` | Decrement first, then use |
| `x--` | Use first, then decrement |

When used alone:

```c
++x;
```

and

```c
x++;
```

produce the same final value.

---

# ⚙️ Bitwise Operators

| Operator | Meaning |
|----------|---------|
| `&` | Bitwise AND |
| `\|` | Bitwise OR |
| `^` | Bitwise XOR |
| `~` | Bitwise NOT |
| `<<` | Left Shift |
| `>>` | Right Shift |

Remember:

```
Logical

&& ||

↓

Conditions
```

```
Bitwise

& |

↓

Bits
```

---

# ❓ Conditional (Ternary) Operator

Syntax:

```c
condition ? value_if_true : value_if_false
```

Example:

```c
max = (a > b) ? a : b;
```

Equivalent to:

```c
if (a > b)
    max = a;
else
    max = b;
```

---

# 📊 Operator Precedence

Most important order:

```text
()

↓

Highest

↓

Unary

++, --, !

↓

* / %

↓

+ -

↓

< <= > >=

↓

== !=

↓

&&

↓

||

↓

=

↓

Lowest
```

---

# 📌 Common Mistakes

❌ Using:

```c
=
```

instead of

```c
==
```

---

❌ Expecting:

```c
7 / 2
```

to produce

```
3.5
```

---

❌ Confusing:

```c
&&
```

with

```c
&
```

---

❌ Confusing:

```c
||
```

with

```c
|
```

---

❌ Writing:

```c
x = x++;
```

---

❌ Forgetting operator precedence.

---

# 💡 Professional Tips

✔ Prefer readable expressions.

✔ Use parentheses to make intent clear.

✔ Don't rely on remembering every precedence rule.

✔ Avoid clever one-line expressions.

✔ Keep conditions simple whenever possible.

✔ Learn the meaning before memorizing symbols.

---

# 🏆 Chapter 7 Mastery Checklist

## Arithmetic

- [ ] I know every arithmetic operator.
- [ ] I understand integer division.
- [ ] I know how `%` works.

---

## Assignment

- [ ] I know every compound assignment operator.
- [ ] I know the difference between `=` and `==`.

---

## Comparison

- [ ] I know all comparison operators.
- [ ] I understand that comparisons return `1` or `0`.

---

## Logical

- [ ] I understand `&&`.
- [ ] I understand `||`.
- [ ] I understand `!`.
- [ ] I know how to build complex conditions.

---

## Increment & Decrement

- [ ] I know the difference between prefix and postfix.
- [ ] I know when they behave differently.

---

## Bitwise

- [ ] I know every bitwise operator.
- [ ] I understand the difference between logical and bitwise operators.

---

## Conditional Operator

- [ ] I can write simple ternary expressions.
- [ ] I know when to prefer `if...else`.

---

## Operator Precedence

- [ ] I know the most common precedence rules.
- [ ] I use parentheses to improve readability.

---

# 🎉 End of Chapter 7

Congratulations!

You have completed the entire **Operators** chapter.

You now understand:

- ✔ Arithmetic Operators
- ✔ Assignment Operators
- ✔ Comparison Operators
- ✔ Logical Operators
- ✔ Complex Conditions
- ✔ Increment & Decrement
- ✔ Bitwise Operators
- ✔ Conditional (Ternary) Operator
- ✔ Operator Precedence & Associativity

These operators are the foundation of nearly every C program.

---

# 🚀 What's Next?

The next chapter is:

# 🔀 Chapter 8 — Control Flow

Control flow statements let a program make decisions and repeat work instead of executing every line once, top to bottom. Everything from here on builds directly on this chapter.

---

## if

The `if` statement runs a block of code only when a condition is true.

```c
if (condition)
{
    /* runs only if condition is true (non-zero) */
}
```

Example:

```c
int age = 20;

if (age >= 18)
{
    printf("Adult\n");
}
```

Remember: in C, any non-zero value is treated as **true**, and `0` is treated as **false**. There is no dedicated boolean type unless you `#include <stdbool.h>` (C99+).

```c
if (5)          // true, always runs
if (0)          // false, never runs
if (age - 18)   // true unless age is exactly 18
```

### Common Mistake — `=` vs `==`

```c
if (age = 18)   // ❌ assigns 18 to age, always true
if (age == 18)  // ✅ compares age to 18
```

This is one of the most common bugs in beginner C code. Some compilers warn about it (`-Wall` will catch this) — always compile with warnings enabled.

---

## else

`else` runs when the `if` condition is false.

```c
if (age >= 18)
{
    printf("Adult\n");
}
else
{
    printf("Minor\n");
}
```

### else if

Chain multiple conditions with `else if`. They are checked in order, top to bottom, and only the first true branch executes.

```c
if (score >= 90)
{
    printf("A\n");
}
else if (score >= 80)
{
    printf("B\n");
}
else if (score >= 70)
{
    printf("C\n");
}
else
{
    printf("F\n");
}
```

Order matters. If you checked `score >= 70` first, a score of 95 would incorrectly print `C`.

### Dangling else

```c
if (a > 0)
    if (b > 0)
        printf("both positive\n");
    else
        printf("a positive, b not\n");
```

The `else` always binds to the **nearest unmatched `if`** — here, the inner one, even though indentation might suggest otherwise. Always use braces `{}` to remove ambiguity, especially in nested conditions.

---

## switch

`switch` compares one value against several possible constant cases. It's often cleaner than a long `else if` chain when checking a single variable against many exact values.

```c
switch (expression)
{
    case value1:
        /* code */
        break;
    case value2:
        /* code */
        break;
    default:
        /* code */
}
```

Example:

```c
int day = 3;

switch (day)
{
    case 1:
        printf("Monday\n");
        break;
    case 2:
        printf("Tuesday\n");
        break;
    case 3:
        printf("Wednesday\n");
        break;
    default:
        printf("Unknown day\n");
}
```

Output:

```
Wednesday
```

### Fall-Through

Without `break`, execution continues into the next case — this is called **fall-through**, and it's a frequent source of bugs.

```c
switch (day)
{
    case 1:
        printf("Monday\n");
    case 2:
        printf("Tuesday\n");
        break;
}
```

If `day == 1`, this prints **both** `Monday` and `Tuesday`, because there's no `break` after case 1.

Fall-through is sometimes used intentionally to group cases:

```c
switch (grade)
{
    case 'A':
    case 'B':
    case 'C':
        printf("Passed\n");
        break;
    case 'D':
    case 'F':
        printf("Failed\n");
        break;
}
```

### switch Rules

- The expression must evaluate to an integer type (`int`, `char`, `enum`...) — not `float`, `double`, or strings.
- `case` labels must be **constant expressions**, known at compile time.
- `default` is optional but should almost always be included.
- `break` is not mandatory but its absence must be intentional.

> 📌 **42 Norm note:** `switch` and `case` are both on the Norm's forbidden list (Chapter 18) — at 42/1337 you'll rewrite this kind of logic as an `if`/`else if` chain instead.

---

## while

`while` repeats a block **as long as** its condition is true. The condition is checked **before** each iteration — so the loop body may run zero times.

```c
while (condition)
{
    /* repeats while condition is true */
}
```

Example:

```c
int i = 0;

while (i < 5)
{
    printf("%d\n", i);
    i++;
}
```

Output:

```
0
1
2
3
4
```

### Infinite Loops

```c
while (1)
{
    /* runs forever unless broken out of */
}
```

Common when the exit condition depends on something inside the loop body (like user input or a `break`).

### Common Mistake — Forgetting to Update the Condition

```c
int i = 0;

while (i < 5)
{
    printf("%d\n", i);
    /* forgot i++ — infinite loop */
}
```

Always make sure something inside the loop moves the condition toward becoming false.

---

## do while

`do while` is like `while`, except the condition is checked **after** the loop body runs. This guarantees the body executes **at least once**.

```c
do
{
    /* runs at least once */
} while (condition);
```

Example:

```c
int i = 0;

do
{
    printf("%d\n", i);
    i++;
} while (i < 5);
```

Output is identical to the `while` example above, but the key difference shows when the condition starts false:

```c
int i = 10;

while (i < 5)
{
    printf("%d\n", i);   // never runs
}

do
{
    printf("%d\n", i);   // runs once, prints 10
} while (i < 5);
```

`do while` is most useful for menus and input validation, where you need to show something or ask for input at least once before checking whether to repeat.

⚠️ Don't forget the semicolon after `while (condition);` in a `do while` — it's easy to omit and the compiler error can be confusing.

> 📌 **42 Norm note:** `do...while` is on the Norm's forbidden list (Chapter 18 covers this in full) — know it well for general C, but don't use it in Norm-checked code.

---

## for

`for` combines initialization, condition, and increment into a single line. It's the standard choice when the number of iterations is known or countable.

```c
for (initialization; condition; increment)
{
    /* repeats while condition is true */
}
```

Example:

```c
for (int i = 0; i < 5; i++)
{
    printf("%d\n", i);
}
```

Execution order:

```
initialization (once)
    ↓
condition check
    ↓
body runs
    ↓
increment
    ↓
condition check
    ↓
... repeats until condition is false
```

### Any Part Can Be Omitted

```c
int i = 0;

for (; i < 5; i++)      // no initialization
for (int i = 0; ; i++)  // no condition — infinite unless broken
for (int i = 0; i < 5;) // no increment — must update i inside body
for (;;)                // all omitted — infinite loop
```

### Multiple Variables

```c
for (int i = 0, j = 10; i < j; i++, j--)
{
    printf("%d %d\n", i, j);
}
```

### while vs for

Use `for` when you know how many times to loop (counting, array traversal). Use `while` when the stopping condition depends on something checked dynamically (waiting for input, searching until found).

> 📌 **42 Norm note:** `for` is on the Norm's forbidden list (Chapter 18) — at 42/1337 every loop, counted or not, is written with `while`. The syntax above is standard C and essential to know, but you won't be able to write it in Norm-checked code.

---

## break

`break` immediately exits the nearest enclosing loop or `switch`, skipping any remaining iterations.

```c
for (int i = 0; i < 10; i++)
{
    if (i == 5)
        break;
    printf("%d\n", i);
}
```

Output:

```
0
1
2
3
4
```

`break` only exits **one** level. In nested loops, it only breaks the innermost loop.

```c
for (int i = 0; i < 3; i++)
{
    for (int j = 0; j < 3; j++)
    {
        if (j == 1)
            break;   // only exits the inner loop
        printf("%d %d\n", i, j);
    }
}
```

---

## continue

`continue` skips the rest of the current iteration and jumps straight to the next one (the condition check in `while`/`do while`, or the increment step in `for`).

```c
for (int i = 0; i < 5; i++)
{
    if (i == 2)
        continue;
    printf("%d\n", i);
}
```

Output:

```
0
1
3
4
```

Notice `2` is skipped, but the loop continues instead of stopping.

⚠️ Inside a `while` loop, make sure the update happens **before** `continue`, or you'll create an infinite loop:

```c
int i = 0;

while (i < 5)
{
    if (i == 2)
    {
        i++;
        continue;   // safe — i was already updated
    }
    printf("%d\n", i);
    i++;
}
```

---

## goto (theory only)

`goto` jumps directly to a labeled statement anywhere in the same function.

```c
goto label;

...

label:
    /* code */
```

Example:

```c
int i = 0;

start:
if (i < 5)
{
    printf("%d\n", i);
    i++;
    goto start;
}
```

### Why goto Is Rarely Used

`goto` can jump anywhere, which makes code harder to read, harder to trace, and easy to misuse — creating what's sometimes called "spaghetti code." Every use case for `goto` can normally be rewritten with `if`, `while`, `for`, `break`, or `continue`.

One legitimate, commonly accepted use is centralized cleanup on error paths in C (common in kernel and systems code):

```c
int process(void)
{
    char *buf1 = malloc(100);
    if (!buf1)
        goto error;

    char *buf2 = malloc(100);
    if (!buf2)
        goto cleanup_buf1;

    /* ... use buf1 and buf2 ... */

    free(buf2);
cleanup_buf1:
    free(buf1);
error:
    return (-1);
}
```

At 42/1337, `goto` is almost always **forbidden by the Norm**. Know it exists and understand it when you see it — but don't reach for it in your own code.

---

## 🧾 Chapter 8 Cheat Sheet

| Statement | Purpose | Runs body at least once? |
|---|---|---|
| `if` / `else` | Conditional branching | — |
| `switch` | Multi-way branch on one value | — |
| `while` | Loop while condition is true | ❌ |
| `do while` | Loop while condition is true | ✅ |
| `for` | Counted / structured loop | ❌ |
| `break` | Exit nearest loop/switch | — |
| `continue` | Skip to next iteration | — |
| `goto` | Unconditional jump (avoid) | — |

### Common Mistakes
- Using `=` instead of `==` in a condition.
- Forgetting `break` in a `switch`, causing fall-through.
- Writing an infinite loop by forgetting to update the loop variable.
- Assuming `break` exits all nested loops (it only exits one).
- Forgetting the semicolon after `do { } while(condition);`.

### 🎯 42 Piscine Notes
✅ Always compile with `-Wall -Wextra -Werror`.
✅ Use braces `{}` even for single-line bodies — it's safer and matches the Norm.
✅ Prefer `for` for counted loops, `while` for condition-driven loops.
✅ Avoid `goto` — it's forbidden by the 42 Norm in almost all cases.

### 🚀 Mastery Checklist
- [ ] I understand how `if`/`else`/`else if` chains evaluate.
- [ ] I know how `switch` and fall-through work.
- [ ] I understand the difference between `while` and `do while`.
- [ ] I can write a `for` loop with any part omitted.
- [ ] I know the difference between `break` and `continue`.
- [ ] I understand why `goto` is discouraged.


---

# Part V — Functions

# 🔧 Chapter 9 — Functions

A function is a named, reusable block of code that performs a specific task. Functions let you break a program into smaller, testable, reusable pieces instead of writing everything inside `main()`.

---

## Function Declaration (Prototype)

A declaration — also called a **prototype** — tells the compiler a function exists, what it returns, and what parameters it takes, without providing the implementation yet.

```c
int add(int a, int b);
```

Declarations are usually placed in header files (`.h`) so multiple `.c` files can use the same function.

```c
/* math_utils.h */
int add(int a, int b);
int subtract(int a, int b);
```

Without a prototype visible before a function is called, older compilers may assume incorrect argument types — always declare before use.

---

## Definition

The definition contains the actual body — the code that runs when the function is called.

```c
int add(int a, int b)
{
    return (a + b);
}
```

A definition **is** a declaration too (it includes the same information), but a declaration is not always a definition.

```c
int add(int a, int b);        // declaration only

int add(int a, int b)         // definition
{
    return (a + b);
}
```

---

## Parameters

Parameters are the variables listed in a function's definition. **Arguments** are the actual values passed when the function is called.

```c
int add(int a, int b)   // a and b are parameters
{
    return (a + b);
}

int result = add(5, 3); // 5 and 3 are arguments
```

### Pass by Value

C passes arguments **by value** — the function receives a *copy*, not the original variable.

```c
void increment(int x)
{
    x++;   // modifies the copy only
}

int main(void)
{
    int number = 5;
    increment(number);
    printf("%d\n", number);   // still 5
    return (0);
}
```

To actually modify the caller's variable, you must pass its **address** (a pointer) — covered in Chapter 12.

```c
void increment(int *x)
{
    (*x)++;   // modifies the original
}

increment(&number);   // now number becomes 6
```

### void Parameters

A function that takes no parameters should be declared with `void`, not empty parentheses (which in old-style C means "unspecified arguments").

```c
int get_random(void);   // ✅ explicit: takes no arguments
int get_random();       // ⚠️ ambiguous in old C — avoid
```

---

## Return Values

`return` sends a value back to the caller and immediately ends the function.

```c
int square(int n)
{
    return (n * n);
}
```

A function that returns nothing uses `void`:

```c
void greet(void)
{
    printf("Hello\n");
    return;   // optional here
}
```

⚠️ A non-`void` function that doesn't return a value on every path produces **undefined behavior** if the caller uses the result.

```c
int check(int x)
{
    if (x > 0)
        return (1);
    /* missing return for x <= 0 — bug */
}
```

A function can only return **one** value directly. To "return" multiple values, use pointers (output parameters) or a `struct` (Chapter 13).

---

## Scope

Scope determines where a variable or function name is visible and usable.

### Local Scope

Variables declared inside a function exist only within that function (technically, within the block `{ }` where they're declared).

```c
void foo(void)
{
    int x = 5;   // local to foo
}

void bar(void)
{
    printf("%d\n", x);   // ❌ error — x doesn't exist here
}
```

### Block Scope

Variables declared inside `{ }` (including inside `if`, `for`, `while`) are only visible inside that block.

```c
if (condition)
{
    int y = 10;   // only visible inside this if-block
}
printf("%d\n", y);   // ❌ error
```

### Global Scope

Variables declared outside every function are visible to the whole file (and other files, if declared `extern`).

```c
int counter = 0;   // global

void increment(void)
{
    counter++;   // accessible here
}
```

Global variables are convenient but make code harder to reason about and test — use them sparingly.

---

## Storage Duration

Storage duration determines **how long** a variable's memory exists, independent of scope.

| Duration | Keyword | Lives... |
|---|---|---|
| Automatic | (default for locals) | Only while the enclosing block executes (Stack) |
| Static | `static` | Entire program run, but scope stays local |
| Static/Global | (default for globals) | Entire program run |

### static Local Variables

A `static` local variable keeps its value between function calls — it is not re-initialized every time.

```c
void counter(void)
{
    static int count = 0;   // initialized only once

    count++;
    printf("%d\n", count);
}

int main(void)
{
    counter();   // prints 1
    counter();   // prints 2
    counter();   // prints 3
    return (0);
}
```

Without `static`, `count` would reset to `0` on every call and always print `1`.

`static` variables live in the Data/BSS segment (from Chapter 4), not the Stack — that's why they persist.

---

## Recursion

A function that calls itself is called **recursive**. Every recursive function needs a **base case** (a condition that stops the recursion) or it will recurse forever, eventually causing a **stack overflow**.

```c
int factorial(int n)
{
    if (n <= 1)          // base case
        return (1);
    return (n * factorial(n - 1));   // recursive case
}
```

Trace for `factorial(4)`:

```
factorial(4)
= 4 * factorial(3)
= 4 * (3 * factorial(2))
= 4 * (3 * (2 * factorial(1)))
= 4 * (3 * (2 * 1))
= 24
```

Each recursive call creates a new **stack frame** (from Chapter 4). Deep recursion without a base case, or with a base case that's never reached, exhausts the Stack.

```c
int broken(int n)
{
    return (broken(n));   // no base case — stack overflow
}
```

### Recursion vs Iteration

Anything recursive can be rewritten iteratively (with a loop), and vice versa. Recursion is often more elegant for tree-like or divide-and-conquer problems; iteration is usually more memory-efficient since it doesn't grow the Stack.

---

## 🧾 Chapter 9 Cheat Sheet

| Concept | Meaning |
|---|---|
| Declaration | Tells the compiler the function exists |
| Definition | Contains the function's actual code |
| Parameter | Variable in the function definition |
| Argument | Actual value passed at the call site |
| Pass by value | Function receives a copy, not the original |
| Scope | Where a name is visible |
| Storage duration | How long a variable's memory persists |
| Recursion | A function calling itself, with a base case |

### Common Mistakes
- Forgetting a prototype before using a function defined later in the file.
- Expecting a function to modify a caller's variable without using a pointer.
- Missing a `return` on some code path in a non-`void` function.
- Writing recursion without a base case.
- Confusing scope (visibility) with storage duration (lifetime).

### 🎯 42 Piscine Notes
✅ Every `.c` file should have a matching `.h` with prototypes.
✅ Use `void` explicitly for functions with no parameters.
✅ 42 Norm limits functions to 25 lines and 4 parameters — write small, focused functions.
✅ Recursion is common in Piscine exercises (e.g. `ft_recursive_power`) — always identify the base case first.

### 🚀 Mastery Checklist
- [ ] I know the difference between declaration and definition.
- [ ] I understand pass-by-value and why it doesn't modify the caller's variable.
- [ ] I understand local, block, and global scope.
- [ ] I understand the difference between automatic and static storage duration.
- [ ] I can write a recursive function with a correct base case.


---

# Part VI — Arrays & Strings

# 📚 Chapter 10 — Arrays

An array is a fixed-size collection of elements of the **same type**, stored in **contiguous memory** (back-to-back, no gaps).

---

## One-dimensional Arrays

### Declaration

```c
int numbers[5];
```

This reserves space for 5 consecutive `int` values. Memory:

```
numbers[0]  numbers[1]  numbers[2]  numbers[3]  numbers[4]
   ↓            ↓            ↓            ↓            ↓
 4 bytes      4 bytes      4 bytes      4 bytes      4 bytes
```

Total size: `5 * sizeof(int)` — typically 20 bytes.

### Initialization

```c
int numbers[5] = {10, 20, 30, 40, 50};

int numbers[] = {10, 20, 30};       // size inferred: 3

int numbers[5] = {1, 2};            // remaining elements = 0
                                     // → {1, 2, 0, 0, 0}

int numbers[5] = {0};               // all elements = 0
```

### Accessing Elements

Arrays are **zero-indexed** — the first element is at index `0`, the last at `size - 1`.

```c
int numbers[5] = {10, 20, 30, 40, 50};

printf("%d\n", numbers[0]);   // 10
printf("%d\n", numbers[4]);   // 50
```

### Modifying Elements

```c
numbers[2] = 99;
```

### ⚠️ Out-of-Bounds Access

```c
int numbers[5];
numbers[5] = 100;   // ❌ undefined behavior — index 5 doesn't exist
                     //    (valid indices are 0–4)
```

C does **not** check array bounds. Writing outside the array corrupts adjacent memory — this is one of the most dangerous and common bugs in C, and the root cause of many buffer overflow vulnerabilities.

---

## Multi-dimensional Arrays

A 2D array is essentially an array of arrays — commonly used to represent grids, tables, and matrices.

```c
int grid[3][4];   // 3 rows, 4 columns
```

### Initialization

```c
int grid[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

### Accessing Elements

```c
printf("%d\n", grid[0][2]);   // 3
printf("%d\n", grid[1][0]);   // 4
```

### Memory Layout

Despite looking like a grid, a 2D array is stored as one continuous block in memory, **row by row** (this is called **row-major order**):

```
grid[0][0] grid[0][1] grid[0][2] grid[1][0] grid[1][1] grid[1][2]
```

---

## Array Traversal

The most common way to process every element of an array is a `for` loop paired with `sizeof`.

```c
int numbers[5] = {10, 20, 30, 40, 50};
int size = sizeof(numbers) / sizeof(numbers[0]);

for (int i = 0; i < size; i++)
{
    printf("%d\n", numbers[i]);
}
```

`sizeof(numbers) / sizeof(numbers[0])` gives the number of elements — total bytes divided by one element's size. This only works on the actual array, not a pointer to it (see Chapter 12).

### 2D Traversal

```c
for (int i = 0; i < 2; i++)
{
    for (int j = 0; j < 3; j++)
    {
        printf("%d ", grid[i][j]);
    }
    printf("\n");
}
```

### Arrays and Functions

When an array is passed to a function, it **decays into a pointer** to its first element — the function does not receive a copy of the whole array, and `sizeof` inside that function will not give the array's size.

```c
void print_array(int arr[], int size)   // arr is really a pointer here
{
    for (int i = 0; i < size; i++)
        printf("%d\n", arr[i]);
}
```

This is why array functions almost always take an explicit `size` parameter — the function has no way to know the array's length on its own.

---

## 🧾 Chapter 10 Cheat Sheet

| Concept | Key Fact |
|---|---|
| Indexing | Starts at `0`, ends at `size - 1` |
| Memory | Elements are contiguous |
| Bounds checking | None — out-of-bounds access is undefined behavior |
| 2D arrays | Stored row-major, one continuous block |
| Arrays in functions | Decay to a pointer — size must be passed separately |

### Common Mistakes
- Off-by-one errors (`numbers[5]` on a 5-element array).
- Forgetting arrays are zero-indexed.
- Assuming `sizeof` works on an array parameter inside a function.
- Leaving uninitialized elements and assuming they're zero (only guaranteed with partial `{}` initialization).

### 🎯 42 Piscine Notes
✅ Always pass array size explicitly to functions.
✅ Double-check loop bounds (`i < size`, not `i <= size`).
✅ Practice both 1D and 2D traversal — matrix exercises are common in the Piscine.

### 🚀 Mastery Checklist
- [ ] I understand zero-indexing.
- [ ] I know arrays are stored contiguously in memory.
- [ ] I understand why out-of-bounds access is dangerous.
- [ ] I can traverse 1D and 2D arrays with `for` loops.
- [ ] I know why array size must be passed explicitly to functions.

---

# 🔤 Chapter 11 — Strings

C has no built-in string type. A string in C is simply a `char` array that ends with a special marker: the **null terminator**.

---

## Character Arrays

A string is stored as consecutive characters in a `char` array.

```c
char word[6] = {'H', 'e', 'l', 'l', 'o', '\0'};
```

Memory:

```
word[0]  word[1]  word[2]  word[3]  word[4]  word[5]
  H        e        l        l        o       \0
```

---

## String Literals

Writing a string in double quotes automatically creates a `char` array **and appends the null terminator for you**.

```c
char word[] = "Hello";
```

This is equivalent to the character array above — `"Hello"` becomes 6 bytes: `H`, `e`, `l`, `l`, `o`, `\0`.

```c
char word[6] = "Hello";   // exactly fits
char word[10] = "Hello";  // remaining bytes are unused
char word[3] = "Hello";   // ❌ error — not enough room for "Hello\0"
```

String literals used directly (not stored in an array) are typically stored in read-only memory:

```c
char *greeting = "Hello";
greeting[0] = 'h';   // ❌ undefined behavior — modifying a string literal
```

---

## Null Terminator

The null terminator `'\0'` (ASCII value `0`) marks the **end** of a string. Every C string function relies on it to know where the string stops.

```c
char word[] = "Hi";
```

Memory:

```
word[0] = 'H'
word[1] = 'i'
word[2] = '\0'
```

Without the null terminator, functions like `printf("%s", ...)` or `strlen()` would keep reading past the array into unrelated memory — undefined behavior.

### Finding String Length

```c
int my_strlen(char *str)
{
    int len = 0;

    while (str[len] != '\0')
        len++;
    return (len);
}
```

This is essentially what the standard `strlen()` function does.

---

## Common Mistakes

### Forgetting the Null Terminator (Manual Arrays)

```c
char word[5] = {'H', 'e', 'l', 'l', 'o'};   // ❌ no room for '\0'
printf("%s\n", word);                        // undefined behavior
```

### Confusing Character and String

```c
'A'    // a single character (1 byte, no null terminator)
"A"    // a string: 'A' + '\0' (2 bytes)
```

### Buffer Too Small

```c
char name[3];
strcpy(name, "Abdullah");   // ❌ overflows — "Abdullah" needs 9 bytes
```

This is a **buffer overflow** — one of the most common and dangerous bugs in C, and a classic source of security vulnerabilities.

### Comparing Strings with `==`

```c
char *a = "Hello";
char *b = "Hello";

if (a == b)   // ❌ compares addresses/pointers, not content
```

Use `strcmp()` instead:

```c
if (strcmp(a, b) == 0)   // ✅ compares actual content
```

`strcmp` returns `0` when the strings are equal — not `1` as many beginners expect.

---

## String Manipulation

Common functions from `<string.h>`:

| Function | Purpose |
|---|---|
| `strlen(s)` | Returns the length (not counting `'\0'`) |
| `strcpy(dst, src)` | Copies `src` into `dst` |
| `strcat(dst, src)` | Appends `src` to the end of `dst` |
| `strcmp(a, b)` | Compares two strings (`0` = equal) |
| `strncpy`, `strncat`, `strncmp` | Safer, bounded versions (limit by length) |

Example:

```c
char full[50] = "Hello, ";

strcat(full, "world!");
printf("%s\n", full);
```

Output:

```
Hello, world!
```

⚠️ `strcpy` and `strcat` do not check destination size — always make sure the destination buffer is large enough, or prefer the `n`-bounded variants (`strncpy`, `strncat`).

At 42/1337, you'll implement your own versions of these (`ft_strlen`, `ft_strcpy`, `ft_strcmp`...) as part of **libft** — understanding exactly how the null terminator drives every one of these functions is essential.

---

## 🧾 Chapter 11 Cheat Sheet

| Concept | Key Fact |
|---|---|
| String | A `char` array ending in `'\0'` |
| String literal | Auto-adds `'\0'`, often stored read-only |
| `strlen` | Counts characters up to (not including) `'\0'` |
| `strcmp` | Returns `0` when strings are equal |
| Buffer overflow | Writing past the destination array's capacity |

### Common Mistakes
- Forgetting the null terminator in manually built char arrays.
- Confusing `'A'` (char) with `"A"` (string).
- Comparing strings with `==` instead of `strcmp`.
- Copying into a buffer too small for the source string.

### 🎯 42 Piscine Notes
✅ You will rebuild most of `<string.h>` yourself in libft — know the null terminator rule cold.
✅ Always verify buffer sizes before `strcpy`/`strcat`.
✅ Practice manual string traversal with `while (str[i] != '\0')`.

### 🚀 Mastery Checklist
- [ ] I understand that a string is a char array ending in `'\0'`.
- [ ] I know why string literals shouldn't be modified.
- [ ] I can manually compute string length with a loop.
- [ ] I know why `strcmp`, not `==`, is used to compare strings.
- [ ] I understand what causes a buffer overflow.


---

# Part VII — Pointers

# 👉 Chapter 12 — Pointers

A pointer is a variable that stores a **memory address** instead of an ordinary value. Pointers are the concept that connects everything from Chapter 4 (Memory) into something you can actually manipulate in code.

---

## Memory Addresses (Review)

Every variable lives at some address in RAM.

```c
int age = 25;

printf("%p\n", &age);
```

The `&` operator ("address-of") returns the memory address where a variable is stored.

```
Variable      Value      Address
age           25         0x7ffeefbff56c
```

---

## Pointer Variables

A pointer variable stores an address. It is declared using `*`.

```c
int age = 25;
int *ptr = &age;
```

Breakdown:

```
int *ptr
  ↑    ↑
type  pointer to int

= &age
    ↑
  address of age
```

`ptr` doesn't hold `25` — it holds the **address** where `25` lives.

```
age                ptr
0x1000             0x2000
+------+           +----------+
|  25  |  <------  | 0x1000   |
+------+           +----------+
```

Every pointer type must match the type of data it points to.

```c
int x;
int *p1 = &x;      // pointer to int

char c;
char *p2 = &c;      // pointer to char

double d;
double *p3 = &d;    // pointer to double
```

---

## Dereferencing

Dereferencing means using `*` to access the **value stored at** the address a pointer holds.

```c
int age = 25;
int *ptr = &age;

printf("%d\n", *ptr);   // 25 — the value age holds
printf("%p\n", ptr);    // the address of age
printf("%p\n", &age);   // same address
```

`*` has two different meanings depending on context — this confuses many beginners:

```c
int *ptr;         // here, * means "declare a pointer"
*ptr = 10;         // here, * means "dereference — access the value"
```

### Modifying Through a Pointer

```c
int age = 25;
int *ptr = &age;

*ptr = 30;             // changes age itself
printf("%d\n", age);   // 30
```

Because `ptr` points to `age`'s exact address, writing through `*ptr` modifies `age` directly. This is exactly how functions can modify a caller's variable (Chapter 9 — pass by pointer).

```c
void increment(int *x)
{
    (*x)++;
}

int main(void)
{
    int number = 5;
    increment(&number);
    printf("%d\n", number);   // 6
    return (0);
}
```

---

## Pointer Arithmetic

Adding to a pointer moves it forward by **element-sized** steps, not raw bytes — the compiler automatically scales by `sizeof(type)`.

```c
int numbers[5] = {10, 20, 30, 40, 50};
int *ptr = numbers;    // points to numbers[0]

printf("%d\n", *ptr);        // 10
printf("%d\n", *(ptr + 1));  // 20
printf("%d\n", *(ptr + 2));  // 30
```

```
ptr + 0   ptr + 1   ptr + 2   ptr + 3   ptr + 4
  ↓          ↓          ↓          ↓          ↓
 10         20         30         40         50
```

If `ptr` is an `int*`, `ptr + 1` moves forward by `sizeof(int)` bytes (typically 4), not 1 byte.

### Pointer Increment

```c
int *ptr = numbers;

ptr++;                  // now points to numbers[1]
printf("%d\n", *ptr);   // 20
```

### Array Indexing Is Pointer Arithmetic

```c
numbers[2]
```

is exactly equivalent to:

```c
*(numbers + 2)
```

This is why array names "decay" into pointers when passed to functions (Chapter 10).

---

## NULL

`NULL` represents a pointer that points to **nothing** — an invalid or unset address (conceptually address `0`).

```c
int *ptr = NULL;
```

Always initialize pointers, and always check before dereferencing:

```c
int *ptr = NULL;

if (ptr != NULL)
{
    printf("%d\n", *ptr);
}
```

### ⚠️ NULL Pointer Dereference

```c
int *ptr = NULL;

printf("%d\n", *ptr);   // ❌ crash — segmentation fault
```

Dereferencing `NULL` (or any invalid pointer) is one of the most common causes of a **segmentation fault** — the operating system stopping your program because it tried to access memory it doesn't own.

---

## Pointer to Pointer

A pointer can store the address of another pointer, using `**`.

```c
int age = 25;
int *ptr = &age;
int **ptr_to_ptr = &ptr;
```

```
age              ptr                 ptr_to_ptr
0x1000           0x2000              0x3000
+------+         +----------+        +----------+
|  25  | <------ | 0x1000   | <----- | 0x2000   |
+------+         +----------+        +----------+
```

Dereferencing twice reaches the original value:

```c
printf("%d\n", **ptr_to_ptr);   // 25
printf("%p\n", *ptr_to_ptr);    // address of age (0x1000)
printf("%p\n", ptr_to_ptr);     // address of ptr (0x2000)
```

Common use case: functions that need to modify a pointer itself (not just the value it points to) — for example, allocating memory inside a function and returning it through a `char **` parameter.

---

## Arrays & Pointers

Arrays and pointers are closely related but **not identical**.

```c
int numbers[5] = {10, 20, 30, 40, 50};
int *ptr = numbers;   // no & needed — array name decays to a pointer
```

Both of these work the same way:

```c
numbers[i]
*(numbers + i)
ptr[i]
*(ptr + i)
```

### Key Difference

`sizeof` behaves differently:

```c
int numbers[5];
int *ptr = numbers;

printf("%zu\n", sizeof(numbers));   // 20 (5 * sizeof(int))
printf("%zu\n", sizeof(ptr));       // 8 (size of a pointer, on 64-bit)
```

`numbers` is the array itself; `ptr` is just a pointer that happens to point to its first element. This is exactly why, as noted in Chapter 10, array size must be passed explicitly to functions.

---

## Function Pointers (Introduction)

A function pointer stores the **address of a function**, allowing you to call that function indirectly — or pass it as an argument to another function.

```c
int add(int a, int b)
{
    return (a + b);
}

int main(void)
{
    int (*operation)(int, int) = add;

    printf("%d\n", operation(3, 4));   // 7
    return (0);
}
```

Breakdown:

```
int (*operation)(int, int)
     ↑
  pointer to a function that
  takes two ints and returns an int
```

Function pointers are used for things like callback functions, dispatch tables (arrays of function pointers, e.g. one per command), and implementing custom sorting comparators (like the `compar` parameter of `qsort()`).

This is an advanced topic — full mastery comes later in your C journey, but recognizing the syntax now removes a major source of confusion.

---

## 🧾 Chapter 12 Cheat Sheet

| Symbol | Meaning |
|---|---|
| `&x` | Address-of — gives the address of `x` |
| `*p` | Dereference — gives the value `p` points to |
| `int *p` | Declares `p` as a pointer to `int` |
| `p + 1` | Moves forward by one element (`sizeof(type)` bytes) |
| `NULL` | A pointer that points to nothing |
| `int **pp` | Pointer to a pointer |

### Common Mistakes
- Dereferencing an uninitialized or `NULL` pointer.
- Confusing `*` in a declaration (`int *p`) with `*` for dereferencing (`*p = 5`).
- Assuming pointer arithmetic moves by 1 byte instead of `sizeof(type)`.
- Using `sizeof` on a pointer expecting the array's total size.
- Forgetting `&` when passing a variable's address to a function.

### 🎯 42 Piscine Notes
✅ Pointers are the single biggest jump in difficulty in the Piscine — expect to revisit this chapter often.
✅ Draw memory diagrams (boxes and arrows) by hand until pointer arithmetic feels automatic.
✅ Always initialize pointers to `NULL` and check before dereferencing.
✅ Understand `char **` deeply — it appears constantly (argv, split functions, linked structures).

### 🚀 Mastery Checklist
- [ ] I understand what an address is and what `&` returns.
- [ ] I understand dereferencing with `*`.
- [ ] I can modify a variable through a pointer passed to a function.
- [ ] I understand pointer arithmetic and how it relates to array indexing.
- [ ] I understand why `NULL` checks matter before dereferencing.
- [ ] I understand pointer-to-pointer (`**`) at a basic level.
- [ ] I recognize function pointer syntax.


---

# Part VIII — User Defined Types

# 🏗️ Chapter 13 — Structures

A `struct` groups several related variables (possibly of different types) into a single named unit. Where an array holds many values of the **same** type, a struct holds several values of **different** types that belong together.

---

## struct

### Declaring a Structure Type

```c
struct Student
{
    char name[50];
    int age;
    float gpa;
};
```

This defines a new type, `struct Student` — it does not create a variable yet.

### Creating and Using a Variable

```c
struct Student s1;

s1.age = 20;
s1.gpa = 3.8;
```

The `.` operator accesses a member of a struct variable.

### Initialization

```c
struct Student s1 = {"Abdullah", 20, 3.8};

struct Student s2 = {
    .name = "Sara",
    .age = 22,
    .gpa = 3.9
};
```

The second form (**designated initializers**) is clearer and doesn't depend on member order.

### Memory Layout

Members are typically stored in the order they're declared, though the compiler may add **padding** between them for alignment — so `sizeof(struct Student)` isn't always exactly the sum of its members' sizes.

```
struct Student
+------------------+
| name[50]         |
+------------------+
| age  (int)       |
+------------------+
| gpa  (float)     |
+------------------+
```

---

## typedef

`typedef` creates an alias for a type — most commonly used with structs to avoid repeatedly writing `struct` before the type name.

```c
typedef struct Student
{
    char name[50];
    int age;
    float gpa;
} Student;
```

Now you can write:

```c
Student s1;          // instead of: struct Student s1;

s1.age = 20;
```

`typedef` can alias any type, not just structs:

```c
typedef unsigned int uint;

uint counter = 0;
```

---

## Nested Structures

A struct can contain another struct as a member.

```c
typedef struct
{
    int day;
    int month;
    int year;
} Date;

typedef struct
{
    char name[50];
    Date birthdate;
} Person;
```

Accessing nested members chains the `.` operator:

```c
Person p1;

p1.birthdate.day = 15;
p1.birthdate.month = 6;
p1.birthdate.year = 2001;
```

---

## Passing Structures

### By Value (Copy)

```c
void print_student(struct Student s)
{
    printf("%s\n", s.name);
}
```

The entire struct is **copied** when passed this way. For large structs, this can be inefficient — every member gets duplicated onto the Stack.

### By Pointer (Reference)

```c
void print_student(struct Student *s)
{
    printf("%s\n", s->name);
}
```

The `->` operator dereferences a struct pointer **and** accesses a member in one step — it's shorthand for `(*s).name`.

```c
(*s).name       // works, but awkward
s->name         // equivalent, and idiomatic
```

Passing by pointer avoids copying the whole struct, and is the only way for a function to **modify** the caller's struct.

```c
void set_age(struct Student *s, int age)
{
    s->age = age;   // modifies the original struct
}
```

---

## Arrays of Structures

Structs and arrays combine naturally — an array of structs represents a collection of records.

```c
struct Student class[3];

class[0].age = 20;
class[1].age = 21;
class[2].age = 19;
```

### Initialization

```c
struct Student class[3] = {
    {"Abdullah", 20, 3.8},
    {"Sara", 21, 3.9},
    {"Youssef", 19, 3.5}
};
```

### Traversal

```c
for (int i = 0; i < 3; i++)
{
    printf("%s - %d\n", class[i].name, class[i].age);
}
```

This pattern — an array of structs — is the foundation of how real programs represent things like a list of users, a table of database rows, or a set of game entities.

---

## 🧾 Chapter 13 Cheat Sheet

| Concept | Key Fact |
|---|---|
| `struct` | Groups related variables of different types |
| `.` | Access a member on a struct variable |
| `->` | Access a member through a struct pointer |
| `typedef` | Creates an alias, avoids repeating `struct` |
| Passing by pointer | Avoids copying, allows modification |

### Common Mistakes
- Using `.` on a struct pointer instead of `->`.
- Passing large structs by value unnecessarily (performance cost).
- Forgetting that struct assignment (`s2 = s1;`) copies all members.
- Assuming `sizeof(struct)` equals the exact sum of member sizes (padding exists).

### 🎯 42 Piscine Notes
✅ `struct` and `typedef struct` appear constantly once you reach linked lists and more advanced projects.
✅ Master `->` early — it's used everywhere once pointers to structs appear.
✅ Get comfortable with arrays of structs — they model real-world collections of data.

### 🚀 Mastery Checklist
- [ ] I can declare and initialize a struct.
- [ ] I understand the difference between `.` and `->`.
- [ ] I know why passing structs by pointer is often preferred.
- [ ] I can nest structs inside other structs.
- [ ] I can build and traverse an array of structs.

---

# 📚 Chapter 14 — Enumerations

An `enum` gives meaningful names to a set of related integer constants, making code more readable than using raw numbers.

---

## enum

### Basic Declaration

```c
enum Day
{
    MONDAY,
    TUESDAY,
    WEDNESDAY,
    THURSDAY,
    FRIDAY,
    SATURDAY,
    SUNDAY
};
```

By default, enum values are assigned integers **starting at 0**, increasing by 1:

```
MONDAY     = 0
TUESDAY    = 1
WEDNESDAY  = 2
THURSDAY   = 3
FRIDAY     = 4
SATURDAY   = 5
SUNDAY     = 6
```

### Using an enum

```c
enum Day today = WEDNESDAY;

printf("%d\n", today);   // 2
```

### Custom Values

You can assign specific starting values; unassigned members continue counting from the last explicit value.

```c
enum Day
{
    MONDAY = 1,
    TUESDAY,     // 2
    WEDNESDAY,   // 3
    THURSDAY,    // 4
    FRIDAY,      // 5
    SATURDAY,    // 6
    SUNDAY       // 7
};
```

```c
enum Status
{
    OK = 0,
    ERROR = -1,
    PENDING = 100
};
```

### typedef with enum

```c
typedef enum
{
    RED,
    GREEN,
    BLUE
} Color;

Color favorite = GREEN;
```

---

## Practical Uses

### Replacing Magic Numbers

Without an enum:

```c
if (status == 2)   // what does 2 mean?
```

With an enum:

```c
enum Status { PENDING, APPROVED, REJECTED };

if (status == APPROVED)   // immediately clear
```

### switch with enum

Enums pair naturally with `switch`, since both work on integer values:

```c
enum Day today = WEDNESDAY;

switch (today)
{
    case MONDAY:
        printf("Start of the week\n");
        break;
    case FRIDAY:
        printf("Almost weekend\n");
        break;
    default:
        printf("Midweek\n");
}
```

### State Machines

Enums are the standard way to represent a finite set of states — a game's state, a connection's status, a parser's mode.

```c
typedef enum
{
    STATE_IDLE,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED
} GameState;

GameState current = STATE_IDLE;
```

### ⚠️ Common Mistake — Assuming Type Safety

C's `enum` is really just an `int` under the hood — the compiler does **not** stop you from assigning an out-of-range integer to an enum variable.

```c
enum Day today = 100;   // compiles — no real type safety
```

Unlike languages such as Java or Rust, C enums provide readability, not strict safety. Treat them as a naming convention for integers, not a guarantee.

---

## 🧾 Chapter 14 Cheat Sheet

| Concept | Key Fact |
|---|---|
| Default values | Start at `0`, increment by 1 |
| Custom start | `enum { A = 5, B, C };` → `B = 6, C = 7` |
| Underlying type | Always an `int` — no real type safety |
| Best use | Replacing magic numbers, representing states |

### Common Mistakes
- Assuming enums are a distinct, safe type — they're just named integers.
- Forgetting that unassigned members continue counting from the previous value.
- Using raw numbers instead of enum names, losing the readability benefit.

### 🎯 42 Piscine Notes
✅ Use enums to replace magic numbers whenever a variable has a small fixed set of meaningful states.
✅ Combine enums with `switch` for clean, readable state handling.

### 🚀 Mastery Checklist
- [ ] I know how default enum values are assigned.
- [ ] I can assign custom starting values.
- [ ] I understand enums are just named integers, not a safe distinct type.
- [ ] I can use an enum with a `switch` statement.


---

# Part IX — Dynamic Memory

# 🧠 Chapter 15 — Dynamic Memory

Chapter 4 introduced the Heap conceptually. This chapter covers the actual functions used to allocate and release Heap memory: `malloc`, `calloc`, `realloc`, and `free`.

All four are declared in `<stdlib.h>`.

---

## malloc

`malloc` ("memory allocation") reserves a block of memory on the Heap and returns a pointer to it. The memory is **uninitialized** — it contains garbage values.

```c
void *malloc(size_t size);
```

Example:

```c
int *numbers = malloc(5 * sizeof(int));

if (numbers == NULL)
{
    /* allocation failed — handle the error */
    return (1);
}
```

Breakdown:

```
5 * sizeof(int)
    ↓
5 * 4 bytes
    ↓
20 bytes requested
```

`malloc` returns `void *`, a generic pointer, which C automatically converts to any pointer type — no explicit cast is needed (and casting it is often discouraged in C, unlike C++).

```c
int *numbers = malloc(5 * sizeof(int));        // ✅ preferred
int *numbers = (int *)malloc(5 * sizeof(int));  // also valid, but unnecessary in C
```

### ⚠️ Always Check for NULL

```c
char *buffer = malloc(1000000000000);   // huge request

if (buffer == NULL)
{
    printf("Allocation failed\n");
    return (1);
}
```

`malloc` returns `NULL` if the system cannot satisfy the request. Skipping this check is one of the most common robustness bugs in C programs.

---

## calloc

`calloc` ("clear allocation") allocates memory for an array of elements **and initializes every byte to zero**.

```c
void *calloc(size_t num, size_t size);
```

Example:

```c
int *numbers = calloc(5, sizeof(int));
```

This allocates space for 5 integers, all initialized to `0`.

### malloc vs calloc

| | `malloc` | `calloc` |
|---|---|---|
| Arguments | Total bytes | Number of elements, size of each |
| Initial contents | Garbage (uninitialized) | Zeroed out |
| Speed | Slightly faster | Slightly slower (due to zeroing) |

```c
int *a = malloc(5 * sizeof(int));   // garbage values
int *b = calloc(5, sizeof(int));    // all zeros
```

Use `calloc` when you need guaranteed zeroed memory (e.g. a buffer you'll fill incrementally and want clean of leftover data).

---

## realloc

`realloc` resizes a previously allocated block — growing or shrinking it — while attempting to preserve its existing contents.

```c
void *realloc(void *ptr, size_t new_size);
```

Example:

```c
int *numbers = malloc(5 * sizeof(int));

/* ... use numbers ... */

numbers = realloc(numbers, 10 * sizeof(int));   // now holds 10 ints

if (numbers == NULL)
{
    /* realloc failed — original block is untouched but not freed */
}
```

### ⚠️ Critical Pattern — Never Overwrite the Original Pointer Directly

```c
numbers = realloc(numbers, 10 * sizeof(int));   // ❌ risky
```

If `realloc` fails, it returns `NULL` — and this assignment would **lose the original pointer**, making the original block unreachable and impossible to `free`. This is a **memory leak** waiting to happen. The safe pattern:

```c
int *temp = realloc(numbers, 10 * sizeof(int));

if (temp == NULL)
{
    /* numbers is still valid — handle the error, then free(numbers) if done */
}
else
{
    numbers = temp;
}
```

`realloc(ptr, 0)` behaves like `free(ptr)` on many implementations (but this is implementation-defined — avoid relying on it). `realloc(NULL, size)` behaves like `malloc(size)`.

---

## free

`free` releases memory previously allocated with `malloc`, `calloc`, or `realloc`, returning it to the system so it can be reused.

```c
void free(void *ptr);
```

Example:

```c
int *numbers = malloc(5 * sizeof(int));

/* ... use numbers ... */

free(numbers);
```

Every successful `malloc`/`calloc`/`realloc` should eventually have exactly **one** matching `free`.

### ⚠️ Don't Use Memory After Freeing It

```c
free(numbers);
numbers[0] = 10;   // ❌ undefined behavior — use-after-free
```

### ⚠️ Set Freed Pointers to NULL

```c
free(numbers);
numbers = NULL;   // prevents accidental reuse
```

This doesn't undo the free, but it turns an accidental reuse into an immediate, obvious crash (dereferencing `NULL`) rather than silent memory corruption.

---

## Memory Leaks

A memory leak happens when allocated Heap memory becomes **unreachable** — no pointer refers to it anymore — without ever being freed.

```c
void leak(void)
{
    int *ptr = malloc(sizeof(int));
    *ptr = 42;
    /* function ends — ptr goes out of scope, memory is never freed */
}
```

Once `leak()` returns, the local pointer `ptr` is gone, but the memory it pointed to still exists on the Heap — permanently unreachable until the program exits.

### Losing the Pointer

```c
int *ptr = malloc(sizeof(int));

ptr = NULL;   // ❌ original block is now unreachable — leaked
```

### Why Leaks Matter

A single leak in a short-lived program is harmless. In a long-running program (a server, a game, a background service), repeated leaks slowly consume all available memory, eventually crashing the program or the whole system.

### Detecting Leaks

At 42/1337, memory leaks are typically caught with tools like **valgrind**:

```bash
valgrind --leak-check=full ./your_program
```

This is standard practice before submitting any project involving `malloc`.

---

## Dangling Pointers

A dangling pointer points to memory that has already been freed (or otherwise no longer valid).

```c
int *ptr = malloc(sizeof(int));

free(ptr);
/* ptr still holds the old address — it is now dangling */

*ptr = 5;   // ❌ undefined behavior
```

### Double Free

Freeing the same pointer twice is also undefined behavior and can corrupt the Heap's internal bookkeeping.

```c
free(ptr);
free(ptr);   // ❌ double free
```

### Preventing Dangling Pointers

```c
free(ptr);
ptr = NULL;

if (ptr != NULL)
{
    *ptr = 5;   // never reached — safe
}
```

Setting a pointer to `NULL` immediately after freeing it is the standard defensive habit that prevents both use-after-free and double-free bugs.

---

## 🧾 Chapter 15 Cheat Sheet

| Function | Purpose |
|---|---|
| `malloc(size)` | Allocate uninitialized memory |
| `calloc(n, size)` | Allocate and zero-initialize memory |
| `realloc(ptr, size)` | Resize existing allocation |
| `free(ptr)` | Release allocated memory |

### Golden Rules
1. Every `malloc`/`calloc`/`realloc` needs exactly one matching `free`.
2. Always check the return value for `NULL`.
3. Never use memory after `free`.
4. Never `free` the same pointer twice.
5. Set pointers to `NULL` after freeing them.
6. Never assign `realloc`'s result directly back to the original pointer — use a temporary variable.

### Common Mistakes
- Forgetting to `free` allocated memory (memory leak).
- Using memory after it's been freed (dangling pointer / use-after-free).
- Freeing the same pointer twice (double free).
- Losing the original pointer before freeing it.
- Overwriting a pointer with a failed `realloc()`'s `NULL` result.

### 🎯 42 Piscine Notes
✅ `valgrind --leak-check=full` before every submission — leaks fail evaluations.
✅ Every project involving `malloc` should be traceable: know exactly where every allocation is freed.
✅ `free(NULL)` is explicitly safe and does nothing — no need to guard every `free` with a `NULL` check.

### 🚀 Mastery Checklist
- [ ] I understand the difference between `malloc` and `calloc`.
- [ ] I know the safe pattern for using `realloc`.
- [ ] I always check allocation results for `NULL`.
- [ ] I understand what causes a memory leak.
- [ ] I understand what a dangling pointer is and how to prevent it.
- [ ] I know why double-free is dangerous.


---

# Part X — File Handling

# 📂 Chapter 16 — File I/O

Programs often need to read from or write to files — configuration files, logs, saved data. C provides file handling through `<stdio.h>`, using a `FILE *` to represent an open file.

---

## fopen

`fopen` opens a file and returns a `FILE *` pointer used for all further operations on it.

```c
FILE *fopen(const char *filename, const char *mode);
```

| Mode | Meaning |
|---|---|
| `"r"` | Read (file must exist) |
| `"w"` | Write (creates file, **overwrites** if it exists) |
| `"a"` | Append (creates file if needed, writes at the end) |
| `"r+"` | Read and write (file must exist) |
| `"w+"` | Read and write (overwrites/creates) |
| `"a+"` | Read and append |

Example:

```c
FILE *file = fopen("data.txt", "r");

if (file == NULL)
{
    printf("Could not open file\n");
    return (1);
}
```

⚠️ Always check for `NULL` — `fopen` fails if the file doesn't exist (in read mode), permissions are wrong, or the path is invalid.

---

## fclose

`fclose` closes an open file, flushing any buffered writes and releasing the associated resources.

```c
int fclose(FILE *stream);
```

Example:

```c
fclose(file);
```

Every successful `fopen` should have a matching `fclose`, the same way every `malloc` needs a `free`. Forgetting to close files can lead to data not being written (buffered content lost) or running out of available file handles in long-running programs.

---

## fread

`fread` reads raw binary data from a file into memory.

```c
size_t fread(void *ptr, size_t size, size_t nmemb, FILE *stream);
```

Example:

```c
int numbers[5];
FILE *file = fopen("numbers.bin", "rb");

fread(numbers, sizeof(int), 5, file);
fclose(file);
```

Parameters:

```
ptr     → where to store the data
size    → size of each element
nmemb   → how many elements to read
stream  → the file to read from
```

`fread` returns the number of elements actually read — always check this against the number requested to detect a short read or end-of-file.

---

## fwrite

`fwrite` writes raw binary data from memory into a file.

```c
size_t fwrite(const void *ptr, size_t size, size_t nmemb, FILE *stream);
```

Example:

```c
int numbers[5] = {10, 20, 30, 40, 50};
FILE *file = fopen("numbers.bin", "wb");

fwrite(numbers, sizeof(int), 5, file);
fclose(file);
```

`fread`/`fwrite` work with **binary** data — the bytes are written exactly as they exist in memory, not as human-readable text.

---

## fprintf

`fprintf` writes **formatted text** to a file — it works exactly like `printf`, but targets a file instead of the terminal.

```c
int fprintf(FILE *stream, const char *format, ...);
```

Example:

```c
FILE *file = fopen("log.txt", "w");

fprintf(file, "Score: %d\n", 100);
fclose(file);
```

`log.txt` now contains:

```
Score: 100
```

---

## fscanf

`fscanf` reads **formatted text** from a file — the file-based equivalent of `scanf`.

```c
int fscanf(FILE *stream, const char *format, ...);
```

Example:

```c
FILE *file = fopen("data.txt", "r");
int score;

fscanf(file, "%d", &score);
fclose(file);
```

Like `scanf`, `fscanf` returns the number of items successfully matched — check this to detect malformed or incomplete input.

---

## fgets

`fgets` reads a full line of text (up to a newline or buffer limit) from a file — much safer than older line-reading functions like `gets`, which is unbounded and unsafe.

```c
char *fgets(char *str, int n, FILE *stream);
```

Example:

```c
char line[100];
FILE *file = fopen("data.txt", "r");

while (fgets(line, sizeof(line), file) != NULL)
{
    printf("%s", line);
}

fclose(file);
```

`fgets` reads at most `n - 1` characters, leaving room for the null terminator, and stops early at a newline (which it **keeps** in the buffer, unlike some other line-reading functions).

`fgets(buffer, sizeof(buffer), stdin)` is also the standard safe way to read a line of user input from the terminal, replacing the unsafe `gets()`.

---

## fputs

`fputs` writes a string to a file (without automatically adding a newline, unlike `puts`).

```c
int fputs(const char *str, FILE *stream);
```

Example:

```c
FILE *file = fopen("log.txt", "a");

fputs("New entry\n", file);
fclose(file);
```

Because the mode was `"a"` (append), this adds `"New entry\n"` to the **end** of the existing file content rather than overwriting it.

---

## 🧾 Chapter 16 Cheat Sheet

| Function | Purpose |
|---|---|
| `fopen` | Open a file, get a `FILE *` |
| `fclose` | Close an open file |
| `fread` | Read raw binary data |
| `fwrite` | Write raw binary data |
| `fprintf` | Write formatted text |
| `fscanf` | Read formatted text |
| `fgets` | Read a line of text safely |
| `fputs` | Write a string (no auto-newline) |

### Common Mistakes
- Not checking `fopen`'s return value for `NULL`.
- Forgetting `fclose`, losing buffered writes.
- Using `"w"` when you meant `"a"`, accidentally overwriting existing content.
- Mixing binary functions (`fread`/`fwrite`) with text-mode files, or vice versa.
- Not checking `fread`/`fscanf` return values to detect incomplete reads.

### 🎯 42 Piscine Notes
✅ Always pair `fopen` with `fclose` — treat it like `malloc`/`free`.
✅ Use `fgets`, never `gets` — `gets` has no bounds checking and is considered unsafe/deprecated.
✅ For line-by-line file processing, the `fgets` + `while` pattern above is the standard idiom.

### 🚀 Mastery Checklist
- [ ] I know the common `fopen` modes and when to use each.
- [ ] I always check `fopen`'s return value.
- [ ] I understand the difference between binary (`fread`/`fwrite`) and formatted text (`fprintf`/`fscanf`) I/O.
- [ ] I can safely read a file line by line with `fgets`.
- [ ] I always close files I've opened.


---

# Part XI — Debugging

# 🐞 Chapter 17 — Common Errors

Understanding *when* and *why* an error appears is more valuable than memorizing fixes. Errors in C fall into distinct categories, each caught at a different stage.

```
Source Code
    ↓
Syntax Errors        ← caught by the compiler, before compilation finishes
    ↓
Compiler Errors       ← caught during compilation
    ↓
Linker Errors         ← caught while combining object files
    ↓
Runtime Errors         ← occur while the program is executing
```

---

## Syntax Errors

A syntax error means the code doesn't follow the grammar rules of the C language — the compiler cannot even parse it.

```c
int age = 25    // ❌ missing semicolon

if (age > 18)
{
    printf("Adult\n")   // ❌ missing semicolon
```

Typical causes: missing semicolons, unbalanced braces/parentheses, misspelled keywords.

---

## Compiler Errors

Compiler errors occur when the syntax is valid but the code violates the language's type or usage rules.

```c
int x = "hello";        // ❌ type mismatch

undeclared_function();  // ❌ used before declared

int x;
int x;                  // ❌ redeclaration in the same scope
```

Compiler *warnings* (not fatal errors) are just as important — always compile with `-Wall -Wextra` and treat warnings seriously. Many "runtime mysteries" are warnings that were ignored.

---

## Linker Errors

Linker errors occur after compilation, when the linker tries to combine object files and external libraries into a final executable, but can't find something it needs.

```c
/* file1.c */
int add(int a, int b)
{
    return (a + b);
}

/* file2.c */
int main(void)
{
    printf("%d\n", multiply(3, 4));   // ❌ multiply was never defined anywhere
    return (0);
}
```

```
undefined reference to `multiply`
```

Typical causes: a function is declared (in a header) but never defined, a `.c` file wasn't included in compilation, or a required library wasn't linked (e.g. forgetting `-lm` for `<math.h>` functions).

---

## Runtime Errors

Runtime errors occur while the program is running — the code compiles and links fine, but something goes wrong during execution.

```c
int a = 10;
int b = 0;

printf("%d\n", a / b);   // ❌ division by zero
```

---

## Segmentation Fault

A segmentation fault ("segfault") happens when a program tries to access memory it doesn't have permission to use.

```c
int *ptr = NULL;
*ptr = 5;                 // ❌ segfault — dereferencing NULL

int arr[5];
arr[100] = 1;              // ❌ segfault (or silent corruption) — out of bounds

char *str = "Hello";
str[0] = 'h';               // ❌ segfault — modifying a read-only string literal
```

Segfaults are the operating system stopping your program before it can corrupt memory it doesn't own — a crash is actually the *safe* outcome; the dangerous case is when invalid access silently succeeds and corrupts something else instead.

---

## Undefined Behavior

Undefined behavior (UB) means the C standard places **no requirements** on what happens — the compiler is free to do anything: crash, produce wrong output, appear to "work," or behave differently between runs or compilers.

```c
int x = 2147483647;
x = x + 1;                     // signed integer overflow — UB

int arr[5];
printf("%d\n", arr[10]);        // out-of-bounds read — UB

int *ptr;
printf("%d\n", *ptr);            // uninitialized pointer — UB
```

UB is uniquely dangerous because it can appear to work correctly for a long time and then fail unpredictably — often only after a compiler upgrade, a different optimization level, or on a different machine. Never rely on "it worked when I tested it" as proof that UB is safe.

---

## Buffer Overflow

A buffer overflow happens when a program writes past the boundary of an allocated buffer (array, string, or Heap block), overwriting adjacent memory.

```c
char name[5];

strcpy(name, "Abdullah");   // ❌ "Abdullah" + '\0' needs 9 bytes, buffer has 5
```

Buffer overflows are one of the most historically significant classes of security vulnerabilities — overwriting adjacent memory can corrupt other variables, return addresses, or Heap metadata, sometimes exploitably.

Prevention: always know your buffer's real capacity, prefer bounded functions (`strncpy`, `snprintf`) over unbounded ones (`strcpy`, `sprintf`, `gets`), and validate lengths before copying.

---

## Memory Leaks (Review)

Covered in depth in Chapter 15 — worth repeating here as a "common error" because it's a runtime error that produces no crash and no visible symptom until memory is exhausted, making it easy to miss without tools like `valgrind`.

```c
void leak(void)
{
    int *ptr = malloc(sizeof(int));
    /* forgot free(ptr) */
}
```

---

## 🧾 Chapter 17 Cheat Sheet

| Error Type | Caught When | Typical Cause |
|---|---|---|
| Syntax Error | Compilation (parsing) | Missing `;`, unbalanced braces |
| Compiler Error | Compilation (type-checking) | Type mismatch, undeclared identifier |
| Linker Error | Linking | Missing definition, missing library |
| Runtime Error | Execution | Division by zero, bad logic |
| Segmentation Fault | Execution | Invalid memory access |
| Undefined Behavior | Anytime — unpredictably | Overflow, uninitialized memory, out-of-bounds |
| Buffer Overflow | Execution (sometimes silent) | Writing past a buffer's capacity |

### 🎯 42 Piscine Notes
✅ Compile with `-Wall -Wextra -Werror` from day one — this turns many future runtime bugs into immediate compiler errors.
✅ Run every project through `valgrind` before submitting.
✅ A segfault is your friend, not your enemy — it tells you exactly that something is wrong, unlike silent memory corruption.

### 🚀 Mastery Checklist
- [ ] I can distinguish syntax, compiler, linker, and runtime errors.
- [ ] I understand what causes a segmentation fault.
- [ ] I understand why undefined behavior is dangerous even when code "seems to work."
- [ ] I know what causes a buffer overflow and how to prevent it.
- [ ] I use `-Wall -Wextra` and `valgrind` as standard habits.

---

# Part XII — Professional Programming

# 🏆 Chapter 18 — Best Practices

Writing code that *works* is only the first step. Writing code that is *readable*, *maintainable*, and *defensible* is what separates a beginner from a professional — and is exactly what the 42 Norm exists to enforce.

---

## Readable Code

Code is read far more often than it is written — by teammates, evaluators, and your future self. Readable code favors clarity over cleverness.

```c
/* Hard to read */
int f(int a,int b){return a>b?a:b;}

/* Readable */
int max(int a, int b)
{
    if (a > b)
        return (a);
    return (b);
}
```

Principles:
- One clear idea per line.
- Consistent spacing and indentation.
- Avoid deeply nested logic when a simpler structure exists.

---

## Naming Conventions

Names should describe **purpose**, not just satisfy the compiler (Chapter 5 covered identifier rules — this is about *style*, on top of those rules).

```c
int x;              // ❌ meaningless
int student_count;  // ✅ self-documenting
```

C convention (and the 42 Norm) favors `snake_case`:

```c
int total_score;
char *user_name;

int get_max_value(int a, int b);
```

Function names should usually read like an action:

```c
int calculate_total(int a, int b);
void print_report(Report *r);
int is_valid(char *input);
```

---

## Code Organization

Group related functionality into separate files, and expose only what's needed through headers.

```
project/
├── main.c
├── utils.c
├── utils.h
└── student.c
    student.h
```

```c
/* student.h */
#ifndef STUDENT_H
# define STUDENT_H

typedef struct
{
    char name[50];
    int age;
} Student;

void print_student(Student *s);

#endif
```

Header guards (from Chapter 2) prevent double-inclusion; each `.c` file should have exactly one matching `.h` exposing its public interface.

---

## Defensive Programming

Defensive programming means anticipating things that could go wrong and handling them explicitly, rather than assuming the "happy path" always holds.

```c
int divide(int a, int b)
{
    if (b == 0)
    {
        printf("Error: division by zero\n");
        return (0);
    }
    return (a / b);
}
```

Common defensive habits, most already covered in earlier chapters:
- Check `malloc`/`fopen` return values for `NULL`.
- Validate function parameters before using them (e.g. reject `NULL` pointers).
- Initialize variables rather than relying on them starting at zero.
- Check array bounds before indexing.

```c
void process(int *arr, int size)
{
    if (arr == NULL || size <= 0)
        return;

    for (int i = 0; i < size; i++)
        printf("%d\n", arr[i]);
}
```

---

## Code Review

Code review is the practice of having another person (or, later in your career, yourself with fresh eyes) examine code before it's merged or submitted — catching bugs, unclear logic, and style issues early.

At 42/1337, this takes the form of peer evaluations: another student reviews your code against the project requirements and the Norm. Treat this process seriously in both directions:

- **As the author:** write code assuming someone else will need to understand it in five minutes, with no context beyond what's on screen.
- **As a reviewer:** focus on correctness, readability, and edge cases — not just "does it run."

---

## 42 Norm

The **Norm** is 42/1337's mandatory C coding style (currently **Version 2.0.2**). A Norm error gives you a **0 for the exercise, or even the whole project** — one Norm error is treated exactly the same as ten. During evaluation, your grader runs the `norminette` tool, which checks the *mandatory* part automatically (the *advice* part is checked by humans, not the tool).

### Naming

- Structure names must start with `s_`.
- Typedef names must start with `t_`.
- Union names must start with `u_`.
- Enum names must start with `e_`.
- Global variable names must start with `g_`.
- Variable and function names may only contain lowercase letters, digits, and `_` (snake_case / "Unix case").
- File and directory names follow the same rule.
- Only non-standard-ASCII characters and unclear/non-English names are disallowed.

```c
typedef struct s_point
{
    int x;
    int y;
}   t_point;
```

### Formatting

- Every file starts with the standard 42 header (auto-generated by the `emacs`/`vim` config in the dumps).
- Indentation is **4-space tabs** — real tab characters, not 4 literal spaces.
- Each function is **max 25 lines**, not counting its own curly braces.
- Each line is **max 80 columns** (a tab counts as the number of spaces it visually represents, not as 1 column).
- **One instruction per line.**
- No trailing whitespace on any line, and no whitespace-only "empty" lines.
- A new line follows every closing curly brace / end of a control structure.
- Commas and semicolons are followed by a space (unless at end of line).
- Exactly **one** space separates each operator/operand.
- Every C keyword is followed by a space, **except** type keywords (`int`, `char`, `float`...) and `sizeof`.
- Variable declarations in the same block are aligned in the same column.
- The `*` of a pointer sticks to the **variable name**, not the type: `int *ptr`, not `int* ptr`.
- **One variable declared per line.**
- You cannot combine declaration and initialization on the same line — **except** for global and `static` variables.
- Declarations go at the **top of the function**, separated from the rest of the body by one empty line, and there is no blank line *between* declarations.
- **Multiple assignment is strictly forbidden**: `a = b = c;` is a Norm error.

```c
int ft_max(int a, int b)
{
    int result;

    if (a > b)
        result = a;
    else
        result = b;
    return (result);
}
```

### Function Parameters & Functions

- Max **4 named parameters** per function.
- A function taking no arguments must be prototyped explicitly with `void`, never empty parentheses.
- Prototype parameters must be named (not just typed).
- Each function is separated from the next by one empty line.
- **Max 5 variables declared per block.**
- A `return` value must be wrapped in parentheses: `return (result);`

### Typedef, struct, enum, union

- Indent (tab) the members when declaring a `struct`/`enum`/`union`.
- When declaring a variable of one of these types, put a single space in the type: `struct s_point pt;`
- Add a tab between the two parts of a `typedef`.
- When combining a `struct`/`union`/`enum` with a `typedef`, align the typedef's name with the type's name.
- **You cannot declare a structure inside a `.c` file** — declare it in a header.

### Headers

- Header files may only contain: includes, declarations, `#define`s, prototypes, and macros — no logic.
- All includes go at the top of the file.
- Every header must use an include guard. For `ft_foo.h`, the guard macro is `FT_FOO_H`.
- Function prototypes must live exclusively in `.h` files.
- Unused `#include`s are forbidden.

### Macros & Preprocessor

- `#define` constants may only be used for literal/constant values.
- Any `#define` written to sneak around the Norm or obfuscate code is forbidden (checked by a human, not the tool).
- Multiline macros are forbidden.
- Only macro names are written in UPPERCASE.
- Indent the lines following `#if`, `#ifdef`, `#ifndef`.

### ⚠️ Forbidden Statements & Constructs

```
for
do...while
switch
case
goto
```

Also forbidden:
- **Nested** ternary operators (`a ? b : c ? d : e`). A single, non-nested ternary (`a ? b : c`) **is allowed**.
- VLAs (Variable-Length Arrays).

Since `for`, `switch`, and `do...while` are all banned, virtually every loop at 42/1337 is written with a plain `while`, and multi-branch logic is written with `if`/`else if` chains instead of `switch`.

```c
/* Norm: use while, never for */
int i;

i = 0;
while (i < 5)
{
    printf("%d\n", i);
    i++;
}
```

### Comments

- Comments are allowed in source files, but **not inside a function's body**.
- A comment block must start and end on their own single line; every line in between must be aligned and start with `**`.
- `//` comments are forbidden entirely — only `/* */` blocks are allowed.
- A comment can never excuse a poorly designed ("bastard") function.

### Files

- You cannot `#include` a `.c` file.
- **Max 5 function definitions per `.c` file.**

### Makefile

- `$(NAME)`, `clean`, `fclean`, `re`, and `all` rules are mandatory.
- The Makefile must **never relink** unnecessarily — if it does, the project is considered non-functional.
- A multi-binary project needs a rule that builds everything, plus one rule per individual binary.
- If the project depends on a library (e.g. `libft`), the Makefile must build that library automatically.
- Every source file the project needs must be explicitly listed in the Makefile.

---

⚠️ **A note on accuracy:** the Norm is versioned and does occasionally change between releases. The rules above are transcribed from the official **Norm v2.0.2** document. Always cross-check against the current version for your campus at [github.com/42school/norminette](https://github.com/42school/norminette) before relying on any specific number or rule.

---

## 🧾 Chapter 18 Cheat Sheet

| Practice | Why It Matters |
|---|---|
| Readable code | Code is read more than it's written |
| Naming conventions | Names should explain purpose |
| Code organization | Separate concerns into files/headers |
| Defensive programming | Handle failure cases explicitly |
| Code review | Catches bugs and unclear logic early |
| 42 Norm | Mandatory style — one Norm error fails the exercise, same as ten |

### Quick Forbidden List (Norm v2.0.2)
`for` · `do...while` · `switch` / `case` · `goto` · nested ternary · VLAs · multiple assignment · `//` comments · declaring a struct in a `.c` file

### 🎯 42 Piscine Notes
✅ Run `norminette` before every submission — it checks the mandatory part automatically.
✅ Since `for`/`switch`/`do...while` are all banned, get very comfortable rewriting counted loops and multi-way branches using `while` and `if`/`else if`.
✅ Small, single-purpose functions (under 25 lines, under 5 variables per block) aren't just a rule — they genuinely make code easier to debug and test.
✅ Header guards, one clear responsibility per file, and consistent `s_`/`t_`/`u_`/`e_`/`g_` prefixes will save you time in every project after the Piscine.

### 🚀 Mastery Checklist
- [ ] I write code with clear, descriptive names.
- [ ] I organize related code into separate files with header guards.
- [ ] I check for failure cases (`NULL`, invalid input) before using values.
- [ ] I know exactly what the Norm forbids: `for`, `do...while`, `switch`/`case`, `goto`, nested ternary, VLAs.
- [ ] I know a single (non-nested) ternary and a plain `while` are both allowed.
- [ ] I treat code review (peer evaluation) as a normal, valuable part of the process.


---

# 📋 Final Appendix

---

## C Cheat Sheet

### Data Types & Format Specifiers

| Type | Typical Size | printf | scanf |
|---|---|---|---|
| `char` | 1 byte | `%c` / `%d` | `%c` |
| `short` | 2 bytes | `%hd` | `%hd` |
| `int` | 4 bytes | `%d` | `%d` |
| `long` | 4/8 bytes | `%ld` | `%ld` |
| `long long` | 8 bytes | `%lld` | `%lld` |
| `float` | 4 bytes | `%f` | `%f` |
| `double` | 8 bytes | `%f` | `%lf` |
| pointer | 8 bytes (64-bit) | `%p` | — |
| `size_t` | platform-dependent | `%zu` | — |

### Control Flow Skeletons

```c
if (condition) { }
else if (condition) { }
else { }

switch (x)
{
    case 1: break;
    default: break;
}

while (condition) { }
do { } while (condition);
for (int i = 0; i < n; i++) { }
```

### Function Skeleton

```c
return_type function_name(type param1, type param2)
{
    /* body */
    return (value);
}
```

### Pointer Quick Reference

```c
int x = 5;
int *p = &x;    // p holds the address of x
*p = 10;         // modifies x through p
p++;              // moves to the next int-sized address
```

### Dynamic Memory Quick Reference

```c
int *p = malloc(n * sizeof(int));
if (p == NULL) { /* handle error */ }
free(p);
p = NULL;
```

### Struct Quick Reference

```c
typedef struct
{
    int x;
    int y;
} Point;

Point pt = {1, 2};
Point *ptr = &pt;

ptr->x = 10;      // via pointer
pt.y = 20;         // direct
```

---

## ASCII Table (Common Values)

| Char | Dec | Char | Dec | Char | Dec |
|---|---|---|---|---|---|
| `NUL` | 0 | `A`–`Z` | 65–90 | `a`–`z` | 97–122 |
| `\n` | 10 | `0`–`9` | 48–57 | `space` | 32 |
| `\t` | 9 | `!` | 33 | `?` | 63 |
| `\0` | 0 | `[` | 91 | `]` | 93 |

Key anchors worth memorizing:

```
'A' = 65     'a' = 97     '0' = 48
'Z' = 90     'z' = 122    '9' = 57
```

Difference between uppercase and lowercase of the same letter is always **32**:

```c
'a' - 'A' == 32
```

---

## Data Type Sizes (Typical, 64-bit Linux)

| Type | Size |
|---|---|
| `char` | 1 byte |
| `short` | 2 bytes |
| `int` | 4 bytes |
| `long` | 8 bytes |
| `long long` | 8 bytes |
| `float` | 4 bytes |
| `double` | 8 bytes |
| pointer (`*`) | 8 bytes |

⚠️ Always confirm with `sizeof()` — these vary by platform and compiler.

---

## Operator Precedence (High → Low, Common Subset)

| Level | Operators |
|---|---|
| 1 | `()` `[]` `->` `.` |
| 2 | `!` `~` `++` `--` unary `+`/`-` `(type)` `*` (deref) `&` (address-of) `sizeof` |
| 3 | `*` `/` `%` |
| 4 | `+` `-` |
| 5 | `<<` `>>` |
| 6 | `<` `<=` `>` `>=` |
| 7 | `==` `!=` |
| 8 | `&` (bitwise AND) |
| 9 | `^` |
| 10 | `\|` |
| 11 | `&&` |
| 12 | `\|\|` |
| 13 | `?:` |
| 14 | `=` `+=` `-=` `*=` `/=` `%=` |

When in doubt, use parentheses — they cost nothing and remove all ambiguity.

---

## Common GCC Commands

```bash
gcc file.c -o program              # compile to executable "program"
gcc -Wall -Wextra -Werror file.c   # compile with all warnings as errors
gcc -g file.c -o program           # include debug symbols (for gdb)
gcc -c file.c                       # compile to object file only (.o)
gcc file1.o file2.o -o program      # link object files into an executable
gcc -o program *.c                  # compile all .c files in the directory
```

Recommended default for 42/1337 work:

```bash
gcc -Wall -Wextra -Werror -g file.c -o program
```

---

## Useful Terminal Commands

```bash
ls -la              # list all files, including hidden, with details
cd path/            # change directory
pwd                 # print working directory
mkdir name          # create a directory
rm file             # remove a file
rm -rf dir/         # remove a directory and its contents (use carefully)
cp src dst          # copy a file
mv src dst          # move or rename a file
cat file             # print file contents
man command          # open the manual page for a command
chmod +x file         # make a file executable
./program              # run an executable in the current directory
valgrind ./program      # check for memory leaks and invalid access
norminette file.c        # check 42 Norm compliance
```

---

## Glossary

| Term | Definition |
|---|---|
| **Argument** | The actual value passed to a function at the call site |
| **Array** | A fixed-size collection of same-type elements in contiguous memory |
| **Bit** | The smallest unit of data — `0` or `1` |
| **Buffer overflow** | Writing past the bounds of an allocated buffer |
| **Byte** | A group of 8 bits |
| **Compiler** | Translates source code into machine code |
| **Dangling pointer** | A pointer referencing memory that has been freed |
| **Declaration** | Tells the compiler a variable/function exists |
| **Definition** | Provides the actual implementation/storage |
| **Dereference** | Accessing the value a pointer points to, via `*` |
| **Fall-through** | Execution continuing into the next `switch` case without `break` |
| **Header file** | A `.h` file containing declarations shared across `.c` files |
| **Heap** | Memory region for dynamic allocation (`malloc`/`free`) |
| **Initialization** | Giving a variable its first value at declaration |
| **Linker** | Combines object files and libraries into an executable |
| **Memory leak** | Allocated memory that becomes unreachable without being freed |
| **NULL** | A pointer value representing "points to nothing" |
| **Null terminator** | `'\0'`, marks the end of a C string |
| **Overflow** | A value exceeding the range its type can represent |
| **Parameter** | The variable listed in a function's definition |
| **Pointer** | A variable that stores a memory address |
| **Recursion** | A function calling itself, with a base case to stop |
| **Scope** | Where a name is visible in the code |
| **Segmentation fault** | A crash from accessing memory the program doesn't own |
| **Stack** | Memory region for local variables and function calls |
| **Stack overflow** | Exhausting the Stack, often from unbounded recursion |
| **struct** | A user-defined type grouping related variables |
| **Undefined behavior (UB)** | Behavior the C standard does not define — anything can happen |
| **Variable** | A named location in memory that stores a value |

---

🎉 **End of the C Language Handbook.**

You've now covered the complete path from a single bit to dynamic memory, file I/O, and professional C style — the full foundation expected before and during the 1337/42 Piscine.
