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
