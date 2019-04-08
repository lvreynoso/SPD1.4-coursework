```
Create a dictionary/hashmap where the keys are individual letters, and the values are integers.
For every character in the first string:
  If the character is a key in the dictionary, add 1 to its value.
  If not, make a new key-value pair with the character as the key and the value set to 1.
Create a boolean "result" variable and set it to TRUE.
For every character in the second string:
  If the character is not a key in the dictionary, set the result to FALSE.
  If the character is a key in the dictionary:
    If the value is 1 or greater, subtract 1 from it.
      If the value is now zero, delete the key from the dictionary.
    Else set the result to FALSE.
If the dictionary is not empty, set the result to FALSE.
Return the result.
```
