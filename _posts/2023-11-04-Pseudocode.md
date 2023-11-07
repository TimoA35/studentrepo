---
toc: true
comments: true
layout: post
title: Pseudo Code notes
description: Python
type: hacks
courses: { csse: {week: 1}, csp: {week: 10, categories: [4.A]}, csa: {week: 0} }
categories: [C1.4]
---

**Pseudo Code vs Python**

Example 1: Finding the Maximum of Two Numbers

Pseudo Code 

```script
Start
  Input num1
  Input num2
  If num1 > num2
    Display num1
  Else
    Display num2
  End If
Stop
```

Python

```python
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: ")

if num1 > num2:
    print(num1)
else:
    print(num2)
```
Example 2: Calculating the Sum of Integers from 1 to N

Pseudo Code 

```script
Start
  Input N
  sum = 0
  For i from 1 to N
    sum = sum + i
  End For
  Display sum
Stop
```

Python

```python
N = int(input("Enter a number: "))
sum = 0

for i in range(1, N + 1):
    sum += i

print(sum)
```
