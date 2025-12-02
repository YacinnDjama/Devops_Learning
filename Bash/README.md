# Welcome to the Bash Scripting section of this repository.

## 📌 What Is Bash?

Bash (Bourne Again SHell) is a command-line interpreter and scripting language used on:
Linux
macOS
WSL (Windows Subsystem for Linux)
And any POSIX-compatible shell environment
It allows you to automate tasks, write tools, and interact with the system efficiently.

Also, it Works on Any Shell! (Including ZSH) 🌍

Although this section is about Bash, most of the scripts here run perfectly in other shells like:
ZSH
Dash
KornShell (ksh)
sh
ZSH users can even run Bash scripts explicitly using:
bash scriptname.sh

<p align="center"><b>💡Fun Fact: All Bash scripts begin with a shebang line: #!/bin/bash💡</b></p>
  
## ⁉️ Why Bash in VS Code?

VS Code makes Bash scripting much easier:
Syntax highlighting
Extensions like ShellCheck
Built-in terminal
Run scripts instantly
Easy file navigation and Git versioning
Clean environment for learning and testing
This is the best way to learn scripting because you can write + test at the same time.
The Shebang Line
The shebang tells your system which interpreter should run your script.

Example:
#!/bin/bash

This ensures your script always runs using Bash, no matter what your default shell is.


# 🔑 Key learning points in Bash:

## Comments

Comments in Bash are ignored by the interpreter and used to explain the purpose of commands or sections of a script. They start with the # symbol and help make scripts easier to read and maintain. Comments can be placed on their own line or at the end of a command.

## Parameters

Parameters allow you to pass information into a Bash script when you run it. Instead of hard-coding values, parameters make your script flexible by letting the user provide input at execution time. Each parameter is stored in a positional variable, which Bash automatically assigns based on the order the arguments are given.

* $1 represents the first argument
* $2 represents the second argument
* $@ contains all arguments
* $# shows the number of arguments passed
* Parameters are read-only values set at runtime

```bash 
 #!/bin/bash

echo "First argument: $1"
echo "Second argument: $2"
echo "All arguments: $@"
echo "Total arguments: $#"
 ```



## Piping

Piping allows you to connect commands so that the output of one command becomes the input of another. This makes it possible to build powerful command chains without creating temporary files. It’s commonly used for filtering, transforming, and processing text or data efficiently.

* Uses the | symbol
* Sends output from one command to another
* Often combined with tools like grep, awk, or tr
* Reduces the need for intermediate files
* Helps build complex operations from simple commands

```bash 
 #!/bin/bash

ls | grep ".sh"
 ```

## Set-x

set -x enables debugging mode in Bash. When activated, Bash prints each command to the terminal before executing it. This helps you understand the script’s behavior and identify mistakes or unexpected results. It is usually turned on only in specific sections during troubleshooting.

* Prints each command before execution
* Helps track script flow
* Useful for debugging complex scripts
* Can be turned on and off at any point
* Does not affect the script's logic, only displays what happens

```bash 
 #!/bin/bash

set -x
echo "Testing script..."
name="Yacin"
echo "Hello, $name"
set +x
 ```

