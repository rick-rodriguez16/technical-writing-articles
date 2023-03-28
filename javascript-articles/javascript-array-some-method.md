# Javascript .some() method

The `some()` method in Javascript is used to determine if there exists at least one element in the array (or array-like object) that satisfies a given condition by a provided callback function. If such an element exists, the method stops immeditately and returns true.  If such an element does not exist, the method will return false upon completion.

## Key details of the `some()` method

The `some()` method is one of the many iterative methods of the Javascript Array class.  That is, the `some()` method takes a callback function and applies it to each element in an array in consecutive order. The return value of the callback function is what determines the outcome of `some()` method, either `true` or `false`.  The `some()` method does not directly change (mutate) the element values of the array that is used with it.  However, the callback function can do so.

The syntax for the `some()` method is as follows:

![Syntax of the Javascript some method](./images/javascript-img/some-method-syntax.svg)

*Figure 1: Syntax of the Javascript `some()` method*



| Method part | Description                                                            |
| ----------- | ---------------------------------------------------------------------- |
| `myArray`   | The array whose elements are being tested by the callback function.    |
| `.some()`   | The method used to apply the callback function to the `myArray` array. |
| `callbackFunction` | The function that is tested on each element of `myArray`. It should return `true` if an element passes the `callbackFunction` test, `false` otherwise. |
| `element`   | The current element, or value, in `myArray` being tested. |
| `index`     | *(optional)* The position that the current element is located in `myArray`. |
| `array`     | *(optional)* The array that the `some()` method owas used on (in this case, `myArray`).|
| `thisArg`   | *(optional)* Used as the `this` value when calling the `callbackFunction`. Defaults to undefined when not used. |

*Table 1: Breakdown of the parts used in the execution of the .some() method. Parts are required unless noted as optional.*

## What does the `some()` method return?

The `some()` method should return true at the first instance an element meets the conditions of the `callbackFunction`, regardless of where in the array that element is indexed.   For example, if the first element in an array of 100 elements meets the condition of its `callbackFunction`, the `some()` method stops checking and immediately returns a value of true. It will not need to check the rest of the array because the condition has been satisfied.

![The some method returning a value of true](./images/javascript-img/some-method-returning-true.svg)

*Figure 2: The `some()` method returning a value of true the moment an element meets the condition of the `callbackFunction`.*


If, however, every element in an array is checked and none of them pass the condition of the `callbackFunction`, the `some()` method will return false.

![The some method returning a value of false](./images/javascript-img/some-method-returning-false.svg)

*Figure 3: The `some()` method returning a value of false after all elements have failed the condition of the `callbackFunction`.*

## Applications

### Using a named function as a callback

You can apply a named function as a parameter to the `some()` method.  In the example below, the function `isEqualToFive` is applied as the callback function to `testArray1.some()` call.

![Testing an array using the some method with a named callback function](./images/javascript-img/some-named-callback.svg)

*Figure 4: Testing an array using the `some()` method with a named callback function.*

### Using an anonymous arrow function as a callback

