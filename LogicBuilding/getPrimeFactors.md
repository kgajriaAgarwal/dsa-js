#### Get Prime factors

```
function getPrimeFactors(num){
	var factors = [];
    var divisor = 2;
  
  while(num >2){
  	if(num%divisor ==0){
    	factors.push(divisor);
        num = num/divisor;
    }else divisor++
  }
	return factors;
}

console.log(getPrimeFactors(36));
```