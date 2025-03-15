

## 📚 **Array Problems: Built-in vs. Manual Implementation (20 Problems)**

---

### 🔸 **1. Find the Largest Element in an Array**

✅ **With In-Built Function:**

```javascript
const arr = [10, 5, 8, 20];
console.log(Math.max(...arr)); // 20
```

❌ **Without In-Built Function:**

```javascript
function findMax(arr) {
  let max = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i];
    }
  }
  return max;
}
console.log(findMax([10, 5, 8, 20])); // 20
```

---

### 🔸 **2. Find the Smallest Element in an Array**

✅ **With In-Built Function:**

```javascript
console.log(Math.min(...arr)); // 5
```

❌ **Without In-Built Function:**

```javascript
function findMin(arr) {
  let min = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] < min) {
      min = arr[i];
    }
  }
  return min;
}
console.log(findMin([10, 5, 8, 20])); // 5
```

---

### 🔸 **3. Remove Duplicates from an Array**

✅ **With In-Built Function:**

```javascript
const uniqueArr = [...new Set(arr)];
console.log(uniqueArr); // [10, 5, 8, 20]
```

❌ **Without In-Built Function:**

```javascript
function removeDuplicates(arr) {
  const uniqueArr = [];
  for (let i = 0; i < arr.length; i++) {
    let found = false;
    for (let j = 0; j < uniqueArr.length; j++) {
      if (arr[i] === uniqueArr[j]) {
        found = true;
        break;
      }
    }
    if (!found) uniqueArr.push(arr[i]);
  }
  return uniqueArr;
}
console.log(removeDuplicates([10, 5, 8, 10, 20, 8])); // [10, 5, 8, 20]
```

---

### 🔸 **4. Reverse an Array**

✅ **With In-Built Function:**

```javascript
console.log(arr.reverse()); // [20, 8, 5, 10]
```

❌ **Without In-Built Function:**

```javascript
function reverseArray(arr) {
  const reversed = [];
  for (let i = arr.length - 1; i >= 0; i--) {
    reversed.push(arr[i]);
  }
  return reversed;
}
console.log(reverseArray([10, 5, 8, 20])); // [20, 8, 5, 10]
```

---

### 🔸 **5. Check if an Array Contains a Specific Value**

✅ **With In-Built Function:**

```javascript
console.log(arr.includes(10)); // true
```

❌ **Without In-Built Function:**

```javascript
function containsValue(arr, value) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === value) return true;
  }
  return false;
}
console.log(containsValue([10, 5, 8, 20], 10)); // true
```

---

### 🔸 **6. Flatten a Nested Array (1 Level Deep)**

✅ **With In-Built Function:**

```javascript
const nestedArr = [1, [2, 3], 4];
console.log(nestedArr.flat()); // [1, 2, 3, 4]
```

❌ **Without In-Built Function:**

```javascript
function flattenArray(arr) {
  const flat = [];
  for (let i = 0; i < arr.length; i++) {
    if (Array.isArray(arr[i])) {
      for (let j = 0; j < arr[i].length; j++) {
        flat.push(arr[i][j]);
      }
    } else {
      flat.push(arr[i]);
    }
  }
  return flat;
}
console.log(flattenArray([1, [2, 3], 4])); // [1, 2, 3, 4]
```

---

### 🔸 **7. Find the Index of an Element**

✅ **With In-Built Function:**

```javascript
console.log(arr.indexOf(8)); // 2
```

❌ **Without In-Built Function:**

```javascript
function findIndex(arr, value) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === value) return i;
  }
  return -1;
}
console.log(findIndex([10, 5, 8, 20], 8)); // 2
```

---

### 🔸 **8. Sort an Array (Ascending Order)**

✅ **With In-Built Function:**

```javascript
console.log(arr.sort((a, b) => a - b)); // [5, 8, 10, 20]
```

❌ **Without In-Built Function (Bubble Sort):**

```javascript
function bubbleSort(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length - i - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        let temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
    }
  }
  return arr;
}
console.log(bubbleSort([10, 5, 8, 20])); // [5, 8, 10, 20]
```

---

### 🔸 **9. Merge Two Arrays**

✅ **With In-Built Function:**

```javascript
const arr2 = [30, 40];
console.log(arr.concat(arr2)); // [10, 5, 8, 20, 30, 40]
```

❌ **Without In-Built Function:**

```javascript
function mergeArrays(arr1, arr2) {
  const merged = [];
  for (let i = 0; i < arr1.length; i++) {
    merged.push(arr1[i]);
  }
  for (let j = 0; j < arr2.length; j++) {
    merged.push(arr2[j]);
  }
  return merged;
}
console.log(mergeArrays([10, 5], [8, 20])); // [10, 5, 8, 20]
```

---

### 🔸 **10. Sum All Elements in an Array**

✅ **With In-Built Function:**

```javascript
console.log(arr.reduce((sum, num) => sum + num, 0)); // 43
```

❌ **Without In-Built Function:**

```javascript
function sumArray(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}
console.log(sumArray([10, 5, 8, 20])); // 43
```

## 📚 **Array Problems: Built-in vs. Manual Implementation (20 Problems)**

---

### 🔸 **11. Count Occurrences of an Element**

✅ **With In-Built Function:**

```javascript
const count = arr.filter(x => x === 10).length;
console.log(count); // Count of 10s
```

❌ **Without In-Built Function:**

```javascript
function countOccurrences(arr, value) {
  let count = 0;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === value) count++;
  }
  return count;
}
console.log(countOccurrences([10, 5, 10, 8], 10)); // 2
```

---

### 🔸 **12. Find the Second Largest Element**

✅ **With In-Built Function:**

```javascript
const sortedArr = [...new Set(arr)].sort((a, b) => b - a);
console.log(sortedArr[1]); // Second largest element
```

❌ **Without In-Built Function:**

```javascript
function secondLargest(arr) {
  let max = -Infinity, secondMax = -Infinity;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > max) {
      secondMax = max;
      max = arr[i];
    } else if (arr[i] > secondMax && arr[i] !== max) {
      secondMax = arr[i];
    }
  }
  return secondMax;
}
console.log(secondLargest([10, 5, 8, 20])); // 10
```

---

### 🔸 **13. Rotate Array to the Right**

✅ **With In-Built Function:**

```javascript
const rotate = arr.splice(-2).concat(arr);
console.log(rotate);
```

❌ **Without In-Built Function:**

```javascript
function rotateArray(arr, k) {
  k = k % arr.length;
  return arr.slice(-k).concat(arr.slice(0, arr.length - k));
}
console.log(rotateArray([1, 2, 3, 4], 2)); // [3, 4, 1, 2]
```

---

### 🔸 **14. Check if Two Arrays Are Equal**

✅ **With In-Built Function:**

```javascript
const isEqual = JSON.stringify(arr1) === JSON.stringify(arr2);
console.log(isEqual);
```

❌ **Without In-Built Function:**

```javascript
function areArraysEqual(arr1, arr2) {
  if (arr1.length !== arr2.length) return false;
  for (let i = 0; i < arr1.length; i++) {
    if (arr1[i] !== arr2[i]) return false;
  }
  return true;
}
console.log(areArraysEqual([1, 2, 3], [1, 2, 3])); // true
```

---

### 🔸 **15. Find Missing Number in Sequence**

✅ **With In-Built Function:**

```javascript
const n = arr.length + 1;
const sum = (n * (n + 1)) / 2;
console.log(sum - arr.reduce((a, b) => a + b));
```

❌ **Without In-Built Function:**

```javascript
function findMissingNumber(arr) {
  const n = arr.length + 1;
  let total = (n * (n + 1)) / 2;
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return total - sum;
}
console.log(findMissingNumber([1, 2, 4, 5])); // 3
```

---

### 🔸 **16. Find Intersection of Two Arrays**

✅ **With In-Built Function:**

```javascript
const intersection = arr1.filter(x => arr2.includes(x));
console.log(intersection);
```

❌ **Without In-Built Function:**

```javascript
function arrayIntersection(arr1, arr2) {
  const result = [];
  for (let i = 0; i < arr1.length; i++) {
    for (let j = 0; j < arr2.length; j++) {
      if (arr1[i] === arr2[j] && !result.includes(arr1[i])) {
        result.push(arr1[i]);
      }
    }
  }
  return result;
}
console.log(arrayIntersection([1, 2, 3], [2, 3, 4])); // [2, 3]
```

---




