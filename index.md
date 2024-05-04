# Basics

## Variables
* Dulu guna var tapi sekarang guna let atau const sahaja
```
let name = 'Syakir';
```

## Constants
* camelCase
```
const lastName = 'Naka';
```

## Objects
* Syntax curly braces
```
let person = {
    name: 'Syakir',
    age: 25
}
```

## Arrays
* Syntax square braces
```
let favouriteFruits = ['Apple', 'Durian']
```

## Functions
* Pass (  parameter  ) inside curly braces
```
function displayFruits(){
    console.log(favouriteFruits);
}
```

```
function square(number){
    return number * number;
}

---> call the function back and passed the argument inside the parameter ( )
let number = square(5);
console.log(number);
```

```
//another way to perform same operation
function square(number){
    return number * number;
}

console.log(square(2));
```

# Operators

## Arithmetic
```
let x = 3;
let y = 10;

console.log(x + y);
console.log(x - y);
console.log(x * y);
console.log(x / y);
console.log(x % y);
console.log(x ** y);


increment
console.log(++x); ---> add first
console.log(x++); ---> add later

decrement
console.log(--x);
console.log(x--);

```

## Assignment Operator
```
let x = 10;
x++;
equals to ---> x = x + x;
x += x;

x = x + 5;
x += 5;
x *= 5;

```
## Comparison Operator
* Output boolean
```
let x = 1;
console.log(x > 0);
console.log(x >= 1);
console.log(x < 1);
console.log(x <= 1);

```
## Equality operator
* Output boolean
```
console.log(x === 1); strict
console.log(x == 1); loose
console.log(x !== 1); not equal to

```
## Ternary operator
* Output boolean
```
let points = 110;
let type = points > 100 ? 'Gold' : 'Silver';
console.log (type) --> will be Gold

```
## Logical Operator
```
AND
console.log(false&&true);

OR
console.log(false || true);


NOT?

let highIncome = false;
let goodCreditScore = true;
let eligibleForLoan = highIncome || goodCreditScore;

let applicationRefused = !eligibleForLoan;
console.log(eligibleForLoan); ---> will output true because using OR and goodCreditScore is true

Non-boolean values
let useColor = undefined;
let defaultColor = 'blue';
let currentColor = useColor || defaultColor;

console.log(currentColor); ---> will output blue

When console.log(a,b) will output red,blue
Now,want to switch the output to blue,red
let a = 'red';
let b = 'blue';
let c = a;

a = b;
b = c;

console.log(a);
console.log(b);

```
## Control Flow
```
If...else
if (condition) {
    statement
}
else if (anotherCondition){
    anotherStatement
}
else
    anotherStatement

Example :-
let hour = 10;

if (hour >= 6 && hour < 12)
    console.log('Good Morning');
else if (hour >=12 && hour <=18)
    console.log('Good Afternoon');
else 
    console.log('Good Evening');

```
```
Switch and case

let role;

switch (role) {
    case 'guest':
        console.log('Guest User');
        break;

    case 'moderator':
        console.log('Moderator User');
        break;

    default:
        console.log('Unknown User');
}

if (role === 'guest') console.log('Guest User');
else if (role === 'moderator') console.log('Moderator User');
else console.log('Unknown User');
```
## For loops
* To iterate
```
For loops

for (initialExpression; condition; incrementExpression) {
    statement
}

for (let i = 5;i >= 1; i-- ) {
    console.log('Hello World');
}
```
## While Loops
```
While Loops

While (initialExpression) {
    condition
    incrementExpression
}

let i = 0;
while (i <= 5){
    console.log('Hello World');
    i++;
}
```
## Do..while loops
* Jarang guna
```
Do While Loops ---> run at least once at the first time

let i = o;
do {
    console.log('Hello World');
    i++;
} while (i <= 5);
```
## Infinite Loops
```
---> This loop will run forever

let i = 0;
while (i < 5){
    console.log(i);
}
```
## For..in loops
```
For ... in loops ---> iterate over properties of an object
let person = {
    name: 'Syakir',
    age: 29
}
for (let key in person){
    console.log(key, person[key]);
}

This will print 
name Syakir
age 29

---> can also used in array but better use for..of loops to iterate over an array
let colors = ['red', 'blue', 'green'];

for(let index in colors){
        console.log(index, colors[index]);
}

---> Output 0 red 1 blue 2 green
```
## For..of loops
```
//For...of loop ---> to iterate elements of item of an object
let colors = ['red', 'blue', 'green'];

for (let color of colors){
    console.log(color);
}

---> Output red blue green

```
## Break and continue
```
let i = 0;

while (i <= 10){
    if (i === 5) break;

    if (i % 2 === 0) {
        i++;
        continue;
    }

    console.log(i);
    i++;
}
```

## Ex 1
1. Write a function that takes 2 numbers and return the maximum of the two
```
let a = 10;
let b = 5;

//One way
if (a > b) console.log(a);
else console.log(b);

//Second way
let max = a > b? a : b;
console.log(max);
```

## Ex 2
1. Return true or false. If landscape return true based on given function.
```
Given function:

function isLandscape (width, height) {

}

Solution:
function isLandscape (width, height) {
    let size = width > height? 'True' : 'False';
    console.log(size);
}

isLandscape(30,20)
```
## Ex 3 Fizzbuzz
* If number divisible by 3 is Fizz
* If number divisible by 5 is Buzz
* If number divisible by both 3 and 5 is FizzBuzz
* If number not divisible by both 3 and 5 is the same input.
* If not number display message not a number
```
function fizzBuzz(number) {
    if (typeof number !== 'number')console.log('Not a number');
    else if ((number % 3 === 0) && (number % 5===0) ) 
        console.log('FizzBuzz');
    else if (number % 3 === 0)
        console.log('Fizz');
    else if (number % 5 === 0)
        console.log('Buzz');
    else if ((number % 3 !== 0) || (number % 5!==0))
        console.log(number);
}

fizzBuzz('ketnaka');
```
## Ex 4
* Demerit points
* If speed = 70 display 'Ok'
* For every 5km increase 1 point
* use Math.floor
* If more than 12 points display 'License Suspended'
```
function checkSpeed (speed){
    const speedLimit = 70;
    const kmPerPoint = 5;

    if (speed < speedLimit + kmPerPoint) console.log('Ok');
    else {
        const points = Math.floor((speed - speedLimit) / kmPerPoint);
        if (points <= 12) console.log('Points', points);
        else console.log('License Suspended');
    }
}

checkSpeed(74)
```

## Ex 5
* Show numbers and display Even or Odd
```
function showNumbers(limit) {
    for (let i = 0; i <= limit; i++) {
        if (i % 2 === 0) console.log(i, 'Even');
            
        else console.log(i, 'Odd');    
    } 
}showNumbers(10)
```

## Ex 6
*count truthy element in the array
```
const array = [0, null, undefined, '', 2, 3];
console.log(countTruthy(array));

function countTruthy (array){
    let count = 0;

    for (let value of array)
        if (value) 
            count++;
    return count;
}
```

## Ex 7
```
function showProperties (obj) {
    for (let key in obj){
        if (typeof obj[key] === 'string')
            console.log(key, obj[key]);
    }
}

let obj = {
    title: 'a',
    year: 2019,
    director: 'b'
}

showProperties(obj)
```

## Ex 8
* Sums of multiple of 3 and 5
```
function sum (limit){
    let sum = 0;

    for (let index = 0; index <= limit; index++) 
        if (index % 3 === 0 || index % 5 === 0)
            sum += index;
    
    return sum;
}
console.log(sum(10));
```

## Ex 9
* Calculate grade of students
```
function calculateGrade(marks){
    const average = calculateAverage(marks);
    if (average < 60) return 'F';
    if (average < 70) return 'D';
    if (average < 80) return 'C';
    if (average < 90) return 'B';
    return 'A';
}

function calculateAverage(array){
    let sum = 0;
    for (let value of array)
        sum += value;
    return sum / array.length;
}

marks = [100,20,30];
console.log(calculateGrade(marks));
```
## Ex 10
*Stars
```
function showStars(rows){
    for (let row = 1; row <= rows; row++){
        let pattern = '';

        for (let i = 0; i < row; i++)
            pattern += '*';
    console.log(pattern);
    }
}

showStars(10)
```

## Ex 11
```
function showPrimes(limit){
    for (let number = 2; number <= limit; number ++)
        if (isPrime (number)) console.log(number);
}

function isPrime (number){
    for (let factor =2; factor < number; factor++)
        if (number % factor ===0)
            return false;
    
    return true;
}

showPrimes(20)
```
