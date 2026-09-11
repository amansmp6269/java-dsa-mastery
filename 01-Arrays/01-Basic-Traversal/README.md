# 📌 Basic Array Traversal

## What is Array Traversal?

Array traversal means visiting each element of an array one by one, usually from left to right.

Example:

```java
int[] arr = {10, 20, 30, 40, 50};

for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

---

## 🔹 Array Indexing

Array indexing starts from `0`.

```text
Index:  0   1   2   3   4
Value: 10  20  30  40  50
```

* First element → `arr[0]`
* Last element → `arr[arr.length - 1]`
* Number of elements → `arr.length`

---

## 🔹 Basic Traversal

```java
for (int i = 0; i < arr.length; i++) {
    // process arr[i]
}
```

### Flow

```text
i = 0
 ↓
process arr[0]
 ↓
i++
 ↓
process arr[1]
 ↓
...
 ↓
process arr[n-1]
```

---

## 🔹 Enhanced For Loop

When the index is not required:

```java
for (int num : arr) {
    // process num
}
```

### Difference

**Normal for loop**

Use when you need:

* Index
* Position
* Modification using index
* Access to neighboring elements

**Enhanced for loop**

Use when you only need:

* Element values

---

## 🔹 Common Operations

### Sum

```java
int sum = 0;

for (int i = 0; i < arr.length; i++) {
    sum += arr[i];
}
```

### Maximum

```java
int max = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
        max = arr[i];
    }
}
```

### Minimum

```java
int min = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] < min) {
        min = arr[i];
    }
}
```

### Counting

```java
int count = 0;

for (int i = 0; i < arr.length; i++) {
    if (arr[i] > 10) {
        count++;
    }
}
```

---

## 🔹 Traversing in Reverse

```java
for (int i = arr.length - 1; i >= 0; i--) {
    System.out.println(arr[i]);
}
```

---

## 🔹 Traversing with a Condition

```java
for (int i = 0; i < arr.length; i++) {
    if (arr[i] % 2 == 0) {
        System.out.println(arr[i]);
    }
}
```

---

## 🔹 Time Complexity

If we visit every element once:

```text
Time: O(n)
```

If we only use a few variables:

```text
Space: O(1)
```

---

## ⚠️ Common Mistakes

### Wrong boundary

```java
i <= arr.length
```

❌ Can cause `ArrayIndexOutOfBoundsException`.

Correct:

```java
i < arr.length
```

### Last index

```java
arr.length - 1
```

Not:

```java
arr.length
```

---

## 🧠 Pattern Recognition

Think **Basic Traversal** when:

* Every element needs to be checked.
* You need to calculate something from all elements.
* You need to count elements.
* You need to find minimum/maximum.
* You need to modify each element.
* No advanced data structure or algorithm is required.

---

## 🎯 Core Template

```java
for (int i = 0; i < arr.length; i++) {

    // process arr[i]

}
```

### Remember

> **Array traversal = visit → process → move to next element.**
