### Check Prime

```
//num  --> 1, num
function checkPrime(num){
	let isPrime = true;
	for(let i=2;i<num;i++){
  	if(num%i == 0){
    	isPrime = false;
    }
  }
	return isPrime
}

console.log("check Prime:", checkPrime(147))
```