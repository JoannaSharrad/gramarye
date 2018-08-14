# Gramarye
*Type Error Debugging Tool.*

Gramarye is a console and GUI based tool for discovering the line number of a type error in functional programming languages. Currently the language support consists of Haskell only.

Gramarye uses the Isolating Delta Debugging algorithm from Andreas Zeller and, a Blackbox Compiler.  

**Release date:** 

Soon!

**Prerequisites:**

For Haskell Type Error Support:
- GHC

For GUI Support:
- WX/WXCore

**GUI Notes**

Currently WX/WXCore does not work with the latest version of Haskell. To counter this the GUI code has been left intact in the source but has been commented out with "{-GUI-" and "-GUI-}" meaning that when it is available replacing all of the instances of these keywords will re-instate the GUI.

![Gramarye GUI](https://github.com/JoannaSharrad/gramarye/blob/master/images/gui.png)

![Gramarye GUI after locating Type Error](https://github.com/JoannaSharrad/gramarye/blob/master/images/gui2.png)


**Using Gramarye**

Build the program with:

ghc -o Gramarye Gramarye.hs

This has been tested and works on both Mac and Linux. 

*GUI*

Either double click the executable or run ./Main in the console.
Choose 'File -> Open' or just 'Open' from the toolbar and select your program source.
The debugger will run automatically and result in a giving you a line number of your type error.
Edit the original program source again and you can just press the recompile button to see if your change has vanquished the type error!

*Console*

Run with ./Main *pathToProgramSource*
The debugger will run automatically and result in a giving you a line number of your type error.
It will auto-quit the debugger so if you want to change your original program and re-test just re-run the first command.

![Gramarye Console after locating Type Error](https://github.com/JoannaSharrad/gramarye/blob/master/images/console.png)
