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
  console.log(array1.copyWithin(-2, -4, -1));
```

## 3. Array.prototype.fill()
### The fill() method fills (modifies) all the elements of an array from a start index (default zero) to an end index (default array length) with a static value. It returns the modified array.
#### Syntax
```
  arr.value(value[, start[, end]])
```
```javascript
  var arrfill = [1, 2, 3, 4];
  console.log(arrfill.fill(3, 1, 4));
```

## 4. Array.prototype.pop()
### The pop() method removes the last elements of an array and return that element. This method changes the length of the array
#### Syntax
```
  arr.pop()
```
```javascript
  var arrpop = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];
  console.log('arrpop', arrpop.pop());
  // expected output: arrpop = 'tomato'
```

## 5. Array.prototype.push()
### The push() method adds one or more elements to the end of an array and returns the new length of the array
#### Syntax
```
  arr.push(element1[, ...[, elementN]])
```
```javascript
  var arrPush = ['pigs', 'goats', 'sheep'];
  console.log('arrPush', arrPush.push('cows'));
  // expected output: arrPush 4
```

## 6. Array.prototype.reverse()
### The reverse() method reverses an array. The first array element becomes the last and the last element becomes the first
#### Syntax
```
  arr.reverse()
```
```javascript
  var arrReserve = [1, 2, 3];
  console.log('arrReserve', arrReserve);
  var reserved = arrReserve.reserve();
  console.log('reserved', reserved);
  // expected output: arrReserve = [3, 2, 1];
```

## 7. Array.prototype.shift()
### The shift() method removes the first element from an array and returns that removed element. This method changes the length of the array
#### Syntax
```
  arr.shift()
```
```javascript
  var arrShift = [1, 2, 3];
  var shiftElement = arrShift.shift();
  console.log('shiftElement', shiftElement);
  console.log('arrShift', arrShift);
```

## 8. Array.prototype.sort()
### The sort() method sorts the elements of an array and returns the array. The default sort order is built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values
#### Syntax
```
  arr.sort([compareFunction])
```
```javascript
  var months = ['March', 'Jan', 'Feb', 'Dec'];
  console.log('months before:', months)
  months.sort();
  console.log('months after:', months);
```

## 9. Array.prototype.splice()
### The splice() method changes the contents of an array by removing or replacing existing elements add/or adding new elements.
#### Syntax
```
  array.splice(start[, deleteCount[, item1[, item2[, ...]]]])
```
```javascript
  var monthSplice = ['March', 'Jan', 'Feb', 'Dec'];
  console.log('monthSplice', monthSplice);
  monthSplice.splice(1, 0, 'Feb');
  console.log('monthSplice', monthSplice);
```

## 10. Array.prototype.unshift()
### The unshift() method adds one more elements to the begining of an array and returns the new length of the array.
#### Syntax
```
  arr.unshift(element[, ...[, elementN]])
```
```javascript
  var arrUnshift = [1, 2, 3];
  console.log('unshift', arrUnshift.unshift(4, 5));
  console.log('arrUnshift', arrUnshift);
```

## 11. Array.prototype.concat()
### Return a new array that is this array joined with other array(s) and/or value(s).
#### Syntax
```
  var new_array = old_array.concat([value1[, value2[, ...[, valueN]]]])
```
```javascript
  const num1 = [1, 2, 3];
  const num2 = [4, 5, 6];
  const num3 = [7, 8, 9];
  const numbers = num1.concat(num2, num3);
  console.log(numbers);
```

## 12. Array.prototype.includes()
### The includes() method determines whether an array includes a certain value among its entries, returning true or false as appropriate
#### Syntax
```
  arr.includes(searchElement, [fromIndex])
```
```javascript
  var arrIncludes = [1, 2, 3];
  console.log('arrIncludes', arrIncludes.includes(1));
  console.log([1, 2, 3].includes(3, 2));
```

## 13. Array.prototype.indexOf()
### The indexOf() method Returns the first(least) index of an element within the array equal to the specified value, or -1 if none is found
#### Syntax
```
  arr.indexOf(searchElement, [fromIndex])
```
```javascript
  var arrIndexOf = ['ant', 'bison', 'camel', 'duck', 'bison'];
  console.log('arrIndexOf', arrIndexOf);
  console.log('arrIndexOf', arrIndexOf.indexOf('camel'));
  console.log('arrIndexOf', arrIndexOf.indexOf('bison', 5));
```

## 13. Array.prototype.filter()
### Create a new array with all of the elements of this array for which the provided filtering function retuns true
#### Syntax
```
  var newArray = arr.filter(callback(element[, index[, array]])[, thisArg])
```
```javascript
  var arrFilter = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
  const result = arrFilter.filter(word => word.length > 6);
  console.log('result', result);

  var fruits = ['apple', 'banana', 'grapes', 'mango', 'orange'];
  const filterItems = (arr, query) => arr.filter((el) => el.toLowerCase().indexOf(query.toLowerCase()) > -1);
  console.log(filterItems(fruits, 'ap')); // ['apple', 'grapes']
  console.log(filterItems(fruits, 'an')); // ['banana', 'mango', 'orange']
```

## 14. Array.prototype.map()
### The map() method creates a new array with the results of calling a provided function on every element in the calling array
#### Syntax
```
  var newArray = arr.map(function callback(currentValue[, index[, array]]){
    // Return element for new_array
  }, [, thisArg])
```
```javascript
  var arrFilter = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
  const result = arrFilter.filter(word => word.length > 6);
  console.log('result', result);

  var fruits = ['apple', 'banana', 'grapes', 'mango', 'orange'];
  const filterItems = (arr, query) => arr.filter((el) => el.toLowerCase().indexOf(query.toLowerCase()) > -1);
  console.log(filterItems(fruits, 'ap')); // ['apple', 'grapes']
  console.log(filterItems(fruits, 'an')); // ['banana', 'mango', 'orange']
```

## 14. Array.prototype.reduce()
### The reduce() method executes a reducer function (that you provide) on earch member of the array resulting in a single output value
#### Syntax
```
  arr.reduce(callback[, initialValue])
```
```javascript
  var arrReduce = [1, 2, 3, 4];
  const reducer = (a, b) => a + b;
  console.log('arrReduce', arrReduce.reduce(reducer));
```

