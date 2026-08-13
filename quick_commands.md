# Quick Commands
### Task → command. Organized by what you're trying to do, not by tool name.

---

## "I want to compile my code"

| I want to... | Command |
|---|---|
| Compile one file with the standard flags | `gcc -Wall -Wextra -Werror file.c -o program` |
| Compile without linking | `gcc -c file.c -o file.o` |
| Compile several files at once | `gcc -Wall -Wextra -Werror main.c utils.c -o program` |
| Compile with debug symbols | `gcc -g file.c -o file` |
| Compile with a specific C standard | `gcc -std=c99 file.c -o program` |
| See the preprocessed output | `gcc -E file.c -o file.i` |
| See generated assembly | `gcc -S file.c -o file.s` |
| Link a library | `gcc main.c -L. -lft -o program` |
| Build a static library from .o files | `ar rcs libft.a *.o` |

## "I want to run make"

| I want to... | Command |
|---|---|
| Build using the Makefile | `make` |
| Force a full rebuild | `make re` |
| Remove object files only | `make clean` |
| Remove object files + binary | `make fclean` |
| Build a specific target | `make target_name` |
| See what make WOULD run, without running it | `make -n` |

## "Something broke and I need to debug it"

| I want to... | Command |
|---|---|
| Step through my program | `gdb ./program` then `run` |
| See the call stack after a crash | inside gdb: `backtrace` |
| Check for memory leaks | `valgrind --leak-check=full ./program` |
| Check for leaks with full detail | `valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./program` |
| Check for buffer overflows fast | `gcc -g -fsanitize=address file.c -o file && ./file` |

## "I need to find something"

| I want to... | Command |
|---|---|
| Find a file by name | `find . -name "filename"` |
| Find all .c files | `find . -name "*.c"` |
| Find text inside files | `grep -Rn "text" .` |
| Find which files contain a function name | `grep -Rl "function_name" .` |
| Check if a command exists / where it lives | `which command_name` |
| Count how many .c files exist | `find . -name "*.c" | wc -l` |

## "I need to move/copy/clean up files"

| I want to... | Command |
|---|---|
| Copy a file | `cp file.c backup.c` |
| Copy a whole folder | `cp -r folder/ backup_folder/` |
| Move / rename | `mv old.c new.c` |
| Delete a file | `rm file.c` |
| Delete a folder and everything inside | `rm -rf folder/` *(pwd + ls first — no undo)* |
| Create a folder + parent folders in one go | `mkdir -p path/to/folder` |
| Make a script executable | `chmod +x script.sh` |

## "I need to check permissions / ownership"

| I want to... | Command |
|---|---|
| See a file's permissions | `ls -l file` |
| Give owner rw, everyone else read-only | `chmod 644 file` |
| Give owner full access, everyone else read+execute | `chmod 755 file` |
| Add execute permission without changing anything else | `chmod +x file` |

## "I need to inspect a file"

| I want to... | Command |
|---|---|
| Print a whole file | `cat file` |
| Read a long file page by page | `less file` |
| See just the first lines | `head -20 file` |
| See just the last lines | `tail -20 file` |
| Watch a file update live (e.g. a log) | `tail -f file` |
| Count lines/words/bytes | `wc file` |
| Count lines only | `wc -l file` |
| Compare two files | `diff -u file1 file2` |
| Identify what type a file actually is | `file mystery_file` |

## "I need to manage a running process"

| I want to... | Command |
|---|---|
| See what's running | `ps aux` |
| Watch processes live | `top` (or `htop`) |
| Kill a process politely | `kill PID` |
| Force-kill an unresponsive process | `kill -9 PID` |
| Kill every process with a given name | `killall name` |
| Run something in the background | `command &` |
| See background jobs in this shell | `jobs` |
| Bring a background job to the foreground | `fg` |

## "I need to archive / compress"

| I want to... | Command |
|---|---|
| Bundle + compress a folder | `tar -czvf archive.tar.gz folder/` |
| Extract a .tar.gz | `tar -xzvf archive.tar.gz` |
| List a tarball's contents without extracting | `tar -tvf archive.tar` |

## "I need networking basics"

| I want to... | Command |
|---|---|
| Check if a host is reachable | `ping -c 4 hostname` |
| Download a file (keep original name) | `curl -O url` |
| Download a file (choose a name) | `wget -O name url` |
| Log into a remote machine | `ssh user@host` |
| Copy a file to a remote machine | `scp file.txt user@host:/path/` |

## "I need to check system status"

| I want to... | Command |
|---|---|
| Check disk space | `df -h` |
| Check how big a folder is | `du -sh folder/` |
| Check RAM usage | `free -h` |
| Check how long the system's been up | `uptime` |
| Check my username / user info | `whoami` / `id` |

## "I need Git basics"

| I want to... | Command |
|---|---|
| Check current status | `git status` |
| Stage everything | `git add .` |
| Commit | `git commit -m "message"` |
| Push | `git push` |
| Pull latest | `git pull` |
| See commit history, condensed | `git log --oneline` |
| See what changed, unstaged | `git diff` |
| Create + switch to a new branch | `git checkout -b branch-name` |
| Undo local changes to a file (careful — destructive) | `git checkout -- file` |

## "I want to save time typing"

| I want to... | Command |
|---|---|
| Re-run the last command | `!!` |
| Re-run a specific history entry | `!457` |
| Search command history interactively | `Ctrl + R`, then type |
| Repeat last argument of the previous command | `!$` |
| Make a permanent shortcut | add `alias name="command"` to `~/.bashrc`, then `source ~/.bashrc` |
