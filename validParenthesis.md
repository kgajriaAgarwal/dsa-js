#### Valid Parentheses - leetcode problem no 20 - Difficulty easy

- Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

An input string is valid if:

- Open brackets must be closed by the same type of brackets.
- Open brackets must be closed in the correct order.
- Every close bracket has a corresponding open bracket of the same type.
 
```
Example 1:

Input: s = "()"
Output: true
Example 2:

Input: s = "()[]{}"
Output: true
Example 3:

Input: s = "(]"
Output: false

```

***Solution 1:*** 
- Brute force approach
- Here we are going to use stack implementation of array.

***Approach***
This is a simple question 😃. We will traverse the string s from left to right and see if left and right parentheses are matching with their corresponding counterpart.
1. Traverse the string from left to right.
2. If we encounter the open/left parenthesis, then we will push it to the Stack data structure due to its Last In First Out (LIFO) property.
3. If we encounter any of the close/right parentheses, we will check it with the top of the stack. If it is the correct corresponding open/left parenthesis, we will move further, else we will return false.
4. At last, for valid string, the stack should be empty because all the left parentheses should have matched with the right ones.

***Code***
```
/**
 * @param {string} s
 * @return {boolean}
 */
function isValid(s){
    let stack = [];

    for(let i = 0 ;i<s.length; i++){
        let top = stack[stack.length -1];
        // if encounter opening brackets push to stack
        if(s[i] == "(" || s[i] == "{" || s[i] == "["){
            stack.push(s[i]);
        }
        // if encounter corresponding matching brackets , then pop from stack
        else if(top == '(' && s[i] ==')' || top == '{' && s[i] == '}' || top == '[' && s[i] == ']'){
            stack.pop();
        }
        else return false
    }
        if(stack.length == 0){
            return true;
        }
        else return false;

};

console.log("is valid parenthesis:", isValid('{{(]}}]'))
```
***output***
```
Output:

isAnagram: true
```

***Complexity***
- Time complexity:
- We are traversing the string once, hence the time complexity will be O(n).
- Space complexity:
- We are using Stack to store characters of the string, hence the space complexity will be O(n).

 

***solution 2***


```
