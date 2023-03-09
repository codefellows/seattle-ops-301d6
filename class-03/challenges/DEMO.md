# Ops Challenge - File Permissions

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```bash
#!/bin/bash

# Script:                       Ops 301 Ops Chall ##
# Author:                       Your Name
# Date of latest revision:      MM/DD/YYYY
# Purpose: xxx

# WARNING: Take care to only perform this operation in user-created directories and/or in a VM. Changing permissions in system files/directories is not advised, as this can cause malfunctions in the OS.

# In Unix the permissions are split up into three main parts:
  # The User is usually the original creator of the file/folder and is often referred to as the owner.
  # The Group owns the file/folder and is the group which the user is a part of.
  # Others which is everyone, the public/world, that is neither the owner or part of the owning group.


# How to view file permissions

# The ls -al command shows the User and Group that owns that file.
ls -al

# Add file name if you want to filter the view
touch testfile.txt
echo "Brand New Test File and Permissions: "
ls -al testfile.txt


# How to set file permissions to a single file

# File permissions can be manipulated using the chmod command, also known as "Change Mode"
# chmod 777: Everything for everyone
# This command will give read, write and execute permission to the owner, group and public.
echo "Give our Test File ALL the permissions: "
chmod 777 testfile.txt
ls -al testfile.txt


# How to set file permissions on this directory and all its contents

# "Recursively" means to perform the same task over and over again, on every item in a collection.
# The flag, -R, means recursively set permissions on this directory and all its contents
# When used with the chmod command, it means to configure multiple files and sub-directories using a single command.

# chmod 755: 7 in the first position means the owner gets +r +w +x. The 55 means the group and the public both get +r and +x.
chmod -R 755 ./
# chmod -R 777 ./
echo "What about the rest of the files: "
ls -al
# or use --recursive instead
# chmod --recursive 755 ./

```
