1. `3`

   The variable i is declared using var, which has function scope (not block scope). That means it's still accessible outside the for loop, even after the loop ends. Since the loop runs while i < prices.length, and prices.length is 3, the final value of i is 3 once the loop stops. So, console.log(i) prints 3.

2. `150`

   The variable finalPrice is declared using var, which gives it function scope — meaning it's accessible anywhere inside the function, even outside of the for loop. In the last loop iteration: `prices[2] = 300`, `discount = 0.5`, so     `discountedPrice = 300 * (1 - 0.5) = 150`, `finalPrice = Math.round(150 * 100) / 100 = 150`
  That value (150) stays assigned to finalPrice, so when you log it after the loop ends (line 13), it prints: 150

3. `150`

   The variable finalPrice is declared with var, which gives it function scope. That means it can be accessed anywhere inside the function, including outside the for loop. By the time the loop finishes: The last value of `prices[i]`     is `300`, `discount = 0.5`, `discountedPrice = 300 * (1 - 0.5) = 150`, `finalPrice = Math.round(150 * 100) / 100 = 150`. So at line 14, `console.log(finalPrice)` prints: `150`

4. `[50, 100, 150]`

   This function applies a 50% discount (0.5) to each price in the array [100, 200, 300], then rounds the result and adds it to the discounted array.
    Step-by-step:
   
    `100 * (1 - 0.5) = 50`, rounded → 50

    `200 * (1 - 0.5) = 100`, rounded → 100
  
    `300 * (1 - 0.5) = 150`, rounded → 150
  
    Each value is pushed into the discounted array, which is returned at the end. No errors occur because all variables are properly scoped using var and the logic is valid.

5. `ReferenceError: i is not defined`

   The variable `i` is declared with `**let**`, which has block scope. That means `i` only exists inside the loop block (between {}). So when you try to access i outside the loop, on line 12, JavaScript throws a `ReferenceError`,           because `i` is not visible outside of its block.

6. `ReferenceError: discountedPrice is not defined`

     The variable `discountedPrice` is declared inside the for loop using `let`, which means it has block scope. This means it only exists within the curly braces {} of the for loop. Once the loop ends, `discountedPrice` is no longer       accessible, so trying to use it on line 13 (outside the loop) throws a `ReferenceError`.

7. `150`

   The variable finalPrice is declared using let outside the loop at line 4, which means it is in scope for the entire function. Each time through the loop, finalPrice is updated with a new discounted value. On the last iteration of      the loop:

     `prices[2] = 300`

    `discount = 0.5`

    `discountedPrice = 300 * (1 - 0.5) = 150`

    `finalPrice = Math.round(150 * 100) / 100 = 150`

    Since no reassignment restriction exists on let, and `finalPrice` is still in scope, line 14 prints: 150

8. `[50, 100, 150]`

   The function applies a 50% discount (0.5) to each price in the array `[100, 200, 300]`. It uses `let` for `discounted`, `finalPrice`, `i`, and `discountedPrice`, which means all variables are block scoped and safely used within         their appropriate sections.
    Here’s what happens in each iteration:

    `100 * (1 - 0.5) = 50` → rounded → 50

    `200 * (1 - 0.5) = 100` → rounded → 100

    `300 * (1 - 0.5) = 150` → rounded → 150

    Each of these values gets pushed to the discounted array, and then the function returns it.

9. `ReferenceError: i is not defined`

     The variable i is declared using let inside the for loop:

     `for (let i = 0; i < length; i++) {`
 
    Since let is block scoped, `i` only exists within the curly braces `{}` of the for loop. Line 11 is outside of that block, so trying to access `i` throws a `ReferenceError`, because it is out of scope.

10. `3`

    The variable `length` is declared on line 4 with `const`:

    `const length = prices.length;`

    `const variables` are block-scoped, but in this case, it’s declared in the function's top-level block, so it is accessible anywhere inside the function. Since the input array is `[100, 200, 300]`, `prices.length` is `3`, and             that's what gets logged at line 12.

11. `[50, 100, 150]`

    This function: Calculates a 50% discount for each price in the input array `[100, 200, 300]`. Stores the discounted values in the `discounted array`. Returns that array. Breakdown:

    `100 * (1 - 0.5) = 50`

    `200 * (1 - 0.5) = 100`

    `300 * (1 - 0.5) = 150`

    Each value is calculated using `const discountedPrice`, which is scoped to one loop iteration using `let i`.


12. A. `student.name`

    B. `student["Grad Year"]1`

    C. `student.greeting()`

    D. `student["Favorite Teacher"].name`

    E. `student.courseLoad[0]`

13. A. `32`

    The + operator with a string triggers string concatenation. The number 2 is converted to a string, so '3' + 2 becomes '3' + '2' → '32'.

    B. `1`

    The - operator forces numeric conversion. '3' becomes the number 3, so 3 - 2 = 1.

    C. `3`

    Null converts to 0 in numeric context. So this becomes 3 + 0 = 3.

    D. `'3null'`

    With the + operator, if either operand is a string, JavaScript performs string concatenation. So this becomes '3' + 'null' → '3null'.

    E. `4`

    True converts to 1 in numeric context. So 1 + 3 = 4.

    F. `0`

    False converts to 0 and null converts to 0. So 0 + 0 = 0.
    
    G. `'3undefined'`

    The + operator treats undefined as a string when combined with another string. '3' + 'undefined' → '3undefined'.
    
    H. `Nan`

    The - operator tries to convert both operands to numbers. '3' becomes 3, but undefined becomes NaN, so 3 -          NaN = NaN.

14. A. `true`

      JavaScript converts '2' to number 2, then compares: 2 > 1 → true.
   
    B. `false`

       Both are strings, so it's a lexicographic (alphabet) comparison: '2' comes after '1', so it’s false.

    C. `true`

       == does type coercion, so '2' is converted to number 2, and 2 == 2 → true.

    D. `false`

       === checks both value and type — number 2 is not the same type as string '2'.

    E. `false`

    Ttrue becomes 1, so 1 == 2 → false.

    F. `true`

       Boolean(2) is true because 2 is truthy. So it becomes true === true → true.

15.  `==` Is loose equality and compares values and allows type conversion. `===` Is strict equality and compares both value and type, with no conversion.

16. Separate file

17. `[2, 4, 6]`

    How I got to the result:

    1. `modifyArray` takes in:

         An array: `[1, 2, 3]`

         A callback function: `doSomething`, which doubles a number `(num * 2)`

    2. Inside the function:

         It creates an empty array: `newArr = []`

         It loops through `[1, 2, 3]`, and for each element:

         Calls `callback(array[i]) → doSomething(array[i])`

          Pushes the result into `newArr`

    3. Iteration:

         `doSomething(1) → 2`

         `doSomething(2) → 4`

         `doSomething(3) → 6`

    4. `newArr` becomes: `[2, 4, 6]`


18. Separate file
19.
   ```
   1

   4

   3

   2 
   ```




   
    
    
