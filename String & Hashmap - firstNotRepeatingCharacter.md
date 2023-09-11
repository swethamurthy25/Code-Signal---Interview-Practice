Given a string s consisting of small English letters, find and return the first instance of a non-repeating character in it. If there is no such character, return '_'.

### Example:

* For s = "abacabad", the output should be solution(s) = 'c'.

  There are 2 non-repeating characters in the string: 'c' and 'd'. Return c since it appears in the string first.

* For s = "abacabaabacaba", the output should be solution(s) = '_'.

  There are no characters in this string that do not repeat.
____________________________________________________________________________________________________________________________________________________________________

### Understanding of the question:

1. We are given an input string of characters, we need to iterate over all characters and find which character is not repeating.
2. In order to do that, we need to know the count/occurrence of each character.
3. If the count is 1, it means the character is the non-repeating one.
4. Return that as output , if no non-repeating characters are found return "_"

TC is O(n) and SC is O(n) since we are going to store the occurrence of each character in hashmap/dictionary.

```python
def solution(s):
    hashmap = {}
    for i in s:
        if i not in hashmap:
            hashmap[i] = 1
        else:
            hashmap[i] += 1
            
    for ch in hashmap:
       if hashmap[ch] == 1:
           return ch
    return "_"
````
_________________________________________________________________________________________________
