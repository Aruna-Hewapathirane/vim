# vim
Getting Started with Vim

Once Vim is installed, you can start it by typing the following command in your terminal:

vim

You will enter Normal mode (the default mode), where you can navigate, edit, and manipulate your files.
Vim Modes

Vim operates in several modes:

    Normal Mode: This is the default mode for navigation and manipulation of text. You can press Esc to return to Normal mode.
    Insert Mode: This mode allows you to insert text. You can enter Insert mode by pressing i, I, a, or A.
    Visual Mode: This mode is used for selecting text. Press v to enter Visual mode, and use y to yank (copy) or d to delete the selection.
    Command Mode: Use this mode for executing commands like saving, quitting, or searching. Enter Command mode by pressing :.

Basic Commands

    Open a file:

    vim filename

    Exit Vim:
        To exit without saving:
        :q!
        To save and exit:
        :wq
        To save the file:
        :w
        To quit Vim (if no changes have been made):
        :q

Editing and Navigation
Moving the Cursor:

    h: Move left
    j: Move down
    k: Move up
    l: Move right

Inserting Text:

    Press i to enter Insert mode before the cursor.
    Press a to enter Insert mode after the cursor.
    Press o to open a new line below the current line.
    Press O to open a new line above the current line.

Deleting Text:

    d: Delete a character (place the cursor over it and press d).
    dd: Delete the entire line.
    d$: Delete from the cursor to the end of the line.
    d0: Delete from the cursor to the beginning of the line.

Copying and Pasting Text:

    yy: Yank (copy) the current line.
    y$: Yank from the cursor to the end of the line.
    p: Paste below the current line.
    P: Paste above the current line.

Searching and Replacing

    Search for a word:
    Press / and then type the word you want to search for. Press Enter to find the first occurrence.

    Search and replace:
    To replace all instances of a word in a file:

    :%s/old_word/new_word/g

    Search backwards:
    Press ? and then type the word you want to search for.

Vim Configuration (.vimrc)

Your Vim configuration file is named .vimrc and is typically located in your home directory. This file allows you to customize Vim's behavior and appearance.
Example .vimrc:

" Enable line numbers
set number

" Enable syntax highlighting
syntax enable

" Set the background color
set background=dark

" Enable auto-indentation
set smartindent
set tabstop=4
set shiftwidth=4

" Enable line wrapping
set wrap

" Show line and column number in the status line
set ruler

" Enable search highlighting
set hlsearch

Using Plugins with Vim

Vim's functionality can be extended with plugins. The most common plugin manager is vim-plug.
Installing vim-plug:

    Open a terminal and run the following command:

curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

Add the following lines to your .vimrc file:

call plug#begin('~/.vim/plugged')

" Example plugins
Plug 'tpope/vim-fugitive'  " Git integration
Plug 'junegunn/fzf.vim'    " Fuzzy file search

call plug#end()

To install the plugins, open Vim and run:

    :PlugInstall

Advanced Tips and Tricks
Use Macros to Automate Tasks:

You can record sequences of commands and play them back to automate repetitive tasks. For example, press q followed by a register key (like a) to start recording a macro, then perform the actions you want to automate. Press q again to stop recording. Replay the macro by pressing @a.
Split Windows:

Vim allows you to split the window for editing multiple files side-by-side:

    Horizontal split:

:split filename

Vertical split:

    :vsplit filename

You can switch between splits using Ctrl-w followed by the direction (h, j, k, l).
Useful Resources

    Vim Documentation
    Vim Cheat Sheet
    Vim Adventures (Interactive Learning)
    Vim Wiki

Happy Vimming! 🎉

Feel free to explore, experiment, and customize your Vim setup as you learn more about it. Enjoy the journey of mastering one of the most powerful text editors!
