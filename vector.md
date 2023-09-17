## **std::vector Cheat Sheet**

`std::vector` is a dynamic array implementation in the C++ Standard Library.

### **1. Initialization:**

Include the necessary header:
```cpp
#include <vector>
```

Declare a vector\:
```cpp
std::vector<int> vec;
```

Initialize with values:
```cpp
std::vector<int> vec = {1, 2, 3, 4, 5};
```

### **2. Common Methods:**

- **Size and Capacity**:
  - `vec.size()` - Returns the number of elements.
  - `vec.capacity()` - Returns the current capacity.
  - `vec.empty()` - Checks if the vector is empty.
  - `vec.resize(n)` - Resizes the vector to contain `n` elements.

- **Element Access**:
  - `vec[i]` - Access element at index `i`.
  - `vec.at(i)` - Access element at index `i` with bounds checking.
  - `vec.front()` - Access the first element.
  - `vec.back()` - Access the last element.

- **Modifiers**:
  - `vec.push_back(value)` - Adds an element to the end.
  - `vec.pop_back()` - Removes the last element.
  - `vec.insert(it, value)` - Inserts `value` before iterator `it`.
  - `vec.erase(it)` - Erases element at iterator `it`.
  - `vec.clear()` - Removes all elements.

- **Comparing Vectors**:
  - `vec1 == vec2` - Checks if two vectors are equal.
  - `vec1 != vec2` - Checks if two vectors are not equal.

### **3. Advanced Operations:**

To get a vector containing elements that are not in both vectors:
```cpp
#include <algorithm>

std::vector<int> vec1 = {1, 2, 3, 4, 5};
std::vector<int> vec2 = {4, 5, 6, 7, 8};
std::vector<int> result;

std::set_difference(vec1.begin(), vec1.end(), vec2.begin(), vec2.end(), std::back_inserter(result));
```
The `result` vector will contain `{1, 2, 3}`.

---

This cheat sheet provides a basic overview of `std::vector`'s main features. Always refer to the official C++ documentation for a more comprehensive understanding and additional details.
