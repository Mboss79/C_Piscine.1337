# Terminal Tips
### Productivity habits and shortcuts — not command syntax (see quick_commands.md / cheatsheet.md for that). This is about being fast and not losing work.

---

## Keyboard shortcuts that save real time

| Shortcut | Effect |
|---|---|
| `Tab` | Auto-complete filenames, commands, paths — press twice to list all options if ambiguous |
| `Ctrl + A` | Jump cursor to the start of the line |
| `Ctrl + E` | Jump cursor to the end of the line |
| `Ctrl + U` | Delete from cursor to start of line |
| `Ctrl + K` | Delete from cursor to end of line |
| `Ctrl + W` | Delete the word before the cursor |
| `Ctrl + L` | Clear the screen (same as typing `clear`, but faster) |
| `Ctrl + C` | Kill/interrupt the currently running command |
| `Ctrl + D` | End input / exit the current shell (same as typing `exit`) |
| `Ctrl + R` | Search backward through command history — type a few letters, it finds the last matching command |
| `Ctrl + Z` | Suspend the current process (pauses it — use `bg`/`fg` to control it after, see quick_commands.md) |
| `↑` / `↓` | Step through command history one at a time |
| `Alt + .` (or `Esc` then `.`) | Insert the last argument of the previous command |

**The one habit worth building immediately:** stop retyping commands. `Ctrl + R` + a few characters finds almost anything you've run recently, faster than typing it out again — especially for long `gcc`/`valgrind` commands.

---

## Tab completion is not optional

Get in the habit of typing 2–3 characters of a filename and pressing `Tab` instead of typing the whole thing. Beyond saving keystrokes, it prevents typos in paths — a mistyped `rm` target is exactly the kind of mistake tab completion catches for you (if the file doesn't exist, tab completion won't complete it, which is itself a warning sign).

Double-`Tab` when it's ambiguous shows you every match instead of guessing — use it before running something destructive on a wildcard-based path you're not 100% sure of.

---

## History is more useful than people realize

```bash
history                # see your full history, numbered
!457                    # re-run entry 457
!!                      # re-run the previous command
!$                       # reuse the previous command's last argument
sudo !!                  # forgot sudo? re-run the last command WITH sudo
```

`sudo !!` specifically is worth remembering — you type a command, get "Permission denied," and instead of retyping the whole thing with `sudo` in front, `sudo !!` does it for you.

---

## Confirm before you destroy

Before any `rm -rf`, `git checkout --`, or overwrite-style redirection (`>`), get in the habit of running the read-only version first:

```bash
ls foldername/*.o        # see what WOULD be affected
echo *.c                  # see what a wildcard actually expands to before using it in rm
```

This costs two seconds and has no downside. Skipping it has no upside either — it's pure risk reduction, not slowdown.

---

## Multiple terminals / panes beat one crowded terminal

If your setup supports it (most 1337 clusters do), open a second terminal tab/pane instead of constantly clearing and re-scrolling one. A typical split:

- One pane: editing code
- One pane: compiling/running
- One pane free for `man`, `grep`, or `git status` checks

If you have access to `tmux` or `screen`, learning basic pane-splitting is worth the 20 minutes it takes — it lets you keep a long-running process (like a `tail -f` on a log) visible while working elsewhere, and survives disconnecting from a remote session without killing what was running.

---

## Reading errors top-to-bottom is usually wrong

When `gcc` throws a wall of errors, **read the first one first**, fix it, recompile. A single early mistake (a missing `;`, an unclosed brace) often cascades into a dozen unrelated-looking errors below it that all disappear once the real one is fixed. Scrolling to the bottom and trying to fix the last error first usually wastes time chasing symptoms.

---

## `man` and `--help` are faster than searching the web mid-task

```bash
man grep        # full manual, use / to search inside it, q to quit
grep --help      # quick flag summary, no need to leave the terminal
```

Once you're inside `man`, `/searchterm` then `n` for next match is the fast way to jump straight to the flag you're trying to remember, instead of reading top to bottom.

---

## Keep your prompt informative

If your shell doesn't already show your current directory and Git branch in the prompt, it's worth setting up — cuts down on redundant `pwd`/`git status` calls just to orient yourself. Not essential during the Piscine crunch, but a small one-time setup that pays off over weeks of terminal use.

---

## Aliases: automate what you type more than twice a day

```bash
alias gcw="gcc -Wall -Wextra -Werror"
alias ll="ls -la"
alias vg="valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes"
```

Add these to `~/.bashrc`, then `source ~/.bashrc` to load them without restarting the terminal. If you find yourself typing the same 40-character `valgrind` flag combo for the fifth time in a session, that's the signal to alias it — not a nice-to-have, a direct time cost you're paying repeatedly.

---

## Don't fight the shell — verify, then act

The recurring theme across all of the above: cheap verification (`pwd`, `ls`, `echo`, tab-complete, `man`) before an expensive or irreversible action (`rm -rf`, `git checkout --`, overwriting with `>`). None of these checks cost more than a second or two. The mistakes they prevent cost much more.
