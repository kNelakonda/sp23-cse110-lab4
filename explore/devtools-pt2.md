# DevTools Debugging

1. The bug was that `num1` and `num2` are treated as strings, so when they are added together with `+` operator, they are concatenated together instead of added as if they were numbers, and `result` is also a string. In the example in the pictures, `num1` is '1', and `num2` is '12', and since they are strings that are concatenated together, `result` is '112'.
2.  To fix it, I would typecast `num1` and `num2` inside `calculateSum` using `Number()`.