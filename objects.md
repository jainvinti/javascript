
### objects
```
// objects in javascript can have any type of data type 
// all the related variables, function can be put inside the object
// group related variables, function, object
// object orianted programming

const circle = {
 radius: 1,
 location: {
  x: 1,
  y: 1
 },
 isVisible: true,
 draw: function() {
  console.log('draw');
 }
};

circle.draw(); // method

// difference between method and function - 
//if a function is part of object in object programming terms, refer that function as method.
```

### factory function
```
// imagine we want 2 circle object, than we copy the same circle object
// problem here is that we would have duplicate implementation of draw method
// suppose is there is bug in draw method than it would present in duplicate draw methods
// to solve this we use factory functions
const circle = {
 radius: 1,
 location: {
  x: 1,
  y: 1
 },
 isVisible: true,
 draw: function() {
  console.log('draw');
 }
};

const circle2 = {
 radius: 1,
 location: {
  x: 1,
  y: 1
 },
 isVisible: true,
 draw: function() {
  console.log('draw'); // duplicate logic 
 }
};

------------------------
// factory function
// whenever we call createCircle, it will create the circle object
// however we will pass radius and location 
// camel notation used to create factory function
function createCircle(radius, location){
  return {
   // radius: radius, 
   // in modern javascript if key and value are same
   // we can make the code shorter by removing the value and simply adding key
   radius,
   location: location,
   isVisible: true,
   // function can be defined as we define outside object without the keyword function
   draw: function() { 
    console.log('draw'); 
   }
  };
}

// factory function 
// beauty of the factory function is that we define the logic in one place,
// we can call this function with different values or different argument, 
// we get different circle objects
// if there is bug in logic, will fix in single place
function createCircle(radius){
  return {
   radius,
   draw() {
    console.log('draw'); 
   }
  };
}

const circle1 = createCircle(1);
console.log(circle1);
console.log(circle1.draw());

const circle2 = createCircle(1);
console.log(circle2);
```

### constructor functions
```
// another method to create objects
// job of constructor function is to create an object
// naming convention used for constructor is different
// we should use pascal notaion for constructor, that is OneTwoThree

function Circle(radius){
  this.radius = radius;
  this.draw = function() {
    console.log('draw'); 
   }
};

const circle = new Circle(1); // new operator does three things under the hood

// just to understand what happens with new operator
//function Circle(radius){
//  this.radius = radius; // 2 set this to point newly created object
//  this.draw = function() { // 2 set this to point newly created object
//    console.log('draw'); 
//   }
// return this; // 3 will return newly created object from Circle function
//};

//const x = {}; //1 new creates an empty js object 


// difference between factor and constructor function
// in factory object is created like - const circle1 = createCircle(1);  object return by createCircle
// in constructor object is created like - const circle = new Circle(1); object return by this
// factory have camel notation and constructor have pascal notaion
// constructor is familiar with c# and java
// no other diffecence  
```
