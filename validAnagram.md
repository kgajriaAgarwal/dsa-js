#### Valid Anagram - leetcode problem no 242

- An anagram is a phrase/word formed by rearranging the lettersthe letters of a different word or phrase, typically using all the original letters exactly once

```
Example 1:

Input: s = "anagram", t = "nagaram"
Output: true

Example 2:

Input: s = "rat", t = "car"
Output: false
```

***Solution 1:***
- simple one liner solution

1. s= 'anagram'
2. t= 'nagaram'
*** Algorithm ***
3. Take first 's' string  -> convert it into array -> sort the array -> again convert it into string.
4. Repeat the same step 3 with string 't'.
5. If Both the sorted strings 's' and 't' are equal, then they are valid anagrams, otherwise they are not valid anagrams 

***Code***
```
var isAnagram = function(s, t) {
    return s.split('').sort().join('') === t.split('').sort().join('')
};

console.log("isAnagram:", isAnagram("anagram","nagaram"))
```
***output***
```
Output:

isAnagram: true
```

***Complexity***
- Time complexity:
- O(n) - We iterate over the array once.
- Space complexity:
- O(n) 

***solution 2***
- This is a better an a precise solution of the above problem using hash map.

***Example 1***
- s = 'anagram'
- t = 'nagaram' 

![Alt text](<autodraw 9_12_2023 (1).png>)

***Example 2***
- s = 'anagram'
- t = 'pgram' 

![Alt text](image.png)

***Example 3***
- s = 'anagram'
- t = 'gram' 

![Alt text](image-1.png)

***Explanation***
1. Firstly we need to check if length of both strings, if s.length !== t.length, then we will directly return false, as they are not valid anagrams
```
if(s.length !== t.length) return false
```

2. Now, If length of both the s and t string are equal then we need to check the occourances.
   - for eg. -> count of character 'a' in string 's' and string 't' , should be equal.
   - Similarly we need to do it for all the characters found.
   - For checking the ocoourances and maintaining the count of each and every chararcter in the string , we'll create a map
   - After creating the hashmap, we'll iterate over the characters of the first string 's'
   - Now, if we have encounterd the ch of string 's', that was already there in the hashmap, then we increment its occourance value in the hashmap by one
   - Incase we have encounterd the ch of string 's' for the first time then we'll set its coourance value 1 in the hashmap
```
const map = new Map();
for (const c of s){
    if(map.has(c)) map.set(c, map.get(c) + 1)
    else map.set(c, 1);
}
```








