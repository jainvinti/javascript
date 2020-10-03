### if..else
```
if (expression) {
   Statement(s) to be executed if expression is true
}
else if (expression){
  Statement(s) to be executed if expression is true
}
else {
  Statement(s) to be executed if expression is true
}
```

### switch case
```
switch (expression) {
   case 'condition 1': 
   statement(s)
   break;
   
   case 'condition 2':
   statement(s)
   break;
   ...
   
   case 'condition n':
   statement(s)
   break;
   
   default: statement(s)
}
```

### for loop
```
for(count = 0; count < 10; count++) {
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






