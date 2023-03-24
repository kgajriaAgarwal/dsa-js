### Remove Duplicates

```
function removeDuplicate(arr){
		let res= [];
    for(let i=0;i<arr.length;i++){
			if(res.indexOf(arr[i]) ==-1){
      res.push(arr[i]);
      }
    }
    return res;
    
}

const arr1 = [5, 1, 1, 2, 3, 5, 8, 13, 2, 34, 55];

console.log("removeDuplicate:", removeDuplicate(arr1));
```