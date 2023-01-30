## Array

#### Reverse An Array
```
const arr = [1,2,3,4,5];

const reverseArr = () => {
	for(let i=0;i<=arr.length/2;i++){
	   let first = arr[i];
    	   let last = arr[arr.length-1-i];
           let temp;
    
           temp = arr[i];
           arr[i] = arr[arr.length-1-i];
           arr[arr.length-i-1] = temp;
	}
	return arr;
}

console.log("reverse array:", reverseArr());
```
