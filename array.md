## Trả lời các câu hỏi
#### 1. Nó là gì
#### 2. Cú pháp và giải thích ý nghĩa từng parameters
#### 3. Ví dụ đơn giản
#### 4. Trong thực tế
##

### I. map() method
### 1. Nó là gì:
```javascript
Phương thức map() tạo ra 1 mảng mới với các phần tử mới được thực thi 1 hàm trên từng phần tử của mảng cũ.
```
### 2. Cú pháp:
```javascript
var new_array = arr.map((value, index, array), thisArg);
```
#### 3 Arguments:
- value: Giá trị hiện tại của phép lặp
- index: Index của vòng lặp
- array: Mảng ban đầu được gọi
##### ThisArg:
- Value được sử dụng như this khi thực hiện callback
### 3. Ví dụ đơn giản:
```javascipt
var numbers = [1, 2, 3];
var doubles = numbers.map(num => num * 2);
console.log('numbers', numbers); // [1, 2, 3];
console.log('doubles', doubles); // [2, 4, 6];
```
### 4. Bài toán thực tế:
```javascript
let distances = [
 { from: 'New York', to: 'Dhaka', distance: 12654},
 { from: 'Sydney', to: 'chittagong', distance: 8858},
 { from: 'Kolkata', to: 'Sylhet', distance: 670}
];
let convertedDistances = distances.map(item => ({
  ...item,
  distance: item.distance * 0.621371
}))
console.log('convertedDistances:', convertedDistances);
```

### II. filter() method
### 1. Nó là gì:
```javascript
Phương thức filter() lọc 1 số items ra khỏi mảng ban đầu.
```
### 2. Cú pháp:
```javascript
var new_array = arr.filter((value, index, array), thisArg);
```
#### 3 Arguments:
- value: Giá trị hiện tại của phép lặp
- index: Index của vòng lặp
- array: Mảng ban đầu được gọi
##### ThisArg:
- Value được sử dụng như this khi thực hiện callback
### 3. Ví dụ đơn giản:
```javascipt
var numbers = [1, 2, 3];
function isBigEnough(value) {
  return value >= 2;
}
var filtered = numbers.filter(value => value >= 2);
console.log('numbers', numbers); // [1, 2, 3];
console.log('filtered', filtered); // [2, 3];
```
### 4. Bài toán thực tế:
```javascript
 let distances = [
   { from: 'New York', to: 'Dhaka', distance: 12654},
   { from: 'Sydney', to: 'chittagong', distance: 8858},
   { from: 'Kolkata', to: 'Sylhet', distance: 670}
  ];
  let filterDistances = distances.filter(item => item.distance > 10000);
  console.log('filterDistances:', filterDistances);
```

### III. reduce() method
### 1. Nó là gì:
```javascript
Phương thức reduce() thực thi 1 hàm lên các phần tử của mảng( từ trái sáng phải) với một biến tích luỹ để thu về 1 giá trị duy nhất
```
### 2. Cú pháp:
```javascript
var new_array = arr.reduce(callback[, initialValue]);
```
#### 4 Arguments:
- accumulator: biến tích luỹ, được trả về sau mỗi lần 
- currentValue: phần tử mảng đang được xử lý
- currentIndex: index mảng đang được xử lý
- array: mảng hiện tại gọi reduce()
##### initialValue:
- là giá trị trả về cho tham số thứ nhất(accumulator) của hàm callback trong lần gọi đầu tiên, nếu giá trị này không được cung cấp thì giá trị phần tử đầu tiên của mảng sẽ được sử dụng
##### return value:
- chính là giá trị của accumulator sau lần gọi callback cuối cùng
### 3. Ví dụ đơn giản:
```javascipt
var numbers = [1, 2, 3];
var reduced = numbers.reduce((acc, cur) => {
  return acc + cur;
});
console.log('numbers', numbers); // 6
console.log('reduced', reduced); // [2, 3];
```
### 4. Bài toán thực tế:
- get request time trong React
```javascript
 let distances = [
   { from: 'New York', to: 'Dhaka', distance: 12654},
   { from: 'Sydney', to: 'chittagong', distance: 8858},
   { from: 'Kolkata', to: 'Sylhet', distance: 670}
  ];
  let reduceDistances = distances.reduce((acc, cur) => acc + cur.distance, 0);
  console.log('reduceDistances:', reduceDistances); // 22182
```

#### Mix 3 method trong 1 bài toán: Tìm quãng đường đi theo miles < 10000km
```javascript
let distances = [
  { from: 'New York', to: 'Dhaka', distance: 12654},
  { from: 'Sydney', to: 'chittagong', distance: 8858},
  { from: 'Kolkata', to: 'Sylhet', distance: 670}
];

let total = distances.filter(item => item.distance < 10000)
                     .map(item => item.distance * 0.621371)
                     .reduce((acc, cur) => acc + cur, 0);
console.log('total:', total);
```

