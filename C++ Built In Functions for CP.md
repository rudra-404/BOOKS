# C++ Built In Functions for CP

### **1. String & Container Size**
- ### `length()` / `size()`
Both return the number of elements in a string or container.

```cpp
string str = "Hello";
cout << str.size();    // Output: 5
cout << str.length();  // Output: 5
```

For vectors:
```cpp
vector<int> v = {1, 2, 3, 4};
cout << v.size();  // Output: 4
```

---

### **2. Maximum & Minimum**
- ### `max(a, b)` / `min(a, b)`
Returns the maximum/minimum of two values.

```cpp
cout << max(10, 20); // Output: 20
cout << min(10, 20); // Output: 10
```

For arrays:
```cpp
int arr[] = {4, 1, 7, 3};
cout << *max_element(arr, arr + 4);  // Output: 7
cout << *min_element(arr, arr + 4);  // Output: 1
```

---

### **3. Sorting**
- ### `sort()`
Sorts an array/vector in ascending order by default.

```cpp
vector<int> v = {5, 2, 8, 1};
sort(v.begin(), v.end());  // {1, 2, 5, 8}
```

#### **Descending Order Sort**
```cpp
sort(v.rbegin(), v.rend());  // {8, 5, 2, 1}
```

For arrays:
```cpp
int arr[] = {4, 2, 8, 1};
sort(arr, arr + 4);  // {1, 2, 4, 8}
```

---

### **4. Searching**
- ### `binary_search(start, end, value)`
Checks if a value exists in a **sorted** array/vector.

```cpp
vector<int> v = {1, 3, 5, 7};
cout << binary_search(v.begin(), v.end(), 3);  // Output: 1 (true)
cout << binary_search(v.begin(), v.end(), 4);  // Output: 0 (false)
```

---

### **5. Finding Elements**
- ### `find(start, end, value)`
Returns an iterator pointing to the first occurrence of a value.

```cpp
vector<int> v = {10, 20, 30, 40};
auto it = find(v.begin(), v.end(), 30);
if (it != v.end()) cout << "Found at index " << (it - v.begin());  // Output: 2
```

---

### **6. Lower & Upper Bound**
- ### `lower_bound(start, end, value)`
Finds the **first position** where `value` can be inserted without breaking order.

```cpp
vector<int> v = {1, 3, 3, 5, 7};
cout << (lower_bound(v.begin(), v.end(), 3) - v.begin()); // Output: 1
```

- ### `upper_bound(start, end, value)`
Finds the **first position greater than** `value`.

```cpp
cout << (upper_bound(v.begin(), v.end(), 3) - v.begin()); // Output: 3
```

---

### **7. Accumulate (Sum of Elements)**
- ### `accumulate(start, end, initial_value)`
Finds the sum of all elements in a container.

```cpp
#include <numeric>
vector<int> v = {1, 2, 3, 4};
cout << accumulate(v.begin(), v.end(), 0);  // Output: 10
```

---

### **8. Count Occurrences**
- ### `count(start, end, value)`
Counts occurrences of a value.

```cpp
vector<int> v = {1, 2, 3, 2, 2, 4};
cout << count(v.begin(), v.end(), 2);  // Output: 3
```

---

### **9. Reverse a String/Array**
- ### `reverse(start, end)`
Reverses a string or container.

```cpp
string s = "hello";
reverse(s.begin(), s.end());  
cout << s;  // Output: "olleh"
```

For arrays:
```cpp
int arr[] = {1, 2, 3, 4};
reverse(arr, arr + 4);  // {4, 3, 2, 1}
```

---

### **10. Next & Previous Permutation**
- ### `next_permutation(start, end)`
Generates the next lexicographical permutation.

```cpp
vector<int> v = {1, 2, 3};
next_permutation(v.begin(), v.end());  
// v becomes {1, 3, 2}
```

- ### `prev_permutation(start, end)`
Generates the previous permutation.

```cpp
prev_permutation(v.begin(), v.end());  
// v becomes {1, 2, 3} again
```

---

### **11. GCD & LCM**
- ### `gcd(a, b)` / `lcm(a, b)`
Computes the greatest common divisor & least common multiple.

```cpp
#include <numeric>
cout << gcd(8, 12);  // Output: 4
cout << lcm(8, 12);  // Output: 24
```

---

### **12. Power & Square Root**
- ### `pow(base, exponent)`
Returns `base^exponent`.

```cpp
cout << pow(2, 3);  // Output: 8
```

- ### `sqrt(value)`
Finds the square root.

```cpp
cout << sqrt(25);  // Output: 5
```

---

### **13. Logarithm**
- ### `log(x)` (Natural log, base **e**)
```cpp
cout << log(10);  // Output: 2.30258
```

- ### `log10(x)` (Logarithm base **10**)
```cpp
cout << log10(100);  // Output: 2
```

---

### **14. Bit Manipulation**
- ### `__builtin_popcount(x)`
Counts the number of `1`s in the binary representation.

```cpp
cout << __builtin_popcount(7);  // Output: 3 (since 7 = 111 in binary)
```

- ### `__builtin_ctz(x)` (Count trailing zeros)
```cpp
cout << __builtin_ctz(16);  // Output: 4 (since 16 = 10000 in binary)
```

---

### **15. Random Number Generation**
- ### `rand()`
Generates a random number.

```cpp
cout << rand() % 100;  // Output: Random number between 0-99
```

---

### **16. Ceil & Floor**
- ### `ceil(x)` / `floor(x)`
```cpp
cout << ceil(2.3);   // Output: 3
cout << floor(2.9);  // Output: 2
```