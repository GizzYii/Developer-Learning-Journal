# HTTP Metodları – Detaylı Anlatım

HTTP metodları, istemcinin (tarayıcı, frontend, Postman) sunucuya **ne yapmak istediğini** belirtir.  
REST API’lerin ve web servislerinin temelini oluşturur.

## GET – Veri Okuma
**Amaç:** Sunucudan veri almak  
- Veriyi değiştirmez  
- Sadece okuma yapar  

**Örnek:**
GET /users

**Özellikler:**
- Body yoktur  
- Parametreler URL’de taşınır  
- Cache edilebilir  

**Kullanım Alanı:**
- Listeleme  
- Detay görüntüleme  
- Arama işlemleri  

## POST – Yeni Veri Oluşturma
**Amaç:** Sunucuya yeni veri eklemek  

**Örnek:**
POST /users

**Body (JSON):**
{
  "name": "Ahmet",
  "email": "ahmet@mail.com"
}

**Özellikler:**
- Body kullanır  
- URL’de görünmez  
- Genelde 201 Created döner  

**Kullanım Alanı:**
- Kayıt olma  
- Form gönderme  
- Login işlemleri  

## PUT – Tüm Veriyi Güncelleme
**Amaç:** Var olan bir kaydı tamamen güncellemek  

**Örnek:**
PUT /users/5

**Body:**
{
  "name": "Ahmet Yılmaz",
  "email": "ahmety@mail.com"
}

> Eksik alan gönderilirse eski veriler silinebilir.

## PATCH – Kısmi Güncelleme
**Amaç:** Verinin sadece belirli alanlarını güncellemek  

**Örnek:**
PATCH /users/5

**Body:**
{
  "email": "new@mail.com"
}

**Not:** PUT’a göre daha esnek ve güvenlidir.

## DELETE – Veri Silme
**Amaç:** Sunucudan veri silmek  

**Örnek:**
DELETE /users/5

**Başarılı Cevaplar:**
- 200 OK  
- 204 No Content  

## HEAD – Sadece Header Almak
**Amaç:** Kaynağın varlığı ve meta bilgileri  
- Response body yoktur  
- Sadece header döner  

**Kullanım:**
- Dosya var mı?  
- Boyutu nedir?  

## OPTIONS – İzin Verilen Metodlar
**Amaç:** Sunucunun hangi metodlara izin verdiğini öğrenmek  

**Örnek:**
OPTIONS /users

**Response:**
Allow: GET, POST, PUT, DELETE

**Önemli:** CORS işlemlerinde kullanılır.

## HTTP Metodları Karşılaştırma

| Metod | Amaç | Veri Değiştirir mi |
|------|------|------------------|
| GET | Veri al | Hayır |
| POST | Yeni veri ekle | Evet |
| PUT | Tam güncelle | Evet |
| PATCH | Kısmi güncelle | Evet |
| DELETE | Veri sil | Evet |
| HEAD | Header al | Hayır |
| OPTIONS | Yetki sorgula | Hayır |

## Postman ile HTTP Metodları
Postman sayesinde:
- Tüm HTTP metodlarını test edebilirsin  
- Header, Body ve Status Code’ları görebilirsin  
- Frontend gelmeden API davranışını anlayabilirsin  

## Özet
- HTTP metodları istemci–sunucu iletişiminin temelidir  
- REST API’lerin bel kemiğidir  
- Frontend ve backend arasındaki dili oluşturur  
- Postman bu yapıyı öğrenmenin en pratik yoludur  
# HTTP Metot Kavramları ve REST API Temel Terimleri

## SAFE Metotlar
**SAFE metotlar**, sunucunun **state (durum)** bilgisinde herhangi bir değişiklik yapmayan, sadece **okuma (read-only)** amaçlı kullanılan HTTP metotlarıdır.

**SAFE metotlar:**
- GET  
- HEAD  
- OPTIONS  

**Özellikleri:**
- Sunucudaki veriyi değiştirmezler
- Tekrar tekrar çağrılmaları güvenlidir
- Veri okuma ve bilgi alma için kullanılırlar

> Örnek:  
> `GET /users` → Kullanıcıları listeler, veritabanını değiştirmez

---

## IDEMPOTENT Metotlar
**Idempotent metotlar**, aynı isteğin **bir veya birden fazla kez** gönderilmesi durumunda, sunucu **state** yapısında **ek bir yan etki oluşturmayan** metotlardır.

**Idempotent metotlar:**
- GET  
- HEAD  
- OPTIONS  
- PUT  
- DELETE  
- TRACE  

**Özellikleri:**
- Aynı istek tekrarlandığında sonuç değişmez
- Ağ hataları sonrası tekrar denemek güvenlidir
- **Tüm SAFE metotlar idempotent’tır**

> Örnek:  
> `DELETE /users/5`  
> İlk çağrıda silinir, sonraki çağrılarda ek bir etki oluşmaz

---

## SAFE vs IDEMPOTENT Farkı
- **SAFE** → Veri değiştirmez  
- **IDEMPOTENT** → Tekrarlandığında ekstra etki oluşturmaz  

> POST metodu **ne safe ne de idempotent** kabul edilir.

---

## Endpoint (Sorgu Adresi)
**Endpoint**, REST API kullanımında istemcinin gönderdiği istek ile sunucunun verdiği cevabın **buluştuğu adrestir**.

Başka bir deyişle:
> İstemci ile API arasındaki iletişim noktasıdır.

---

## Endpoint Yapısı
Endpoint’ler şu parçalardan oluşur:

- **Root (Base URL)**  
