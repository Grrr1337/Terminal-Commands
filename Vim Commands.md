# Vim Commands - cheatsheet

This is a **CheatSheet** README.md file that provides information on useful **``vim`` / ``nvim`` commands** and their shortcuts.

## ``how to exit VIM ?`` -

1. **Exiting** and **Saving** Changes:
    - Press ``Esc`` to ensure you are in normal mode.
    - Type ``:wq`` and press ``Enter``.
2. **Exiting** **without Saving** Changes:
    - Press ``Esc`` to ensure you are in normal mode.
    - Type ``:q!`` and press ``Enter``.

You may be looking specifically for this so
you are welcome!


## **Note:**
- Many commands are common between Vim and Neovim (``nvim``), providing a familiar experience for users of either editor.
- For specific features or differences in Neovim, refer to the Neovim documentation using `:help` within Neovim.

# Table of Contents
1. [Navigation](#1-navigation)
2. [Editing](#2-editing)
3. [Search and Replace](#3-search-and-replace)
4. [Saving and Quitting](#4-saving-and-quitting)
5. [Visual Mode](#5-visual-mode)
6. [Undo and Redo](#6-undo-and-redo)
7. [Author / Contributor](#author--contributor)

## 1. Navigation

### 1.1 Moving the Cursor
   - **h**: Move left
   - **j**: Move down
   - **k**: Move up
   - **l**: Move right

### 1.2 Word Movement
   - **w**: Move to the beginning of the next word
   - **e**: Move to the end of the current word
   - **b**: Move to the beginning of the previous word

### 1.3 Line Movement
   - **0**: Move to the beginning of the line
   - **^**: Move to the first non-whitespace character of the line
   - **$**: Move to the end of the line

### 1.4 Scrolling
   - **Ctrl + u**: Scroll up half a page
   - **Ctrl + d**: Scroll down half a page
   - **Ctrl + b**: Scroll up one page
   - **Ctrl + f**: Scroll down one page

## 2. Editing

### 2.1 Inserting and Appending
   - **i**: Insert before the cursor
   - **I**: Insert at the beginning of the line
   - **a**: Append after the cursor
   - **A**: Append at the end of the line
   - **o**: Open a new line below the current line
   - **O**: Open a new line above the current line

### 2.2 Deleting
   - **x**: Delete the character under the cursor
   - **dd**: Delete the entire line
   - **D**: Delete from the cursor position to the end of the line
   - **dw**: Delete from the cursor position to the start of the next word
   - **db**: Delete from the cursor position to the start of the previous word

### 2.3 Copying and Pasting
   - **yy**: Yank (copy) the entire line
   - **yw**: Yank from the cursor position to the start of the next word
   - **y$**: Yank from the cursor position to the end of the line
   - **p**: Paste after the cursor
   - **P**: Paste before the cursor

## 3. Search and Replace

### 3.1 Searching
   - **/pattern**: Search forward for the pattern
   - **?pattern**: Search backward for the pattern
   - **n**: Move to the next occurrence
   - **N**: Move to the previous occurrence

### 3.2 Replacing
   - **:s/old/new**: Replace the first occurrence of "old" with "new" on the current line
   - **:s/old/new/g**: Replace all occurrences of "old" with "new" on the current line
   - **:%s/old/new/g**: Replace all occurrences of "old" with "new" in the entire file

## 4. Saving and Quitting

### 4.1 Saving
   - **:w**: Save the current file

### 4.2 Quitting
   - **:q**: Quit (close) the current file
   - **:q!**: Quit without saving changes
   - **:wq**: Save changes and quit

## 5. Visual Mode

### 5.1 Entering Visual Mode
   - **v**: Start visual mode character-wise
   - **V**: Start visual mode line-wise
   - **Ctrl + v**: Start visual mode block-wise

### 5.2 Selecting Text
   - Use movement commands to select text
   - Once text is selected, you can perform actions like copy and delete

## 6. Undo and Redo

### 6.1 Undo
   - **u**: Undo the last action

### 6.2 Redo
   - **Ctrl + r**: Redo the last undone action

## Author / Contributor
These snippets were gathered and organized by **Vladimir Balabanov** / username: __Grrr1337__.
