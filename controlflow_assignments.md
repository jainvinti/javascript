```
function max(num1, num2)
{
    return num1 > num2 ? num1 : num2;
}

console.log(max(40,20));
```

> **output -  40**

```
function isLandScape (height, width){
    return (width > height) ;
}

console.log(isLandScape(10,50));
```

> **output - true**
```
function fizzBuzz(input){
    if (typeof(input) !== 'number')
       return 'NaN';
    else if (((input % 3) === 0) && (input % 5) === 0)
        return 'FizzBuzz';
    else if ((input % 5) === 0)
        return 'Buzz';
    else if ((input % 3) === 0)
        return 'Fizz';
    
    return input;  
    
}

console.log(fizzBuzz(5));
```
> **output - Buzz**
```
checkspeed(152);

function checkspeed(speed){
    const speedlimit = 70;
    const kmPerPoint = 5;
    
    if (speed < speedlimit + kmPerPoint){
        isSpeedInLimit = true;
        console.log('Ok');
    }
    else {
        const points = Math.floor((speed - speedlimit) / kmPerPoint);
        if (points >= 12)
            console.log('Licensed Suspended');
        else 
            console.log('Points', points);   
    }  
}
```
> **output - Licensed Suspended**

```
showNumbers(10);

function showNumbers(numbers){
    for(let i = 0; i <= numbers; i++){
        if ((i % 2) === 0)
            console.log(i, 'EVEN');
        else
            console.log(i, 'ODD');
    }
}
```
> **output -   
0 "EVEN"
1 "ODD"
2 "EVEN"
3 "ODD"
4 "EVEN"
5 "ODD"
6 "EVEN"
7 "ODD"
8 "EVEN"
9 "ODD"
10 "EVEN"**

```
const array = [1,2,3,4,5,'',null,undefined];
console.log(countTruthy(array));

function countTruthy(array){
    let count = 0;
    for(value of array){
        if (value)
        count++;
    }
    return count;
}
```
> **output - 5**
```
const movie = {
    title: 'Titanic',
    releaseYear: 2000,
    rating: 4.5,
    actor: 'Rose'
};

showProperties(movie);

function showProperties(obj){
    for(let key in obj)
        if( typeof obj[key] === 'string')
            console.log(key, obj[key]);
}
```
> **output -  title Titanic <br>
              actor Rose**
```
console.log(sum(10));

function sum(number){
    let sum = 0;
    for(let i =1; i<=number;i++)
        if (i%3 === 0 || i%5 === 0)
            sum += i;
    return sum;
}
```
> **output - 33**
```
const marks = [80,80,40];
console.log(clalculateGrade(marks));

function clalculateGrade(marks){
    let avg = 0;
    for(let value of marks)
        avg += value;
    avg = avg / marks.length;
    
    if (avg < 60) return 'F';
    if (avg < 70) return 'D';
    if (avg < 80) return 'C';
    if (avg < 90) return 'B';
    return 'A';
}
```
> **output - D**
```
showStar(5);

function showStar(star){
    for(let i = 1; i <= star; i++){
        pattern = '';
        for(let j =0;j <i;j++)
            pattern +='*';
    console.log(pattern);
    }
}
```
> **output - 
$ <br>
$$ <br>
$$$ <br>
$$$$ <br>
$$$$$**
```
showPrime(20);

function showPrime(limit){
    for(let number = 2; number <= limit; number ++){
        let isPrime = true;
        for(let factor = 2; factor < number; factor++){
            if(number % factor === 0){
                isPrime = false;
                break;
            }
        }
        if (isPrime)
            console.log(number);
    }

}
```
> **output - 2
3
5
7
11
13
17
19**
