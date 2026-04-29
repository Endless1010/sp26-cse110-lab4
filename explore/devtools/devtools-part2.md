1. The bug was that num1 and num2 were being passed into calculateSum() as strings instead of numbers. This caused the + operator to perform string concatenation instead of arithmetic addition, so inputs like 1 and 2 would produce "12" instead of 3.

2. Fix is a screenshot.
