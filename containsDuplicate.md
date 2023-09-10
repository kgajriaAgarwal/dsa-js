### Leetcode 217 - contains duplicate

##### que
```
Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

Example 1:

Input: nums = [1,2,3,1]
Output: true
Example 2:

Input: nums = [1,2,3,4]
Output: false
Example 3:

Input: nums = [1,1,1,3,3,4,3,2,4,2]
Output: true
```

##### solution 1 - easy approach
###### Approach
- We can solve this problem using a hash set. We can iterate over the array and add each element to the hash set. If we encounter an element that is already in the hash set, we can return True, since it means that we have found a duplicate. If we finish iterating over the entire array and have not found a duplicate, we can return False.

*** Algorithm: ***

- Create an empty hash set.
- Iterate over the array.
- If an element is already in the hash set, return True.
- Otherwise, add the element to the hash set.
- If we finish iterating over the array and have not found a duplicate, return False.

***Complexity***
- Time complexity:
- O(n) - We iterate over the array once.
- Space complexity:
- O(n) - We use a hash set to store the elements.

```
var containsDuplicate = function(nums) {
  //create an empty hash set
  const map = new Map();
  //Iterate over the array of nums
  for(const n of nums){
    //If element is already in the hashset, return true
    console.log("map:", map);
    if(map.has(n)) return true;
    //Otherwise add the elemnet to the hashset
    map.set(n, true);
    // console.log(map);
  };
  //If we finish iterating over the array and have not found any dupliocate, return false
  return false;
};

console.log("containsDuplicate :",containsDuplicate([1,2,3,1]))
```
```
*** Output: ***
Output:

map: Map(0) {}
map: Map(1) { 1 => true }
map: Map(2) { 1 => true, 2 => true }
map: Map(3) { 1 => true, 2 => true, 3 => true }
containsDuplicate : true
```

*** Better Approach to this solution ***
- In js, we have set, which conatins only distinct element, no duplicate entries. Here we can create a set out of this array
and then compare the length of the set with the length of the array, If the length of the set and array is same then no duplicate entries are found , otherwise duplicate entries are there in the array, and return true

```
var containsDuplicate = function(nums) {
    const s = new Set(nums); return s.size !== nums.length
};

console.log("containsDuplicate :",containsDuplicate([1,2,3,10]))
```

*** Complexity ***
- Time complexity:
- O(n) - We iterate over the array once.
- Space complexity:
- O(n) 


