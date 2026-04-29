1. Line 12 will print 3. This happens because the variable i is declared using the var keyword within the for loop initialization. Variables declared with var are function-scoped rather than block-scoped, meaning i remains accessible anywhere within the discountPrices function even after the loop finishes. The loop terminates when i reaches 3 (since 3 is not less than prices.length), so 3 is the final value that gets printed to the console.

2. Line 13 will print 150. Because discountedPrice is declared using the var keyword inside the for loop, it is function-scoped rather than block-scoped. This means it is accessible outside the loop block. It retains the value calculated during the final iteration of the loop (where prices[i] was 300, so 300 \* 0.5 = 150).

3. Line 14 will print 150. The variable finalPrice was explicitly declared with var at the top of the function scope, so it is naturally accessible here. Like discountedPrice, it simply outputs the value that was assigned to it during the very last iteration of the for loop.

4. The function will return the array [50, 100, 150]. The code executes without errors because all variables are properly scoped within the function. The for loop successfully iterates through the input array [100, 200, 300], calculates a 50% discount for each item, pushes the rounded results into the discounted array, and returns that array.

5. Line 12 returns a ReferenceError because the variable i is declared using let in the for loop initialization. This makes i block-scoped strictly to the for loop, meaning it cannot be accessed outside of that block.

6. Line 13 returns a ReferenceError because the variable discountedPrice is declared using let inside the for loop. Like i, this makes it block-scoped to the loop, so it is completely inaccessible once the loop finishes executing.

7. Line 14 will print 150. The variable finalPrice was declared using let at the very beginning of the function block (line 4). This means it is block-scoped to the entire discountPrices function and is accessible anywhere inside it. It prints the value from the last iteration of the loop (where prices[i] was 300, resulting in 150).

8. The function will return the array [50, 100, 150]. It executes perfectly because all the variables are scoped appropriately. The discounted array is initialized at the function level, the loop calculates the 50% discount for each item without any scope leaks, pushes the results to the array, and successfully returns it at the end.

9. Line 11 returns a ReferenceError because the variable i is declared using let within the for loop initialization. This makes i block-scoped to the loop, meaning it cannot be accessed outside of the loop block.

10. Line 12 will print 3. The variable length is declared using const at the beginning of the discountPrices function. This makes it block-scoped to the entire function, so it is accessible anywhere inside the function. The value of prices.length is 3, which is what gets printed.

11. The function will return the array [50, 100, 150]. The code executes without errors. The discounted array is declared with const, meaning the variable cannot be reassigned to a new array, but its contents can still be mutated (which is what .push() does). The discountedPrice is calculated correctly in each iteration and added to the array, which is then returned.

12. Given the student object, here is the notation for each request:
    A. student.name (or student['name'])
    B. student['Grad Year'] (bracket notation is required because of the space in the property name)
    C. student.greeting()
    D. student['Favorite Teacher'].name
    E. student.courseLoad[0]

13. A evaluates to '32' because the + operator prefers string concatenation when one operand is a string. B evaluates to 1 because the - operator coerces the string to a number for subtraction. C evaluates to 3 because null coerces to 0 in numeric operations. D evaluates to '3null' because the + operator concatenates the string and the word 'null'. E evaluates to 4 because true coerces to 1. F evaluates to 0 because both false and null coerce to 0. G evaluates to '3undefined' because the + operator concatenates strings. H evaluates to NaN because undefined coerces to NaN in numeric operations, resulting in Not a Number.

14. A evaluates to true because the string '2' is coerced into a number for comparison. B evaluates to false because strings are compared alphabetically character by character, and '2' is greater than '1'. C evaluates to true because the == operator performs type coercion, converting the string '2' to a number before comparing. D evaluates to false because the === operator checks strict equality without type coercion, and a number is not a string. E evaluates to false because true coerces to the number 1, which does not equal 2. F evaluates to true because Boolean(2) evaluates to true, and true === true exactly.

15. The == operator checks for loose equality, meaning it will automatically attempt to convert the operands to the same data type before making the comparison. The === operator checks for strict equality, meaning it evaluates both the value and the exact data type; if the types are different, it immediately evaluates to false without converting anything.

16. js file

17. The result will be [2, 4, 6]. The modifyArray function iterates through the input array [1, 2, 3]. During each iteration, it passes the current element to the doSomething callback function, which multiplies the value by 2. The new values (2, 4, and 6) are pushed into the newArr array, which is returned at the end of the loop.

18. js file

19. The output is:
    1
    4
    3
    2
    This happens because 1 and 4 are executed synchronously on the main thread. The setTimeout for 3 has a 0ms delay, so it is sent to the callback queue and executes immediately after the main thread finishes its synchronous tasks. The setTimeout for 2 is placed in the queue and executes after a 1000ms delay.
