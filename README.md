# Longest palindrome in linked list

## [Solution](max-palindrome.py)

[GeekForGeeks Explaination](http://practice.geeksforgeeks.org/problems/length-of-longest-palindrome-in-linked-list/1)

## Notes 

Result in n^2 time complexity

Iterate over the items of the list while constructing a reverse list

Uses symetry of palindrom to check if it is one by comparing the reverse and current lists

Treats separately even and uneven palindroms (for each step, check both the even and uneven case)


### Max of more then 2 values

python's max can be used to keep track of max value when comparing more then 2 values

current_max = 2

current_max = max(current_max, some_value, other_value)

### copy and reference 

When you assign an object as attribute of an object, you assign the value that it references

Therefore if after that you change the reference associated with this second variable, you don't affect the original object


Example : 

```python
class Node:
    def __init__(self, data, next_=None):
        self.data = data
        self.next_ = next_

next_next_n = Node(4)
next_n = Node(3, next_next_n)
current = Node(2, next_n)
next_n = None # next_n no longer points to the same spot as current.next_
print(current.next_.data) # prints 3
```

## logical and

**and** is the keyword !

# First non repeating char in stream 

## [Solution](first-non-repeating-character-in-stream.py)

[GeekForGeeks Explanation](http://www.geeksforgeeks.org/find-first-non-repeating-character-stream-characters/)

Two data structures : 

- a list to keep track of the candidates for the next unrepeated character

- another list or dic to record number of instances of the character up to the current char

## Complexity

O(n^2) in time (for each char, if second-time it is met, might have to go through the candidate list to remove it)

O(n) in space

# Rotate image 90 degrees

## [Solution](rotate-im-square.py)

Do it in place by cyclic permutations

Mostly indexing problems, check manually results with specific values

## Complexity 

O(n) in time

additional space O(1)

# All unique characters

Exo 1.1 in HTCI

## [Solution](all_unique_chars.py)

## Notes 

`in` operation is usually O(1) for dic (and O(n) for list)

worse case for dic if all keys in dic have same hash value, then complexity is O(n)
