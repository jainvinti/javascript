### dynamic nature of objects
```
// objects in js are dynamic which means 
// once you create them you can always 
// add new properties or methods
// also can remove the existing properties
// this mostly confuse what kind of const it is, 
// const means here is that we cannot reassign the circle variable

const circle = {
  radius: 1
};

circle = {}; // this we cannot do as it is const

circle.color = 'yellow';
circle.draw = function() {}

delete circle.color;
delete circle.draw;

console.log(circle);
```

### constructor property
```
// every object in js have property called constructor 
// and that references the function that was used to create the object

obj.constructor

// built in constructor called when 
// factory function calls constructor, js engine used built in constructor.
// constructor called itself when constructor function called
```

### functions are object
```
functions are basicly are objects

function Circle(radius){
  this.radius = radius;
  this.draw = function() {
    console.log('draw'); 
   }
};

when we do Circle., we can see methods and objects are defined for Circle.
Go to console and try some

Circle.name - returns name of function
Circle.lenght - returns number of arguments
Circle.constructor - returns buildin constructor

It means, when we create a function like this function Circle(radius)
internally java script engine will use function contructor to create this object.
For ex, 
const Circle1 = new Function('radius', ` this.radius = radius;
  this.draw = function() {
    console.log('draw'); `);
    
const circle = new Circle1(1);
we can call this function as Circle

creating the object using call method


const circle = new Circle(1); // both the expression are same 
Circle.call({},1); // empty object and arguments explicitly

Similary there is one more method for functions
Circle.apply({},[1,2,3]; // this method is also like call method, 
but instead of passing all the arguments explicitly, it passed in an array. 

```

### value and reference type
```
Value/Primite Type - Number, String, Boolean, Symbol, undefined, null

Reference/Object Type - Object, Function, Array (Function are objects and Arrays are also object)

In nutshell, we have two types primitives and objects.

Primitive Type:
let x = 10;
let y = x;

x = 20;

on console
x // 20
y // 10
its because x and y are two individual variable
independent to each other

Object Type
let x = {value: 10};
let y = x;

x.value = 20;
on console

x // {value: 20}
y // {value: 20}

when we create object, its not store in the variable, it stores somewhere else in the memory,
so, x is holding the address of that memory location.
when we copy x = y, both x and y are pointing to same memory object

Primitives are copied by their value
Objects are copied by their reference.

Examples:

let number = 10;
function increase(number){
  number++;
}

increase(number)
console.log(number); // result is 10 as its copied by value



let obj = {value: 10};
function increase(obj){
  obj.value++;
}

increase(obj)
console.log(obj); // result is 11 as its copied by reference

```
### enumerating the properties of object
```
const circle = {
 radius: 1,
 draw: function() {
  console.log('draw');
 }
};

for(let key in circle)
  console.log(key, circle[key]); // prints key and its value of circle object
  

for(let key of circle)
  console.log(key); // gives error - for of loops can be only used with ittrable like array and maps.
  //objects are not ittrable
  
for(let key of Object.keys(circle)) //Object.keys returns an array of keys, 
//since arrays are ittrable we can use for of loop
  console.log(key); 
  
Object is builtin constructor function, so somehere we have
function Object() {} // constructor function
when ever object is created,
const x = {value: 1};
internally its called
const x = new Object();

for(let entries of Object.entries(circle)) //Object.entries returns an array of keys and value, 
//since arrays are ittrable we can use for of loop
  console.log(entries);
  
if we wnat to check a particular property existes in object

if ('radius' in circle) console.log('yes'); // prints yes
```

### cloning of object
```
const circle = {
 radius: 1,
 draw: function() {
  console.log('draw');
 }
};

const another = {};

for(let key in circle)
  another[key]= circle[key]; // copying the object
  
console.log(another);


in modern java script its another method to clone object

const another = Object.assign({}, circle);// copying the object

const another = Object.assign({coloe: 'yellow'}, circle);// new object can also have existing properties or additional properties
console.log(another);


Another simpler and elegant way to clone the object
const another = { ...circle }; // spread operator   
console.log(another);

```
### Garbage Collection
```
runs automatically and deallocate the variables. 
developer have no control over it.

```
### built in objects - Math , String
```

```

### Templete Literals
```
There are literals
Object {}
Boolean true, false
String '', ""
Tempelete ``

const name = 'john';

const  another = `HI ${name} ${2 + 3}
I can write this way without
using backslash.`

in templetes literals we can put any expression that returns value
```

### date
```
google javascript date - dateString
const now = new Date();
const date1 = new Date('May 11 2020 1:00');
const date2 = new Date(2020, 4, 14, 9 ); // months start with 0 - jan

these date objects have set and get methods:

now.get....
now.set....

now.toDateString();
now.toTimeString();
now.toISOString();
```






