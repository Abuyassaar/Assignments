No. 1
Hoisting is calling a function before declaring it. 
It can also be referred to the process whereby the interpreter appears to move the declaration of functions, variables or classes to the top of their scope, prior to execution of the code. Hoisting allows functions to be safely used in code before they are declared. 
In simple term, it is the default behavior of moving declarations to the top.
Examples: 
let x;
x = 5;

a = 5
console.log(a)
 
Closure is accessing a child though the mother. 
A closure is a function having access to the parent scope, even after the parent function has closed.
It is also a function that references variables in the outer scope from its inner scope. The closure preserves the outer scope inside its inner scope. 
A closure is also the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.
 Example 1:
 function outer() {
   var fName = 'Abdulmajeed';
   
   function inner() {
         var lName = 'Abdulrasaq'; 
         console.log(fName + lName);
    }
   return inner;
}
 
Example 2:
 function profile() {
  var name = 'Abdulmajeed';
  function displayName() { 
    alert(name);
  }
  displayName();
}
profile();




No. 2
1. Regular functions created using function declarations or expressions are constructible and callable. Since regular functions are constructible, they can be called using the new keyword. 
However, the arrow functions are only callable and not constructible, i.e arrow functions can never be used as constructor functions. Therefore, they can never be invoked with the new keyword.

2. Arrow functions do not have an arguments binding. However, they have access to the arguments object of the closest non-arrow parent function. Named and rest parameters are heavily relied upon to capture the arguments passed to arrow functions.

3. The behavior of this inside of an arrow function differs considerably from the regular function's this behavior. The arrow function doesn't define its own execution context.

4. No matter how or where being executed, this value inside of an arrow function always equals this value from the outer function. In other words, the arrow function resolves this lexically.

5. In regular function, you always have to return any value, but in Arrow function you can skip return keyword and write in single line.

6. In regular function, function gets hoisting at top. 
In arrow function, function get hoisted where you define. So, if you call the function before initialisation you will get referenceError.




No. 3
1. Pure functions take objects and/or primitive data types as arguments but does not modify the objects. Impure functions change the state of received objects. 
2. Pure functions doesn't have side effects. Impure functions have side effects.
3. Pure functions is predictable. Impure functions is not predictable.
4. Pure functions are easier to read and debug than their impure alternatives.
5. Pure functions are so readable because they are solely dependent on themselves.

Pure Functions
function add(x,y){
    return x + y;
}
console.log(add(2, 2))


function updateMyName(newName) {
   const myNames = ["Abdulmajeed", "Abdulrasaq"];
   myNames[myNames.length] = newName;
   return myNames;
}

Impure Functions
const myNames = ["Abdulmajeed", "Abdulrasaq"];

function updateMyName(newName) {
  myNames.push(newName);
  return myNames;
}

