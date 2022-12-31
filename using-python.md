# How to read from the console in Python

To read input from the console in Python for CodeForces, you can use the `input()` built-in function. Here is an example of how to read integers and other values from the console:

```python
# A. Read An Integer
number = int(input())

# B. Read Multiple Integers
first_number, second_number = map(int, input().split())

# C. Read A Line Of Text
line = input()

# D. Read Multiple Words
first_word, second_word = input().split()

# E. Read An List
size = int(input()) # E.1. Read List's Size
array = list(map(int, input().split())) # E.2. Create A List/Store Elements
```

P.S: The `input()` function returns a string, so you may need to convert the input to the appropriate data type (e.g., `int`, `float`, etc) before using it in your code.

Also, ensure that your code follows the CodeForces submission guidelines and adheres to the specified time and memory limits for the problem. You can find more information about these guidelines in the [README](./README.md) page.

Try to solve [this problem](https://codeforces.com/problemset/problem/677/A) 😉🏆 Try not to cheat, but if you got stuck, here is our recommended solution:

```python
friends_number, fence_height = map(int, input().split())
friends_sum = 0
friends = list(map(int, input().split()))
for friends_height in friends:
    if friends_height > fence_height: friends_sum += 2
    else: friends_sum += 1

print(friends_sum)
```
