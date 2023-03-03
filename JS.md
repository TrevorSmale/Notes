# Javascript Learning in FreeCodeCamp.org

## Variables

Variables can container many different data types

### Declare JavaScript Variables

In computer science, data is anything that is meaningful to the computer. JavaScript provides eight different data types which are undefined, null, boolean, string, symbol, bigint, number, and object.

For example, computers distinguish between numbers, such as the number 12, and strings, such as "12", "dog", or "123 cats", which are collections of characters. Computers can perform mathematical operations on a number, but not on a string.

Variables allow computers to store and manipulate data in a dynamic fashion. They do this by using a "label" to point to the data rather than using the data itself. Any of the eight data types may be stored in a variable.

Variables are similar to the x and y variables you use in mathematics, which means they're a simple name to represent the data we want to refer to. Computer variables differ from mathematical variables in that they can store different values at different times.

We tell JavaScript to create or declare a variable by putting the keyword var in front of it, like so:

var ourName;

creates a variable called ourName. In JavaScript we end statements with semicolons. Variable names can be made up of numbers, letters, and $ or _, but may not contain spaces or start with a number.


### Declaring a sting variable

Variables can be declared in multiple ways.

var myName;
var myName = "your name";

### Initializing Variable with the Assignment Operator

var myVar = 0;

### Declare String Variables

var myName = "your name";

### Understanding Uninitialized Variables

When JavaScript variables are declared, they have an initial value of undefined. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a string of undefined.

## Camelcase

In camelCase, multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized.

exampleCamelCase
anotherExampleOfThis

## JS mathematics



The remainder operator % gives the remainder of the division of two numbers.

Example

    5 % 2 = 1 because
    Math.floor(5 / 2) = 2 (Quotient)
    2 * 2 = 4
    5 - 4 = 1 (Remainder)

Usage
In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by 2.

    17 % 2 = 1 (17 is Odd)
    48 % 2 = 0 (48 is Even)

Note: The remainder operator is sometimes incorrectly referred to as the modulus operator. It is very similar to modulus, but does not work properly with negative numbers.

## Golf script

    const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

    function golfScore(par, strokes) {
    // Only change code below this line

    if (strokes == 1) {
        return names[0];
    } else if (strokes <= par - 2) {
        return names[1];
    } else if (strokes === par - 1) {
        return names[2];
    } else if (strokes === par) {
        return names[3];
    } else if (strokes === par + 1) {
        return names[4];
    } else if (strokes === par + 2) {
        return names[5];
    } else {
        return names[6];
    }

    // Only change code above this line
    }

    golfScore(5, 4);
