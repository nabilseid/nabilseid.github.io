---
date: 2024-02-27
authors:
  - almightyPush
categories:
  - Soln
  - Python
---

# Soln: Python Challenge Solutions

<!-- more -->

## Hackerrank

### [Loops](https://www.hackerrank.com/challenges/python-loops/problem?isFullScreen=true)

The provided code stub reads and integer _`n`_ from STDIN. For all non-negative integers _`i`_ < _`n`_, print _`i`_^2^.

??? note "Further Explanation" 
    
    **Example**
    
    _`n`_ = 3
    
    The list of non-negative integers that are less than _`n`_ = 3 is [0, 1, 2]. Print the square of each number on a separate line.
    
    ```
    0
    1
    4
    ```
    
    **Input Format**
    
    The first and only line contains the integer, _`n`_.
    
    **Constraints**
    
    1 ≤ _`n`_ ≤ 20
    
    **Output Format**
    
    Print _`n`_ lines, one corresponding to each _`i`_.
    
    **Sample Input 0**
    
    ```
    5
    ```
    
    **Sample Output 0**
    
    ```
    0
    1
    4
    9
    16
    ```

**Solution**

```python 
if __name__ == '__main__':
    n = int(input())
    
    for i in range(n):
      print(i**2)
```


### [Write a Function](https://www.hackerrank.com/challenges/write-a-function/problem?isFullScreen=true)

Given a year, determine whether it is a leap year. If it is a leap year, return the Boolean True, otherwise return False.

Note that the code stub provided reads from STDIN and passes arguments to the is_leap function. It is only necessary to complete the is_leap function.

??? note "Further Explanation"
    
    An extra day is added to the calendar almost every four years as February 29, and the day is called a leap day. It corrects the calendar for the fact that our planet takes approximately 365.25 days to orbit the sun. A leap year contains a leap day.
    
    In the Gregorian calendar, three conditions are used to identify leap years:
    
    - The year can be evenly divided by 4, is a leap year, unless:
        - The year can be evenly divided by 100, it is NOT a leap year, unless:
            - The year is also evenly divisible by 400. Then it is a leap year.

    This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years. [Source](http://www.timeanddate.com/date/leapyear.html)
    
    **Input Format**

    Read _`year`_, the year to test.

    **Constraints**
    
    1900 ≤ _`year`_ ≤ 10^5^

    **Output Format**

    The function must return a Boolean value (True/False). Output is handled by the provided code stub.

    **Sample Input 0**
    
    ```
    1990
    ```

    **Sample Output 0**
    
    ```
    False
    ```

    **Explanation 0**
    
    1990 is not a multiple of 4 hence it's not a leap year.
