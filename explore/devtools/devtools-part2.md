1. The inputs from the text fields were strings, not numbers. When added together, they were being concatenated instead of added numerically.
2. Convert the inputs to numbers using `Number(num1)` and `Number(num2)` before performing the addition.  

