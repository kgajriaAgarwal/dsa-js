
#### Valid Parenthesis

##### brute force - approach

function isValidParenthesis(s){
	let stack = [];
  
  for(let i = 0 ;i <s.length;i++){
  	let top = stack[stack.length-1];
    if(s[i] == "(" || s[i] == "[" || s[i] == "{"){
    	stack.push(s[i]);
    }
    else if(s[i] == ")" && top == "(" || s[i] == "}" && top == "{" ||s[i] == "]" && top == "["){
    	stack.pop();
    }
    else return false;
  }
  
  if(stack.length == 0){
  	return true
  }else{
   return false
  }

}

const input1 = '({{[]}})';
console.log("isValidParenthesis:", isValidParenthesis(input1));