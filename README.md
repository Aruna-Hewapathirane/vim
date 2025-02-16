# Getting started with Vim

## 1. Opening and Exiting Vim

To start Vim and open a file:

```sh
vim filename
```

To exit Vim:

```sh
:q   # Quit if no changes were made
:q!  # Quit without saving
:wq  # Save and quit
:x   # Save only if changes were made, then quit
```

## 2. Vim Modes

Vim has three main modes:

- **Normal Mode** - Default mode for navigation and commands.
- **Insert Mode** - Used for typing text (`i` to enter, `Esc` to exit).
- **Visual Mode** - Used for selecting text (`v` for characters, `V` for lines).

## 3. Moving the Cursor

Use these keys for navigation:

```sh
h - Move left
l - Move right
j - Move down
k - Move up
```

Other useful commands:

```sh
w  # Jump forward by one word
b  # Jump backward by one word
0  # Move to beginning of the line
$  # Move to end of the line
G  # Move to end of the file
gg # Move to beginning of the file
```

## 4. Editing Text

Entering Insert Mode:

```sh
i  # Insert before cursor
I  # Insert at the beginning of the line
a  # Append after cursor
A  # Append at the end of the line
```

## 5. Deleting Text

```sh
x   # Delete character under cursor
dd  # Delete current line
dw  # Delete a word
d$  # Delete to end of line
```

## 6. Copying and Pasting

```sh
yy  # Copy current line
p   # Paste after cursor
P   # Paste before cursor
```

## 7. Undo and Redo

```sh
u       # Undo last change
Ctrl+r  # Redo last undone change
```

## 8. Searching and Replacing

```sh
/word   # Search forward for 'word'
?word   # Search backward for 'word'
n       # Repeat last search forward
N       # Repeat last search backward
```

Replace all occurrences of 'old' with 'new':

```sh
:%s/old/new/g
```

## 9. Splitting Windows

```sh
:split filename   # Horizontal split
:vsplit filename  # Vertical split
Ctrl-w w         # Switch between windows
```

## 10. Running Shell Commands

```sh
:!ls     # Run a shell command
:r !date # Insert the output of a command
```

## 11. Recording Macros

To record a macro into register 'a':

```sh
qa  # Start recording
[Perform actions]
q   # Stop recording
```

To replay the macro:

```sh
@a  # Play macro 'a'
@@  # Repeat last macro
```

## 12. Spell Checking

```sh
:set spell     # Enable spell checking
:set nospell  # Disable spell checking
```

## 13. Viewing Text as Hex

```sh
:%!xxd   # View file in hex mode
:%!xxd -r # Convert back to text
```

## 14. Basic Vim Configuration (`.vimrc`)

Example `.vimrc` configuration:

```sh
set number       " Show line numbers
set tabstop=4    " Set tab width to 4 spaces
set shiftwidth=4 " Auto-indent width
set expandtab    " Use spaces instead of tabs
syntax enable    " Enable syntax highlighting
```

## Conclusion

Vim is a powerful editor that rewards practice and learning. For more help, type:

```sh
:help
```

or visit [Vim's official website](https://www.vim.org/).

Happy Vimming! 🎉

Feel free to explore, experiment, and customize your Vim setup as you learn more about it. Enjoy the journey of mastering one of the most powerful text editors!
