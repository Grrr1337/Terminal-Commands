# Batch Script Commands CheatSheet

This is a **CheatSheet** README.md file that provides information on the classification and detailed usage of common **Batch Script commands** for the Command Prompt on Windows.

# Table of Contents
1. [Echo Command](#1-echo-command)
2. [Variables](#2-variables)
3. [Conditionals](#3-conditionals)
4. [Loops](#4-loops)
5. [File and Directory Operations](#5-file-and-directory-operations)
6. [User Input](#6-user-input)
7. [Functions](#7-functions)
8. [Error Handling](#8-error-handling)
9. [System Commands](#9-system-commands)

## 1. Echo Command

### 1.1 Basic Text Output
- **Usage:** `echo <message>`
- **Description**: Displays a message on the screen.

```batch
echo Hello, Batch Script!
```

### 1.2 Displaying Variables
- **Usage**: `echo %variable%`
- **Description**: Displays the value of a variable.

```batch
set message=Welcome
echo %message%
```

## 2. Variables
### 2.1 Variable Assignment
- **Usage**: `set variable=value`
- **Description**: Assigns a value to a variable.
```batch
set username=John
```

### 2.2 Variable Expansion
- **Usage**: `%variable%`
- **Description**: Expands the value of a variable.

```batch
set greeting=Hello
echo %greeting% %username%!
```

## 3. Conditionals
### 3.1 If Statement
- **Usage**: `if condition command`
- **Description**: Executes a command based on a specified condition.
```batch
if %number% equ 0 (
    echo Number is zero
) else (
    echo Number is not zero
)
```

## 4. Loops
### 4.1 For Loop
- **Usage**: `for %%variable in (set) do command`
- **Description**: Executes a command for each item in a set.
```batch
for %%i in (1 2 3 4 5) do (
    echo Item: %%i
)
```

## 5. File and Directory Operations
### 5.1 Creating a Directory
- **Usage**: `mkdir <directory>`
- **Description**: Creates a new directory.
```batch
mkdir MyFolder
```

### 5.2 Copying Files
- **Usage**: `copy <source> <destination>`
- **Description**: Copies files from source to destination.
```batch
copy file.txt C:\DestinationFolder\
```

## 6. User Input
### 6.1 Input from User
- **Usage**: `set /p variable=Prompt Message:`
- **Description**: Prompts the user for input.

```batch
set /p username=Enter your name: 
echo Hello, %username%!
```

## 7. Functions
### 7.1 Defining a Function
- **Usage**: `:label`
- **Description**: Defines a label for a function.

```batch
:myFunction
echo This is a function.
goto :eof
```

## 8. Error Handling
### 8.1 Handling Errors
- **Usage**: `if errorlevel n command`
- **Description**: Executes a command if the error level is greater than or equal to n.

```batch
some_command
if errorlevel 1 (
    echo An error occurred.
) else (
    echo Command executed successfully.
)
```

## 9. System Commands
### 9.1 Running System Commands
- **Usage**: `command`
- **Description**: Executes a system command.

```batch
ipconfig
```

## Author / Contributor
These snippets were gathered and organized by **Vladimir Balabanov** / **Grrr1337** .

