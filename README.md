# bash-tip


## Introduction

The `tip` script provided here is inspired by the [cheat](https://github.com/cheat/cheat)
project.  If you've never used `cheat`, I encourage you to try it.

This utility is meant to be a more lightweight implementation of the same
idea with the code rewritten in bash.  The fancier features from `cheat` are
not present.  However, the core functionality of creating, editing, and
reading "cheat sheets" is intact.


## Installation

To install `tip` as a personal program, clone this repository to your local
machine and copy the script into your `~/bin/` directory.  Next, decide on
a folder that you will use to store your tip files.  When you've made your
decision, add this line...

```bash
export TIP_DIR='/path/to/tips'
```

... to your `.profile` or `.bash_profile` script.  Log out and log back in
for the configuration change to take effect.  At this point, you can create
your first tip file with `tip -e COMMAND`.

The `tip -h` command will tell you everything else you need to know.


## Usage

Simply put, `tip` lets you create "tip files" to remind yourself at a later
time how to run a tricky command.

You may only run, for example, the `rsync` command rarely, and you don't
bother to remember how you did it.  If you add some reminders for yourself
in a tip file, the `tip rsync` command may show something like this:

```
# Sync from the "/path/to/foo" directory to the "/path/to/bar/foo" directory.
# Note that extraneous files in the destination will be preserved.
rsync -ahv /path/to/foo /path/to/bar

# A trailing slash on the source directory means to copy the contents of the
# source directory.  The above command is thus equivalent to:
rsync -ahv /path/to/foo/ /path/to/bar/foo/

# Use the "--delete" option to mirror the two directories.  That is, delete
# extraneous files in the destination directory.
rsync -ahv --delete /path/to/foo/ /path/to/bar/foo/

# The "-c" option will cause rsync to use a checksum to see if a file needs to
# be updated.  This is useful when you cannot rely on timestamps.
rsync -ac ~/src/foo/ ~/dest/foo/
```

This can be helpful when you want to avoid unnecessary trips to Stack
Overflow.

## License

See the `LICENCSE` file.
