# bash-tip


## Introduction

The `tip` script provided here is inspired by the [cheat](https://github.com/cheat/cheat)
project.  If you've never used `cheat`, I encourage you to try it.

This utility is meant to be a more lightweight implementation of the same
idea with the code rewritten for the Bash shell.  The fancier features from
`cheat` are not present.  However, the core functionality of creating,
editing, and reading "cheat sheets" is intact.


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

## License

See the `LICENCSE` file.
