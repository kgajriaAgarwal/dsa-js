##### Given 2 sorted arrays. Merge those 2 sorted array and returns a new array in sorted order. Try to do without sorting . Example arr1=[5,6,7,19] arr2=[4,12,21,27,31,42] output: [4,5,6,7,12,19,21,27,31,42] 

```
function mergeSortedArr(arr1, arr2){
	const arr = [...arr1, ...arr2];
  return arr.sort(function(a,b) { 
  	//return b-a;(descending)
    //(ascending)
    return a-b;
  })
}

const arr1=[5,6,7,19];
const arr2=[4,12,21,27,31,42];
//output: [4,5,6,7,12,19,21,27,31,42]

console.log(mergeSortedArr(arr1, arr2));
```