# tmux Commands Classification and Usage

This is a **CheatSheet** README.md file that provides information on the classification and detailed usage of common **`tmux` commands**.


# Table of Contents
1. [Session Management](#1-session-management)
2. [Window Management](#2-window-management)
3. [Pane Management](#3-pane-management)
4. [Detach and Attach](#4-detach-and-attach)
5. [Miscellaneous](#5-miscellaneous)
6. [Hierarchy Overview](#6-hierarchy-overview)
7. [Author / Contributor](#7-author-or-contributor)


## Session Management

### 1. Create a New Session
- **Usage**: `tmux new-session -s <session_name>`
- **Description**: Creates a new tmux session with the specified name.
```bash
# Create a new session named 'my_session'
tmux new-session -s my_session
```

### 2. List Sessions
- **Usage**: `tmux list-sessions`
- **Description**: Lists all existing tmux sessions.
```bash
# List all tmux sessions
tmux list-sessions
```

### 3. Attach to a Session
- **Usage**: `tmux attach-session -t <session_name>`
- **Description**: Attaches to the specified tmux session.
```bash
# Attach to the 'my_session' session
tmux attach-session -t my_session
```

### 4. Rename a Session
- **Usage**: `tmux rename-session -t <old_name> <new_name>`
- **Description**: Renames an existing tmux session.
```bash
# Rename the 'old_session' to 'new_session'
tmux rename-session -t old_session new_session
```

## Window Management
### 5. Create a New Window
- **Usage**: `tmux new-window -n <window_name>`
- **Description**: Creates a new window within the current tmux session.
```bash
# Create a new window named 'my_window'
tmux new-window -n my_window
```
### 6. Switch Between Windows
- **Usage**: `tmux switch-window -t <window_number>`
- **Description**: Switches to the specified window.
```bash
# Switch to window number 2
tmux switch-window -t 2
```

### 7. Rename a Window
- **Usage**: `tmux rename-window -t <old_name> <new_name>`
- **Description**: Renames an existing window.
```bash
# Rename the 'old_window' to 'new_window'
tmux rename-window -t old_window new_window
```
### 8. List Windows
- **Usage**: `tmux list-windows`
- **Description**: Lists all windows in the current session.
```bash
# List all windows in the current session
tmux list-windows
```

## Pane Management
### 9. Split the tmux Window
- **Usage**: `tmux split-window -h (horizontal) / -v (vertical)`
- **Description**: Splits the current pane either horizontally or vertically.
```bash
# Split the current pane horizontally
tmux split-window -h

# Split the current pane vertically
tmux split-window -v
```
### 10. Navigate Between Panes
- Usage: `tmux select-pane -[UDLR]`
- Description: Allows navigation between panes (Up, Down, Left, Right).
```bash
# Move to the pane above the current one
tmux select-pane -U

# Move to the pane below the current one
tmux select-pane -D

# Move to the pane on the left of the current one
tmux select-pane -L

# Move to the pane on the right of the current one
tmux select-pane -R
```
### 11. Resize Panes
- **Usage**: `tmux resize-pane -[UDLR] <size>`
- **Description**: Resizes the current pane in the specified direction.
```bash
# Increase the height of the current pane
tmux resize-pane -U 10

# Decrease the width of the current pane
tmux resize-pane -L 5
```

## Detach and Attach
### 12. Detach from tmux Session
- **Usage**: `tmux detach-client`
- **Description**: Detaches from the currently attached tmux session, leaving it running in the background.
```bash
# Detach from the tmux session
tmux detach-client
```
### 13. Detach All Clients
- **Usage**: `tmux detach-client -a`
- **Description**: Detaches all clients from the tmux session, leaving it running in the background.
```bash
# Detach all clients from the tmux session
tmux detach-client -a
```
### 14. Attach to tmux Session
- **Usage**: `tmux attach-session -t <session_name>`
- **Description**: Attaches to the specified tmux session.
```bash
# Attach to the 'my_session' session
tmux attach-session -t my_session
```
## Miscellaneous
### 15. Show tmux Commands
- **Usage**: `tmux list-commands`
- **Description**: Lists and shows usage of various tmux commands.
```bash
# List tmux commands and their usage
tmux list-commands
```
16. Show tmux Options
- **Usage**: `tmux show-options -g`
- **Description**: Displays global tmux options and their values.
```bash
# Show global tmux options and their values
tmux show-options -g
```

# `tmux` Hierarchy Explanation

In `tmux`, the hierarchy consists of sessions, windows, and panes. Here's a brief explanation of each:

## Session

- A `tmux` session is the highest-level container.
- It represents a collection of one or more windows and their associated panes.
- Sessions are useful for organizing and managing multiple tasks or projects within a single terminal.

## Window

- Within a `tmux` session, you can have multiple windows.
- Each window is an independent workspace that can contain one or more panes.
- Windows are useful for organizing different tasks or activities related to the same project or session.

## Pane

- Panes are subdivisions within a window, allowing you to view and interact with multiple terminal sessions simultaneously.
- A window can be split into multiple panes horizontally or vertically.
- Each pane behaves like an independent terminal, and you can run different commands in each pane.


## Hierarchy Overview

- A `tmux` session contains one or more windows.
- Each window can be divided into multiple panes.
- Panes provide a way to work on multiple tasks within a single window.

### Common Operations

- **Switching Between Sessions:**
  - `tmux switch-client -t <session_name>`

- **Switching Between Windows:**
  - `tmux switch-window -t <window_number>`

- **Navigating Between Panes:**
  - `tmux select-pane -[UDLR]`

- **Splitting Windows:**
  - `tmux split-window -h` (horizontal split)
  - `tmux split-window -v` (vertical split)

- **Creating New Windows:**
  - `tmux new-window -n <window_name>`

- **Creating New Sessions:**
  - `tmux new-session -s <session_name>`



## Author / Contributor
These snippets were gathered and organized by **Vladimir Balabanov** / username: __Grrr1337__.