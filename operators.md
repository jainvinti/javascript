# operators

### airthmetic operators
```
let x = 10;
let y = 20;
console.log(x + y);
console.log(x - y);
console.log(x * y);
console.log(x / y);
console.log(x % y); //modulus (remainder)
console.log(x ** y); //exponentiation 
console.log(x++);
console.log(++x);
console.log(--x);
console.log(x--);
```

### assignment operators
```
let x = 10;
x += 3; // result 13
x -= 5; // result 5
//similary other operators
```

### comparison operators
```
let x = 1;
//relational
console.log(x > 0); //true
console.log(x >= 1); //true
console.log(x < 1); //false
console.log(x <= 1); //true

//strict equality (same type + same value) recommended to use
console.log(x === 1); //true
console.log(x !== 1); //false
console.log(1 === 1); //true
console.log('1' === 1); //false

//loose equality (same value)
console.log(1 == 1); //true
console.log('1' == 1); //true
console.log(true == 1); //true
```

### conditional or ternary operator
```
let points = 110;
let type = points > 100 ? 'gold member' : 'silver member';
console.log(type);
```

### logical operators with non booleans
```
let highIncome = false;
let goodCreditScore = false;
let eligibleForLoan = highIncome || goodCreditScore;
console.log('eligible', eligibleForLoan);
let applicationRefused = !eligibleForLoan;
console.log('application refused', applicationRefused);

let userColor = 'red';
let defaultColor = 'blue';
let currentColor = userColor || defaultColor; 
console.log(currentColor); //red

//it works on falsy and truthy
//falsy are undefined, null, 0, false, '', NaN
```

### bitwise operator
```
// read     0000100
// write    0000010
// execute  0000001
const readPermission = 4;
const writePermission = 2;
const executePermission = 1;

let myPermission = 0;
myPermission = myPermission | readPermission | writePermission;
console.log(myPermission); //result 6
```

