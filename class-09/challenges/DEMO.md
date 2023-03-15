# Ops Challenge - Python Conditionals

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python
#!/usr/bin/env python3

a = 33
b = 200
if b > a:
  print("b is greater than a")


# Be sure to indent while writing an if statement, or else Python will error out.

a = 33
b = 200
if b > a:
print("b is greater than a") # you will get an error

# Use elif to add a condition that only checks if previous condition is not met

a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")

# Use and to make two conditions

a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")

# You can nest conditionals within each other

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```
