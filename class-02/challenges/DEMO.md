# Ops Challenge - Append; Date and Time

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```bash
#!/bin/bash

# Script:         Ops 301 Ops Chall 02
# Purpose:        Append, date and time
# Why:            Time stamping is a critical step in automating log generation.

# How to show time and date

# Running date command from terminal gives a general output
echo `date`
# or
echo $(date)

# Here we assign variables but you can run these commands on their own without the ` outside the command string. These are modifiers shown.
year=`date +%Y`
echo $year
month=`date +%m`
echo $month
day=`date +%d`
echo $day

# The date command displays the local system's date and time

hour=`date +%H`
echo $hour
minute=`date +%M`
echo $minute
second=`date +%S`
echo $second

# Put it all together
echo "Current Date: $day-$month-$year"
echo "Current Time: $hour:$minute:$second"


# How to row append

# First create a file testfile.txt and add some lines to it.
echo "Original file before append:"
cat testfile.txt

# The >> double carrot will row append
echo "My new string with date: `date`" >> testfile.txt
echo "Appended file:"
cat testfile.txt

# End

```
