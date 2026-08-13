# Cheatsheet
### Condensed reference — C, GCC, Makefile, Shell. No explanations, just syntax. (See the handbooks for the "why.")

---

## C Syntax

```c
// Types
int  char  float  double  long  short  unsigned  void
size_t  ssize_t          // <stddef.h> / <unistd.h>

// Variables & pointers
int x = 5;
int *p = &x;
*p = 10;
int arr[5];
int arr2d[3][4];

// Structs
typedef struct s_point
{
    int x;
    int y;
}   t_point;

t_point pt = {1, 2};
t_point *ptr = &pt;
ptr->x;                   // arrow for pointer-to-struct
pt.x;                     // dot for direct struct access

// Control flow
if (cond) {} else if (cond) {} else {}
while (cond) {}
for (int i = 0; i < n; i++) {}
do { } while (cond);
switch (x) { case 1: break; default: break; }

// Functions
int add(int a, int b) { return (a + b); }
void print_thing(void);           // no args
int  *make_array(int size);       // returns pointer

// Ternary
int max = (a > b) ? a : b;

// Bitwise
&  |  ^  ~  <<  >>

// Common string.h / stdlib.h
strlen(s)  strcpy(dst,src)  strcat(dst,src)  strcmp(a,b)  strncmp(a,b,n)
strdup(s)  strchr(s,c)      strrchr(s,c)     strstr(hay,needle)
malloc(n)  free(p)          calloc(n,size)   realloc(p,n)
atoi(s)    itoa (not standard — you write your own in libft)
memset(p,val,n)  memcpy(dst,src,n)  memmove(dst,src,n)
```

---

## GCC

```bash
gcc -Wall -Wextra -Werror file.c -o program     # standard compile line
gcc -c file.c -o file.o                          # compile only, no link
gcc file.o -o program                             # link only
gcc main.c -Iinclude -L. -lft -o program           # with a library
gcc -Wall -Wextra -Werror -g -fsanitize=address file.c -o file   # debug build
```

```bash
ar rcs libft.a *.o          # build a static library
```

---

## Makefile skeleton

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

---

## Debugging

```bash
gdb ./program
  run / break <loc> / next / step / continue / print <var> / backtrace / quit

valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./program
```

---

## Shell — Navigation & Files

```bash
pwd  ls -la  cd path  cd -  cd ..
mkdir -p a/b/c
touch file.c
cp -r src/ dst/
mv old new
rm -rf folder/        # pwd + ls FIRST, always
ln -s target link
```

## Shell — Viewing / Searching

```bash
cat file        less file        head -20 file       tail -f file
wc -l file
find . -name "*.c" -type f
grep -Rn "pattern" .
diff -u file1 file2
```

## Shell — Permissions

```bash
chmod +x script.sh
chmod 644 file      # rw- r-- r--
chmod 755 program   # rwx r-x r-x
```

## Shell — Redirection / Pipes

```bash
cmd > file            # overwrite stdout
cmd >> file            # append stdout
cmd 2> errors.txt       # stderr only
cmd > out.txt 2>&1       # both, same file
cmd1 | cmd2               # pipe
find . -name "*.c" | xargs wc -l
```

## Shell — Processes

```bash
ps aux | grep name
kill PID       # polite
kill -9 PID     # force
cmd &            # background
jobs  bg  fg
```

## Shell — Archives

```bash
tar -czvf archive.tar.gz folder/
tar -xzvf archive.tar.gz
```

## Shell — Git (not covered elsewhere — added since you'll use it daily)

```bash
git status
git add file / git add .
git commit -m "message"
git push
git pull
git log --oneline
git diff
git checkout -b branch-name
git branch
```

---

## C Standard Compile + Run, One Block

```bash
gcc -Wall -Wextra -Werror main.c -o main && ./main
```
