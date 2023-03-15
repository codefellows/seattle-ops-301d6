# Ops Challenge: Directory Creation

## Overview

Functions are universally useful across all coding languages for their role as a subroutine within a script that can accept input parameters. Today, you will be creating a Python script that utilizes a function from the `os` library to generate directory information.

## Objectives

Create a Python script that generates all directories, sub-directories and files for a user-provided directory path.

- Script must ask the user for a file path and read a user input string into a variable.
- Script must use the `os.walk()` function from the `os` library.
- Script must enclose the `os.walk()` function within a python function that hands it the user input file path.

## Template

Paste this code into a Python script as a starting point for you to work from.

```python
#!/usr/bin/env python3

# Import libraries

import os

# Declaration of variables

### Read user input here into a variable

# Declaration of functions

### Declare a function here

for (root, dirs, files) in os.walk("testdir"):
    ### Add a print command here to print ==root==
    print(root)
    ### Add a print command here to print ==dirs==
    print(dirs)
    ### Add a print command here to print ==files==
    print(files)

# Main

### Pass the variable into the function here

# End

```

## Stretch Goals (Optional Objectives)

Perform these optional objectives if you are an advanced user or have remaining lab time.

- Have the script save the output as a .txt file.
- Have the script open the .txt file with Libre Office Writer.

Add a function to your Python script that performs the following as a first step to prepare a test directory.

- Takes a user input string
- Creates a directory named the string using `os.makdirs` function
- Create sub-directories within the directory named 'string_01', 'string_02', and 'string_03'

## Submission Instructions

- When you are ready to submit your shell script for grading, ACP it from VS Code to your **public** [GitHub](https://github.com/){:target="_blank"} repository. Name the file according to your course code and assignment, e.g. `ops-301d1: Challenge 01`.
- Copy the URL to your GitHub file and paste below as your submission. Add a comment in your Canvas assignment which includes the following:
  - A question within the context of today's lab assignment
  - An observation about the lab assignment, or related 'Ah-hah!' moment
  - How long you spent working on this assignment
