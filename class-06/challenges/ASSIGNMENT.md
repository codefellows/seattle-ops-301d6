# Ops Challenge: Bash in Python

## Overview

Reputed in the cyber community for its various applications ranging from malware analysis to penetration testing, Python is one of the most in-demand and recommended coding languages to learn for a career in cyber security. Today, you will be executing a Linux terminal commands from within a Python script.

## Resources

Python.org is a great encyclopedia of Python commands and will be a common reference as you practice this new language.

- [os — Miscellaneous operating system interfaces](https://docs.python.org/3/library/os.html){:target="_blank"}
- [Python.org's PEP8 Style Guide](https://www.python.org/dev/peps/pep-0008/){:target="_blank"}

Refer to [README.md](README.md){:target="_blank"} for more helpful resources in learning Python.

## Objectives

Before proceeding, ensure that course prework assignment "Setup Python" is complete.

Microsoft Visual Studio Code is the recommended IDE for Python assignments throughout the Ops sequence.

In Ubuntu, create a Python script that executes a few bash commands successfully. Indicate in comments how you achieved this.

Requirements:

- The Python module "os" must be utilized
- At least three variables must be declared in Python that contain results of bash operations
- The Python function print() must be used at least three times

Include execution of the following bash commands inside your Python script:

- `whoami`
- `ip a`
- `lshw -short`

## Stretch Goals (Optional Objectives)

Pursue stretch goals if you are a more advanced user or have remaining lab time.

- Instead of the `os` module, utilize the `subprocess` module instead. Refer to [python.org](https://docs.python.org/3/library/subprocess.html#module-subprocess){:target="_blank"} for how this can be achieved.

## Submission Instructions

- When you are ready to submit your shell script for grading, ACP it from VS Code to your **public** [GitHub](https://github.com/){:target="_blank"} repository. Name the file according to your course code and assignment, e.g. `ops-301d1: Challenge 01`.
- Copy the URL to your GitHub file and paste below as your submission. Add a comment in your Canvas assignment which includes the following:
  - A question within the context of today's lab assignment
  - An observation about the lab assignment, or related 'Ah-hah!' moment
  - How long you spent working on this assignment
