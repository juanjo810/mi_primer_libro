# Session 0. Ubuntu Terminal for Verilog

This session helps you become comfortable with the terminal. Before writing Verilog circuits, it is useful to know how to move through folders, find files, and run the tools that compile and simulate our designs.

```{admonition} Learning objectives
:class: tip

- Open an Ubuntu terminal and know which folder you are in.
- Navigate the file system with `pwd`, `ls`, and `cd`.
- Create a working folder and organize Verilog files.
- Create a simple file with `gedit` and show it from the terminal.
- Prepare the first compilation command with `iverilog`.
```

## The terminal as a workbench

A terminal is a window where we type text commands. In this course we will use it as a workbench: enter a folder, inspect its files, open an editor, and run simple commands.

In Ubuntu you can open it with `Ctrl` + `Alt` + `T`, or by searching for **Terminal** in the applications menu.

## Where am I: `pwd`

The command `pwd` prints the path of the current folder.

```bash
pwd
```

A possible output is:

```text
/home/user
```

This path means that we are inside the user's home folder. If the terminal were a file browser, `pwd` would be like looking at the address bar.

## What is here: `ls`

The command `ls` lists the contents of the current folder.

```bash
ls
```

Useful variants:

```bash
ls -l
ls -a
ls -lh
```

| Command | What it is for |
|---|---|
| `ls` | Lists visible files and folders. |
| `ls -l` | Shows more details: permissions, size, and date. |
| `ls -a` | Includes hidden files, whose names start with a dot. |
| `ls -lh` | Shows more readable sizes, for example `4K` or `2M`. |

## Change folder: `cd`

The command `cd` changes the current folder.

```bash
cd Documents
pwd
```

To go one folder back:

```bash
cd ..
```

To go directly to your home folder:

```bash
cd
```

To enter a specific path:

```bash
cd ~/verilog/session_00
```

The symbol `~` represents your home folder. In many installations it is equivalent to something like `/home/user`.

## Create and prepare a practice folder

Create one folder for the course and another one for this session.

```bash
mkdir -p ~/verilog/session_00
cd ~/verilog/session_00
pwd
```

The command `mkdir` creates folders. The option `-p` allows several nested folders to be created if they do not exist yet.

## Check installed tools

To compile Verilog in Ubuntu we will mainly use:

- `iverilog`: compiles the design and the testbench.

Check whether they are available:

```bash
iverilog -V
```

If Ubuntu prints a version message, the tool is installed. If it prints `command not found`, the tool still needs to be installed.

````{admonition} Installation on Ubuntu
:class: note

If you are working on a machine where you have permission to install packages, you can prepare the tools with:

```bash
sudo apt update
sudo apt install iverilog
```
````

## Create a first text file

Create the file `hello.txt` with `gedit`:

```bash
gedit hello.txt
```

```{admonition} Other terminal editors
:class: note

Besides `gedit`, there are editors that open inside the terminal itself, such as `nano`, `pico`, or `vim`. In this session we will use `gedit` because it is a visual and simple starting point.
```

Write a single word:

```text
hello
```

Save the file and close `gedit`.

Check that the file exists:

```bash
ls -l
```

Show its contents from the terminal:

```bash
cat hello.txt
```

The expected output is:

```text
hello
```

## Compile and run

Later we will write Verilog files. The cycle will be very similar: be in the right folder, list the files, compile, and run the result.

Create this file `greeting.v`:

```bash
gedit greeting.v
```

Content:

```verilog
module greeting;
  initial begin
    $display("Hello from Verilog");
    $finish;
  end
endmodule
```

Compile the file with `iverilog`:

```bash
iverilog -o greeting greeting.v
```

This command reads `greeting.v` and creates an executable file named `greeting`.

Run it with:

```bash
./greeting
```

The expected output is:

```text
Hello from Verilog
```

## Work pattern for the sessions

In this course we will repeat the same sequence many times:

```bash
cd ~/verilog/session_00
ls
iverilog -o simulation file.v
./simulation
```

When the example has a testbench, we will normally compile two files:

```bash
iverilog -o simulation design.v testbench.v
./simulation
```

## Basic help commands

| Command | Typical use |
|---|---|
| `clear` | Clears the terminal screen. |
| `history` | Shows previously used commands. |
| `man ls` | Opens the manual page for `ls`. Exit with `q`. |
| `cat file.txt` | Shows the contents of a short file. |
| `cp source.v copy.v` | Copies a file. |
| `mv old.v new.v` | Renames or moves a file. |
| `rm file.txt` | Deletes a file. Use it carefully. |

## Common mistakes

| Message or situation | What to check |
|---|---|
| `command not found` | The tool is not installed or its name is misspelled. |
| `No such file or directory` | You are not in the right folder or the file has a different name. Use `pwd` and `ls`. |
| `cat hello.txt` prints nothing | The file is empty or was not saved in `gedit`. |
| `./greeting` does not work | Check that you first compiled with `iverilog -o greeting greeting.v`. |

## Guided practice

1. Open an Ubuntu terminal.
2. Create the folder `~/verilog/session_00`.
3. Enter that folder and confirm the path with `pwd`.
4. Open `gedit` from the terminal with `gedit hello.txt`.
5. Write `hello`, save the file, and close `gedit`.
6. Use `ls` to check that `hello.txt` appears in the folder.
7. Use `cat hello.txt` to show its contents.
8. Change the text to `hello world`, save again, and show it again with `cat hello.txt`.

## Closing checkpoint

Before moving to session 1, you should be able to answer without looking at notes: where am I (`pwd`), which files do I have (`ls`), how do I enter a folder (`cd`), how do I open a file with `gedit`, and how do I show a short file with `cat`.
