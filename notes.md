# Truffula Notes
As part of Wave 0, please fill out notes for each of the below files. They are in the order I recommend you go through them. A few bullet points for each file is enough. You don't need to have a perfect understanding of everything, but you should work to gain an idea of how the project is structured and what you'll need to implement. Note that there are programming techniques used here that we have not covered in class! You will need to do some light research around things like enums and and `java.io.File`.

PLEASE MAKE FREQUENT COMMITS AS YOU FILL OUT THIS FILE.

## App.java
- This class is the starting point of the program. It's where execution begins. 
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
- ColorPrinter.java uses PrintStream to print text to the terminal using ansi escape codes. 
- There's an option to keep text color active or not
- Gets the ansi codes from ConsoleColor.java
- Sets the color of the text depending on the ansi code
- ColorPrinterTest.java runs a test to make sure you can set the color to a text, print that color text and also reset the color.

## TruffulaOptions.java / TruffulaOptionsTest.java
- TruffulaOptions.java controls where the directory tree starts printing from
- Uses flags to determine whether to show hidden files or use color for text
- Throws exceptions for unknown arguments and missing directories
- Constructs an object with the values that were entered into the terminal regarding where to start building the tree from and whether to show hidden files and use color so other parts of the program can use them. 
- TruffulaOptionsTest.java creates a new directory with the arguments to have no color text, to show hidden files and gives it a root to start building from and checks if the directory is built correctly.

## TruffulaPrinter.java / TruffulaPrinterTest.java
- TruffulaPrinter.java handles printing the directory tree structure
- It uses TruffulaOptions to determine how the tree shuold be printed (like showing hidden files, using color, and where to start).
- It uses ColorPrinter to handle colored output.
- colorSequence uses multiple colors to show the differet levels of the directory tree
- It's where the logic lives for buidling and displaying the tree.
- TruffulaPrinterTest.java is used to make sure TruffulaPrinter prints the directory tree correctly.
- There is a created directory structure using all of the associated classes and checks if the output matches the created directory. 
- There is what looks like a helper method to check if the current operating system is windows and another helper method to make sure tests work on windows and UNIX-like systems.

## AlphabeticalFileSorter.java
- Sorts the files in the directory tree in alphabetical order by name ignoring case. 
- Returns a sorted array of files
- Takes in a single argument of File[] called 'files'