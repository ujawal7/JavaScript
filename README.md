# JavaScript Interview Questions

**1. Difference Between Undefine and Null in JavaScript**<br>
when there is no value assigned to the javaScript variable then it is 'Undefine' & 
The data type of that variable will also be 'Undefined'
```javascript
let x;
console.log(x); //undefined
console.log(typeof(x)); //undefined
```
**2. Can we assign undefine explicitly to the javascript variable**<br>
Yes, we can. This is used to check whether any variable is undefined or not.
```javascript
 let z = undefined;
 console.log(z); // undefined 
```

**3. Difference Between == and === in JavaScript**<br>
'==' will check only data where as '===' will check of data type also. That's why we see true and false in the below snippet.
```javascript
let a = null;
let b;
console.log(a==b); //True
console.log(a===b); //False
```
a is null and b is an undefined variable both are the same for '==' so it will give true,
whereas for '===' it will check for data type also for a & b. where b is an undefined datatype
and a is null which is a primitive data type so it will give a false.<br>

**4. Function Scope & Block Scope**<be>
This will give an error that x is undefined Because the Scope of variable X is limited to function a()
```javascript
function a(){
    let x = 10;
}
function b(){
    console.log(x)
}
a();
b();//Error
```
The below snippet will refer to the same y global variable in both functions.
First It will run the first function function a(), whatever value we get of y will be used in function b().
we get 10 in function a() and that 10 is used in function b().
```javascript
let y = 10
function a(){
     y = y+5;
}
function b(){
    console.log(y)
}
a();
b(); output: 15
```
**4. Hoisting**<br>
Hoisting is a mechanism in JavaScript where variables and functions are moved on top of their containing scope.
```javascript
console.log(x); // Output: undefined
var x = 5;
console.log(x); // Output: 5
```
In the above code, even though console.log(x) appears before the declaration of var x, it doesn't throw an error. Instead, it prints undefined, because var x is hoisted to the top of its containing scope during the compilation phase, making it available throughout the function (or global scope, if it's not in a function). However, its initialization (x = 5) is not hoisted, so x is undefined until it's assigned a value.<br>

**5. Difference between let and var**<br>
```javascript
let g = 9;
{
    let g = 7;
    console.log(g); //7
}
console.log(g) // 9
```
little differences between var and let are shown above and below.
```javascript
var g = 9;
{
    var g = 7;
    console.log(g); //7
}
console.log(g) // 7
```
The main difference between var and let is if we declare a variable with var and use it before declaring it will do hoisting and give output as undefined whereas if we use let, it will give a direct error.
```javascript
console.log(x); // Output: undefined
var x = 5;

console.log(y); // Throws ReferenceError: Cannot access 'y' before initialization
let y = 10;
```
