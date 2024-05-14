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
whereas for '===' it will check for data type also for a & b. where b is undefined datatype
and a is null which is a primitive data type so it will give a false.

