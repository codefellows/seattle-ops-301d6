# Ops Challenge: File Permissions

## Overview

Linux sets file permissions by User, Group, and Other. Linux also sorts permission by Read, Write, and Execute. Today, you will be create a bash script that alters file permissions of everything in a directory.

## Objectives

Take care to only perform this operation in user-created directories. Changing permissions in system files/directories is not advised, as this can cause malfunctions in the OS.

Create a new bash script that performs the following:

- Prompts user for input directory path.
- Prompts user for input permissions number (e.g. `777` to perform a `chmod 777`)
- Navigates to the directory input by the user and changes all files inside it to the input setting.
- Prints to the screen the directory contents and the new permissions settings of everything in the directory.

## Stretch Goals (Optional Objectives)

Pursue stretch goals if you are a more advanced user or have remaining lab time.

- Design your script to output a log file of all actions that were taken by the script.
- Design your script to output to the screen each file changed one by one, with a slight delay between each file changed.

## Submission Instructions

- When you are ready to submit your shell script for grading, copy your script to a new file in your **public** [GitHub](https://github.com/){:target="_blank"} repository. Name the file according to your cose code and assignment, e.g. `ops-301d1: Challenge 01`.
- Copy the URL to your GitHub file and paste below as your submission. Add a comment in your Canvas assignment which includes the following:
  - A question within the context of today's lab assignment
  - An observation about the lab assignment, or related 'Ah-hah!' moment
  - How long you spent working on this assignment
