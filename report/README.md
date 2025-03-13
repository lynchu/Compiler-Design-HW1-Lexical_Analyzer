# hw1 report

|Field|Value|
|-:|:-|
|Name|朱致伶|
|ID|110550062|

## How much time did you spend on this project

Toal: 6 hours.

## Project overview (Describe the project structure and how you implemented it.)

This project is divided into four key parts:

1. **Defining Regular Expressions for Token Names**
2. **Setting Actions for Token Types Using `listToken` and `listLiteral`**
3. **Implementing Custom Functions for Complex Token Types (e.g., Strings and Keywords)**
4. **Handling C/C++ Comments with Start Conditions**

### Part 1: Lexical Definition
I categorized tokens into delimiters, operators, digits, integers, floating points, octal integers, real numbers, spaces, letters, and strings. Well-defined regular expressions simplify action design for each token type.

### Part 2 & 3: Token Actions
Most token actions are implemented using `listToken` and `listLiteral`. However, strings require special handling since double quotes can appear as consecutive characters within string constants. A dedicated action ensures correct parsing of these cases. Additionally, the `isKeyword` function verifies whether an identifier matches a reserved keyword.

### Part 4: Handling C/C++  and Pseudo Comments
C++-style comments are easier to handle as they terminate with `\n`. In contrast, C-style comments can span multiple lines, requiring carefully designed regular expressions. Both types are managed using exclusive start conditions. As for Pseudo comment, it is managed with `opt_src` and `opt_tok`.

## What is the hardest you think in this project

The most challenging aspects were designing regular expressions for C-style comments and scientific numbers. Expressing these correctly took multiple iterations of trial and error to me.

## Feedback to T.A.s

> Please help us improve our assignment, thanks.
