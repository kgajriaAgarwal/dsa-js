### Reverse a string

input --> hello, my name is karishma
output --> "reverse:", "amhsirak si eman ym ,olleh"

```
function reverse(str){
	let result = [];
	if(str.length < 1 && typeof str !== "string") console.log("Empty string , cannot be reversed");
	for(let i=str.length-1;i>=0;i--){
  	result.push(str[i])
  }
	return result.join('');
}

console.log("reverse:", reverse("hello, my name is karishma"));
```