# Ops Challenge - Python Requests Library

## Demo Code

The demo code below introduces concepts necessary to complete the challenge. 

```python
#!/usr/bin/env python3

# First you'll need to install the requests library to your system
# Next, like any library, import it into your Python script
import requests

# Assign a requests.get function to a variable. Be sure to pass a parameter (the URL) into the function for it to work.
response = requests.get('https://api.github.com')

# Print the status code obtained by the function using [var name].status code
print(response.status_code)

# This will return status code 200. Look it up at https://developer.mozilla.org/en-US/docs/Web/HTTP/Status
```
