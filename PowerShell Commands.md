# PowerShell Commands CheatSheet

This is a **CheatSheet** README.md file that provides information on the classification and detailed usage of common **PowerShell commands**.

# Table of Contents
1. [Echo Command](#1-echo-command)
2. [Variables](#2-variables)
3. [Conditionals](#3-conditionals)
4. [Loops](#4-loops)
5. [File and Directory Operations](#5-file-and-directory-operations)
6. [User Input](#6-user-input)
7. [Functions](#7-functions)
8. [Error Handling](#8-error-handling)
9. [Remote Management](#9-remote-management)
10. [Modules](#10-modules)

## 1. Echo Command

### 1.1 Basic Text Output
- **Usage:** ``Write-Host <message>``
- **Description**: Displays a message on the screen.

```powershell
Write-Host "Hello, PowerShell!"
```

### 1.2 Displaying Variables
- **Usage**: ``Write-Host $variable``
- **Description**: Displays the value of a variable.

```powershell
$greeting = "Welcome"
Write-Host $greeting
```

## 2. Variables
### 2.1 Variable Assignment
- **Usage**: ``$variable = value``
- **Description**: Assigns a value to a variable.

```powershell
$username = "John"
```

### 2.2 Variable Expansion
- **Usage**: ``$variable``
- **Description**: Expands the value of a variable.
```powershell
$greeting = "Hello"
Write-Host "$greeting $username!"
```

## 3. Conditionals
### 3.1 If Statement
- **Usage**: ``if (condition) { command }``
- **Description**: Executes a command based on a specified condition.
```powershell
if ($number -eq 0) {
    Write-Host "Number is zero"
} else {
    Write-Host "Number is not zero"
}
```

## 4. Loops
### 4.1 ForEach-Object Loop
- **Usage**: ``foreach ($item in $collection) { command }``
- **Description**: Executes a command for each item in a collection.

```powershell
foreach ($i in 1..5) {
    Write-Host "Item: $i"
}
```

## 5. File and Directory Operations
### 5.1 Creating a Directory
- **Usage**: ``New-Item -ItemType Directory -Path <directory>``
- **Description**: Creates a new directory.
```powershell
New-Item -ItemType Directory -Path C:\MyFolder
```

## 5.2 Copying Files
- **Usage**: ``Copy-Item -Path <source> -Destination <destination>``
- **Description**: Copies files from source to destination.
```powershell
Copy-Item -Path file.txt -Destination C:\DestinationFolder\
```

## 6. User Input
### 6.1 Input from User
- **Usage**: ``$variable = Read-Host "Prompt Message"``
- **Description**: Prompts the user for input.
```powershell
$username = Read-Host "Enter your name"
Write-Host "Hello, $username!"
```

## 7. Functions
### 7.1 Defining a Function
- **Usage**: ``function FunctionName { command }``
- **Description**: Defines a function.
```powershell
function MyFunction {
    Write-Host "This is a function."
}
MyFunction
```


## 8. Error Handling
### 8.1 Handling Errors
- **Usage**: ``try { command } catch { command }``
- **Description**: Executes a command and catches errors.
```powershell
try {
    some_command
} catch {
    Write-Host "An error occurred: $_"
}
```

## 9. Remote Management
### 9.1 Running Commands Remotely
- **Usage**: ``Invoke-Command -ComputerName <computer> -ScriptBlock { command }``
- **Description**: Executes a command on a remote computer.
```powershell
Invoke-Command -ComputerName RemoteComputer -ScriptBlock {
    Write-Host "Executing command on a remote computer."
}
```

## 10. Modules
### 10.1 Importing a Module
- **Usage**: ``Import-Module <module>``
- **Description**: Imports a PowerShell module.
```powershell
Import-Module MyModule
```

## Author / Contributor
These snippets were gathered and organized by **Vladimir Balabanov** / **Grrr1337** .
