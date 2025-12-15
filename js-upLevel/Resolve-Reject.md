# 🔁 Promise: resolve & reject

Bu doküman JavaScript'te **Promise** yapısında kullanılan `resolve` ve `reject` kavramlarını açıklar.

---

## 📌 Promise Nedir?

`Promise`, asenkron (zamana bağlı) işlemlerin sonucunu temsil eden bir JavaScript nesnesidir.

Bir Promise **3 durumda** olabilir:

* **pending** → İşlem devam ediyor
* **fulfilled** → İşlem başarılı (**resolve**)
* **rejected** → İşlem hatalı (**reject**)

---

## ✅ resolve(value)

Promise'in **başarılı** olduğunu bildirir.

* Promise durumu: `fulfilled`
* Gönderilen değer (`value`) `.then()` veya `await` ile alınır

### Örnek:

```js
const promise = new Promise((resolve, reject) => {
  resolve("İşlem başarılı");
});
```

### Kullanım:

```js
promise.then(result => {
  console.log(result);
});
```

---

## ❌ reject(reason)

Promise'in **hata** ile sonuçlandığını bildirir.

* Promise durumu: `rejected`
* Gönderilen hata (`reason`) `.catch()` veya `try/catch` ile alınır

### Örnek:

```js
const promise = new Promise((resolve, reject) => {
  reject("Bir hata oluştu");
});
```

### Kullanım:

```js
promise.catch(error => {
  console.error(error);
});
```

---

## 🔧 resolve / reject birlikte kullanım

```js
const promise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Başarılı sonuç");
  } else {
    reject("Hatalı sonuç");
  }
});
```

---

## ⚡ async / await ile kullanım

```js
async function run() {
  try {
    const result = await promise; // resolve
    console.log(result);
  } catch (error) {               // reject
    console.error(error);
  }
}
```

---

## 🧠 Özet

| Kavram         | Açıklama                            | Promise Durumu |
| -------------- | ----------------------------------- | -------------- |
| resolve(value) | İşlemin başarılı olduğunu bildirir  | fulfilled      |
| reject(reason) | İşlemin hata ile bittiğini bildirir | rejected       |

---

## 📎 Notlar

* Bir Promise **yalnızca bir kez** resolve veya reject edilir
* `fetch`, `axios`, `setTimeout` gibi asenkron işlemler Promise döndürür
* `async` fonksiyonlar **otomatik olarak Promise döndürür**

---

✍️ Bu README, Promise yapısını temel seviyeden teknik seviyeye kadar anlamak için hazırlanmıştır.
