# Python - Async

## Project Overview

This project focuses on asynchronous programming in Python, specifically using the `asyncio` library. Through a series of tasks, you will learn how to work with coroutines, asynchronous functions, and concurrent programming. The goal is to develop a deep understanding of how to write efficient, non-blocking code that can handle multiple tasks at once.

### Learning Objectives

By the end of this project, you should be able to:

- Understand the syntax and usage of `async` and `await` in Python.
- Execute asynchronous programs using the `asyncio` library.
- Run concurrent coroutines to perform tasks concurrently.
- Create and manage `asyncio` tasks.
- Use the `random` module to simulate delays and randomize results in asynchronous programs.

---

## Project Tasks

### Task 0: The Basics of Async

Create an asynchronous coroutine `wait_random` that takes an integer argument `max_delay` (default value of 10). The coroutine should wait for a random delay between 0 and `max_delay` seconds and return the delay value.

#### Example:

```python
#!/usr/bin/env python3

import asyncio
wait_random = __import__('0-basic_async_syntax').wait_random

print(asyncio.run(wait_random()))
print(asyncio.run(wait_random(5)))
print(asyncio.run(wait_random(15)))
Task 1: Execute Multiple Coroutines
In this task, you will import wait_random and write a new asynchronous coroutine wait_n that spawns wait_random multiple times (specified by the n argument). The function should return the list of all delays in ascending order, without using sort().

Example:
python
Copy code
#!/usr/bin/env python3

import asyncio
wait_n = __import__('1-concurrent_coroutines').wait_n

print(asyncio.run(wait_n(5, 5)))
print(asyncio.run(wait_n(10, 7)))
print(asyncio.run(wait_n(10, 0)))
Task 2: Measure the Runtime
Modify the previous task to include a measure_time function that measures the total execution time of wait_n. The function should return the total time divided by n.

Example:
python
Copy code
#!/usr/bin/env python3

measure_time = __import__('2-measure_runtime').measure_time

n = 5
max_delay = 9

print(measure_time(n, max_delay))
Task 3: Task - Wait for Random
Write a function task_wait_random that takes an integer max_delay and returns an asyncio.Task.

Example:
python
Copy code
#!/usr/bin/env python3

import asyncio
task_wait_random = __import__('3-tasks').task_wait_random

async def test(max_delay: int) -> float:
    task = task_wait_random(max_delay)
    await task
    print(task.__class__)

asyncio.run(test(5))
Task 4: Task - Wait for Multiple Coroutines
In this task, alter the wait_n function to create a new function task_wait_n. Instead of calling wait_random directly, call task_wait_random to create tasks.

Example:
python
Copy code
#!/usr/bin/env python3

import asyncio
task_wait_n = __import__('4-tasks').task_wait_n

n = 5
max_delay = 6
print(asyncio.run(task_wait_n(n, max_delay)))
Requirements
General Requirements:
All files should end with a new line.
Your files must be executable.
The first line of each file should be #!/usr/bin/env python3.
Your code should adhere to PEP 8 (Python style guide).
All functions and coroutines must be type-annotated.
All modules and functions should be properly documented.
Resources
Async IO in Python: A Complete Walkthrough
asyncio - Asynchronous I/O
random.uniform Documentation
License
Copyright © 2024 ALX, All rights reserved.

vbnet
Copy code

This `README.md` provides a clear overview of your project and each task, and it also includes the relevant resources and requirements. You can customize it further if needed. Let me know if you need any adjustments!






