# JavaScript Map & Array – Learning Notes

This document is a structured summary of what I learned about **JavaScript Map**, **Array**, primitive vs reference types, and common Map methods. The goal is not only to learn the syntax, but to understand *why* and *when* each structure is used.

---

## 1️⃣ What is Map?

`Map` is a data structure that works with **key–value pairs**.

### Core Features of Map

* Keys can be **any data type** (number, string, object, array, etc.)
* Preserves insertion order
* Has a `size` property
* Fast `get`, `set`, and `has` operations

```js
const map1 = new Map();
```

---

## 2️⃣ Map Methods

### 🔹 set(key, value)

Adds a new key–value pair to the Map.

```js
map1.set(34, "Istanbul");
map1.set(35, "Izmir");
map1.set(6, "Ankara");
map1.set(1, "Adana");
```

---

### 🔹 get(key)

Returns the value associated with the given key.

```js
map1.get(34); // "Istanbul"
```

---

### 🔹 size

Returns the number of elements in the Map.

```js
map1.size; // 4
```

---

### 🔹 delete(key)

Removes an element from the Map.

```js
map1.delete(34); // true
```

---

### 🔹 has(key)

Checks whether the Map contains the given key.

```js
map1.has(35); // true
map1.has(88); // false
```

---

## 3️⃣ Iterating Over a Map

### 🔹 Using for...of

```js
for (let [key, value] of map1) {
  console.log(key, value);
}
```

```js
for (let key of map1.keys()) {
  console.log(key);
}
```

```js
for (let value of map1.values()) {
  console.log(value);
}
```

---

### 🔹 keys() + Array.from + forEach

```js
const keys = Array.from(map1.keys());

keys.forEach(key => {
  console.log(key, map1.get(key));
});
```

➡️ `keys()` returns only keys. Values are accessed using `get(key)`.

---

## 4️⃣ Converting Map → Array

Maps are often converted to arrays for data processing.

```js
const array = Array.from(map1);
```

Resulting structure:

```js
[
  [34, "Istanbul"],
  [35, "Izmir"],
  [6, "Ankara"],
  [1, "Adana"]
]
```

```js
array.forEach(([key, value]) => {
  console.log(key, value);
});
```

---

## 5️⃣ Converting Array → Map

```js
const array2 = [
  [34, "Istanbul"],
  [35, "Izmir"],
  [6, "Ankara"],
  [1, "Adana"],
];

const mapFromArray = new Map(array2);
```

---

## 6️⃣ Primitive vs Reference Types (VERY IMPORTANT)

### 🔹 Primitive Types

* number, string, boolean, null, undefined
* Compared **by value**

```js
map1.set(34, "Istanbul");
map1.get(34); // works
```

---

### 🔹 Reference Types

* object, array, function
* Compared **by memory reference**

```js
const obj1 = { id: 1 };
const obj2 = { id: 1 };

map1.set(obj1, "Data");

map1.get(obj1); // "Data"
map1.get(obj2); // undefined ❌
```

❗ Same content does NOT mean same reference.

---

### 🔹 Common Mistake

```js
map1.set({ id: 1 }, "Ankara");
map1.get({ id: 1 }); // undefined
```

### ✔️ Correct Usage

```js
const key = { id: 1 };
map1.set(key, "Ankara");
map1.get(key); // works
```

---

## 7️⃣ When to Use Map vs Array

| Purpose                | Best Choice |
| ---------------------- | ----------- |
| Listing data           | Array       |
| filter / map / reduce  | Array       |
| Key–Value relationship | Map         |
| Fast lookup            | Map         |
| UI rendering (React)   | Array       |

---

## 🔥 Key Takeaway

> **Map is powerful for storing data, Array is powerful for processing data.**
> **Primitive keys match by value**
> **Reference keys match by memory address**

Understanding this makes Map, Array, and their conversions much clearer.
