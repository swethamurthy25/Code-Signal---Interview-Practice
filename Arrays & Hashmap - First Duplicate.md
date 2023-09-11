Given an array a that contains only numbers in the range from 1 to a.length, find the first duplicate number for which the second occurrence has the minimal index. 
In other words, if there is more than 1 duplicated number, return the number for which the second occurrence has a smaller index than the second occurrence of the other 
number does. If there are no such elements, return -1.

### Example:

For a = [2, 1, 3, 5, 3, 2], the output should be solution(a) = 3.

There are 2 duplicates: numbers 2 and 3. The second occurrence of 3 has a smaller index than the second occurrence of 2, so the answer is 3.

For a = [2, 1, 3, 5, 3, 2], the output should be solution(a) = 3.

There are 2 duplicates: numbers 2 and 3. The second occurrence of 3 has a smaller index than the second occurrence of 2, so the answer is 3.

_______________________________________________________________________________________________________________________________________

### Solution:

1. Here first we need to iterate through the array and find the duplicate numbers
2. If duplicate numbers are found, check for their second occurrence and return their index
3. If no duplicate numbers are found, just return -1

When we need to check for occurrences and their indices, we can make use of a hashmap/dictionary or the HashSet to solve this problem.

### Using hashmap

```python
def solution(a):
    hashmap = {}
    for i,num in enumerate(a):
        if num not in hashmap:
            hashmap[num] = i
        else:
            if hashmap[num] < i:
                return num
    return -1
```


### Using HashSet

```python
def solution(a):
    hashset = set()
    for i in a:
        if i not in hashset:
            hashset.add(i)
        else:
            return i
    return -1
```




