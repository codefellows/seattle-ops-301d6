# Ops Challenge - Python Malware Analysis

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

How to we analyze code written by others? Let's practice.

```python
#!/usr/bin/env python3

def changeme( mylist ):
   mylist.append([1,2,3,4]);
   print("Values inside the function: ", mylist)
   return

mylist = [10,20,30];
changeme( mylist );
print("Values outside the function: ", mylist)

```

Break the code into pieces. Identify each component. Use what you know; for example, you know functions must be declared before they can be called.

```python
#!/usr/bin/env python3

# Function definition is here

def changeme( mylist ):
# This changes a passed list into this function

   mylist.append([1,2,3,4]);
   print("Values inside the function: ", mylist)
   return

# The function changeme has been declared. Now you can call changeme function.

# First, the script declares a variable called "mylist" as [10,20,30]
mylist = [10,20,30];

# The function changeme is called with the parameter "mylist" inserted.
changeme( mylist );

# Prints a string then the contents of "mylist" variable
print("Values outside the function: ", mylist)
```

By translating the code line by line and using the concepts we know, we can gradually interpret the meaning of code written by another person.
