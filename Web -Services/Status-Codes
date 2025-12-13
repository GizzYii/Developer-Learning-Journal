# HTTP Status Codes – Tam Liste (Full README)

Bu doküman, HTTP isteklerine sunucuların verdiği **tüm önemli status code’ları** geliştirici bakış açısıyla açıklar.

---

## 🔵 1xx – Bilgilendirme (Informational)

İstek alındı, işlem devam ediyor.

* **100 Continue** → İstek gövdesi gönderilmeye devam edilebilir
* **101 Switching Protocols** → Protokol değiştirildi (ör: HTTP → WebSocket)
* **102 Processing** → Sunucu isteği işliyor (nadiren kullanılır)

---

## 🟢 2xx – Başarılı (Success)

İstek başarıyla işlendi.

* **200 OK** → İstek başarılı
* **201 Created** → Yeni kaynak oluşturuldu (POST sonrası)
* **202 Accepted** → İstek alındı ama henüz işlenmedi
* **203 Non-Authoritative Information** → Cache üzerinden bilgi
* **204 No Content** → Başarılı ama body yok
* **205 Reset Content** → Form resetlenmeli
* **206 Partial Content** → Kısmi veri döndü (video/stream)

---

## 🟡 3xx – Yönlendirme (Redirection)

Kaynak başka bir yerde.

* **300 Multiple Choices** → Birden fazla seçenek
* **301 Moved Permanently** → Kalıcı yönlendirme
* **302 Found** → Geçici yönlendirme
* **303 See Other** → GET ile başka URL’ye git
* **304 Not Modified** → Cache geçerli
* **307 Temporary Redirect** → Geçici (method değişmez)
* **308 Permanent Redirect** → Kalıcı (method değişmez)

---

## 🔴 4xx – İstemci Hataları (Client Errors)

Hata istemci kaynaklı.

* **400 Bad Request** → Hatalı istek
* **401 Unauthorized** → Kimlik doğrulama yok
* **402 Payment Required** → Rezerve (nadiren kullanılır)
* **403 Forbidden** → Yetki yok
* **404 Not Found** → Kaynak bulunamadı
* **405 Method Not Allowed** → HTTP method hatalı
* **406 Not Acceptable** → Accept header uyumsuz
* **408 Request Timeout** → İstek zaman aşımı
* **409 Conflict** → Veri çakışması
* **410 Gone** → Kaynak kalıcı silindi
* **413 Payload Too Large** → Body çok büyük
* **415 Unsupported Media Type** → Content-Type hatalı
* **418 I'm a teapot** → Easter egg 😄
* **422 Unprocessable Entity** → Validasyon hatası
* **429 Too Many Requests** → Rate limit

---

## ⚫ 5xx – Sunucu Hataları (Server Errors)

Hata sunucu kaynaklı.

* **500 Internal Server Error** → Genel sunucu hatası
* **501 Not Implemented** → Desteklenmeyen özellik
* **502 Bad Gateway** → Proxy / gateway hatası
* **503 Service Unavailable** → Sunucu geçici kapalı
* **504 Gateway Timeout** → Gateway zaman aşımı
* **505 HTTP Version Not Supported** → HTTP versiyonu desteklenmiyor

---

## 🌐 Frontend’de Kullanım Örneği (fetch)

```js
fetch('/api/data')
  .then(res => {
    if (!res.ok) {
      throw new Error(res.status);
    }
    return res.json();
  })
  .then(data => console.log(data))
  .catch(err => console.error('Hata:', err.message));
```

---

## 🔁 HTTP Status Code + Bizim Konuştuklarımız (Bağlantılı Anlatım)

Bu bölüm, seninle **daha önce konuştuğumuz JavaScript ve frontend konuları** ile HTTP status code’ların nasıl birlikte çalıştığını özetler.

---

## 🌐 fetch / async-await ile Status Code Yönetimi

```js
async function veriGetir() {
  try {
    const response = await fetch('/api/data');

    if (!response.ok) {
      // 4xx / 5xx buraya düşer
      throw new Error(`HTTP Error: ${response.status}`);
    }

    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error.message);
  }
}
```

* `response.ok` → 200–299 arası true döner
* 400 / 500 hataları manuel yakalanır

---

## ⏱️ Timeout (İstek Süresi Aşımı)

```js
const controller = new AbortController();

setTimeout(() => {
  controller.abort(); // 408 benzeri senaryo
}, 5000);

fetch('/api/data', { signal: controller.signal })
  .catch(err => console.log('İstek iptal edildi'));
```

* Gerçek 408 genelde server’dan gelir
* Frontend tarafında **AbortController** kullanılır

---

## 🔁 Promise – resolve / reject ilişkisi

* **resolve** → 2xx (başarılı senaryo)
* **reject** → 4xx / 5xx (hata senaryosu)

```js
new Promise((resolve, reject) => {
  if (status === 200) resolve('Başarılı');
  else reject('Hata');
});
```

---

## 🔐 Auth & Status Code’lar (JWT / API)

* **401 Unauthorized** → Token yok / süresi bitmiş
* **403 Forbidden** → Token var ama yetki yok
* **409 Conflict** → Aynı kayıt zaten var
* **429 Too Many Requests** → Rate limit

---

## 🔑 Public / Private API Key Senaryosu

* **Public API key** → Frontend’de olabilir
* **Private / Secret key** → Asla frontend’e konmaz

Yanlış kullanım sonucu:

* 401 / 403 hataları

---

## 🔌 WebSocket & Status Code

* **101 Switching Protocols** → HTTP → WebSocket geçişi
* WebSocket’te klasik HTTP status code akışı yoktur

---

## 📌 Genel Özet

* HTTP status code’lar **API iletişiminin dili**dir
* `fetch`, `async-await`, `Promise`, `AbortController` ile birlikte çalışır
* Frontend geliştirici için 400–500 ayrımı kritiktir
* Auth, rate limit ve timeout senaryoları status code’larla anlaşılır

Bu README, seninle konuştuğumuz konulara göre **frontend odaklı** hazırlanmıştır.
