# simple_shell


Simple Shell is a basic UNIX command-line interpreter written in C. It provides a minimalistic shell environment with support for executing commands, built-in commands, environment variables, aliases, and more.

## Table of Contents

- [Features](#features)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [How to Compile](#how-to-compile)
- [Examples](#examples)
- [Authors](#authors)

## Features

- Execute external commands.
- Implement built-in commands such as `exit`, `env`, `cd`, and `alias`.
- Handle environment variables and aliases.
- Support for executing commands from files.
- Implement basic shell logical operators `&&` and `||`.
- Handle variable replacement using `$?` and `$$`.
- Interpret comments starting with `#`.
- Provide a user-friendly prompt and interactive mode.
- Display error messages and exit status matching `/bin/sh`.

## Usage

To use the Simple Shell, follow these steps:

1. Compile the shell using the provided compilation command.
2. Run the shell by executing `./hsh`.

In interactive mode, you can enter commands directly, and in non-interactive mode, you can use pipes to provide input.

## Project Structure

The project consists of the following files:

- `main.c`: The main entry point for the shell.
- `shell.c`: Contains shell execution logic and built-in command handling.
- `shell.h`: Header file with function prototypes, constants, and data structures.
- `alias.c`: Provides functionality for alias handling.
- `environment.c`: Manages environment variables.
- `utilities.c`: Contains utility functions used throughout the shell.

## Installation

To set up the Simple Shell on your system, follow these steps:

1. Clone the repository: `git clone https://github.com/001-Software-Engineer/simple-shell.git`
2. Change to the project directory: `cd simple-shell`

## How to Compile

Compile the shell using the provided compilation command:

```bash
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

Examples

    Execute an external command:

    shell

($) /bin/ls
file1  file2  file3
($)

Use built-in commands:

shell

($) exit
($)
($) env
HOME=/home/user
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
($)

Create and use aliases:

shell

($) alias myls='/bin/ls'
($) myls
file1  file2  file3
($)

Use variable replacement:

shell

($) /bin/ls
file1  file2  file3
($) echo $?
0
($)

Handle comments:

shell

($) # This is a comment
($)

Execute commands from a file:

shell

    ($) ./hsh < commands.txt

## Authors

- [Livingstone Bugali](https://github.com/001-Software-Engineer)
- [Mashau Ednah](https://github.com/Mashudu14)


Please customize the `README.md` with your project's specific details, authors, and any additional information you'd like to provide.

