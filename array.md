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

### emptying the array
```
let numbers = [1,2,3,4];
let another = numbers; // reference of array

numbers = []; // this solution doesn't work as the number is assigned to another  and it will not be frees by garbage collector
console.log(numbers);
console.log(another);

numbers.length = 0; // works for both number and reference
console.log(numbers);
console.log(another);

numbers.splice(0, number.length); // works for both number and reference
console.log(numbers);
console.log(another);

while (numbers.length > 0) // not approriate solution for cost
  numbers.pop();
  
console.log(numbers);
console.log(another);
```

### combining and sclicing array
```
const first = [1,2,3];
const second = [4,5,6];

const combined = first.concat(second);

const sclice = combined.sclice(); // if called with arguments it will return a copy of original array

console.log(combined);
console.log(sclice);
```

### the spread operator
```
const first = [1,2,3];
const second = [4.5.6];

const combined = [...first, 'a', ...second, 'b'];

//const copy = combined.sclice();
const copy = [...combined]; // it will return all the elements of combined array and put them in copy

```

### iterating the array
```
const numbers = [1,2,3];

for (let number of numbers)
  console.log(number)
  
numbers.foreach(function(number) {
  console.log(number);
});

//using arrow function
numbers.foreach((number, index)  => console.log(index, number));

```

### joining array
```
const numbers = [1,2,3];
const joined = numbers.join(',');
console.log(joined);

const message = 'this is my first message';
const parts = message.split(' ');
console.log(parts);

const combined = parts.join('-');
console.log(combined);

```

### sorting array
```
const numbers = [2,1,6,5,4];
numbers.sort();
console.log(numbers);

numbers.reverse();
console.log(numbers);

const courses = [
{id:1, name: 'node.js'},
{id:2, name: 'javascript'},
];

//courses.sort();

courses.sort(function(a,b) {
 //a < b => -1
 //a > b => 1
 //a === b => 0
 const nameA = a.name.toUpperCase();
 const nameB = b.name.toUpperCase();
 
 if (nameA < nameB) return -1
 if (nameA > nameB) return 1
 return 0;
});

console.log(courses);
```

### testing elements of array
```
const numbers = [1,2,3];
const numbers1 = [1,-2,3];

const allPositive = numbers.every(function(value) {
  return value >= 0;
});

const atLeastOnePositive = numbers1.some(function(value) {
  return value >= 0;
});

console.log(allPositive)
console.log(atLeastOnePositive);
```

###  filtering array
```
const numbers = [1,-1,2,3];

const filtered = number.filter(function(value){
  return value >= 0;
});

//using arrow function
const filtered = number.filter(n => n >= 0);

console.log(filtered);
```

### mapping an array
```
const numbers = [1,-1,2,3];

const filtered = number.filter(n => n >= 0);
const items = filtered.map(n => '<li>' + n + '</li>')

const html = '<ul>' + items.join('') + '</ul>'; // by default it used comma seperator

//object
const items = filtered.map(n => {
  return obj = { value: n };
});
//const items = filtered.map(n => obj = { value: n }); won't work

const items = filtered.map(n => obj = ({ value: n }) );
console.log(html);


// cleaner and shorter code
const numbers = [1,-1,2,3];

const items = numbers
  .filter(n => n >=0)
  .map(n => ({ value: n}))
  .filter(obj => obj.value > 1)
  .map(obj => obj.value);
  
console.log(items);
```

### reducing an array
```
const numbers = [1,-1,2,3];

let sum = 0;
for (let n of numbers)
  sum += n;

console.log(sum);

//modern way
const sum = numbers.reduce(
  (accumulator, currentvalue) => accumulator + currentvalue
);

console.log(sum);
```
