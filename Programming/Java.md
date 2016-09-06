# Java Style Guide
1. [Formatting](#1---formatting)
2. [Naming Conventions](#2---naming-conventions)
  1. [Variables](#21---variables)
  2. [Classes](#22---classes)
  3. [Files](#23---files)
  4. [Objects](#24---objects)
3. [Documentation](#3---documentation)
  1. [Comments](#31---comments)
  2. [Javadocs](#32---javadocs)
4. [Miscellaneous](#4---miscellaneous)

These guidelines aim to lay out the basic guidelines for SERT software in a clear and concise manner. It does not attempt to cover every possible situation but rather common and ambiguous cases. For cases not addressed here, use common sense or refer to the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html). SERT's rules fall in line with Google's, and the Google guide goes more in depth.

## 1 - Formatting
When it comes code formatting, the most important piece is that its consistent. The style you use normally may be perfectly valid, but if it does match SERT's style, it can produce code that is unorganized, confusing, and less clean. Therefore we ask that all SERT programmers use the following formatting guidelines.

- Left braces should be placed on the same line as the preceding code (if statements, for loop initialization, etc.) with a space in between. Right braces should have their own line at the same indentation level as the beginning of the block. For example:
```java
if (condition) {
    // do something
    // something else
}
```
- Braces should be used with `if`, `else`, `for`, `do` and `while` even if the body is only one line.
- Empty blocks may have the right brace immediately follow the left brace with nothing in between. For example:
```java
void myFunction() {}
```
- Use one tab for each level of indentation.

## 2 - Naming conventions
### 2.1 - Variables
Variables names should use camel case (i.e., camelCase).

Variable names should clearly indicate the variable's purpose. Generic variable names are permissible only in small scopes (e.g., a short function) where the variable's purpose is clear.

### 2.2 - Classes
Classes should use pascal case (i.e., PascalCase).

Command names should clearly state what action the command completes (`TraverseCheval`, `OpenPortcullis`, etc.). If the command name also includes a subsystem name, the subsystem name should be at the end (e.g. `TeleopDrivetrain`, not `DrivetrainTeleop`).

Subsystem names should clearly indicate what physical part of the robot they represent (e.g. `Lock`, `Drivetrain`). If it is a PID subsystem, its name should end in PID.

### 2.3 - Files
Files should have the same name as the class they define.

### 2.4 - Objects
If a class is instantiated only once (which is usually the case with subsystems), the objects name should be the name of the class except with an initial lowercase letter. If it is instantiated more than once, follow normal [variable naming conventions](#1---variables).

## 3 - Documentation
### 3.1 - Comments
Comments should be used to describe short blocks of code and non-public fields, if necessary. (Public fields should be described with Javadocs instead, see the next section.) They can make code much more understandable, but they should not serve as a crutch. Before adding a comment, first ensure that your code is written in the most clear way possible. Comments themselves should be as concise as possible.

When changing code, be sure you change any related comments. Incorrect comments are one of the worst things for code readibility. Likewise, when writing comments make clear exactly what code it's describing so others (or future you) know to update the comment if they update its code.

When using the automatically generated WPILib templates, remove the default comments. Although they may be useful at first, in the long term they clog up code and aren't read by anyone. The information is also redundant because it is readily available online and does not need to be repeated in SERT code.

### 3.2 - Javadocs
Since Javadocs were designed to generate a public API, they should only be used for public fields. In the first paragraph, explain the purpose of the field. In the next, if necessary, explain any needed precautions or possible  problems. Lastly, remember to use the `@param`, `@return`, and `@see` tags if needed.

For more information, see [Oracle's Javadoc guide](http://www.oracle.com/technetwork/articles/java/index-137868.html).

## Miscellaneous
- Before you commit any Java files, please remove all prints and SmartDashboard outputs used for debugging (i.e., anything you don't think drivers actually will need to see). Otherwise they become scattered and difficult to track down while clogging up the console and SmartDashboard.
