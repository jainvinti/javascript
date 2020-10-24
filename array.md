### adding element
```
const numbers = [3,4];

numbers= [];// this will throw an error as numbers is constant
however we can still modify the content of numbers.
arrays are object, by dot notation can see properties of array

numbers.push(5,6); // add at end of array

numbers.unshift(1,2); //add at beginning

numbers.splice(2, 0, 'a', 'b'); // 2 is starting position
0 is how many elements you want to delete
items to add.
```

### finding elements
```
finding elements really depends if you are storing primitives or
reference type of array.

Primitives type:
const numbers= [1,2,3,1,4];

numbers.indexOf(); // if item is present returns index of item 
in array, else returns -1.

numbers.lastIndexOf(1); // returns 3

console.log(numbers.indexOf(1) !== -1); // this statement says
item is present in array, true
console.log(numbers.includes(1)); // modern way of writing it.

all the above methods can have second argument called fromIndex,
from where the search will begun.
```

### finding elements (reference types)
```
const courses = [
{id: 1, name: 'a'},
{id: 2, name: 'b'},
];

console.log(courses.includes({id: 1, name: 'a' }));// will return false
coz these two different object, two different reference type.

const course = courses.find(function(course){ //  callback function
  return course.name === 'a'; // return object if found and
  undefined if not found
});

const course = courses.findIndex(function(course){ 
  return course.name === 'a'; // return index or -1
});

console.log(course); 
```
### arrow function
```
const courses = [
{id: 1, name: 'a'},
{id: 2, name: 'b'},
];

const course = courses.find(course =>  course.name === 'a');

console.log(course); 

```

### removing elements
```
const numbers = [1,2,3,4];

const last = numbers.pop(); // remove at end of array
console.log(numbers); // show the array after removing the last element
console.log(last); // show the removed element

const first = numbers.shift(); //add at beginning
console.log(numbers); // show the array after beginning 
console.log(first); // show the removed element

numbers.splice(2, 1); // 2 is starting position
0 is how many elements you want to delete

console.log(numbers);
```
