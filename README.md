

## 📚 **Popular Array Interview Questions (with Single Example)**

### 🔸 **1. Find the largest element in an array**

```javascript
const arr = [10, 5, 8, 20];
console.log(Math.max(...arr)); // 20
```

### 🔸 **2. Find the smallest element in an array**

```javascript
console.log(Math.min(...arr)); // 5
```

### 🔸 **3. Remove duplicates from an array**

```javascript
const uniqueArr = [...new Set(arr)];
console.log(uniqueArr); // [10, 5, 8, 20]
```

### 🔸 **4. Reverse an array**

```javascript
console.log(arr.reverse()); // [20, 8, 5, 10]
```

### 🔸 **5. Check if an array contains a specific value**

```javascript
console.log(arr.includes(10)); // true
```

### 🔸 **6. Flatten a nested array**

```javascript
const nestedArr = [1, [2, [3, 4]]];
console.log(nestedArr.flat(2)); // [1, 2, 3, 4]
```

### 🔸 **7. Find the index of an element**

```javascript
console.log(arr.indexOf(8)); // 2
```

### 🔸 **8. Sort an array in ascending order**

```javascript
console.log(arr.sort((a, b) => a - b)); // [5, 8, 10, 20]
```

### 🔸 **9. Sort an array in descending order**

```javascript
console.log(arr.sort((a, b) => b - a)); // [20, 10, 8, 5]
```

### 🔸 **10. Merge two arrays**

```javascript
const arr2 = [30, 40];
console.log(arr.concat(arr2)); // [10, 5, 8, 20, 30, 40]
```

### 🔸 **11. Sum all elements in an array**

```javascript
const sum = arr.reduce((total, num) => total + num, 0);
console.log(sum); // 43
```

### 🔸 **12. Find even numbers in an array**

```javascript
const evens = arr.filter(num => num % 2 === 0);
console.log(evens); // [10, 8, 20]
```

### 🔸 **13. Find odd numbers in an array**

```javascript
const odds = arr.filter(num => num % 2 !== 0);
console.log(odds); // [5]
```

### 🔸 **14. Count the occurrences of each element**

```javascript
const countOccurrences = arr.reduce((acc, num) => {
  acc[num] = (acc[num] || 0) + 1;
  return acc;
}, {});
console.log(countOccurrences); // {10: 1, 5: 1, 8: 1, 20: 1}
```

### 🔸 **15. Remove falsy values from an array**

```javascript
const mixedArr = [0, 1, false, 2, '', 3, null, undefined, NaN];
const truthyArr = mixedArr.filter(Boolean);
console.log(truthyArr); // [1, 2, 3]
```

### 🔸 **16. Split an array into chunks**

```javascript
function chunkArray(array, size) {
  return Array.from({ length: Math.ceil(array.length / size) }, (_, i) => 
    array.slice(i * size, i * size + size)
  );
}
console.log(chunkArray([1, 2, 3, 4, 5], 2)); // [[1, 2], [3, 4], [5]]
```

### 🔸 **17. Rotate an array by ********`k`******** positions**

```javascript
function rotateArray(arr, k) {
  k %= arr.length;
  return arr.slice(-k).concat(arr.slice(0, -k));
}
console.log(rotateArray([1, 2, 3, 4, 5], 2)); // [4, 5, 1, 2, 3]
```

### 🔸 **18. Find the intersection of two arrays**

```javascript
const arrA = [1, 2, 3, 4];
const arrB = [3, 4, 5, 6];
const intersection = arrA.filter(num => arrB.includes(num));
console.log(intersection); // [3, 4]
```

### 🔸 **19. Find the difference between two arrays**

```javascript
const difference = arrA.filter(num => !arrB.includes(num));
console.log(difference); // [1, 2]
```

### 🔸 **20. Shuffle an array**

```javascript
function shuffleArray(array) {
  return array.sort(() => Math.random() - 0.5);
}
console.log(shuffleArray([1, 2, 3, 4, 5]));
```

---

