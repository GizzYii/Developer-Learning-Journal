# 🇹🇷 WEB TEMELLERİ (TR)

Bu konu hakkında daha fazla detayı  
[MDN Web Docs](https://developer.mozilla.org/) üzerinde bulabilirsiniz.


## Protokol Nedir?

Protokol, bilgisayarların birbiriyle **nasıl iletişim kuracağını tanımlayan kurallar bütünüdür**.

Örnek protokoller:

* HTTP / HTTPS
* FTP
* SMTP
* TCP/IP

---

## HTTP Nedir?

**HTTP (HyperText Transfer Protocol)**, tarayıcı ile sunucu arasında veri alışverişi sağlayan protokoldür.

* Stateless’tir (durum tutmaz)
* Request / Response mantığıyla çalışır

HTTPS = HTTP + SSL/TLS (şifreleme)

---

## HyperText Nedir?

Bağlantılar (linkler) içeren metindir. Web’in tıklanabilir olmasını sağlar.

---

## HTTP Request Yapısı

* URL
* Method
* Headers
* Body (opsiyonel)

## HTTP Response Yapısı

* Status Code
* Headers
* Body

---

## HTTP Metotları

* GET → Veri alır
* POST → Veri gönderir
* PUT → Günceller
* PATCH → Kısmi güncelleme
* DELETE → Siler
* OPTIONS → İzin verilen metotlar

---

## HTTP Status Kodları (MDN Referansı)

* 1xx → Bilgilendirme
* 2xx → Başarılı
* 3xx → Yönlendirme
* 4xx → İstemci hatası
* 5xx → Sunucu hatası

Örnekler:

* 200 OK
* 201 Created
* 301 Moved Permanently
* 401 Unauthorized
* 403 Forbidden
* 404 Not Found
* 500 Internal Server Error

---

## MIME Type Nedir?

Sunucunun gönderdiği verinin türünü belirtir.

Örnekler:

* text/html
* application/json
* image/png

---

## Referer & Referrer Policy

Referer, isteğin hangi sayfadan geldiğini gösterir.

Referrer Policy, bu bilginin gönderilip gönderilmeyeceğini kontrol eder.

---

## User Agent Nedir?

Tarayıcının kendini tanıttığı bilgidir.

İçerir:

* Tarayıcı
* İşletim sistemi
* Cihaz türü

---

## Tarayıcı DevTools’ta Nelere Bakılır?

### Console

* JavaScript hataları
* console.log çıktıları

### Network

* HTTP istekleri
* Status code
* Headers
* Cookies

### Application

* Cookies
* LocalStorage
* SessionStorage
* IndexedDB

---

## Cookie Nedir?

Tarayıcıda saklanan küçük veri parçalarıdır.

Kullanım:

* Oturum yönetimi
* Kullanıcı tercihleri

---

## Cookie Hafızası

* Session Cookie → Tarayıcı kapanınca silinir
* Persistent Cookie → Süresi dolana kadar kalır

---

## Cookie Nerede Düzenlenir?

* Response Header: Set-Cookie
* DevTools → Application → Cookies

---

## Cookie Alanları

* Secure → Sadece HTTPS
* HttpOnly → JS erişemez
* Domain → Geçerli domain
* Path → Geçerli yol
* SameSite → CSRF koruması

---

## IndexedDB Nedir?

Tarayıcıda büyük ve yapılandırılmış veri saklamak için kullanılır.

* Asenkron
* Offline destekli

---

## Chromium Nedir?

Açık kaynaklı tarayıcı motorudur.

Kullananlar:

* Chrome
* Edge
* Brave
* Opera

---

