# Event Loop + Async Flow & JWT Auth Flow

Bu README, **frontend geliştiricilerin en çok zorlandığı iki kritik konuyu** pratik ve bağlantılı şekilde açıklar:

* 🧠 JavaScript **Event Loop & Async Flow**
* 🔐 **JWT Authentication (Auth Flow)**

---

# 🧠 1) JavaScript Event Loop & Async Flow

## Event Loop Nedir?

JavaScript **single-threaded** çalışır. Aynı anda tek iş yapar.
Ama async işlemler sayesinde **bloklanmadan** çalışıyormuş gibi görünür.

Bunu sağlayan mekanizma **Event Loop**’tur.

---

## 🧩 Yapı Taşları

### 1️⃣ Call Stack

* Senkron kodlar burada çalışır
* Stack doluyken başka iş çalışmaz

### 2️⃣ Web APIs (Browser)

* `setTimeout`
* `fetch`
* `setInterval`
* DOM events

### 3️⃣ Callback Queue

* `setTimeout`, `setInterval` callback’leri

### 4️⃣ Microtask Queue

* `Promise.then`
* `async / await`

> ⚠️ **Microtask Queue her zaman önceliklidir**

---

## 🔁 Çalışma Sırası

1. Call Stack çalışır
2. Stack boşalır
3. Önce **Microtask Queue** çalışır
4. Sonra **Callback Queue** çalışır

---

## 🧪 Örnek (Çok Sorulan)

```js
console.log('1');

setTimeout(() => console.log('2'), 0);

Promise.resolve().then(() => console.log('3'));

console.log('4');
```

### Çıktı:

```
1
4
3
2
```

---

## async / await Gerçekte Ne Yapar?

```js
async function test() {
  console.log('A');
  await fetch('/api');
  console.log('B');
}
```

* `await` → fonksiyonu **pause eder**
* Alt satırlar **microtask** olarak kuyruğa girer

---

## ⏱️ setTimeout vs Promise

* `Promise.then` → **microtask**
* `setTimeout` → **macrotask**

Bu yüzden Promise her zaman önce çalışır.

---

# 🔐 2) JWT Authentication Flow

## JWT Nedir?

**JSON Web Token**, stateless authentication yöntemidir.

Sunucu session tutmaz, kullanıcıyı **token** ile tanır.

---

## 🧾 JWT Yapısı

```
HEADER.PAYLOAD.SIGNATURE
```

* Header → Algoritma
* Payload → User bilgisi (id, role)
* Signature → Güvenlik imzası

---

## 🔁 Login → Token Flow

1. Kullanıcı login olur
2. Backend **JWT üretir**
3. Frontend token’ı alır
4. Her istekte header’a ekler

```http
Authorization: Bearer <token>
```

---

## 🌐 Frontend Örneği (fetch)

```js
fetch('/api/profile', {
  headers: {
    Authorization: `Bearer ${token}`
  }
});
```

---

## 🚨 Status Code Senaryoları

* **200** → Token geçerli
* **401 Unauthorized** → Token yok / süresi bitmiş
* **403 Forbidden** → Yetki yok

---

## 🔄 Token Süresi Dolarsa (Refresh Flow)

1. Access token biter
2. Refresh token gönderilir
3. Yeni access token alınır
4. İstek tekrar edilir

---

## ⚠️ Güvenlik Notları

* JWT **localStorage**’da risklidir (XSS)
* Tercih: **HttpOnly Cookie**
* Secret key **asla frontend’de olmaz**

---

## 🧠 Event Loop + Auth Bağlantısı

* Token kontrolü async yapılır
* `fetch + await` → microtask
* Auth hataları **catch**’te yakalanır

---

## 📌 Genel Özet

* Event Loop async JS’in kalbidir
* Promise & async/await microtask’tır
* JWT stateless auth çözümüdür
* 401 / 403 farkı kritik bilgidir
* Frontend’de doğru async + auth yönetimi şarttır

Bu README, **frontend mülakat + gerçek proje** için hazırlanmıştır.
