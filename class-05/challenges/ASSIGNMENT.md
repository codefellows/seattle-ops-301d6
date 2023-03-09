# Ops Challenge: Clearing Logs

## Overview

Log clearing can be useful as an administrator of your logs are routinely rotated, or you're in a situation where the log file sizes are getting out of hand. Today, you will be writing a bash script that clears log files for you.

## Objectives

Write a log clearing bash script.

## Tasks

Write a bash script that performs the following tasks:

- Print to the screen the file size of the log files before compression
- Compress the contents of the log files listed below to a backup directory
  - `/var/log/syslog`
  - `/var/log/wtmp`
- The file name should contain a time stamp with the following format `-YYYYMMDDHHMMSS`
  - Example: `/var/log/backups/syslog-20220928081457.zip`
- Clear the contents of the log file
- Print to screen the file size of the compressed file
- Compare the size of the compressed files to the size of the original log files

## Stretch Goals

In offensive security operations, often an attacker will want to use a log clearing script to remove the evidence of their behavior on the targeted computer systems. How can your script be used to clear tracks?

- Watch [How To Clear Tracks & Logs On Linux](https://www.youtube.com/watch?v=TgquV_OA-lU&ab_channel=HackerSploit){:target="_blank"}
- Using the knowledge of various logs described in this video, expand your script; what other system logs can you clear? See how many logs you can clear!
- In your comments per log cleared, explain what the log tracks in the Ubuntu system. Why is this log important?

## Submission Instructions

- When you are ready to submit your shell script for grading, ACP it from VS Code to your **public** [GitHub](https://github.com/){:target="_blank"} repository. Name the file according to your course code and assignment, e.g. `ops-301d1: Challenge 01`.
- Copy the URL to your GitHub file and paste below as your submission. Add a comment in your Canvas assignment which includes the following:
  - A question within the context of today's lab assignment
  - An observation about the lab assignment, or related 'Ah-hah!' moment
  - How long you spent working on this assignment
