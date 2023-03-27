### Two Sum 


/* Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice. You can return the answer in any order.
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1]. */

```
function twoSum(ar, tar){
  var result = [];
  for(let i =0 ;i<= ar.length; i++){
    for(let j =1 ;i<= ar.length; i++){
      if(ar[i] + ar[j] == tar) result.push(i,j)
    }
  }
  if(result.length == 0) console.log("no solution found!!");
  return result;
}

const nums = [2,7,11,15]
console.log("twoSum:", twoSum(nums, 22)); 
```

//Input: nums = [2,7,11,15], target = 9

##### Two Pointers Technique to solve two sum problem
-  ***Note Two pointers is really an easy and effective technique that is typically used for searching pairs in a sorted array.***

```
function twoSumUsingTwoPointerApproach(ar, target){
	var i = 0 ;
    var j = ar.length-1;
    var result = [];
    while(i<j){
     if(ar[i] + ar[j] == target) {
        result.push(i,j); 
        return result;
     }
     else if(ar[i] + ar[j] < target){
        i++;
     }else{
     	j--;
     }
    } 
    if(result.length == 0) console.log("solution not found");
}

const nums = [7,11,15, 23]
console.log("twoSumUsingTwoPointerApproach:", twoSumUsingTwoPointerApproach(nums, 26))
```


   
   