# javascript

### variables
```
let name = 'vinti';
console.log(name);

rules for variable name-
//cannot be a reserved keyword
//should be meaningful 
//cannot start with a number like 1name
//cannot contain space or hyphen (-)
//are case-sensitive
```


### constants
```
const keyword is used for constants
const name = 'vinti';
console.log(name);
```

### primitive data types
```
let name = 'vinti'; //string literal
let age = 30; //number literal
let isApproved = false; //boolean literal
let firstName = undefined; //undefined
let selectColor = null; //object
```

### dynamic typing
```
javascript supports dynamic typing for example
let name = 'vinti';

typeof operator will show it as string and we re-assign name with any other data type, name's data type will change
typeof name 
"string"

name = 1;
typeof name
"number"
```

### referenec data types
**object**
```
let person = {
  name: 'vinti',
  lastName: 'jain'
};
console.log(person);

Suppose you want to update the value in person.
//dot notation
person.name = 'john'

//bracket notation
person['name'] = 'john';
console.log(person.name);

to access the name property in dynamic way
let i = 'name';
person[i] = 'john';
console.log(person.name);
```
**array**
```
let colors = ['red','blue'];
console.log(colors); // print both
console.log(colors[0]); // print red
colors[2] = 'green';
console.log(colors); // print three colors now
colors[2] = 1; // in javascript we can have different types of elements
//array is object in javascript
//array have predefined properties like length
console.log(colors.length); // print 3
```
**function**
```
function greet(name){ // with parameter
  console.log('hello' + name);
}

greet('john') // call of funtion with argument

function square(number){
  return number * number;
}
console.log(square(2)); //call of function from log function
```
