## 1. Array.length
### The ```length``` property of an array: Returns the numner of elements in that array.
#### Syntax
```
  arr.length
```
```javascript
  var clothing = ['shoes', 'shirts', 'socks', 'sweaters'];
  console.log('clothing', clothing.length);
```
#### You can set the ```length``` property to truncate an array at any time. When you extend an array by changing its ```length``` property, the number actual elements increases
```javascript
var arr = [1, 2, 3];
printEntries(arr)
arr.length = 5;
printEntries(arr)
function printEntries(arr) {
  var length = arr.length;
  for(var i = 0; i < length; i ++) {
    console.log(arr[i]);
  }
  console.log('===Print===');
}
```
#### But, the ```length``` property does not necessarily indicate the number of defined values in the array.

## 2.Array.prototype.copyWithin()
### Copies a sequence of array elements within the array. The ```conpyWithin()``` method shallow copies part of an array to another location in the same array and return it, without modifying its size
#### Syntax
```
  arr.copyWithin(target[, start[, end]])
```
```javascript
  var array1 = ['a', 'b', 'c', 'd', 'e'];
  // copy index 0 to index 3
  console.log(array1.copyWithin(0, 3, 4));
```

