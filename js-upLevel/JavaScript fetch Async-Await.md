# JavaScript Fetch & Async/Await – README

Bu doküman, **fetch**, **response**, **response.json()**, **çift await kullanımı** ve **async function** kavramlarını açıklar.

---

## 1️⃣ `response.json()` Nedir?

`response.json()` sunucudan gelen HTTP cevabının **body (gövde)** kısmını alır ve **JSON → JavaScript objesine** çevirir.

### 📌 Özellikler

* Asenkron çalışır
* Promise döndürür
* Genelde `fetch` sonrası kullanılır

### 📄 Örnek

```js
fetch('/api/users')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

## 2️⃣ `response` Hangi Durumlarda Gereklidir?

`response`, fetch isteğinden dönen **ham HTTP cevabıdır**.

### Kullanım Amaçları

#### ✅ 1. İstek başarılı mı kontrol etmek

```js
if (!response.ok) {
  console.log(response.status);
}
```

#### ✅ 2. Veriyi almak

```js
const data = await response.json();
```

#### ✅ 3. Header bilgilerini okumak

```js
response.headers.get('Content-Type');
```

#### ✅ 4. Farklı veri tipleri almak

* JSON → `response.json()`
* Metin → `response.text()`
* Dosya → `response.blob()`

---

## 3️⃣ Neden 2 Tane `await` Kullanılır?

```js
const users = await (await fetch(url)).json();
```

Çünkü **iki ayrı Promise vardır**:

1. `fetch(url)` → Response döndürür (Promise)
2. `response.json()` → Veriyi döndürür (Promise)

### Daha Okunabilir Hali

```js
const response = await fetch(url);
const users = await response.json();
```

---

## 4️⃣ `async function` Sadece Gerektiğinde mi Kullanılır?

### ✔ `async` GEREKLİDİR eğer:

* Fonksiyon içinde `await` varsa
* Promise dönen bir işlem kullanılıyorsa

```js
async function getData() {
  const res = await fetch('/api');
}
```

### ❌ `async` GEREKSİZDİR eğer:

* İçeride `await` yoksa
* Sadece senkron işlemler varsa

```js
function sum(a, b) {
  return a + b;
}
```

### ⚠ Not

`async` yazılan her fonksiyon otomatik olarak **Promise döndürür**.

---

## 📌 Kısa Özet

* `fetch` → Response getirir
* `response.json()` → Veriyi JS objesine çevirir
* 2 `await` → 2 ayrı Promise olduğu için
* `async` → Sadece `await` varsa kullanılmalı

---

🚀 Bu README, frontend geliştirme sürecinde fetch ve async/await kullanımını anlamak için hazırlanmıştır.
