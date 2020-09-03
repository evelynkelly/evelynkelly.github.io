---
layout: post
title: vim Cheat Sheet
date: 2020-08-27 19:53:00
last_modified_at: 2020-09-02 20:38:00
---

### Modes

`i` insert mode

`:` line mode

`esc` normal mode

### File navigation

`$ vim filename` open "filename" in vim

`[h,j,k,l]` move one character in indicated direction (left, down, up, right, respectively); key can be held to repeat movement

`ctrl+f` forward (page down)

`ctrl+b` back (page up)

`w` move cursor forward by a word (string separated by punctuation or whitespace)

`b` move cursor back by a word

`W` move cursor forward by a word (ignoring punctuation)

`B` move cursor back by a word (ignoring punctuation)

`gg` move cursor to first line in file

`G` move cursor to last line in file

`0` move cursor to first character in line

`^` move cursor to first non-whitespace character in line

`$` move cursor to last character in line

### Deleting

`x` deletes character under cursor (note that deletions are stored in the default register)

`X` deletes character before cursor

`dw` delete word (follows common operation+movement syntax, you'll see and use this sort of syntax a lot)

`D` delete from cursor to end of line (shortcut for `d$`, you'll find that many capital letter commands are shorthand for `[command]$`)

`dd` delete current line (likewise, you will find that many double lowercase letter commands make the operation apply linewise)

`.` repeat previous command (you can also have a command repeat by indicating a number: `3dd`, for example, will delete three lines using count+operator+motion syntax)

### Documentation

`:help` opens the help menu

`:q` quits help (also used to quit a file)

`:help [command]` jumps to the section in Help on the specified command

`:help [subject]` jumps to the section in Help on the specified subject

`ctrl+o` back to the previously viewed help section

`ctrl+i` forward to the next viewed help section

`ctrl+]` jumps to the section in Help on the subject under the cursor

### Copypasta

`p` "puts" the contents of the default register under the cursor

`P` puts above the cursor

`y` yanks the character under the cursor into the register (copy)

`yw` yanks word

`y$` yanks to end of line

`yy` yanks entire line

`u` undo last change

`ctrl+r` redo last change

### Registers

`:reg` shows registers

`"Ayy` appends line to register (`"A` specifies append to register, `yy` specifies yank line; you can substitute other operators and motions)

### Inserting

`I` enter insert mode at first non-whitespace character on line

`a` append (enter insert mode after cursor)

`A` append to end of line

`o` enter insert mode, adding a line under the cursor

`O` enter insert mode, adding a line above the cursor

`3i` iterates insert command (can specify any count, inserted text will be iterated [count] times when insert mode is exited)

`3o` iterates insert linewise

`R` enter replace mode

`r` replace only the character under the cursor

`cw` change word (can substitute motion)

`C` change to end of line

`cc` change entire line

`~` change case of character under cursor

`g~w` change case of word (can substitute motion)

`g~~` change case of entire line

`gUw` change case of word to uppercase (can substitute motion)

`guw` change case of word to lowercase (can substitute motion)

`J` join lines (vim intelligently appends a space if it thinks it is necessary)

`gJ` join lines without intelligent spaces

### Search and Replace

`fx` searches line for "x" (character can be substituted)

`Fx` searches line backwards for "x" (character can be substituted)

`;` repeats search

`,` repeats backward search

`tx` search forward for "x" and puts the cursor before "x"

`Tx` search backward for "x" and puts the cursor before "x"

`/` search document for string

`n` iterates / search

`N` iterates / search backward

`*` search for word under cursor

`:s/old/new/g` replace all instances of "old" with "new"

### Text Objects

`daw` delete a word

`diw` delete inner word (retaining whitespace)

`dag` delete a sentence

`dap` delete a paragraph

`ci[` change inner bracket

`ci(` change inner paranthetical

`yi<` yank inner angle bracket

`cit` change inner tag (as in HTML tag)

`ci{` change inner code block

`ci"` change inner double quote

`ci'` change inner single quote

### Macros

`q1` record macro to register 1

`@1` play macro in register 1

`@@` play most recently played macro

### Visual Mode

`v` enter characterwise visual mode

`V` enter linewise visual mode

`ctrl+v` enter blockwise visual mode

`>` indent

`<` unindent
