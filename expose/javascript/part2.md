# Part 2 Answers

1. Line 12 prints out 3. This is because `i` was declared with `var` and it was last incremented to 3 before the loop was exited. Being declared with `var` means `i` is scoped within the function it was declared in, not just the block.

2. Line 13 prints out 150. This is because `discountedPrice` was declared with `var` and it was last redeclared to 150 based on the calculation before the loop was exited. Being declared with `var` means `discountedPrice` is scoped within the function it was declared in, not just the block.

3. Line 14 prints out 150. This is because `finalPrice` was declared within the same function as the print statement on line 14, was changed in the loop, and was last changed to 150 before the loop was exited. Being declared with `var` means `discountedPrice` is scoped within the function it was declared in.

4. The function will return `[50, 100, 150]`. This is because `discounted` was declared with `var` in the scope of the function, and each `finalPrice` was pushed to `discounted` inside the loop, which was run. `discounted` is returned by the function on line 16, having not been changed after the loop.

5. On line 12 there will be an error, specifically a ReferenceError. This is because `i` was declared with the keyword `let`, which means it is only visible inside the the block in which it is declared. Line 12 is outside the block in which `i` was declared, and there was no other variable declared called `i` in the same block as line 12, which results in a ReferenceError.

6. On line 13 there will be an error, a ReferenceError. This is because `discountedPrice` was declared with the keyword `let`, which means it is only visible inside the the block in which it is declared. Line 13 is outside the block in which `discountedPrice` was declared, and there was no other variable declared called `discountedPrice` in the same block as line 13, which results in a ReferenceError.

7. On line 14, the program will print out `150`. This is because `finalPrice` was declared in the same block as line 14 and with the keyword `let`. `finalPrice` was altered in blocks that were within the same block as line 14, and as a result, it has a different number than the number it was declared with, so line 14 prints out `150`.

8. The function `discountPrices` will return `[50, 100, 150]`. The returned value within the function, `discounted` was declared with the keyword `let` within the outer block of the function. It was also returned in the same block. Since it was in the same block and only changed within blocks within the function, there are no errors and it returns the value above.

9.  On line 11 there will be an error, specifically a ReferenceError. This is because `i` was declared with the keyword `let`, which means it is only visible inside the the block in which it is declared. Line 11 is outside the block in which `i` was declared, and there was no other variable declared called `i` in the same block as line 11, which results in a ReferenceError.

10. On line 12, the program will print out `3`. This is because earlier within the block there was a variable declared `length` with the keyword `const`. `length` was also not altered in this program afterwards, so the program runs properly and line 12 will print out the same value that `length` was earlier.

11. The function will return `[50, 100, 150]`. This is because `discounted` was assigned to an array in the same block of code in which it was returned, and the variable was not reassigned. Although the array itself changed, `discounted` was not reassigned to a different array in memory, so the variable did not change, and no errors occur.

12. A. `student.name` \ 
    B. `student.['Grad Year'];` \ 
    C. `student.greeting()` \ 
    D. `student['Favorite Teacher'].name` \ 
    E. `student.courseLoad[0]`

13. A. `'3' + 2` outputs to 32. This is because the `2` will convert to a String and concatenate with the string `'3'`. \ 
    B. `'3' - 2` ouputs to 1. This is because `-` is a mathematical function, so `'3'` will convert to an integer, and 3-2 = 1. \ 
    C. `3 + null` outputs 3. `3` is a number, and in numeric conversion, `null` is 0, and 3 + 0 = 3. \ 
    D. `'3' + null` outputs `'3null'`. Concatentation of a string with `null` starts with `null` converting into `'null'`, followed by normal concatentation rules between two strings. \ 
    E. `true + 3` outputs 4. `true`, as a keyword for booleans, is 1 in arithmetic, so 1 + 3 = 4. \ 
    F. `false + null` outputs `0`. In arithmetic, `false` is 0, and `null` is 0, and 0 + 0 = 0. \ 
    G. `'3' + undefined` outputs `3undefined`. Javascript converts `undefined` into the string `'undefined'` because it is being added to another string, and the `+` concatenates the two strings. \ 
    H. `'3' - undefined` outputs `NaN`. Subtraction is treated as arithmetic, so `'3'` converts to 3, and `undefined` converts to NaN. 3 - NaN is NaN, or Not a Number.
14. 
