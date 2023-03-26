# Part 1 -- Basic Operation

This file gives a guideline for the vim workshop part 2.

---

## Menu

1. Before Start
2. Mode Intro
3. Basic Operation
4. Modify .vimrc(noplugin)

---

## Before Start

Before we start to learn vim's basic operation, there are several things to mention:

1. Use `:help`

   You can use the command in the vim just like what you've done in the matlab

2. Vimtutor

   You can type vimtuor in your terminal to start the vimtutor, a Chinese tutor for vim. It only takes you about 25~30 min. If you feel just give it a try if you want to go over the basic command of vim.

3. Official Website

    Community is an important part of editor. There are a lot of good quality resource made by the developers and experienced vimers on the official website. You can join the community or search on the official website to get supported.

4. Vim Adventure

    Vim adventure is a great game intended to help beginners to learn the vim with fun. Since it is non-free, you can pay for the rest of the game or find a reverse engineered version.

---

## Mode Intro

1. Normal Mode
2. Insert Mode
3. Command Mode
4. Visual Mode
5. Replace Mode*

### Normal Mode

1. Navigating
   1. Basic: hjkl

      You can use hjkl to replace the direction key on your key board.

      h for $\leftarrow$, j for $\downarrow$, k for $\uparrow$, l for $\rightarrow$

   2. Word: bwe

      You can use the wbe to jump word by word.

      Difference between `word` and `WORD`: The `word` is the combination of (a-zA-Z0-9), or the combination of punctuation and character like @#$% while the WORD is any non-empty string between the white-space.

      NOTE THAT as213df%#^>?^& is two `word`, as213df and %#^>?^&.

      - w: go to the beginning of next word
      - b: go to the beginning of previous word
      - e: go to the end of the word
      - W: go to the  beginning of next WORD
      - B: go to the beginning of previous WORD
      - E: end of the WORD

   3. Line: 0, ^, $

      - 0: Go to the beginning of line
      - ^: Go to the beginning of line (after whitespace)
      - $: Go to the end of line

   4. Char:

      - f{char}: Go forward to character
      - F{char}: Go backward to character

   5. Document

      - gg: First line
      - G: Last line
      - :{number}: Go to line {number}
      - {number}G: Go to line {number}
      - {number}j: Go down {number} lines
      - {number}k: Go up {number} lines

   6. Window

      - zz: Center this line
      - zt: Top this line
      - zb: Bottom this line
      - H: Move to top of screen
      - M: Move to middle of screen
      - L: Move to bottom of screen

   7. Search

### Why key in vim is so uncomfortable?

![keyboard](src/keyboard.jpeg)

---