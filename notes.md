# Truffula Notes
As part of Wave 0, please fill out notes for each of the below files. They are in the order I recommend you go through them. A few bullet points for each file is enough. You don't need to have a perfect understanding of everything, but you should work to gain an idea of how the project is structured and what you'll need to implement. Note that there are programming techniques used here that we have not covered in class! You will need to do some light research around things like enums and and `java.io.File`.

PLEASE MAKE FREQUENT COMMITS AS YOU FILL OUT THIS FILE.

## App.java
- This file is the starting point of the program. It's where execution begins. 
- Looks like it uses the command line arguments to create objects and start the truffula app.
- Arguments like -h triggers specific actions, like showing showing hidden files.
- It's where we call our methods. 

## ConsoleColor.java
- It looks like we have a fixed set of colors.
- Each color is tied to an ansi escape code
- When we enter an ansi escape code into the terminal whatever color
that code is associated with will turn the text that color
- I think the purpose of enum is to allow the program to use and reference these colors when printing the directory tree

## ColorPrinter.java / ColorPrinterTest.java
- This file uses PrintStream to print text to the terminal using ansi escape codes. 
- There's an option to keep text color active or not
- Gets the ansi codes from ConsoleColor.java
- Sets the color of the text depending on the ansi code

## TruffulaOptions.java / TruffulaOptionsTest.java

## TruffulaPrinter.java / TruffulaPrinterTest.java

## AlphabeticalFileSorter.java