## The Minimalist IT Survival Guide
_For reasonable people and alike._

--- work in progress ---

This is a collection of tips for computer workers who need decent cross-platform tools.

---
### Collections of unix tools ###

[Busybox](https://www.busybox.net) _aims to be the smallest and simplest correct implementation of the_ ___standard Linux command line tools___, packaged as a single executable. With millions of installed copies, it's a proven and mature solution, unless you need special command line options. A subset has been ported to **Windows** as [busybox-w32](https://frippery.org/busybox) (500KB), which is also actively maintained and regularly synchronised with upstream. As a bonus, the **Almquist shell** `ash` is included.

[uutils](https://uutils.github.io) _aims to be a drop-in replacement for the_ ___GNU utils___, but modernized, reimplemented in Rust and working on _as many platforms as possible_. 

[PerlPowerTools](https://perlpowertools.com) (1MB, only the scripts) - **BSD utilities** written in pure Perl.

### Alternatives for Windows ###

[UnxUtils](https://en.wikipedia.org/wiki/UnxUtils) (6MB) ports of many **GNU utilities**, built as standalone executables (unmaintained since 2003).

If you just want to run Bash on Windows (now!), then installs [Git for Windows](https://gitforwindows.org) (380MB). It comes with **Git Bash**, over 200 utilities, `vim` and `perl`.

---

### Cross-platform scripting languages and shells ###

[Perl](https://www.perl.org) is reliable and available everywhere. Actively developped with a very strong backward-compatibility policy. The code you write today will probably still run in ten (or twenty) years[^2].

[Nushell](https://www.nushell.sh) is a modern, **cross-platform shell** that looks promising.

---

### Windows ###

**Windows is Windows**. It's not Posix compliant. Accept it.

`CMD.exe` is neither a terminal emulator nor a Unix shell. Beware that it doesn't do globbing (expansion). Quoting and escaping characters are a nightmare. One-liners won't work or - worse - they will fail in some cases.

However, `CMD.exe` is always available and has a low startup time. **Batch files** are double-clickable, familiar to many non-programmers and therefore an effective mechanism to distribute code. They are also the best solution to mimic shell aliases (and make `CMD.exe` tolerable).

- If you're serious about **Windows scripting**, learn `Powershell` immediately.
- If you want a **terminal**, have a look at [Windows Terminal](https://en.wikipedia.org/wiki/Windows_Terminal).
- If you want a **lightweight Unix shell**, I recommend the **Almquist shell** `ash` from [busybox-w32](https://frippery.org/busybox).
- If you want **bash on Windows**, use **Git Bash** from [Git for Windows](https://gitforwindows.org).

---

### Vim colors ###

Final word and reminder for myself : the color scheme [noctu.vim](https://github.com/noahfrederick/vim-noctu) uses only the 16 ANSI colors configured in the terminal emulator, so you get the same consistent colors for all programs (locally or remotely executed). [Source](https://jeffkreeftmeijer.com/vim-16-color/)

---

### Unix shell tips ###

The **most useful shell command** is `cd -` (change to previous directory)[^1].

---

For deduplicated, locally encrypted, **remote backup** check [BorgBackup](https://www.borgbackup.org/).

---

Robin Bowes [flac2mp3](https://github.com/robinbowes/flac2mp3) script is the best around for collection of files. Defaults to VBR v2, just needs `perl`, `flac` and `lame`.

---

[^1]: No, there's no way to make it work in CMD.exe.
[^2]: As of 2024.
