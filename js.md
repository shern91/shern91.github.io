## [Home](index.md)

#### 1. Five Uses for the Spread Operator
##### i. Copying an array.
```
let arr = [1,2,3,4]
let copy = [...arr]
// copy is [ 1, 2, 3, 4 ]
```

##### ii. Concatenate arrays.
```
let arr1 = [1,2,3,4]
let arr2 = [5,6,7,8]
let concat = [...arr1, ...arr2]
// concat is [ 1, 2, 3, 4, 5, 6, 7, 8 ]
```

##### iii. Pass arguments as arrays
```
function dev(x, y, z) { 
    console.log(`${x}, ${y}, ${z}`);
}

var args = [0, 1, 2]

dev(...args) // call function
// output 
// '0, 1, 2'
```

##### iv. Copy an object.
```
let obj = {a: 1, b: 2, c: 3}
let copy = {...obj}
// copy is {a: 1, b: 2, c: 3}
```

##### v. Merge object.
```
let obj1 = {a: 1, b: 2, c: 3}
let obj1 = {d: 4, e: 5, f: 6}

let merge = {...obj1, ...obj2}
// merge is {a: 1, b: 2, c: 3, d: 4, e: 5, f: 6}

// Note that for merging objects, the keys in the later objects take precedence. e.g.
let obj1 = { a:1, b:2, c:3 };
let obj2 = { a:2 };

let obj3 = {...obj1, ...obj2};
// obj3 is { a:2, b:2, c:3 }
```


#### Date Function (Native JavaScript)

##### Get day of year
```
Math.floor(
  (new Date() - new Date(new Date().getFullYear(), 0, 0)) / 1000 / 60 / 60 / 24
);
```