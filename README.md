## Scope, hoisting and compartmentalization

### Answer the following:
In you own words, explain the concepts of scope, hoisting, compartmentalization.
Scope is vision or accessibility of a function to a variable.  Hoisting is how Javascript actually reads the code that is written.  There is a priority in which items are done. Such as all the variable declarations are pulled to the top and executed first.  Compartmentalization is having code completely shielded from the outside global scope to run. An example is an IIFE

### Provide examples for all three, below:

#### Scope:
var x =0;

function(){
  var x = 2;
}
console.log(x) => returns 0 because the scope of the variable x on line 10 is global and line 13 x is only local to the function.

#### Hoisting:

x = x+2;
var x = 2
console.log(x) => will return undefined because the variable declaration is hoisted to the top.

#### Compartmentalization:

var y = 3;
(function(){
  var y = 2;
  console.log(y)
  })()
console.log(y)
  This will return a y value of 2 from inside the IIFE and 3 from outside the IIFE.  The IIFE compartmentalized the var y on the inside.
