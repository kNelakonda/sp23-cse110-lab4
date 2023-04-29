# Part 2 Answers

1. Line 12 prints out 3. This is because `i` was declared with `var` and it was last incremented to 3 before the loop was exited. Being declared with `var` means `i` is scoped within the function it was declared in, not just the block.

2. Line 13 prints out 150. This is because `discountedPrice` was declared with `var` and it was last redeclared to 150 based on the calculation before the loop was exited. Being declared with `var` means `discountedPrice` is scoped within the function it was declared in, not just the block.

3. Line 14 prints out 150. This is because `finalPrice` was declared within the same function as the print statement on line 14, was changed in the loop, and was last changed to 150 before the loop was exited. Being declared with `var` means `discountedPrice` is scoped within the function it was declared in.

4. The function will return `[50, 100, 150]`. This is because `discounted` was declared with `var` in the scope of the function, and each `finalPrice` was pushed to `discounted` inside the loop, which was run. `discounted` is returned by the function on line 16, having not been changed after the loop.

5. On line 12 there will be an error, a ReferenceError. This is because `i` was declared with the keyword `let`, which means it is only visible inside the the block in which it is declared. Line 12 is outside the block in which `i` was declared, and there was no other variable declared called `i` in the same block as line 12, which results in a ReferenceError.

6. On line 13 there will be an error, a ReferenceError. This is because `discountedPrice` was declared with the keyword `let`, which means it is only visible inside the the block in which it is declared. Line 13 is outside the block in which `discountedPrice` was declared, and there was no other variable declared called `discountedPrice` in the same block as line 13, which results in a ReferenceError.

7. On line 14, the program will print out `150`. This is because `finalPrice` was declared in the same block as line 14 and with the keyword `let`. `finalPrice` was altered in blocks that were within the same block as line 14, and as a result, it has a different number than the number it was declared with, so line 14 prints out `150`.

8. The function `discountPrices` will return `[50, 100, 150]`. The returned value within the function, `discounted` was declared with the keyword `let` within the outer block of the function. It was also returned in the same block. Since it was in the same block and only changed within blocks within the function, there are no errors and it returns the value above.
9. 
