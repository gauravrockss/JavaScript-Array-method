# Mastering JavaScript Array Methods: A Comprehensive Guide

Boost your JavaScript skills with this handy reference of array methods! Save it for future use and share with your network!

## 🔗 Array Methods

### 1.`concat()` - Combine arrays

Example:

```javascript
let arr = [1, 2, 3];
arr = arr.concat(4, 5, 6); // [1, 2, 3, 4, 5, 6]
```

### 2. `join()` - Joins all elements of an array into a string.

Example:

```javascript
const myArray = ['Wind', 'Rain', 'Fire'];
const list = myArray.join(' - '); // list is "Wind - Rain - Fire"
```

### 3. `push()` - Adds one or more elements to the end of an array and returns the resulting length of the array.

Example:

```javascript
const myArray = ['1', '2'];
myArray.push('3'); // myArray is now ["1", "2", "3"]
```

### 4. `pop()` - Removes the last element from an array and returns that element.

Example:

```javascript
const myArray = ['1', '2', '3'];
const last = myArray.pop();
// myArray is now ["1", "2"], last = "3"
```

### 5. `shift()` - Removes the first element from an array and returns that element.

Example:

```javascript
const myArray = ['1', '2', '3'];
const first = myArray.shift();
// myArray is now ["2", "3"], first is "1"
```

### 6. `unshift()` - Adds one or more elements to the front of an array and returns the new length of the array.

Example:

```javascript
const myArray = ['1', '2', '3'];
myArray.unshift('4', '5');
// myArray becomes ["4", "5", "1", "2", "3"]
```

### 7. `slice()` - Extracts a section of an array and returns a new array.

Example:

```javascript
let myArray = ['a', 'b', 'c', 'd', 'e'];
myArray = myArray.slice(1, 4); // [ "b", "c", "d"]
// starts at index 1 and extracts all elements
// until index 3
```

### 8. `at()` - Returns the element at the specified index in the array, or undefined if the index is out of range. It's notably used for negative indices that access elements from the end of the array.

Example:

```javascript
const myArray = ['a', 'b', 'c', 'd', 'e'];
myArray.at(-2); // "d", the second-last element of myArray
```

### 9. `splice()` - Removes elements from an array and (optionally) replaces them. It returns the items which were removed from the array.

Example:

```javascript
const myArray = ['1', '2', '3', '4', '5'];
myArray.splice(1, 3, 'a', 'b', 'c', 'd');
// myArray is now ["1", "a", "b", "c", "d", "5"]
// This code started at index one (or where the "2" was),
// removed 3 elements there, and then inserted all consecutive
// elements in its place.
```

### 10. `reverse()` - Transposes the elements of an array, in place: the first array element becomes the last and the last becomes the first. It returns a reference to the array.

Example:

```javascript
const myArray = ['1', '2', '3'];
myArray.reverse();
// transposes the array so that myArray = ["3", "2", "1"]
```

### 11. `flat()` - Returns a new array with all sub-array elements concatenated into it recursively up to the specified depth.

Example:

```javascript
let myArray = [1, 2, [3, 4]];
myArray = myArray.flat();
// myArray is now [1, 2, 3, 4], since the [3, 4] subarray is flattened
```

### 12. `sort()` - Sorts the elements of an array in place, and returns a reference to the array.

Example:

```javascript
const myArray = ['Wind', 'Rain', 'Fire'];
myArray.sort();
// sorts the array so that myArray = ["Fire", "Rain", "Wind"]

// With a comparison function
const sortFn = (a, b) => {
    if (a[a.length - 1] < b[b.length - 1]) {
        return -1; // Negative number => a < b, a comes before b
    } else if (a[a.length - 1] > b[b.length - 1]) {
        return 1; // Positive number => a > b, a comes after b
    }
    return 0; // Zero => a = b, a and b keep their original order
};
myArray.sort(sortFn);
// sorts the array so that myArray = ["Wind", "Fire", "Rain"]
```

### 13. `indexOf()` - Searches the array for searchElement and returns the index of the first match.

Example:

```javascript
const a = ['a', 'b', 'a', 'b', 'a'];
console.log(a.indexOf('b')); // 1

// Now try again, starting from after the last match
console.log(a.indexOf('b', 2)); // 3
console.log(a.indexOf('z')); // -1, because 'z' was not found
```

### 14. `lastIndexOf()` - Works like indexOf, but starts at the end and searches backwards.

Example:

```javascript
const a = ['a', 'b', 'c', 'd', 'a', 'b'];
console.log(a.lastIndexOf('b')); // 5

// Now try again, starting from before the last match
console.log(a.lastIndexOf('b', 4)); // 1
console.log(a.lastIndexOf('z')); // -1
```

### 15. `forEach()` - Executes callback on every array item and returns undefined.

Example:

```javascript
const a = ['a', 'b', 'c'];
a.forEach(element => {
    console.log(element);
});
// Logs:
// a
// b
// c
```

### 16. `map()` - Returns a new array of the return value from executing callback on every array item.

Example:

```javascript
const a1 = ['a', 'b', 'c'];
const a2 = a1.map(item => item.toUpperCase());
console.log(a2); // ['A', 'B', 'C']
```

### 17. `flatMap()` - Runs map() followed by a flat() of depth 1.

Example:

```javascript
const a1 = ['a', 'b', 'c'];
const a2 = a1.flatMap(item => [item.toUpperCase(), item.toLowerCase()]);
console.log(a2); // ['A', 'a', 'B', 'b', 'C', 'c']
```

### 18. `filter()` - Returns a new array containing the items for which callback returned true.

Example:

```javascript
const a1 = ['a', 10, 'b', 20, 'c', 30];
const a2 = a1.filter(item => typeof item === 'number');
console.log(a2); // [10, 20, 30]
```

### 19. `find()` - Returns the first item for which callback returned true.

Example:

```javascript
const a1 = ['a', 10, 'b', 20, 'c', 30];
const i = a1.find(item => typeof item === 'number');
console.log(i); // 10
```

### 20. `findLast()` - Returns the last item for which callback returned true.

Example:

```javascript
const a1 = ['a', 10, 'b', 20, 'c', 30];
const i = a1.findLast(item => typeof item === 'number');
console.log(i); // 30
```

### 21. `findIndex()` - Returns the index of the first item for which callback returned true.

Example:

```javascript
const a1 = ['a', 10, 'b', 20, 'c', 30];
const i = a1.findIndex(item => typeof item === 'number');
console.log(i); // 1
```

### 22. `findLastIndex()` - Returns the index of the last item for which callback returned true.

Example:

```javascript
const a1 = ['a', 10, 'b', 20, 'c', 30];
const i = a1.findLastIndex(item => typeof item === 'number');
console.log(i); // 5
```

### 23. `every()` - Returns true if callback returns true for every item in the array

Example:

```javascript
function isNumber(value) {
    return typeof value === 'number';
}
const a1 = [1, 2, 3];
console.log(a1.every(isNumber)); // true
const a2 = [1, '2', 3];
console.log(a2.every(isNumber)); // false
```

### 24. `some()` - Returns true if callback returns true for at least one item in the array.

Example:

```javascript
function isNumber(value) {
    return typeof value === 'number';
}
const a1 = [1, 2, 3];
console.log(a1.some(isNumber)); // true
const a2 = [1, '2', 3];
console.log(a2.some(isNumber)); // true
const a3 = ['1', '2', '3'];
console.log(a3.some(isNumber)); // false
```

### 25. `reduce()` - Applies callback(accumulator, currentValue) to reduce the array to a single value.

Example:

```javascript
const a = [10, 20, 30];
const total = a.reduce((acc, item) => acc + item, 0);
console.log(total); // 60
```

### 26. `reduceRight()` - Works like reduce(), but starts with the last element.

Example:

```javascript
const a = [10, 20, 30];
const total = a.reduceRight((acc, item) => acc + item, 0);
console.log(total); // 60
```

### 27. `includes()` - Determines whether an array includes a certain value among its entries, returning true or false as appropriate.

Example:

```javascript
const a = [1, 2, 3];
console.log(a.includes(2)); // true
console.log(a.includes(4)); // false
```

### 28. `keys()` - Returns a new Array Iterator object that contains the keys for each index in the array.

Example:

```javascript
const array1 = ['a', 'b', 'c'];
const iterator = array1.keys();
for (const key of iterator) {
    console.log(key); // 0, 1, 2
}
```

### 29. `values()` - Returns a new Array Iterator object that contains the values for each index in the array.

Example:

```javascript
const array1 = ['a', 'b', 'c'];
const iterator = array1.values();
for (const value of iterator) {
    console.log(value); // 'a', 'b', 'c'
}
```

### 30. `entries()` - Returns a new Array Iterator object that contains the key/value pairs for each index in the array.

Example:

```javascript
const array1 = ['a', 'b', 'c'];
const iterator = array1.entries();
for (const [index, element] of iterator) {
    console.log(index, element); // 0 'a', 1 'b', 2 'c'
}
```
