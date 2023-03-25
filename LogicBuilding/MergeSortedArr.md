### mergeSortedArray

##### Given 2 sorted arrays. Merge those 2 sorted array and returns a new array in sorted order. Try to do without sorting . Example arr1=[5,6,7,19] arr2=[4,12,21,27,31,42] output: [4,5,6,7,12,19,21,27,31,42] 

```
function mergeSortedArray(a,b){
	const merged = [];
  let aelm = a[0];
  let belm = b[0];
  let i =1;
  let j =1;
  
  if(a.length == 0){
  	return b;
  }
  if(b.length ==0){
  	return a;
  }
  
  while(aelm || belm){
  	if(aelm && !belm || aelm < belm){
    	merged.push(aelm);
      aelm = a[i++];
    }else{
    	merged.push(belm);
      belm = b[j++]
    }
  }
	return merged;
}

console.log(mergeSortedArray([2,5,6,9], [1,2,3,29]));
```

##### complexity
- Time Complexity : O(n1 + n2) 
- Auxiliary Space : O(n1 + n2)