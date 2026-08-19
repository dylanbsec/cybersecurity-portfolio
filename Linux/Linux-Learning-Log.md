## Entry 001 - Linux Command Review

**Date:** 7 July 2026

**Focus:** Reviewing basic Linux commands and practising in the CLI.

### Commands Practised

- `pwd` - Display the current working directory
- `ls` - List files and directories
- `cd` - Change directory
- `touch` - Create a new file
- `mkdir` - Create a new directory
- `rm` - Remove files and directories
- `cp` - Copy files and directories
- `mv` - Move or rename files and directories
- `cat` - Display the contents of a file

### Reflection

Today I reviewed Linux commands I had previously learned and practised them directly in the Athena OS terminal. This helped rebuild my confidence using the command line after taking some time away from cybersecurity.

### Next Steps

- Continue Linux practice through Pwn College.
- Learn file permissions and ownership.
- Practise commands without relying on notes.

## Entry 002 - Process Management & Secure File Transfer

**Date:** 12 July 2026

**Focus:** Learning Linux process management and secure file transfer through Hacknet.

### Commands Practised

- `ps` - Display running processes
- `kill` - Terminate a running process using its PID
- `scp` - Securely copy files between systems over SSH

### Reflection

I practised these commands while playing Hacknet. Although the environment is simulated, it provided an enjoyable way to become more comfortable using Linux commands in context rather than simply memorising them.

### Next Steps

- Continue learning Linux commands through practical use.
- Develop a better understanding of SSH and remote administration.

## Entry 003 - Multiple and Mixed Globs

**Date:** 14 July 2026

**Focus:** Using wildcard patterns to match specific groups of files in Bash.

### Commands Practised

- `*p*` - Match every filename containing the letter `p`
- `[cep]*` - Match filenames beginning with `c`, `e`, or `p`

### Reflection

I completed two pwn.college challenges covering multiple and mixed globs.

The first challenge reinforced that `*` can match any sequence of characters. I used `*p*` to select every filename containing the letter `p`.

The second challenge required combining a square bracket glob with `*` to match only `challenging`, `educational`, and `pwning`. I initially focused too much on letters shared within the filenames and overlooked the simpler pattern in their first letters.

After receiving guidance, I understood that `[cep]*` works because `[cep]` matches one starting character from the set, while `*` matches the rest of each filename.

### Next Steps

- Continue practising square bracket globs.
- Pay closer attention to simple filename patterns before testing more complicated expressions.
- Continue the pwn.college globbing module.

---

## Entry 004 - Exclusionary Globbing & Tab Completion

**Date:** 22 July 2026

**Focus:** Learning advanced globbing techniques and using Bash tab completion to safely navigate files and commands.

### Topics Covered

- Exclusionary globbing
- Character negation (`[! ]` and `[^ ]`)
- Safe file selection
- Tab completion
- Multiple tab completion options
- Command tab completion

### Commands Practised

- `[!pwn]*` / `[^pwn]*` - Match files that do **not** begin with the specified characters.
- `TAB` - Auto-complete filenames.
- Double `TAB` - Display available completion options when multiple matches exist.
- `TAB` on commands - Auto-complete executable command names.

### Reflection

Today I completed four pwn.college lessons covering more advanced Bash features.

I learned how exclusionary globbing can be used to match files that do not contain specific characters at a given position by using `!` or `^` inside square brackets. This provides a precise way to filter filenames without relying on broader wildcard patterns.

I also learned the importance of tab completion. Rather than relying on wildcards that may unintentionally match multiple files, tab completion allows filenames and commands to be completed safely and accurately. I practised completing unique filenames, resolving situations where multiple matches existed, and auto-completing executable commands.

These lessons reinforced that efficiency in the terminal should never come at the expense of accuracy. Features such as tab completion help reduce typing mistakes and lower the risk of executing commands against unintended files.

### Next Steps

- Progress on to the Practice Piping module on pwn.college.
- Become more comfortable combining globbing techniques.
- Build habits that prioritise safe and accurate command-line usage.

---

## Entry 005 - Linux Input & Output Redirection

**Date:** 19 August 2026

**Focus:** Understanding Linux standard communication channels and redirecting command output.

### Topics Covered

- Standard Input (`stdin`)
- Standard Output (`stdout`)
- Standard Error (`stderr`)
- Linux process input and output
- Output redirection
- The `>` redirection operator

### Commands Practised

- `echo` - Output text to standard output.
- `>` - Redirect standard output from the terminal into a file.
- `cat` - Display the contents of a file.

### Reflection

Today I started the pwn.college module on Linux input and output redirection.

I learned that Linux processes have three standard communication channels: **stdin** for receiving input, **stdout** for normal output, and **stderr** for error messages.

I then completed the first practical challenge on redirecting standard output. Instead of allowing the output from `echo` to appear in the terminal, I used the `>` operator to redirect it into a file:

`echo PWN > COLLEGE`

This helped demonstrate that command output does not necessarily have to be displayed on the terminal and can instead be redirected elsewhere.

### Next Steps

- Continue the pwn.college input and output redirection module.
- Learn additional methods of redirecting `stdout` and `stderr`.
- Explore how Linux commands can be chained together using their input and output streams.
