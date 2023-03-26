# Part 1 -- Basic Operation

This file gives a guideline for the vim workshop part 2.

---

## Menu

1. Mode Intro
2. Basic Operation
3. Modify .vimrc(noplugin)

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

      - f\<char\>: Go forward to character
      - F\<char\>: Go backward to character
   5. Document
   6. Search

### Why key in vim is so uncomfortable?

![keyboard](src/keyboard.jpeg)

---