# JS


Four essential data types in JavaScript include strings, numbers, booleans, and null.
Data is printed, or logged, to the console with console.log().
Four built-in mathematical operators include +, -, *, and /.
JavaScript associates certain properties with different data types.
JavaScript has built-in methods for different data types.
Libraries are collections of methods that can be called without an instance.
You can write single-line comments with // and multi-line comments between /* and */.


## Vars

```javascript
// This line of code sets the variable location to the string New York City
const location = 'New York City';

// This line of code sets the variable latitude to the number 40.7
let latitude = 40.7;

// This line of code sets the variable inNorthernHemisphere to true
let inNorthernHemisphere = true;

console.log(location);
console.log(latitude);
console.log(inNorthernHemisphere); 
```

## operators

```javascript
let molecule = 16;
let particle = 18;
let assay = 3;


// Add and assign to molecule below
molecule += 16;

// Multiply and assign to particle below
particle *= 6.02;

// Increment assay by 1
assay++;
```

## String Interpolation

In previous exercises, we assigned strings to variables. Here, you will learn how to insert the content saved to a variable into a string.

The JavaScript term for inserting the data saved to a variable into a string is string interpolation.

The + operator, known until now as the addition operator, is used to interpolate (insert) a string variable into a string, as follows:

```javascript
let myPet = 'armadillo';
console.log('I own a pet ' + myPet + '.'); 
// Output: 'I own a pet armadillo.'
```

In the example above, we saved the value 'armadillo' to the myPet variable. On the second line, the + operator is used to combine three strings: I own a pet, the value saved to myPet, and .. We log the result of this interpolation to the console as:

I own a pet armadillo.

## String Interpolation II

In the newest version of JavaScript (ES6) we can insert variables into strings with ease, by doing two things:

Instead of using quotes around the string, use backticks (this key is usually located on the top of your keyboard, left of the 1 key).
Wrap your variable with ${myVariable}, followed by a sentence. No +s necessary.
ES6 string interpolation is easier than the method you used last exercise. With ES6 interpolation we can insert variables directly into our text.

It looks like this:

```javascript
let myPet = 'armadillo'
console.log(`I own a pet ${myPet}.`)
// Output: 'I own a pet armadillo.'
In the example above, the backticks (`) wrap the entire string. The variable (myPet) is inserted using ${}. The resulting string is:

I own a pet armadillo.

let myName  = 'Erika';
let myCity = 'Valencia';
console.log(`My name is ${myName}. My favorite city is ${myCity}.`)
```


### Programa que convierte los grados Kelvin en Fahrenheit

```javascript
// Temperatura en Kelvin
const kelvin = 294;
// Los celsius son 273 menos los kelvin
let celsius = (kelvin - 273);
let fahrenheit =  celsius * (9/5) + 32;
console.log(fahrenheit);
// Round fahrenheit`
console.log(Math.floor(fahrenheit));
// save round in var
fahrenheit = Math.floor(fahrenheit);
console.log(`The temperature is ${fahrenheit} defrees Fahrenheit`);



// Temperatura en Kelvin
const kelvin = 255.5;
// Los celsius son 273 menos los kelvin
let celsius = (kelvin - 273);
let fahrenheit =  celsius * (9/5) + 32;
console.log(fahrenheit);
// Round fahrenheit
console.log(Math.floor(fahrenheit));
// save round in var
fahrenheit = Math.floor(fahrenheit);
console.log(`The temperature is ${fahrenheit} degrees Fahrenheit`);

let newton = celsius * (33/100);
newton = Math.floor(newton);
console.log(`The temperature is ${newton} degrees newton`)
```
## Control flow

```javascript
let userName = 'Erika';
let knowsJavaScript = true;

if (knowsJavaScript && userName) {
  console.log('Great, ' + userName + '! Get ready to practice your JavaScript!');
} else if (knowsJavaScript) {
  console.log('Great! Get ready to practice your JavaScript!');
} else if (userName) {
  console.log('Great, ' + userName + '! Get ready to learn something new!');
} else {
  console.log('Great! Get ready to learn something new!');
};
```

## True and false values

```javascript
let wordCount = 1;

if (wordCount) {
  console.log("Great! You've started your work!");
} else {
  console.log('Better get to work!');
}


let favoritePhrase = '';

if (favoritePhrase) {
  console.log("This string doesn't seem to be empty.");
} else {
  console.log('This string is definitely empty.');
}

let hungerLevel  = 10;
if(hungerLevel > 7){
  console.log('Time to eat!');
}else{
  console.log('We can eat later!');
};
``` 


## Else if Statements

We've explored if/else statements that answer questions that are either yes or no. What can we do if we have a question that has multiple yes conditions, or multiple no conditions?

We can add more conditions to our if/else statement with else if. Check out how this fits into our current knowledge of if/else statements:
```javascript
let stopLight = 'green';

if (stopLight === 'red') {
  console.log('Stop');
} else if (stopLight === 'yellow') {
  console.log('Slow down');
} else if (stopLight === 'green') {
  console.log('Go!');
} else {
  console.log('Caution, unknown!');
};

```

1. We created a variable named stopLight that is assigned to the string green.

2. Then, there's an if/else statement with multiple conditions, using else if. else if allows us to check multiple values of the stopLight variable and output different things based on its color.

3. The block ends with the singular else we have seen before. The else is a catch-all for any other situation. For instance, if the stopLight was blinking blue, the last else would catch it and return a default message.

```javascript
let moonPhase = 'solar eclipse';

if (moonPhase === 'full') {
  console.log('Howl!');
} else if (moonPhase === 'mostly full') {
  console.log('Arms and legs are getting hairier');
} else if (moonPhase === 'mostly new') {
  console.log('Back on two feet');
} else {
  console.log('Invalid moon phase');
}
``` 

## And && y Or || 

```javascript
let moonPhase = 'full';
let isFoggyNight = false;

if (moonPhase === 'full' && isFoggyNight) {
  console.log('Howl!');
} else if (moonPhase === 'mostly full') {
  console.log('Arms and legs are getting hairier');
} else if (moonPhase === 'mostly new') {
  console.log('Back on two feet');
} else {
  console.log('Invalid moon phase');
}
``` 
-------------
```javascript
let moonPhase = 'full';
let isFoggyNight = false;

if (moonPhase === 'full' || isFoggyNight) {
  console.log('Howl!');
} else if (moonPhase === 'mostly full') {
  console.log('Arms and legs are getting hairier');
} else if (moonPhase === 'mostly new') {
  console.log('Back on two feet');
} else {
  console.log('Invalid moon phase');
}
``` 
 

## switch Statements


Before we move on, let's circle back to else if statements.

Using else if is a great tool for when we have a few different conditions we'd like to consider.

else if is limited, however. If we want to write a program with 25 different conditions, like a JavaScript cash register, we'd have to write a lot of code, and it can be difficult to read and understand.

To deal with times when you need many else if conditions, we can turn to a switch statement to write more concise and readable code.

To a computer, a switch statement and an if/else statement are the same, but a switch statement can be easier for other humans to read. Part of being a good developer is writing code that both computers and other humans can read.
```javascript
switch statements look like this:

let groceryItem = 'papaya';

switch (groceryItem) {
  case 'tomato':
 
console.log('Tomatoes are $0.49');
break;
 
  case 'lime':
    console.log('Limes are $1.49');
    break;
  case 'papaya':
    console.log('Papayas are $1.29');
    break;
  default:
    console.log('Invalid item');
    break;
};
```

The switch keyword initiates the statement and is followed by ( ... ), which contains the condition that each case will compare to. In the example, the condition is groceryItem.
Inside the block, { ... }, there are cases. case is like the else if part of an if/else if/else statement. The word following the first case is 'tomato'. If groceryItem equalled 'tomato', that case's console.log() would run.
groceryItem equals 'papaya', so the first and second case statements are skipped. The third case runs since the case is 'papaya', which matches groceryItem's value. This particular program will log Papayas are $1.29.
Then the program stops with the break keyword. This keyword will prevent the switch statement from executing any more of its code. Without adding break at the end of each case, the program will execute the code for all matching cases and the default code as well. This behavior is different from if/else conditional statements which execute only one block of code.
At the end of each switch statement, there is a default condition. If none of the cases are true, then this code will run.
1.
Let's illustrate this by converting our werewolf program to a switch statement. For now, let's also delete the isFoggyNight variable so it doesn't fog up this concept.

moonPhase will become the condition of the switch statement. Then, each moon phase will become each case that the switch statement checks for.

Start by writing a switch statement with moonPhase as its condition.

2.
Then, write each else if condition as a case.

If moonPhase is 'full', then use console.log() to print Howl!.

If moonPhase is 'mostly full', then use console.log() to print Arms and legs are getting hairier.

If moonPhase is 'mostly new', then use console.log() to print Back on two feet.

Remember to add a break after each console.log(), like in the example in the instructions.

3.
Now, add a default at the end of the switch that uses console.log() to print Invalid moon phase, in the case that moonPhase does not equal one of our cases.
```javascript
 let moonPhase = 'full'; 

 switch (moonPhase) {
  case 'full':
    console.log('Howl!');
    break;
  case 'mostly full':
    console.log('Arms and legs are getting hairier');
    break;
  case 'mostly new':
    console.log('Back on two feet');
    break;
  default:
    console.log('Invalid moon phase');
    break;
}
``` 



# CONTROL FLOW

## Ternary Operator


In the previous exercise, we learned shorthand for writing multiple if/else if/else statements to make them easier to read. JavaScript also provides a way to shorten simple if/else statements called the ternary operator.
```javascript
let isNightTime = true;

if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}
In the example above, we see a very familiar pattern. See the example below for an equivalent way to express this.

isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');

```

The code in the example above will operate exactly as the code from the previous example. Let's break this example into its parts:

isNightTime ? — the conditional statement followed by a question mark. This checks if isNightTime is truthy.
console.log ('Turn on the lights!') — this code will be executed if the condition is truthy.
: — a colon separates the two different blocks of code that can be executed.
console.log('Turn off the lights!'); — this code will be executed if the condition is falsy
In this example, we checked if the value of a variable was true or false. The ternary operator can be used for any condition that can be evaluated to true or false, such as those with comparison operators.

age >= 16 ? console.log('You are old enough to drive in the United States!') : console.log('You are not old enough to drive in the United States!');
In the example above, the conditional statement is checking whether the value of the variable age is greater than or equal to 16. If so, a message that states the user is old enough to drive will be logged to the console. Otherwise, a message that states the user is not old enough to drive will be logged.

1.
In main.js, refactor the first if/else block to use the ternary operator.

2.
In main.js, refactor the second if/else block to use the ternary operator.

3.
In main.js, refactor the third if/else block to use the ternary operator. 

```javascript
 let isLocked = false;

isLocked ? console.log('You will need a key to open the door.') : console.log('You will not need a key to open the door.');

let isCorrect = true;

isCorrect ? console.log('Correct!') : console.log('Incorrect!');


let favoritePhrase = 'Love That!';

favoritePhrase === 'Love That!' ? console.log('I love that!') : console.log("I don't love that!");
```

## Review: Control Flow

Way to go! We just learned a lot of control flow concepts:

if/else statements make binary decisions and execute different code based on conditions.
All conditions are evaluated to be truthy or falsy.
We can add more conditional statements to if/else statements with else if.
switch statements make complicated if/else statements easier to read and achieve the same result.
The ternary operator (?) and a colon (:) allow us to refactor simple if/else statements.
Comparison operators, including <, >, <=, and >= can compare two variables or values.
After two values are compared, the conditional statement evaluates to true or false.
The logical operator && checks if both sides of a condition are truthy.
The logical operator || checks if either side is truthy.
The logical operator !== checks if the two sides are not equal.
An exclamation mark (!) switches the truthiness / falsiness of the value of a variable.
One equals symbol (=) is used to assign a value to a variable.
Three equals symbols (===) are used to check if two variables are equal to each other.

# JS

## FUNCTIONS

How does this code work?
```javascript
let calculatorIsOn = false;

const pressPowerButton = () => {
  if (calculatorIsOn) {
    console.log('Calculator turning off.');
    calculatorIsOn = false;
  } else {
    console.log('Calculator turning on.');
    calculatorIsOn = true;
  }
};

pressPowerButton();
// Output: Calculator turning on.

pressPowerButton();
// Output: Calculator turning off.
```

Let's explore each part in detail.

1. We created a function named pressPowerButton.

const pressPowerButton creates a variable with a given name written in camelCase.

The variable is then set equal = to a set of parentheses followed by an arrow token () =>, indicating the variable stores a function. This syntax is known as arrow function syntax.

Finally, between the curly braces {} is the function body, or the JavaScript statements that define the function. This is followed by a semi-colon ;. In JavaScript, any code between curly braces is also known as a block.

2. Inside the function body is an if/else statement. 

3. On the last few lines, we call the function by writing its name followed by a semi-colon pressPowerButton();. This executes the function, running all code within the function body. 

4. We executed the code in the function body twice without having to write the same set of instructions twice. Functions can make code reusable!

1.
Imagine you work at a pizza restaurant and you want to write a JavaScript program to take orders so you don't have to write orders by hand. You can write a function to perform this task!

Start by writing a function using the keyword const and the name takeOrder. Then set the variable = to a set of parentheses followed by an arrow () =>. Inside of its block {}, use console.log() to print 'Order: pizza'.

2.
Under the function, let's take an order.

Call the takeOrder() function on the last line.


## Parameters
So far our function has not required any input. We can also write functions that accept data. We do this with parameters. Parameters are variables in a function definition that represent data we can input into the function.
```javascript
const multiplyByThirteen = (inputNumber) => {
  console.log(inputNumber * 13);
};

multiplyByThirteen(9);
// Output: 117
```
Let's explore how this function works:

We add inputNumber within the parentheses () => of the multiplyByThirteen function. inputNumber is a parameter.
Inside the multiplyByThirteen() function, we use console.log to print the inputNumber multiplied by 13.
When we call the multiplyByThirteen() function on the last line, we set the inputNumber parameter. Here, we set it to 9. Then, inside the function block, 9 is multiplied by 13, resulting in 117 printing to the console.
Note on terminology: inputNumber is a parameter, but when we call multiplyByThirteen(9), the 9 is called an argument. In other words, arguments are provided when you call a function, and parameters receive arguments as their value. When we set the value 9 as the argument, we pass a value to the function.
Parameters let us write logic inside functions that are modified when we call the function. This makes functions more flexible.

1.
Let's include a parameter in the takeOrder() function to make the orders we log to the console more descriptive.

Inside the parentheses of the takeOrder() function, add a parameter named topping.

2.
Now, let's include the topping parameter in the body of the takeOrder function.

Modify the console.log to interpolate the topping parameter to print a string like this:

Order: pizza topped with mushrooms

3.
At the end of the program, modify the takeOrder() function call to include an argument for topping.

const takeOrder = (topping) => {
  console.log(`Order: pizza topped with ${topping}`);
};

takeOrder('muchrooms');

const takeOrder = (topping,crustType) => {
  console.log('Order: pizza topped with ' + topping + ' and ' + crustType);
};

takeOrder('mushrooms','bacon');
takeOrder('cheese','bacon');
takeOrder('tomato','cheese');

Return
Using console.log() as the result of a function isn't the best use of a function. The purpose of a function is to take some input, perform some task on that input, then return a result.

To return a result, we can use the return keyword. Take a look at our function from the last exercise, now re-written slightly:

const getAverage = (numberOne, numberTwo) => {
  const average = (numberOne + numberTwo) / 2;
  return average;
}

console.log(getAverage(365, 27));
// Output: 196
1. Instead of using console.log() inside the getAverage() function, we used the return keyword. return will take the value of the variable and return it. 

2. On the last line, we called the getAverage() function inside of a console.log() statement, which outputted the result of 196. 

3. This code achieved the same output as before, however now our code is better. Why? If we wanted to use the getAverage() function in another place in our program, we could without printing the result to the console. Using return is generally a best practice when writing functions, as it makes your code more maintainable and flexible.

1.
Now that we have the pizza orders, you want to add them up to find the cost of the pizzas for the check. Let's imagine that each pizza is $7.50, no matter the topping and crust type.

We will need to do three things to write this in JavaScript:

Create a variable to hold the number of pizzas ordered.
Whenever a pizza is ordered, add one to the number of pizzas ordered.
Take the total number of pizzas and multiply them by 7.5, since each pizza is $7.50.
Begin by creating a variable named orderCount set equal to 0 at the top of your code.


2.
Inside the takeOrder() function, add 1 to the value of orderCount each time takeOrder() is called.

You can increment the orderCount by +1 using either of the following:

orderCount = orderCount + 1;
orderCount += 1
The shorthand notation for this is:

orderCount++;
3.
Now it's time to calculate the subtotal of the pizzas. This is the perfect job for a function.

On a new line, beneath the closing brackets of the takeOrder function, declare a new function named getSubTotal that has one parameter named itemCount.


4.
Inside the getSubTotal() function's block, use return to output the itemCount multiplied by 7.5.


5.
On the last line of your program, after the takeOrder() function calls, call the getSubTotal() function inside a console.log statement.

getSubTotal has a parameter that represents the number of items ordered. Pass in the orderCount as an argument when making the function call.

Nice work! Now you can see the orders taken and how much it costs.

let orderCount = 0;
const takeOrder = (topping, crustType) => {
  orderCount  = orderCount + 1;
  console.log('Order: ' + crustType + ' pizza topped with ' + topping);
};

const getSubTotal = (itemCount) => {
  return itemCount * 7.5;
}

takeOrder('mushroom', 'thin crust');
takeOrder('spinach', 'whole wheat');
takeOrder('pepperoni', 'brooklyn style');
console.log(orderCount);
console.log(getSubTotal(orderCount));


Return II
In the last exercise, we pointed out that using return makes programs more maintainable and flexible, but how exactly?

When functions return their value, we can use them together and inside one another. If our calculator needed to have a Celsius to Fahrenheit operation, we could write it with two functions like so:

const multiplyByNineFifths = (celsius) => {
  return celsius * (9/5);
};

const getFahrenheit = (celsius) => {
  return multiplyByNineFifths(celsius) + 32;
};

console.log('The temperature is ' + getFahrenheit(15) + '°F');
// Output: The temperature is 59°F
Take a look at the getFahrenheit() function. Inside of its block, we called multiplyByNineFifths() and passed it the degrees in celsius. The multiplyByNineFifths() function multiplied the celsius by (9/5). Then it returned its value so the getFahrenheit() function could continue on to add 32 to it.

Finally, on the last line, we interpolated the function call within a console.log() statement. This works because getFahrenheit() returns its value.

We can use functions to section off small bits of logic or tasks, then use them when we need to. Writing functions can help take large and difficult problems and break them into small and manageable problems.

Instructions
1.
It's your job to calculate two more numbers for each order:

A sales tax of 6% needs to be calculated for every full order. This should be based on the subtotal.
The total, which is the subtotal plus tax, should also be computed.
Let's start with calculating the tax. Under the getSubTotal() function, create a function expression using the variable const named getTax. This function will take one parameter named itemCount.


2.
Inside the getTax() function, call your getSubTotal() function and pass it the argument itemCount to get the subtotal, and then multiply the returned value by 6% (0.06). Make sure to return the result of this operation.

Since you have a getSubTotal() function written, you can call that function inside the getTax() function's block. Since getSubTotal() needs an itemCount, make sure to pass it an argument. It may look like this:

const getTax = (someParameter) => {
  return getSubTotal(someParameter)
};
3.
Nice work! Now that you calculated the tax, declare another function named getTotal() beneath the getTax() function. The getTotal() function should take in one parameter named itemCount.

Inside the getTotal() function's block, add the subtotal to the tax, then return the result.



4.
On the last line of the program, call the getTotal() function with the argument orderCount inside of a console.log() statement to view the result.

Way to go! You wrote four functions from scratch and even passed them into each other. That's incredible!

let orderCount = 0;

const takeOrder = (topping, crustType) => {
  orderCount++;
  console.log('Order: ' + crustType + ' pizza topped with ' + topping);
};

takeOrder('mushroom', 'thin crust');
takeOrder('spinach', 'whole wheat');
takeOrder('pepperoni', 'brooklyn style');

const getSubTotal = (itemCount) => {
  return itemCount * 7.5;
};

const getTax = (itemCount) => {
  return getSubTotal(itemCount) * 0.06
}

const getTotal = (itemCount) => {
  return getTax(itemCount) + getSubTotal(itemCount)
}

console.log(getSubTotal(orderCount));

console.log(getTotal(orderCount))


Function Declarations
Now that we have an understanding of functions in JavaScript, let's take a broader look at the type of functions we'll see. Functions in JavaScript are generally declared as either a function declaration or a function expression.

A function declaration is a function that is bound to an identifier or name.

function square (number) {
  return number * number; 
}

console.log(square(5));
// Output: 25.
Function declarations require the keyword function, a name, and a function body. You can identify this by the use of function square() and the {} below. Function declarations do not end in a semi-colon.

Let's create a basic function declaration.

Instructions
1.
In main.js, use a function declaration to create a new function called isGreaterThan. The function should take two parameters, numberOne and numberTwo.

2.
Inside the function, using an if/else statement, create the following logic:

If numberOne is greater than numberTwo, return true.

Otherwise, return false.

if (some condition) {
  return true;
} else {
  return false;
}
3.
Call the isGreaterThan() function with two arguments of your choice.

function isGreaterThan (numberOne, numberTwo) {
  if (numberOne > numberTwo) {
    return true;
  } else {
   return  false;
  }
};

isGreaterThan(3,5);

Function Expressions
A function expression is similar to function declaration, with the exception that identifier can be omitted, creating an anonymous function. Function expressions are often stored in a variable. You can identify a function expression by the absence of a function name immediately trailing the function keyword.

const square = function (number) {
  return number * number;
};

console.log(square(5));
// Output: 25.
Also note function expressions end with a semi-colon since they are stored in a variable.

In this lesson, we have primarily been using a type of function expression known as an arrow function. Arrow function syntax is a shorter syntax for a function expression. You can identify arrow functions through the use of parentheses and the arrow token () =>.

const square = (number) => {
  return number * number;
};

console.log(square(5));
// Output: 25.
It's important to be familiar with the multiple ways of writing functions, since you will come across these in JavaScript code.

Instructions
1.
Refactor the function declaration to be a function expression using arrow function syntax.

Be sure to call the function at the end.

const isGreaterThan = (numberOne, numberTwo) => {
  if(numberOne > numberTwo){
    return true;
  } else {
    return false;
  }
}

console.log(isGreaterThan(4, 8));

Arrow Functions
JavaScript also provides several ways to refactor arrow function syntax. We'll explore a few of these techniques here, using an example function from a previous exercise.

const multiplyByNineFifths = (celsius) => {
  return celsius * (9/5);
};

const getFahrenheit = (celsius) => {
  return multiplyByNineFifths(celsius) + 32;
};

console.log('The temperature is ' + getFahrenheit(15) + '°F');
We can refactor this function in three ways. The most condensed form of the function is known as concise body.

Functions that take a single parameter should not use parentheses. The code will still work, but it's better practice to omit the parentheses around single parameters. However, if a function takes zero or multiple parameters, parentheses are required.
A function composed of a sole single-line block is automatically returned. The contents of the block should immediately follow the arrow => and the return keyword can be removed. This is referred to as implicit return.
A function composed of a sole single-line block does not need brackets.
In other words, the previous code can be refactored like this:

const multiplyByNineFifths = celsius => celsius * (9/5);

const getFahrenheit = celsius => multiplyByNineFifths(celsius) + 32;

console.log('The temperature is ' + getFahrenheit(15) + '°F');
You'll notice:

The parentheses around celsius have been removed, since it is a single parameter.
The return keyword has been removed since the function consists of a single-line block.
The {} have been removed, again, since the function consists of a single-line block.
Instructions
1.
Refactor the volumeOfSphere function using the principles described above.

const volumeOfSphere = diameter => {
  return (1/6) * Math.PI * diameter * diameter * diameter;
};

console.log('The volume of a sphere is ' + volumeOfSphere(10) + ' cubic centimeters');

## Review Functions
This unit introduced you to functions.

Functions are written to perform a task.
Functions take data, perform a set of tasks on the data, and then return the result.
We can define parameters to be used when calling the function.
When calling a function, we can pass in arguments, which will set the function's parameters.
We can use return to return the result of a function which allows us to call functions anywhere, even inside other functions.

## Global Scope
We'll start with global scope. Variables defined in the global scope are declared outside of a set of curly braces {}, referred to as a block, and are thus available throughout a program. We'll cover more on blocks in subsequent exercises.

Let's take a look at an example of global scope.

const color = 'blue'

const colorOfSky = () => {
  return color; // blue 
};

console.log(colorOfSky()); // blue
Here the variable color is declared outside of the function block, giving it global scope.
In turn, color can be accessed within the colorOfSky function.
Global variables make data accessible from any place within a program.

Instructions
1.
At the top of sky.js, write two global variables using const, one named satellite set equal to 'The Moon', the other named galaxy set equal to 'The Milky Way'.

2.
Using let, write another global variable name stars and set it equal to 'North Star'.

3.
Below these variables, using const, write a function named myNightSky. Inside the function, include a return statement like this:

return 'Night Sky: ' + satellite + ', ' + stars + ', ' + galaxy;
4.
Beneath the myNightSky() function, use console.log() to log the value of myNightSky() to the console.

You'll notice that the myNightSky() function is able to access the global variables without any problem since the variables are available globally.

const satellite = 'The Moon';
const galaxy = 'The Milky Way';
let stars = 'North Star';

const myNightSky = () => {
  return  'Night Sky: ' + satellite + ', ' + stars + ', ' + galaxy;  
};

console.log(myNightSky());  

## SCOPE
### Global Scope II
While it's important to know what global scope is, it's better to avoid defining variables in the global scope. Globally scoped variables can collide with variables that are more locally scoped, causing unexpected behavior in our code.

Let's explore our program a little further.

1.
Let's see what happens if we create a variable that overwrites a global variable.

Inside the myNightSky() function, on the very first line of the function, assign the variable stars to 'Sirius' as such:

stars = 'Sirius';
2.
Outside the function, under the previous console.log() statement, console.log() the value of stars.

You'll notice that the global variable stars was reassigned to 'Sirius'. In other words, we unexpectedly changed the value of the global variable, and this could impact our program in ways we do not intend.

const satellite = 'The Moon';
const galaxy = 'The Milky Way';
let stars = 'North Star';

const myNightSky = () => {
  stars = 'Sirius';
  return  'Night Sky: ' + satellite + ', ' + stars + ', ' + galaxy;  
};

console.log(myNightSky()); 
console.log(stars);

## Block Scope

Because of the challenges with global scope, it is preferable to define variables in block scope.

A block refers to the {} braces of a function, a loop, or an if statement, and serves as an important structural marker for our code. Block scope means that a variable defined in the block is only accessible within the curly braces.

Block scope works like this:

const colorOfSky = () => {
  let color = 'blue'; 
  console.log(color); // blue 
};

colorOfSky(); // blue 
console.log(color); // undefined
You'll notice:

We define a function colorOfSky().
Within the function, the color variable is only available within the curly braces of the function.
If we try to log the same variable outside the function, it logs undefined.
1.
In light.js, using const, define a function visibleLightWaves().

2.
Within the visibleLightWaves() function, using let, create a variable lightWaves and set it equal to 'Moonlight'.

3.
Within the function, beneath the lightWaves variable, add a console.log() statement that will log the value of the lightWaves variable when the function runs.

4.
Call the visibleLightWaves() function from outside the function.

5.
Beneath the function call, log the value of lightWaves to the console from outside the function.

You'll notice that it logs a ReferenceError since the variable is tied to the block scope of the function!

const visibleLightWaves = () => {
  let lightWaves = 'Moonlight';
  console.log(lightWaves);
};

visibleLightWaves();
console.log(lightWaves);

## Block Scope II

Let's take a look at another example of block scope, as defined within an if block:

const colorOfSky = () => {
  const dusk = true;
  let color = 'blue'; 
  if (dusk) {
    let color = 'pink';
    console.log(color); // pink
  }
  console.log(color); // blue 
};

colorOfSky(); // blue
console.log(color); // undefined
Here, you'll notice:

We create a variable dusk inside the colorOfSky() function.
After the if statement, we define a new code block with the {} braces. Here we assign a new value to the variable color if the if statement is true.
Within the if block, the color variable holds the value pink, though outside the if block, in the function body, the color variable holds the value blue.
Block scope is a powerful tool in JavaScript, since it allows us to define variables with precision, and not pollute the global namespace.

Instructions
1.
Remove the statement that erroneously logs the value of the lightWaves variable to the console outside of the function block.

2.
Let's continue by adding another variable to the visibleLightWaves() function. Beneath the lightWaves variable, using let, add a variable region and set it equal to 'The Arctic'.

3.
Beneath the region variable, create an if statement that checks if the region is the 'The Arctic'.

4.
Inside the if block, define a new variable lightWaves and set it equal to 'Northern Lights'.

5.
Beneath the variable in the if block, use console.log() to log the value of the block variable inside the if block.

Notice the ouput. Inside the if block console.log(lightWaves) logs the value Northern Lights to the console. Outside the if block, but still within the function, the same statement logs Moonlight to the console.

const visibleLightWaves = () => {
  let lightWaves = 'Moonlight';
  let region = 'The Arctic';
    if (region === 'The Arctic') {
      let lightWaves = 'Northern Lights';
      console.log(lightWaves);  
    }
  console.log(lightWaves);
};

visibleLightWaves();

## Block Scope III

Let's take a look at one other common example of block scope, as defined within a for loop.

const cloudCount = () => {
  let i = 2;
  console.log(i); // 2
  for (let i = 0; i < 10; i++) {
    console.log(i); // All numbers from 0 to 9
  }
};

cloudCount();
console.log(i); // undefined
Here the variable i is defined in the cloudCount() function.
Within the for loop block, we again define i, as a value that will be incremented.
The local value of i, whether defined in the function block or the for loop, has no impact on the global scope of our program.
Instructions
1.
Using const, declare a new function called starCount().

2.
Within the starCount() function, declare a variable named i and set it equal to 5.

3.
Right beneath the variable declaration, log the value of the i value to the console.

4.
Beneath the previous console.log() statement, create a for loop.

The for loop should begin counting when i = 0, as long as i < 12, and increment the value i by 1 each time the loop runs.

Within the block of the for loop, log the value of i to the console, as demonstrated in the example.

5.
Call starCount() function, from outside of the function.

6.
Finally, beneath the function call, log the value of i to the console from outside of the function.

You will notice that it returns a Reference Error! The value of i is contained in the block scope.

const starCount = () => {
  let i = 5;
  console.log(i); // 25
  for (let i = 0; i < 12; i++) {
    console.log(i); // All numbers from 0 to 9
  }
 
};
starCount();
 console.log(i);

 ## Review: Scope
This unit introduced you to scope.

Scope is the idea in programming that some variables are accessible/inaccessible from other parts of the program.
Global Scope refers to variables that are accessible to every part of the program.
Block Scope refers to variables that are accessible only within the block they are defined.

## Arrays
A foundational concept of programming is how to organize and store data.

One way we organize data in real life is to make lists. Let's make one here:

New Year's Resolutions:
1. Rappel into a cave
2. Take a falconry class
3. Learn to juggle
Let's now write this list in JavaScript, as an array:

let newYearsResolutions = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];
Arrays are JavaScript's way of making lists. These lists can store any data types (including strings, numbers, and booleans) and they are ordered, meaning each item has a numbered position.

Instructions
1.
Run the code to see what is logged to the console.

let bucketList = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];

console.log(bucketList);

## Create an array
Let's start by making an array and then seeing what it can do throughout the rest of this lesson.

Instructions
1.
Make a variable named newYearsResolutions and set it equal to an array with three strings inside of it.


2.
Use console.log to print newYearsResolutions to the screen.

let newYearsResolutions  = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];
console.log(newYearsResolutions);

### ARRAYS
## Property Access

Each item in an array has a numbered position. We can access individual items using their numbers, just like we would in an ordinary list.

Something important to note is that JavaScript starts counting from 0 rather than 1, so the first item in an array will be at position 0. This is because JavaScript is zero-indexed.

We can select the first item in an array like this:

let newYearsResolutions = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];

console.log(newYearsResolutions[0]);
// Output: 'Rappel into a cave'
You can also access individual characters in a string. For instance, you can write:

let hello = 'Hello World';
console.log(hello[6]);
// Output: W
W will be the output since it's the character in the 6th position. This works because JavaScript stores strings in a similar way that it stores arrays.

Instructions
1.
Individual elements of arrays can also be stored to variables.

Create a variable named listItem and set it equal to the first item in your newYearsResolutions array using square bracket notation ([]).

Then use console.log() to print the listItem variable to the console.

The first item within an array is always at position [0].

2.
Now, console.log() the third item in the newYearsResolutions array without using a variable.

3.
Try to log the item at position [3] to the console. What is logged to the console?

let newYearsResolutions  = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];
console.log(newYearsResolutions);

let listItem = newYearsResolutions[0];
console.log(listItem);
console.log(newYearsResolutions[2]);
console.log(newYearsResolutions[3]);

### ARRAYS
## Update Elements
In the previous exercise, you learned how to access elements of an array or a string using their index number. You can also change elements of an array using their indices.

let seasons = ["Winter", "Spring", "Summer", "Fall"];

seasons[3] = "Autumn";
console.log(seasons) 
//Output: 
//Winter 
//Spring
//Summer
//Autumn
In the example above, the seasons array contained the names of the four seasons.

However, we decided that we preferred to say "Autumn" instead of "Fall".

seasons[3] = "Autumn"; tells our program to change the item at index 3 of the seasons array to be "Autumn" instead of what is already there.

Instructions
1.
Change the second element of your newYearsResolutions array to be, 'Learn a new language'.

let newYearsResolutions  = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];
console.log(newYearsResolutions);

let listItem = newYearsResolutions[0];
console.log(listItem);
console.log(newYearsResolutions[2]);
console.log(newYearsResolutions[1]='Learn a new language');


### ARRAYS
## length property
We may wish to know how many items are stored inside of an array.

We can find this out by using one of an array's built-in properties, called length. We can attach this to any variable holding an array and it will return the number of items inside.

let newYearsResolutions = ['Rappel into a cave', 'Take a falconry class'];

console.log(newYearsResolutions.length);
// Output: 2
In the example above, we log newYearsResolutions.length to the console. This code retrieves the length property of the newYearsResolutions array and logs it to the console. This array has two items, so 2 would be logged to the console.

Instructions
1.
Find the length of your newYearsResolutions array and log it to the console.

let newYearsResolutions  = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];
console.log(newYearsResolutions);

let listItem = newYearsResolutions[0];
console.log(listItem);
console.log(newYearsResolutions[2]);
console.log(newYearsResolutions[1]='Learn a new language');
console.log(newYearsResolutions.length); 

### ARRAYS
## push Method
JavaScript has built in methods for arrays that help us do common tasks. Let's learn some of them.

First, .push() allows us to add items to the end of an array. Here is an example of how this is used:

let newYearsResolutions = ['item 0', 'item 1', 'item 2'];

newYearsResolutions.push('item 3', 'item 4');
The method .push() would make the newYearsResolutions array look like:

['item 0', 'item 1', 'item 2', 'item 3', 'item 4'];
How does .push() work?

It connects to newYearsResolutions with a period.

Then we call it like a function. That's because .push() is a function and one that JavaScript allows us to use right on an array.

Another array method, .pop(), is similar to .push(). This method removes the last item of an array.

let newYearsResolutions = ['item 0', 'item 1', 'item 2'];

newYearsResolutions.pop();

console.log(newYearsResolutions); 
// Output: [ 'item 0', 'item 1' ]
In the example above, calling .pop() on the newYearsResolutions array removed item 2 from the end.

Instructions
1.
Add two more items to your newYearsResolutions array using .push().

2.
Now, use console.log to print your newYearsResolutions array to make sure your items were added.

3.
Use the .pop() method to remove the last element from your array.

Log newYearsResolutions to the console to make sure it worked.
let newYearsResolutions  = ['Rappel into a cave', 'Take a falconry class', 'Learn to juggle'];
console.log(newYearsResolutions);

let listItem = newYearsResolutions[0];
console.log(listItem);
console.log(newYearsResolutions[2]);
console.log(newYearsResolutions[1]='Learn a new language');
console.log(newYearsResolutions.length); 
newYearsResolutions.push('Item3');
newYearsResolutions.push('Item4');
console.log(newYearsResolutions); 
newYearsResolutions.pop();
console.log(newYearsResolutions); 
