# Build Your Own Password Manager

This is a (work-in-progress) tutorial that will teach you shell scripting by
showing you how to build the [pass](https://www.passwordstore.org/) password
manager in small steps.

## Assumptions

* Basic shell knowledge (`cd`, `ls`)
* Basic programming experience (variables, functions, conditionals, loops)
* Basic understanding of `git` will help in the section where we add git
  support (not too important)

## The Plan

1. A password generator
  * Step 1: `echo "correcthorsebatterystaple"`
  * Generate a random string
  * The `generate` command
  * The `version` command
  * The `help` command
2. Storing plaintext passwords
  * Save generated password to `$PREFIX`
  * The `show` command
  * Make `show` the default command
  * The `insert` command
  * The `rm` command
  * The `mv` command
  * The `cp` command
  * Subdirectories?
3. Encryption
  * The `init` command
  * GPG options and whether to use `gpg2`
  * `gpg_winpath()` for Cygwin
  * `set_gpg_recipients()`
  * Encrypt with `generate` and `insert` commands
  * Decrypt with `show` command
  * The `rm`, `mv`, and `cp` commands
  * Reencrypt using `init` command
4. Copy to clipboard
  * Generic `clip()`
  * Cygwin `clip()`
  * macOS `clip()`
  * `-c` option for `generate` and `show` commands
  * Pass line number to `-c` option
  * Clear clipboard after 45 seconds
  * Reset 45-second timer before starting a new one
  * Restore previous clipboard contents
5. QR codes
  * Generic `qrcode()`
  * macOS `qrcode()`
  * `-q` option for `generate` and `show` commands
6. Secure text editing
  * The `edit` command
  * Generic `tmpdir()`
  * Sourcing platform-dependent script files
  * macOS `tmpdir()`
  * OpenBSD `tmpdir()`
  * `noplaintext.vim`?
7. Listing and searching
  * The `ls` command
  * The `find` command
  * The `grep` command
8. Git
  * The `git` command
  * `set_git()`
  * `git_add_file()`
  * `git_commit()`
  * Add git support to `generate` and `insert` commands
  * Add git support to `edit`, `rm`, `mv`, `cp` commands
9. Completion
  * `bash` completion
  * `zsh` completion
  * `fish` completion
10. Signing and verification
  * Sign `.gpg_id` in `init` command
  * `verify_file()`
  * Sign git commits
11. Multiple users
  * `--path` option for `init` command
12. User extensions
  * `cmd_extension()`
  * An example: `pass-update`

