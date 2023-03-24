##### Fibonacci series 

```
function fibonacciSeries(n){
	
  let res = [0,1];
  
  for(let i = 2;i<= n ; i++){
  	res[i] = res[i-2] + res[i-1];
  }
  
  return res;

}
```
##### print fibonacci series using recursion
/* function fibonacciUsingRecursion(n){
  
  const res = [];
  if(n<=1) res.push(n);
  else res.push(fibonacciUsingRecursion(n-1)+fibonacciUsingRecursion(n-2));
} */

console.log("res", fibonacciSeries(10));


##### createFibonacciNumber using Iteration
```
function createFibonacciNumber(n) {
	let res = [0,1]
	
  for(let i=2;i<= n;i++){
  	res[i] = res[i-2] +res[i-1]; 
  }
  
  return res[n]
}

console.log("createGFibonacciNumber:", createGFibonacciNumber(10));
```

##### createFibonacciNumber using recursion.

```
function fibonacciUsingRecursion(n){	
  if(n<=1) return n;
  else return fibonacciUsingRecursion(n-1)+fibonacciUsingRecursion(n-2);
}


console.log("fibonacciUsingRecursion:", fibonacciUsingRecursion(10));

```