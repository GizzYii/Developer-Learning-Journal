# JavaScript Map & Array – Öğrenme Notları

Bu doküman, **JavaScript Map**, **Array**, primitive–reference farkı ve Map üzerinde kullanılan temel metotlara dair öğrendiklerimin derli toplu notlarıdır. Amaç; sadece syntax değil, *neden* ve *ne zaman* kullanıldığını anlamaktır.

---

## 1️⃣ Map Nedir?

`Map`, **key–value (anahtar–değer)** mantığıyla çalışan bir veri yapısıdır.

### Map’in Temel Özellikleri

* Key olarak **her veri tipi** kullanılabilir (number, string, object, array…)
* Ekleme sırasını korur
* `size` ile eleman sayısı öğrenilir
* Hızlı `get`, `set`, `has` işlemleri

```js
const map1 = new Map();
```

---

## 2️⃣ Map Metotları

### 🔹 set(key, value)

Map’e eleman ekler.

```js
map1.set(34, "Istanbul");
map1.set(35, "Izmir");
map1.set(6, "Ankara");
map1.set(1, "Adana");
```

---

### 🔹 get(key)

Verilen key’e karşılık gelen değeri döndürür.

```js
map1.get(34); // "Istanbul"
```

---

### 🔹 size

Map içindeki eleman sayısını verir.

```js
map1.size; // 4
```

---

### 🔹 delete(key)

Belirtilen key’i Map’ten siler.

```js
map1.delete(34); // true
```

---

### 🔹 has(key)

Map, verilen key’e sahip mi kontrol eder.

```js
map1.has(35); // true
map1.has(88); // false
```

---

## 3️⃣ Map Üzerinde Dönme (Iteration)

### 🔹 for...of ile

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

➡️ `keys()` sadece anahtarları verir. `get(key)` ile value alınır.

---

## 4️⃣ Map → Array Dönüşümü

Map bazen işlemek için Array’e çevrilir.

```js
const array = Array.from(map1);
```

Ortaya çıkan yapı:

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

## 5️⃣ Array → Map Dönüşümü

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

## 6️⃣ Primitive ve Reference Farkı (ÇOK ÖNEMLİ)

### 🔹 Primitive Tipler

* number, string, boolean, null, undefined
* **Değerle karşılaştırılır**

```js
map1.set(34, "Istanbul");
map1.get(34); // çalışır
```

---

### 🔹 Reference Tipler

* object, array, function
* **Hafızadaki adresle (referansla) karşılaştırılır**

```js
const obj1 = { id: 1 };
const obj2 = { id: 1 };

map1.set(obj1, "Data");

map1.get(obj1); // "Data"
map1.get(obj2); // undefined ❌
```

❗ Aynı içerik ≠ aynı referans

---

### 🔹 Sık Yapılan Hata

```js
map1.set({ id: 1 }, "Ankara");
map1.get({ id: 1 }); // undefined
```

### ✔️ Doğru Kullanım

```js
const key = { id: 1 };
map1.set(key, "Ankara");
map1.get(key); // çalışır
```

---

## 7️⃣ Ne Zaman Map, Ne Zaman Array?

| Amaç                  | Tercih |
| --------------------- | ------ |
| Listeleme             | Array  |
| filter / map / reduce | Array  |
| Key–Value ilişkisi    | Map    |
| Hızlı erişim          | Map    |
| UI render (React)     | Array  |

---

## 🔥 Altın Özet

> **Map saklamak için güçlüdür, Array işlemek için güçlüdür.**
> **Primitive key → değerle eşleşir**
> **Reference key → adresle eşleşir**

Bu mantık anlaşıldığında Map, Array ve dönüşümleri çok daha net hale gelir.
