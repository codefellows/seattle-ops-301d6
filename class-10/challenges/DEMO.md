# Ops Challenge - Python File Handling

## Demo Code

The demo code below introduces concepts necessary to complete the challenge. 

```python
#!/usr/bin/env python3

# Create a new file if it does not exist
f = open("demofile.txt", "w")

# How to open a file
f = open("demofile.txt")

# How to open a file and read it
f = open("demofile.txt", "r")
print(f.read())

# How to return the five first characters of a file
f = open("demofile.txt", "r")
print(f.read(5))

# Close a file when you're finished
f = open("demofile.txt", "r")
print(f.readline())

```
