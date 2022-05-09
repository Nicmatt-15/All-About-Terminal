# Basic Terminal Command

Before starting out, the picture reference in this file will look slightly different from your Terminal. Here is what my default Terminal will look like:
![my iterm2](/My%20Terminal.png)

I've only customized the aesthetic of the terminal. No functionality has
changed. In particular:

1. The Green arrow still indicates where you can start typing out your command.
2. The Red arrow still indicates which directory my Terminal is currently opening. By default, it is opening my <u>Home Directory</u> indicated by the `~` (_tilde_) sign.

> Your terminal may look slightly different. You can look more into Terminal Appearance Customization here: [OhMyZsh](https://ohmyz.sh/) and [iterm2](iterm2.com).

---

## Table of Content

1. [Print Working Directory](#print-working-directory)
2. [List Directory](#list-directory)
3. [Change Directory](#change-directory)
4. [Make Directory](#make-directory)
5. [Remove Directory](#remove-directory)
6. [Create File](#create-file)
7. [Remove File](#remove-file)
8. [Printing the Content of a File](#printing-content-of-a-file)
9. [Opening Vim](#opening-vim)
10. [Compiling Java Code](#compiling-java-code)
11. [Running Java Code](#running-java-code)
12. [Commands Layout](#commands-layout)
13. [Man Command](#man-command)
14. [AutoComplete Your Command](#autocomplete-your-command)
15. [Use Previous Command](#use-previous-command)
16. [Force Stop](#force-stop)
17. [Clearing Terminal Screen](#clearing-terminal-screen)
18. [`;` Operator](#operator)
19. [Wildcard](#wildcard)

---

## Print Working Directory

While your Terminal displays in which folder you are currently in, you can always print it out by typing `pwd` followed by `Enter` to execeute the command.

Example:
![pwd](/pwd.png)

> `pwd` is an abbreviation for Print Working Directory.

[Back to Top](#table-of-content)

---

## List Directory

You can print out what's in the directory that your Terminal is opening by typing `ls` followed by `Enter` to execeute the command.

Example:
![ls](/ls.png)

> `ls` is an abbreviation for List.

[Back to Top](#table-of-content)

---

## Change Directory

You can move to different directory using your Terminal too. Here are three different options that you can try:

1. Moving to a specific directory. You can type in `cd FOLDERNAME`. For example, there is a directory called Desktop in my home folder. If I want my Terminal to open my Desktop folder, I can type in `cd Desktop` followed by Enter to execute the command.

   Example:
   ![cd](/cd.png)

   Try using the `ls` command again! You should see all your files stored in Desktop.

2. Moving to the previous / above directory. You can type in `cd ..` followed by Enter to execute the command.

   Example:
   ![cd prev](/cdprev.png)

   Notice that after the execution of `cd ..` command, my Terminal is pointing back to my Home Directory instead of my Desktop directory. You can confirm this by using the `pwd` command!

3. Move to the Home Directory from anywhere. You can type in `cd` followed by Enter to execute the command.

   Example:
   ![cd home](/cdhome.png)

   Notice that after moving from my Home Directory into another Directory, I can use the `cd` command to instantly move back to my Home Directory.

> `cd` is an abbreviation for Change Directory.

[Back to Top](#table-of-content)

---

## Make Directory

You can create a directory inside the current directory your Terminal is pointing to by typing `mkdir FOLDERNAME` followed by `Enter` to execute the command.

Example:
![mkdir](/mkdir.png)

> `mkdir` is an abbreviation for Make Directory

[Back to Top](#table-of-content)

---

## Remove Directory

You can delete a directory inside the current directory your Terminal is pointing to by typing `rmdir FOLDERNAME` followed by `Enter` to execute the command.

Example:
![rmdir](/rmdir.png)

Notice that the cheesecake directory is gone when the `ls` command is executed after the `rmdir cheesecake` command is executed.

> `rmdir` is an abbreviation for Remove Directory

[Back to Top](#table-of-content)

---

## Create File

You can create an empty file inside the current directory your Terminal is pointing to by typing `touch FILENAME` followed by `Enter` to execute the command.

Example:
![touch](/touch.png)

[Back to Top](#table-of-content)

---

## Remove File

You can remove any file inside the current directory your Terminal is pointing to by typing `rm FILENAME` followed by `Enter` to execute the command.

Example:
![rm](/rm.png)

Notice that the someTextFileIdk.txt file is gone when the `ls` command is executed after the `rm someTextFileIdk.txt` is executed.

> `rm` is an abbreviation for Remove.

[Back to Top](#table-of-content)

---

## Printing Content of a File

There are multiple ways to print content of a file. There are three commands that you can use:

1. `head FILENAME`. By default, the `head` command prints out <u>**the first 10 lines**</u> of your file.
2. `tail FILENAME`. By default, the `tail` command prints out <u>**the last 10 lines**</u> of your file.
3. `cat FILENAME`. By default, the `cat` command prints out <u>**all lines**</u> of your file.

Example:
![cat](/cat.png)

> `cat` is an abbreviation for Concatenate.

[Back to Top](#table-of-content)

---

## Opening Vim

You can use a text editor built into your Terminal called `Vim` to read and edit the content of your file by typing `vim FILENAME` followed by by `Enter` to execute the command.

This should take you to a special window with 2 main modes:

1. Normal Mode. By default, Vim is normal mode. However, if you enter another mode and need to go back to normal mode, click `esc` in your keyboard.

   Normal mode is used to move into different parts of your code efficiently using keyboard shortcuts. You can't edit your file while in normal mode.

2. Insert Mode. Insert mode is used to edit your file. You can access your insert mode by typing `i` in your keyboard. You can't use most shortcut while you are in insert mode.

To quit Vim, you have to enter Normal Mode first. There are two options two quit:

1. Type in `:wq` to save your edit and quit.
2. Type in `:q!` to quit without saving your edit.

> There are other Vim modes that we are not going to talk about here. Vim itself has hundreds if not thousands of available shortcuts that you can use to speed up your workflow.

[Back to Top](#table-of-content)

---

## Compiling Java Code

You can compile a Java code (any file that ends with `.java`) in the <u>**current Terminal directory**</u> by typing `javac FILENAME` followed by by `Enter` to execute the command.

Example:
![javac](/javac.png)

> If your terminal current directory is not in the same directory as your `.java` file, make sure to use the `cd` command to move to the directory that contains your `.java` file you are planning to compile.

> `javac` is an abbreviation for Java Compiler.

[Back to Top](#table-of-content)

---

## Running Java Code

You can run a Java code in the <u>**current Terminal directory**</u> by typing `java FILENAME` followed by by `Enter` to execute the command.

Two important details:

1. You must compile your code first before running
2. The FILENAME should not end with `.java` when you are running. For example, if your java file name is `Demo.java`, you should run it using `java Demo` instead of `java Demo.java`.

Example:
![java](/java.png)

[Back to Top](#table-of-content)

---

## Commands Layout

While there is no consistent definitions on how to write commands, people generally follow the following format:
![cmdstruct](/cmdstruct.png)

Flags and Arguments:

1. Flags are options that you can choose for each command to alter the way they behave. Flags always begin with a `-` (dash) character.
2. If you want to use more than one flag, you can join them altogether without any specific ordering. For example, the picture above uses two different flags: `-a` and `-l`.
3. Arguments are any input that a command need to work on. Sometimes, a command does not need any argument (ex: `cd`).

Example:

```zsh
ls -al dir1
```

1. The **command** `ls` prints / lists out the content of a directory.
2. The `-a` **flag** includes all hidden files and directory when printing out the content of a directory.
3. The `-l` **flag** includes more details when printing out the content of a directory.
4. The `dir1` **argument** means that the `ls` command are instructed to print the content of a directory called `dir1` (which is inside your current directory).

[Back to Top](#table-of-content)

---

## Man Command

If you need to check what does a command do or the available flags that you can use for that command, you can type `man COMMANDNAME` followed by `Enter` to execute the command.

Example:

```zsh
grep rmdir
```

To quit from the manual, click `q` in your keyboard!

To search for keyword(s), type in `/` followed by the keyword that you want to find and hit `Enter`. Use `n` to move from one match to the next one.

> `man` is an abbreviation for manual.

[Back to Top](#table-of-content)

---

## AutoComplete Your Command

When you are in the middle of writing your command, you can use the `tab` key to complete what you're currently typing.

If the Terminal is unsure on how to complete your command, it will usually give you suggestion on which choices you can choose. You would need to type a few letters more and hit `tab` again for your Terminal to autocomplete your command!

[Back to Top](#table-of-content)

---

## Use Previous Command

You can scroll through the previous command that you used using your arrow up and down button!

[Back to Top](#table-of-content)

---

## Force Stop

You can force stop any code that is currently running (Java, C, etc) using `Ctrl + c`. You can use this key to in the middle of typing a command start over.

[Back to Top](#table-of-content)

---

## Clearing Terminal Screen

You can clear your Terminal screen by typing `Cmd + k`

[Back to Top](#table-of-content)

---

## `;` Operator

You can run multiple command by typing all of them on one line and separating one command from another using `;`.

Example:

```zsh
javac Demo.java; java Demo
```

The above command will compile the Java file called `Demo.java` in your current directory. After `Demo.java` has been compiled, it will be run using the second command `java Demo`.

> Note that the `;` does not run multiple command at once. It will run one command at a time in order from left to right.

[Back to Top](#table-of-content)

---

## Wildcard

The `*` symbol can be translated as <u>**all files**</u>. For example, if we have the command:

```zsh
javac *.java
```

The above command can be translated as: "Compile <u>**all files**</u> that ends with `.java`".

**Another example:**

```zsh
rmdir testing*
```

The above command can be translated as: "Remove <u>**all directory**</u> that starts with the name testing".

**Another example:**

```zsh
cat input*.txt
```

The above command can be translated as: "Print out the content of <u>**all files**</u> that starts with the name input and ends with `.txt`"

[Back to Top](#table-of-content)
