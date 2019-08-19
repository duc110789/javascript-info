## Trả lời các câu hỏi
#### 1. Nó là gì
#### 2. Cú pháp và giải thích ý nghĩa từng parameters
#### 3. Ví dụ đơn giản
#### 4. Trong thực tế
##

### map() method
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


