### function declerations and expressions
```
// function decleration
function walk(){
  console.log('walk');
}

//anonymous function expression
let run = function() {
  console.log('run');
};

// we can do this also
let move = run; // now movw nad run both point to same function
run();
move();
```

### Hoisting
```
Hoisting is the process moving function decleration to the top of file
this is done automatically java engine executing this code

// function decleration
walk();// we can call function which declared befor its decleration

function walk(){
  console.log('walk');
}

//anonymous function expression
run(); // error but we cannot do this with expression

let run = function() {
  console.log('run');
};
```

### arguments
```
function sum(a,b){
// arguments object - default special object
  console.log(arguments);
  return a + b; // 1 + undefined = NaN
}

function sum(){
  let total = 0;
  for (let value of arguments)
    total += value;
  return total;
}

console.log(sum(1)); // if we pass only one argument it will result NaN
console.log(sum(1,2,3,4,5)); // valid java code result = 3

```

### rest operator
```
// dont be confused it with spread operator.
spread operator is used with array, means taking the individual element of array
when we take this with parameter with function called as rest operator
when we apply rest operator to the parameter of function we can pass varying number of arguments
and rest operator will take all of them and put them in array
We cannot have parameter after the rest operator

function sum(...args){
  console.log(args); // return array of arguments
  
  return args.reduce((a,b) => a + b); // sum of number
}

console.log(sum(1,2,3,4,5)); 

function sum(discount,...prices){
  const total = return prices.reduce((a,b) => a + b); 
  return total * (1 - discount);
}

console.log(sum(0.1,20,30));
```
