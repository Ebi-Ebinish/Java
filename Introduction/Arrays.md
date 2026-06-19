
An **array** is a collection of elements of the **same data type** stored in a single variable.

Types:

	1. Single Dimensional Array (1D Array)
	2. Multidimensional Array
	3. Jagged Array
	4. Anonymous Array
	5. Array of Objects

## Single Dimensional Array
		Stores elements in a single row.
```code
int[] arr = {10, 20, 30, 40};
```

Representation:

```
Index : 0   1   2   3Value :10  20  30  40
```

Access:

```java
System.out.println(arr[0]); // 10
```

### 2. Multidimensional Array

An array that contains other arrays.

#### 2D Array

```
int[][] arr = {    {1, 2, 3},    {4, 5, 6},    {7, 8, 9}};
```

Representation:

```
1 2 34 5 67 8 9
```

Access:

```
System.out.println(arr[1][2]); // 6
```

#### 3D Array

```
int[][][] arr = new int[2][3][4];
```

You can create 3D, 4D, etc., but 2D is the most commonly used.

---

### 3. Jagged Array

A jagged array is a multidimensional array where **each row can have a different number of columns**.

```
int[][] arr = new int[3][];arr[0] = new int[]{10, 20};arr[1] = new int[]{30, 40, 50, 60};arr[2] = new int[]{70, 80, 90};
```

Representation:

```
10 2030 40 50 6070 80 90
```

Notice:

- Row 0 → 2 elements
- Row 1 → 4 elements
- Row 2 → 3 elements

This is why it is called a **Jagged Array**.

---

### 4. Anonymous Array

An array created **without storing it in a variable**.

Example:

```
sum(new int[]{10, 20, 30});
```

Method:

```
static void sum(int[] arr) {    int s = 0;    for(int x : arr) {        s += x;    }    System.out.println(s);}
```

Output:

```
60
```

---

### 5. Array of Objects

Instead of storing primitive values, you store objects.

```
class Student {    int id;    String name;}Student[] students = new Student[3];students[0] = new Student();students[1] = new Student();students[2] = new Student();
```

Each element stores a reference to a `Student` object.


### The Arrays All methods

# 1. `length` (Array Property)

Returns the number of elements.

```
int[] arr = {10, 20, 30};System.out.println(arr.length);
```

**Output**

```
3
```

---

# 2. `Arrays.toString()`

Converts a 1D array into a readable string.

```
int[] arr = {10, 20, 30};System.out.println(Arrays.toString(arr));
```

**Output**

```
[10, 20, 30]
```

---

# 3. `Arrays.deepToString()`

Used for 2D or multidimensional arrays.

```
int[][] arr = {    {1,2},    {3,4}};System.out.println(Arrays.deepToString(arr));
```

**Output**

```
[[1, 2], [3, 4]]
```

---

# 4. `Arrays.sort()`

Sorts the array in ascending order.

```
int[] arr = {5, 2, 8, 1};Arrays.sort(arr);System.out.println(Arrays.toString(arr));
```

**Output**

```
[1, 2, 5, 8]
```

---

# 5. `Arrays.binarySearch()`

Searches an element in a **sorted** array.

```
int[] arr = {1, 2, 5, 8};int index = Arrays.binarySearch(arr, 5);System.out.println(index);
```

**Output**

```
2
```

---

# 6. `Arrays.equals()`

Checks whether two arrays are equal.

```
int[] a = {1,2,3};int[] b = {1,2,3};System.out.println(Arrays.equals(a,b));
```

**Output**

```
true
```

---

# 7. `Arrays.deepEquals()`

Compares 2D arrays.

```
int[][] a = {    {1,2},    {3,4}};int[][] b = {    {1,2},    {3,4}};System.out.println(Arrays.deepEquals(a,b));
```

**Output**

```
true
```

---

# 8. `Arrays.fill()`

Fills all elements with the same value.

```
int[] arr = new int[5];Arrays.fill(arr, 10);System.out.println(Arrays.toString(arr));
```

**Output**

```
[10, 10, 10, 10, 10]
```

---

# 9. `Arrays.copyOf()`

Copies the array.

```
int[] arr = {1,2,3};int[] copy = Arrays.copyOf(arr, arr.length);System.out.println(Arrays.toString(copy));
```

**Output**

```
[1, 2, 3]
```

---

# 10. `Arrays.copyOfRange()`

Copies only a specified range.

```
int[] arr = {10,20,30,40,50};int[] copy = Arrays.copyOfRange(arr,1,4);System.out.println(Arrays.toString(copy));
```

**Output**

```
[20, 30, 40]
```

> Start index is included, end index is excluded.

---

# 11. `Arrays.stream()`

Creates a stream from an array.

```
int[] arr = {1,2,3,4,5};int sum = Arrays.stream(arr).sum();System.out.println(sum);
```

**Output**

```
15
```

---

# 12. `Arrays.asList()`

Converts an array to a List.

```
String[] arr = {"Java","Python","C"};System.out.println(Arrays.asList(arr));
```

**Output**

```
[Java, Python, C]
```

---

# 13. `Arrays.compare()`

Compares two arrays lexicographically.

```
int[] a = {1,2,3};int[] b = {1,2,4};System.out.println(Arrays.compare(a,b));
```

**Output**

```
-1
```

Because:

```
3 < 4
```

---

# 14. `Arrays.mismatch()`

Finds the first index where arrays differ.

```
int[] a = {1,2,3,4};int[] b = {1,2,5,4};System.out.println(Arrays.mismatch(a,b));
```

**Output**

```
2
```

Because:

```
a[2] = 3b[2] = 5
```

---

# Summary Table

|Method|Purpose|
|---|---|
|`arr.length`|Get size of array|
|`Arrays.toString()`|Print 1D array|
|`Arrays.deepToString()`|Print 2D array|
|`Arrays.sort()`|Sort array|
|`Arrays.binarySearch()`|Search element|
|`Arrays.equals()`|Compare 1D arrays|
|`Arrays.deepEquals()`|Compare 2D arrays|
|`Arrays.fill()`|Fill with same value|
|`Arrays.copyOf()`|Copy array|
|`Arrays.copyOfRange()`|Copy part of array|
|`Arrays.stream()`|Create stream|
|`Arrays.asList()`|Convert to List|
|`Arrays.compare()`|Lexicographical compare|
|`Arrays.mismatch()`|Find first mismatch|