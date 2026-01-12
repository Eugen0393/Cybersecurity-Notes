# Linux Basics: File System Navigation

| Command | Action |
| :--- | :--- |
| `pwd` | **P**rint **W**orking **D**irectory. Outputs the full path of the directory you are currently in. |
| `ls` | **L**i**s**t. Displays a list of files and subdirectories in the current directory. |
| `cd <folder>` | **C**hange **D**irectory. Moves you into the specified folder. |
| `cd ..` | Moves you up one level to the parent directory. |
| `cat <file>` | Con**cat**enate. Reads data from the file and outputs its content to the terminal. |
| `find . -name <file>` | Searches for a specific filename starting from the current directory (`.`). |
| `find . -name "*.txt"` | Searches for all files with a specific extension (e.g., `.txt`) in the current directory. |
| `grep "<text>" <file>` | **G**lobal **R**egular **E**xpression **P**rint. Searches for a specific string of text inside a file (e.g., searching for an IP in a log). |
| `man <command>` | Displays the **man**ual for a command. **Tip:** Press `q` to exit the manual. |

# Linux Basics: Shell Operators

| Operator | Description |
| :--- | :--- |
| `&` | Runs the command in the **background**, allowing you to continue using the terminal while it works. |
| `&&` | Logical **AND**. Allows you to chain commands. The second command runs only if the first one succeeds. |
| `>` | **Redirects** output to a file, **overwriting** any existing content in that file. |
| `>>` | **Redirects** output to a file, **appending** it to the end (does not delete existing content). |


# Linux Basics: File Manipulation

| Command | Action |
| :--- | :--- |
| `touch <filename>` | Creates a new empty file. |
| `mkdir <folder>` | **M**a**k**e **Dir**ectory. Creates a new folder (directory). |
| `cp <source> <destination>` | **C**o**p**y. Copies a file or folder from one location to another. |
| `mv <source> <destination>` | **M**o**v**e. Moves a file or folder. Also used to **rename** files. |
| `rm <file>` | **R**e**m**ove. Permanently deletes a specific file. |
| `rm -R <folder>` | **R**ecursive remove. Permanently deletes a folder and **all** its contents. |
| `file <filename>` | Determines the type of a file (e.g., tells you if it's text, an image, or an executable). |
