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

```
