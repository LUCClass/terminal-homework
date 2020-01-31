# Terminal Driver

In this homework assignment, you will be writing a terminal driver in C. A terminal driver has basically two jobs: (1) print characters to the screen and (2) receive input from the keyboard. In the first homework assignment, we used the BIOS to do all of our I/O for us, but in this project, we will be doing it ourselves.

This repo contains a skeleton for your project with a demo program in assembly that prints a bunch of characters to the screen. You can write your program in either C or assembly.

Whatever language you decide to use, your program should do the following things:

1. `puts` prints a NULL-terminated string to the terminal.
  * Calling `puts` sequentially will print strings one after another. In other words, `puts` should not overwrite text that was previously written to the screen.
  * Printing a '\n' character should advance to the next line on the screen.
  * When the cursor gets to the bottom of the screen, advancing to a new line should scroll the existing text on the screen up one line.

**For extra credit:**

2. Interrupt handler for the keyboard that (a) reads the key's scancode, (b) translates the scancode to an ASCII character, and (c) puts the ASCII character into an input buffer.
3. `getc` reads a character from the keyboard input buffer.

## Printing Characters

See the [OSDev](https://wiki.osdev.org/Printing_To_Screen) page for help on how to do this. Basically, all you have to do is write ASCII values to video memory. There's a demo program in C on the OSDev page that prints a string to the upper left corner of the screen. That would be a good place to start.


## Coding in C

If you want to write your project in C, you need to do the following steps to make it compile:

1. Create a new C file in the `src` directory. Put an empty function in it called `main`:

    int main() {
        for(;;);  // Loop forever
    }

## Searching Google

Googling for answers tends to be difficult because OS development is an arcane topic. Try adding "osdev" to your Google search. For example: "osdev XXX" where XXX is the term you're looking for. This will bring up answers from the OSDev wiki and forums, which tend to be pretty useful.
