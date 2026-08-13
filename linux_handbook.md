# The Complete Linux Command Line Handbook
### For 1337 / 42 Network Piscine Preparation

A self-contained reference for the shell commands, concepts, and habits you need. Every section ends with a short drill. Where the source material had gaps or slightly loose explanations, they're corrected here rather than repeated.

---

## Table of Contents

1. Navigation — `pwd`, `ls`, `cd`, `tree`
2. File & Directory Operations — `mkdir`, `touch`, `cp`, `mv`, `rm`, `rmdir`, `ln`
3. Viewing & Reading Files — `cat`, `less`, `head`, `tail`, `wc`, `nl`
4. Comparing Files — `diff`, `cmp`, `file`
5. Sorting & Filtering Text — `sort`, `uniq`
6. Searching — `find`, `grep`, `which`, `whereis`, `locate`
7. Permissions — `chmod`, `chown`, `chgrp`, `umask`
8. Redirection, Pipes & Wildcards *(missing from most beginner references — essential)*
9. Processes — `ps`, `top`, `htop`, `kill`, `killall`, `jobs`, `bg`, `fg`
10. Archives & Compression — `tar`, `zip`/`unzip`, `gzip`/`gunzip`
11. Networking — `ping`, `curl`, `wget`, `ssh`, `scp`
12. System Information — `uname`, `whoami`, `id`, `df`, `du`, `free`, `uptime`
13. Package Management — `apt`
14. Environment & Shell Basics — `echo`, `export`, `alias`, `history`, `man`
15. Common Beginner Traps (cross-cutting)
16. Full Quick-Reference Cheat Sheet

---

## 1. Navigation

### `pwd` — print working directory

```bash
pwd
```

Prints the absolute path of where you currently are. It doesn't move you anywhere — it only reports. When something behaves unexpectedly, `pwd` is the first sanity check, especially before running anything destructive.

### `ls` — list directory contents

```bash
ls           # current directory
ls -l        # long format: permissions, owner, size, modified date
ls -a        # include hidden files (names starting with .)
ls -la       # both combined
ls -lh       # long format with human-readable sizes (K/M/G instead of raw bytes)
ls -R        # recursive — lists subdirectories' contents too
ls -t        # sort by modification time, newest first
ls -S        # sort by file size, largest first
```

Files starting with `.` (like `.bashrc`, `.git`) are "hidden" only in the sense that plain `ls` skips them — they're ordinary files, not protected or special. `ls -a` reveals them.

### `cd` — change directory

```bash
cd                      # go to your home directory
cd ~                    # same thing
cd /                    # go to filesystem root
cd ..                   # go up one level
cd -                    # go back to the previous directory you were in
cd relative/path        # relative to where you are now
cd /absolute/path       # exact path regardless of where you are
```

`cd -` is genuinely useful and often skipped in beginner guides — it toggles between your last two locations, handy when bouncing between two working directories.

### `tree` — visualize directory structure

```bash
tree           # full tree from current directory
tree -L 2      # limit depth to 2 levels
tree -d        # directories only, no files
tree -a        # include hidden files
```

Not installed by default on most systems (`sudo apt install tree`). Genuinely useful once a project grows past a handful of files — better than repeated `ls`.

### Drill
From your home directory, navigate three levels deep into a nested path, then get back to where you started using `cd -` instead of typing the path again.

---

## 2. File & Directory Operations

### `mkdir` — make directories

```bash
mkdir project                    # single directory
mkdir day01 day02 day03          # multiple at once
mkdir -p project/src/include     # create nested path in one shot, no error if parents don't exist yet
```

Without `-p`, `mkdir project/src` fails if `project` doesn't already exist — `-p` creates the whole chain of parent directories as needed. This is the version you'll actually use in practice.

### `touch` — create empty files / update timestamps

```bash
touch hello.c
touch main.c utils.c README.md
```

`touch` does **not** write content — it creates a zero-byte file if none exists, or updates the file's modification timestamp if it does. This timestamp behavior is not just trivia: `make` decides whether to rebuild a target by comparing timestamps (see the Makefile handbook), so understanding that `touch` updates mtime — and can be used deliberately to force a rebuild — is a real, not cosmetic, use case.

### `cp` — copy

```bash
cp file.c backup.c            # copy a file
cp file.c projects/           # copy into a directory
cp -r project backup_project  # copy a directory and everything inside it (required for directories)
cp -i file.c dest.c           # ask before overwriting
```

`-r` (recursive) is mandatory for directories — `cp` without it refuses to copy a directory and errors out.

### `mv` — move or rename

```bash
mv old.txt new.txt        # rename (same directory)
mv file.c projects/       # move into another directory
mv old_dir new_dir        # rename a directory
```

`mv` is *both* rename and move — which one happens depends entirely on whether the destination is a new filename or an existing directory. There's no separate "rename" command in Linux; this is a deliberate design choice, not a limitation.

### `rm` — delete

```bash
rm file.c              # delete a file
rm -i file.c            # ask for confirmation first
rm -r project           # delete a directory and its contents
rm -rf project          # same, but force — no confirmation, no error if it doesn't exist
```

**This deserves more weight than most references give it:** Linux has no trash bin at the shell level. `rm -rf` is not reversible through any built-in undo. There is no confirmation prompt with `-f`, and combined with `-r` it will silently delete an entire directory tree. Before running `rm -rf` on anything, run `pwd` and `ls` first, every time, without exception — this is the single most damage-causing command in this entire handbook if used carelessly. Never run `rm -rf` with a variable path you haven't manually verified (a classic catastrophic bug is a script where a path variable ends up empty, turning `rm -rf $DIR/*` into `rm -rf /*`).

### `rmdir` — delete empty directories only

```bash
rmdir empty_folder
```

Fails if the directory has anything inside it. In practice `rm -r` is used far more often since it handles both empty and non-empty directories; `rmdir` is a safety-oriented tool for when you specifically want to guarantee you're not about to delete something with contents.

### `ln` — links

```bash
ln file.txt hardlink        # hard link
ln -s file.txt symlink      # symbolic (soft) link
```

**Correction/expansion on what the original material glossed over:** a hard link is not "similar to" the original file — it *is* the same underlying data (same inode) under a second name; editing one edits both, and the data is only actually deleted once every hard link to it is removed. Hard links cannot cross filesystems/partitions and cannot point at directories. A symbolic link is different: a small file that just stores a path to the target — it *can* cross filesystems and *can* target directories, but if the original is deleted, the symlink becomes "dangling" (broken) — unlike a hard link, which keeps the data alive.

### Drill
Create a file, make a hard link and a symlink to it. Delete the original file. Check whether the hard link still contains data (`cat hardlink`) versus whether the symlink is now broken (`ls -l symlink` will show it in red / as broken, or `cat symlink` errors).

---

## 3. Viewing & Reading Files

### `cat` — print file contents

```bash
cat file.c              # dump whole file to terminal
cat file1 file2          # concatenate and print both
cat -n file.c            # with line numbers
cat > notes.txt          # create a file, type content, Ctrl+D to save and exit
cat >> notes.txt         # append instead of overwrite
```

Fine for short files; unreadable for anything long since it dumps everything at once with no pagination.

### `less` — paginated file viewer

```bash
less README.md
```

| Key | Action |
|---|---|
| `Space` | Next page |
| `b` | Previous page |
| `/text` | Search forward for "text" |
| `n` | Next search match |
| `q` | Quit |

Use this instead of `cat` for anything longer than a screen — logs, long source files, man pages. (`more` is an older, more limited predecessor; on modern systems `less` is strictly better and is what you should default to — `more` is worth recognizing by name but not worth practicing.)

### `head` / `tail` — first/last lines

```bash
head file.c          # first 10 lines (default)
head -20 file.c       # first 20 lines
tail file.c           # last 10 lines
tail -20 file.c       # last 20 lines
tail -f logfile       # keep the file open and print new lines as they're appended — live monitoring
```

`tail -f` is the one worth internalizing beyond copy-paste knowledge: it's how you watch a log file update in real time instead of re-running `cat` repeatedly.

### `wc` — word/line/byte count

```bash
wc file.c        # lines, words, bytes — all three, in that order
wc -l file.c      # lines only
wc -w file.c      # words only
wc -c file.c      # bytes
wc -m file.c      # characters (differs from -c only when the file has multi-byte UTF-8 characters)
```

### `nl` — number lines

```bash
nl file.c
```

Similar to `cat -n` but with more formatting control; rarely needed beyond quick reference when discussing a specific line number with someone.

### Drill
Generate a file with 200 lines (`seq 1 200 > numbers.txt`), then use `head`, `tail`, and `wc -l` together to confirm the file has exactly 200 lines without opening it in an editor.

---

## 4. Comparing Files

*(This category existed only as a table-of-contents heading in the source material with zero content underneath — filled in here.)*

### `diff` — show differences between two files

```bash
diff file1.c file2.c
diff -u file1.c file2.c    # unified format — the format used by patches and git diffs, far more readable
```

Output uses `<` for lines only in the first file, `>` for lines only in the second. `-u` format is what you'll actually recognize from Git output — worth using by default.

### `cmp` — byte-by-byte comparison

```bash
cmp file1 file2
```

Reports the position of the *first* byte that differs, then stops — doesn't show you everything different like `diff` does. Useful for binary files where `diff`'s line-based logic doesn't apply cleanly.

### `file` — identify file type

```bash
file mystery_file
```

Inspects the actual content/structure of a file rather than trusting its extension — tells you if something is really an ELF executable, ASCII text, a PNG image, etc., regardless of what it's named. Useful for figuring out what a file actually is when the name is misleading or missing.

### Drill
Rename a `.c` file to have no extension at all, then run `file` on it and confirm it still correctly identifies it as C source / ASCII text.

---

## 5. Sorting & Filtering Text

*(Also promised in the table of contents, never written — filled in here.)*

### `sort`

```bash
sort names.txt              # alphabetical
sort -n numbers.txt          # numeric order (alphabetical sort gets "10" before "2" — wrong for numbers)
sort -r names.txt            # reverse order
sort -k2 data.txt            # sort by the 2nd column
```

**Important correction to a common beginner assumption:** plain `sort` is alphabetical/lexical, not numeric. `sort` on `10, 2, 33` without `-n` gives `10, 2, 33` (string order), not `2, 10, 33`. Always use `-n` for numeric data.

### `uniq`

```bash
uniq file.txt         # removes adjacent duplicate lines
sort file.txt | uniq   # removes ALL duplicates (uniq alone only catches adjacent ones)
uniq -c file.txt       # prefix each line with a count of how many times it appeared
```

**Key gotcha worth stating explicitly:** `uniq` only removes duplicates that are *directly next to each other* in the file — it does not scan the whole file for repeats. That's why `uniq` is almost always used after `sort`, which groups identical lines together first.

### Drill
Create a file with repeated but non-adjacent lines. Run `uniq` alone (nothing removed) versus `sort file | uniq` (actually deduplicated). Confirm you understand why.

---

## 6. Searching

### `find` — search the filesystem

```bash
find . -name "*.c"           # all .c files from current directory down
find . -iname "readme.md"    # case-insensitive name match
find . -type f                # files only
find . -type d                # directories only
find . -empty                 # empty files/directories
find . -size +10M             # larger than 10 MB
find . -mtime -1              # modified in the last 1 day
```

Searches recursively by default from wherever you point it. Avoid `find /` (searches the entire filesystem, slow and mostly irrelevant) — scope it to the smallest directory that could contain what you want.

### `grep` — search inside file contents

```bash
grep "main" file.c              # lines containing "main"
grep -i "hello" file.c           # case-insensitive
grep -n "printf" file.c          # show line numbers
grep -R "printf" .               # recursive through a directory tree
grep -v "TODO" file.c            # invert match — show lines that DON'T match
grep -c "error" logfile          # count matching lines
grep -rl "printf" .              # recursive, list only filenames that match (not the matching lines themselves)
```

One of the most-used commands in real development, not just the Piscine — searching your own codebase for where a function is defined/used is a daily action.

### `which` vs `whereis`

```bash
which gcc        # path to the executable that would run if you typed "gcc"
whereis gcc       # executable + man page + source, if available
```

`which` answers "what will actually run" — critical when you have multiple versions of a tool installed and aren't sure which one is on your `PATH`. `whereis` gives a broader but less precise picture.

### `locate`

```bash
locate filename
sudo updatedb    # refresh locate's database — it's a cached index, not a live search
```

Fast because it searches a prebuilt database rather than scanning the disk live — but that also means it can return stale results (or miss recently created files) until `updatedb` runs. Often not installed by default; `find` is slower but always accurate, and is what you should default to unless you specifically know `locate`'s database is fresh.

### Drill
Use `find` to list every `.c` file in your project, then pipe that into `xargs grep -l "main"` to find which of those files contain a `main` function — your first taste of combining tools (more on this in Section 8).

---

## 7. Permissions

Linux permissions apply to three actors — **owner (user)**, **group**, **others** — and three actions — **read (r)**, **write (w)**, **execute (x)**.

### Reading `ls -l` output

```
-rwxr-xr-x
```

Position 1: `-` = regular file (`d` = directory, `l` = symlink). Then three groups of three: owner (`rwx`), group (`r-x`), others (`r-x`).

### `chmod` — change permissions

```bash
chmod +x script.sh       # add execute permission
chmod -x script.sh       # remove execute permission
chmod 644 file.c          # rw- r-- r-- : owner read/write, everyone else read-only
chmod 755 program         # rwx r-x r-x : owner full access, everyone else read+execute
chmod 600 secret.txt      # rw- --- --- : owner only
```

**Numeric permission logic** (worth actually understanding, not memorizing as magic numbers): each digit is a sum — read=4, write=2, execute=1. `7 = 4+2+1` (rwx), `6 = 4+2` (rw-), `5 = 4+1` (r-x), `4` = (r--). Once you know this, you can derive any combination instead of memorizing a table of presets.

**Avoid `chmod 777`** — it grants everyone read/write/execute, which is almost never actually what you want and is a common beginner "fix" that just papers over a misunderstanding of what permission was actually missing.

### `chown` / `chgrp`

```bash
sudo chown username file.txt          # change owner
sudo chown username:groupname file.txt # change owner and group together
sudo chgrp groupname file.txt          # change group only
```

Both typically require `sudo` since changing ownership is an administrative action. Rare in Piscine day-to-day work — you're almost always working with files you already own.

### `umask`

```bash
umask         # show current default permission mask
umask 022      # set it
```

Determines the default permissions new files/directories get when created, before any explicit `chmod`. Worth knowing it exists; rarely something you'll change deliberately during the Piscine.

### Drill
Create a shell script, confirm it has no execute permission by default (`./script.sh` fails with "Permission denied"), then `chmod +x` it and run it successfully.

---

## 8. Redirection, Pipes & Wildcards

**This entire category was absent from the source material's table of contents — and it's arguably more important day-to-day than several sections that were included.** Every serious shell user relies on this constantly.

### Redirection

```bash
command > file        # redirect stdout to a file, OVERWRITING it
command >> file        # redirect stdout, APPENDING instead
command < file          # use a file as stdin
command 2> errors.txt   # redirect stderr (error output) specifically
command > out.txt 2>&1  # redirect both stdout and stderr to the same file
```

Every running program has three standard streams: **stdin** (input), **stdout** (normal output), **stderr** (error output) — they're separate channels even though both stdout and stderr print to your terminal by default, which is why `2>` lets you split errors away from normal output.

### Pipes — `|`

```bash
cat file.c | grep "main"
ls -la | wc -l
ps aux | grep firefox
find . -name "*.c" | xargs wc -l
```

A pipe takes the stdout of the command on the left and feeds it as stdin to the command on the right. This is the core idea that makes the Unix philosophy work: small single-purpose tools, chained together, instead of one giant tool trying to do everything.

### Wildcards / globbing

```bash
ls *.c              # every file ending in .c
rm *.o               # every file ending in .o
cp day*/notes.md backups/   # every "day..." directory's notes.md
ls file?.txt         # matches file1.txt, fileA.txt — ? is exactly one character
```

`*` matches any sequence of characters (including none), `?` matches exactly one character. This is expanded by the *shell itself* before the command ever runs — `rm *.o` doesn't pass the literal string `*.o` to `rm`; the shell expands it into the actual list of matching filenames first. This matters because it means `echo *.c` will show you exactly what a command would operate on before you run something destructive with the same pattern.

### Command substitution

```bash
echo "Today is $(date)"
files=$(ls *.c)
```

`$(...)` runs the command inside and substitutes its output as text. The older backtick syntax `` `command` `` does the same thing but `$(...)` is preferred — it nests cleanly, backticks don't.

### Drill
Write a command that lists every `.c` file in a directory, counts how many lines each one has, and saves the result to a file — using `find`, a pipe, `wc -l`, and `>` together in one line.

---

## 9. Processes

### `ps` — process snapshot

```bash
ps           # your current shell's processes only
ps -e         # every process on the system
ps -ef        # full detail, every process
ps aux        # BSD-style detailed listing (very commonly used)
```

`ps` shows a snapshot at the moment you run it — it does not auto-update. For that, use `top`.

### `top` / `htop` — live process monitor

```bash
top
htop     # nicer interface, not installed by default: sudo apt install htop
```

| Key (in `top`) | Action |
|---|---|
| `q` | Quit |
| `k` | Kill a process (prompts for PID) |
| `h` | Help |

`htop` adds color, mouse support, and easier scrolling/killing — genuinely worth installing.

### `kill` / `killall`

```bash
kill 1234          # send SIGTERM (polite "please stop") to process ID 1234
kill -9 1234         # send SIGKILL (immediate, un-ignorable termination)
killall firefox      # kill every process matching a name, not just one PID
```

**Correction worth making explicit:** `kill` doesn't necessarily kill anything by default — it sends a *signal*, and `SIGTERM` (the default, signal 15) is a request the target process can catch and handle gracefully (e.g., save state before exiting). `-9` (`SIGKILL`) cannot be caught or ignored — the OS terminates the process immediately. Use plain `kill` first; reach for `-9` only if the process is unresponsive to the polite request.

### `jobs`, `bg`, `fg` — job control

```bash
long_command &    # run in the background immediately (note the &)
jobs               # list background/suspended jobs in this shell
bg                 # resume a suspended job in the background
fg                 # bring a background job to the foreground
```

Workflow: you start a command, realize it'll take a while, press `Ctrl+Z` to suspend it, run `bg` to let it continue in the background while you get your terminal back, then `fg` later to bring it back to the foreground. `jobs` shows you what's currently running/suspended in that shell session.

### Drill
Run `sleep 60 &`, then use `jobs` to confirm it's running in the background, then `kill` it by its job number or PID before the 60 seconds finish.

---

## 10. Archives & Compression

*(Table-of-contents heading with no content in the source — filled in here.)*

### `tar` — archive (bundle) files

```bash
tar -cvf archive.tar folder/        # create
tar -xvf archive.tar                 # extract
tar -tvf archive.tar                 # list contents without extracting
tar -czvf archive.tar.gz folder/     # create + gzip-compress in one step
tar -xzvf archive.tar.gz             # extract a gzip-compressed tarball
```

Flags: `c`=create, `x`=extract, `v`=verbose (show progress), `f`=file (must be followed by the archive filename — always last in the flag group), `z`=gzip compression. `tar` on its own only *bundles* files together — it doesn't compress unless you add `z` (gzip) or `j` (bzip2).

### `gzip` / `gunzip`

```bash
gzip file.txt        # compresses file.txt into file.txt.gz, REMOVES the original
gunzip file.txt.gz    # reverses it
```

Only compresses a single file — this is exactly why it's normally paired with `tar` (bundle many files into one, *then* compress the bundle).

### `zip` / `unzip`

```bash
zip archive.zip file1 file2
zip -r archive.zip folder/    # recursive, for directories
unzip archive.zip
```

Unlike `tar`+`gzip`, `zip` bundles *and* compresses in one step natively — more common when interoperating with Windows/macOS users, since `.zip` is more universally recognized than `.tar.gz`.

### Drill
Archive a project folder with `tar -czvf`, delete the original folder, then restore it with `tar -xzvf` and confirm everything's intact.

---

## 11. Networking

### `ping`

```bash
ping google.com
ping -c 4 google.com    # stop after 4 packets instead of running forever
```

Tests basic reachability/latency to a host. Always use `-c` in scripts or you'll need to `Ctrl+C` it manually.

### `curl` / `wget`

```bash
curl https://example.com              # print a URL's content to the terminal
curl -O https://example.com/file.zip   # download, keeping the remote filename
curl -o myname.zip https://example.com/file.zip  # download with a chosen filename
wget https://example.com/file.zip      # download-focused, simpler for straightforward file grabs
```

`curl` is more general-purpose (can send custom headers, POST data, interact with APIs); `wget` is more specialized for straightforward downloads and can resume interrupted ones easily. Both are commonly available; use whichever the task calls for — `curl` if you need to actually inspect/manipulate an HTTP request, `wget` for "just get me this file."

### `ssh` / `scp`

```bash
ssh username@hostname                  # remote shell login
scp file.txt username@hostname:/path/  # copy a file TO a remote machine
scp username@hostname:/path/file.txt . # copy a file FROM a remote machine
```

`scp` syntax mirrors `cp` — source, then destination — just with `user@host:path` for whichever side is remote.

### Drill
`ping -c 4` a domain you recognize and confirm you can read the round-trip time in the output — this is the fastest way to sanity-check "is my network even working" before debugging anything more complex.

---

## 12. System Information

```bash
uname -a       # kernel name, version, architecture — full system info
whoami          # your current username
id               # your user ID, group ID, and group memberships
date             # current date/time
uptime           # how long the system has been running, plus load average
df -h            # disk space usage per filesystem, human-readable
du -sh folder/   # total size of a specific folder, human-readable
free -h          # RAM usage, human-readable
```

`df` (disk free) shows space at the filesystem/partition level; `du` (disk usage) shows space consumed by a specific file or directory tree — a common point of confusion since the names sound similar but answer different questions ("how much space is left on the disk" vs. "how much space does this folder take up").

### Drill
Run `du -sh` on your home directory versus `df -h` on the whole system — articulate in your own words why the numbers answer different questions.

---

## 13. Package Management

```bash
sudo apt update              # refresh the list of available packages (does NOT install/upgrade anything itself)
sudo apt upgrade              # actually upgrade installed packages to newer available versions
sudo apt install package      # install a new package
sudo apt remove package       # uninstall, keep config files
sudo apt purge package        # uninstall, remove config files too
sudo apt search keyword        # search available packages
```

**Common beginner confusion worth clearing up directly:** `apt update` does not upgrade anything — it only refreshes apt's local index of what versions are available. People frequently run `apt update` expecting their software to be upgraded and are confused when nothing changes; that's `apt upgrade`'s job.

---

## 14. Environment & Shell Basics

```bash
echo "hello"                 # print text
echo $HOME                    # print an environment variable's value
env                            # list all environment variables
export MY_VAR="value"          # set an environment variable for this shell and any child processes
alias ll="ls -la"              # create a shortcut command
history                        # show your command history
!457                            # re-run command number 457 from history
man command                     # full manual page for a command
command --help                  # quick usage summary (faster than man for a quick reminder)
```

`export` matters specifically because a plain variable assignment (`MY_VAR=value`) is only visible in the *current* shell — `export` makes it visible to any program or subshell launched from this one. This is why `PATH`, for instance, has to be exported for other programs to see it.

`alias` definitions set with the command above only last for the current session — to make one permanent, add the line to `~/.bashrc` (or `~/.zshrc`, depending on your shell).

### Drill
Add a permanent alias to your shell config file for a command you type often (e.g. `alias gcw="gcc -Wall -Wextra -Werror"`), reload the config with `source ~/.bashrc`, and confirm it works in a new terminal without re-running the alias command.

---

## 15. Common Beginner Traps (Cross-Cutting)

- **`rm -rf` without checking `pwd` first** — the single highest-damage mistake in this whole list. No confirmation, no trash bin, no undo.
- **Confusing `apt update` with `apt upgrade`** — see Section 13.
- **Assuming `sort` is numeric by default** — it's lexical; use `-n` for numbers.
- **Assuming `uniq` deduplicates a whole file** — it only catches adjacent duplicates; pipe through `sort` first.
- **Running `find /`** — searches the entire filesystem, slow and almost never what you actually want; scope it.
- **Forgetting `-r`/`-R` on directories** — `cp`, `rm`, `chmod`, `chgrp`, and `grep` all need a recursive flag to operate on directory contents; without it they either fail or only touch the top-level item.
- **Chmod 777 as a "fix"** — almost always papers over a misdiagnosed permission problem instead of solving it.

---

## 16. Full Quick-Reference Cheat Sheet

```bash
# Navigation
pwd; ls -la; cd path; cd -; tree -L 2

# Files & directories
mkdir -p a/b/c
touch file.c
cp -r src/ backup/
mv old.txt new.txt
rm -rf folder/        # ALWAYS pwd + ls first
ln -s target linkname

# Viewing
cat file.c
less file.c
head -20 file.c
tail -f logfile
wc -l file.c

# Comparing
diff -u file1 file2
cmp file1 file2
file mystery

# Sorting/filtering
sort -n numbers.txt
sort file.txt | uniq -c

# Searching
find . -name "*.c" -type f
grep -Rn "pattern" .
which gcc

# Permissions
chmod 755 script.sh
chmod +x script.sh

# Redirection & pipes
command > out.txt 2>&1
find . -name "*.c" | xargs wc -l

# Processes
ps aux | grep processname
kill -9 PID
sleep 60 &
jobs

# Archives
tar -czvf archive.tar.gz folder/
tar -xzvf archive.tar.gz

# Networking
ping -c 4 google.com
curl -O https://example.com/file

# System info
df -h; du -sh folder/; free -h; uname -a

# Package management
sudo apt update && sudo apt upgrade
sudo apt install package

# Environment
export VAR="value"
alias ll="ls -la"
man command
```
