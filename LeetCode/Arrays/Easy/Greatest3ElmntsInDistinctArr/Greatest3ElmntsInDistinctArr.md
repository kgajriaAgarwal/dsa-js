##### Greatest 3 Elements Ina Distinct Array , Difficulty - easy

***Explanation for the Approach***

arr = [10,4,3,50,23,80,9]

- Take first =0 , second 0, third = 0
- Iterate over the loop and run the following condition in the loop

![Alt text](image.png)

- Let's start running the loop , with the following conditions

S.no | Element | array | condition run | consditions satisfied | Values
--- | --- | --- | --- |--- |--- 
arr[0] | 10 | ![Alt text](image-1.png) | ![Alt text](image-2.png) | first -  true, so will not go in the else part | first = 10, second = 0, third = 0
arr[1] | 4 | ![Alt text](image-3.png) | ![Alt text](image-4.png) | first - false, second - true, so will not go in the else part | first = 10, second = 4, third = 0
arr[2] | 3 | ![Alt text](image-5.png) | ![Alt text](image-6.png) | first - false, second - true , third - true | first = 10, second = 4, third = 3