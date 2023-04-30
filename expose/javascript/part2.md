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

12. Object Notation:
    1.  A. `student.name`
    2.  B. `student.['Grad Year'];`
    3.  C. `student.greeting()` 
    4.  D. `student['Favorite Teacher'].name` 
    5.  E. `student.courseLoad[0]`

13. Arithmetic:
    1.  A. `'3' + 2` outputs to 32. This is because the `2` will convert to a String and concatenate with the string `'3'`. 
    2.  B. `'3' - 2` ouputs to 1. This is because `-` is a mathematical function, so `'3'` will convert to an integer, and 3-2 = 1. 
    3.  C. `3 + null` outputs 3. `3` is a number, and in numeric conversion, `null` is 0, and 3 + 0 = 3.
    4.  D. `'3' + null` outputs `'3null'`. Concatentation of a string with `null` starts with `null` converting into `'null'`, followed by normal concatentation rules between two strings.
    5.  E. `true + 3` outputs 4. `true`, as a keyword for booleans, is 1 in arithmetic, so 1 + 3 = 4.
    6.  F. `false + null` outputs `0`. In arithmetic, `false` is 0, and `null` is 0, and 0 + 0 = 0.
    7.  G. `'3' + undefined` outputs `3undefined`. Javascript converts `undefined` into the string `'undefined'` because it is being added to another string, and the `+` concatenates the two strings. 
    8.  H. `'3' - undefined` outputs `NaN`. Subtraction is treated as arithmetic, so `'3'` converts to 3, and `undefined` converts to NaN. 3 - NaN is NaN, or Not a Number.

14. Comparison:
    1.  A. `'2' > 1` evaulates to `true`. This is because `'2'` converts to the integer 2, and then is compared to the integer 1.
    2.  B. `'2' < '12'` evaulates to `false`. In this boolean expression, since both values being compared are strings, there is no type conversion, and they are being compared as if they are strings rather than integers. The strings are compared character by character, starting with the first character. Here '2' is greater than '1', so the boolean expression evaluates to false.
    3.   C. `2 == '2'` evaluates to `true`. In this expression, `'2'`, which is a string, is converted into the integer 2. 2 equals 2, so this is true.
    4.   D. `2 === '2'` evaulates to `false`. `===` is a strict equality operator, so it will check without type conversion. Since `2` (integer) and `'2'` (string) are not of the same type, the output is false.
    5.   E. `true == 2` evaluates to `false`. When compared with a number, `true` is treated as the number 1. 1 is not equal to 2, so this evaluates to false.
    6.   F. `true === Boolean(2)` evaluates to `true`. This is because the function `Boolean(2)` is a "true" value, and so `true` has the same type as a "true" value. 
    
15. `==` is a regular equality operator that will convert types to compare equality. Other the other hand, `===` will not convert types and is a strict equality operator. If the two values being compared using the `===` operator are not even of the same type, the expression will evaluate to false.

16. The answer is in `part2-question16.js`

17. The result from `modifyArray([1, 2, 3], doSomething)` is an array returned with the values `[2, 4, 6]`. In this program, `modifyArray` is called with the first parameter being an array. The second parameter is a function, which, in the loop inside `modifyArray`, will be called, taking in a value from the array that was the first parameter. In this specific case, `doSomething` is the second argument that is called back to, and `doSomething` returns 2 times the parameter of it. This entire program results in returning an array that has 2 times every value from the array that was passed into `modifyArray` on line 13.

18. The answer is in `part2-question18.js`

19. The output will be:
(each number is on a new line)
> 1 
> 4 
> 3 
> 2
