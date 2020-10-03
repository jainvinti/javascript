### if..else
```
let i = 5;
if (i < 5) {
   console.log('hello world');
}
else if (i === 5){
  console.log('hello world');
}
else {
  console.log('hello world');
}
```

### switch case
```
let value = 'A';
switch (value) {
   case 'A': 
   console.log('hello world');
   break;
   
   case 'B':
   console.log('hello world');
   break;
   ...
   
   case 'C':
   console.log('hello world');
   break;
   
   default: 
   console.log('hello world');
}
```

### for loop
```
for(let count = 0; count < 10; count++) {
  console.log('hello world', count);
}   
```

### while loop
```
let i = 0;
while (i <= 5) {
  console.log('hello world', count);
  count++;
}
```

### do while
```
// this example shows the difference between the while and do while loop that do while loop executes atleast once
let count = 9;
do {
  console.log('hello world', count);
  count++;
} while (count <= 5);
```

### for in loop
```
let person = {
  name: 'vinti'
  lastName: 'jain'
};

for(let key in person){
  console.log(key); // print name and lastName
  console.log(person[key]); // print vinti and jain
}

let colors = ['red','blue','green'];

for(let index in colors){
  console.log(index); //print index 0,1,2
  console.log(colors[index]); // print red blue green
}
```

### for of loop
```
let colors = ['red','blue','green'];
for(let color of colors){
  console.log(color); // print red blue green
}
```






