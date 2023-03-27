# Javascript .some() method

The `some()` method in Javascript is used to determine if there exists at least one element in the array that satisfies a given condition by a provided callback function. If such an element exists, the method stops immeditately and returns true.  If such an element does not exist, the method will return false upon completion.

The syntax for the `some()` method is as follows:

![Syntax of the Javascript some() method](./images/javascript-img/some-method-syntax.svg)
<figcaption style="margin-top: 0;">
    Figure 1: Syntax of the Javascript <code>some()</code> method
</figcaption>

<p></p>

<p></p>

| Method part | Description                                                            |
| ----------- | ---------------------------------------------------------------------- |
| `myArray`   | The array whose elements are being tested by the callback function.    |
| `.some()`   | The method used to apply the callback function to the `myArray` array. |
| `callbackFunction` | The function that is tested on each element of `myArray`. It should return `true` if an element passes the `callbackFunction` test, `false` otherwise. |
| `element`   | The current element, or value, in `myArray` being tested. |
| `index`     | *(optional)* The position that the current element is located in `myArray`. |
| `array`     | *(optional)* The array that the `some()` method owas used on (in this case, `myArray`).|
| `thisArg`   | *(optional)* Used as the `this` value when calling the `callbackFunction`. Defaults to undefined when not used. |

<figcaption>
    Table 1: Breakdown of the parts used in the execution of the <code>.some()</code> method. Parts are required unless noted as <i>optional</i>.
</figcaption>

## What does the `some()` method return?

The `some()` method should return true at the first instance an element meets the conditions of the `callbackFunction`, regardless of where in the array that element is indexed.   For example, if the first element in an array of 100 elements meets the condition of its `callbackFunction`, the `some()` method stops checking and immediately returns a value of true. It will not need to check the rest of the array because the condition has been satisfied.

<img src='./images/javascript-img/some-method-returning-true.svg' alt='The some method returning true'>


If, however, every element in an array is checked and none of them pass the condition of the `callbackFunction`, the `some()` method will return false.

