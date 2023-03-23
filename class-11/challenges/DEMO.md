# Ops Challenge - Psutil

## Demo Code

The demo code below introduces concepts necessary to complete the challenge. 

```python
#!/usr/bin/env python3

# Libraries are imported at the top of any Python script using syntax import [library]
sudo pip install psutil

# Generate CPU times as a named tuple
print(psutil.cpu_times())

# Show current CPU consumption
print(psutil.cpu_percent())

```
