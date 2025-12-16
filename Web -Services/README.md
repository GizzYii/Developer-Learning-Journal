# Frontend Web Yol Haritası / Frontend Web Roadmap

| Türkçe | English |
|--------|---------|
| ## 1. Web Temelleri (HTTP & Browser) <br> HTTP / HTTPS <br> Request / Response <br> Status Codes <br> Headers <br> Cookies <br> CORS <br> DevTools (Network tab) <br> 🎯 Amaç: Tarayıcı ve backend iletişimini anlamak | ## 1. Web Fundamentals (HTTP & Browser) <br> HTTP / HTTPS <br> Request / Response <br> Status Codes <br> Headers <br> Cookies <br> CORS <br> DevTools (Network tab) <br> 🎯 Goal: Understand how the browser communicates with the backend |
| ## 2. REST API (En Önemli) <br> GET / POST / PUT / DELETE <br> JSON veri formatı <br> Auth (Token / Cookie) <br> Hata yönetimi <br> Pagination & filtering <br> 🎯 Amaç: Backend’den gelen veriyi UI’da göstermek | ## 2. REST API (Most Important) <br> GET / POST / PUT / DELETE <br> JSON data format <br> Authentication (Token / Cookie) <br> Error handling <br> Pagination & filtering <br> 🎯 Goal: Fetch data from the backend and render it in the UI |
| ## 3. State Management <br> Local state <br> Global state <br> Server state (cache vs state) <br> 🎯 Amaç: Verinin nerede tutulacağını bilmek | ## 3. State Management <br> Local state <br> Global state <br> Server state (cache vs state) <br> 🎯 Goal: Decide where data should live and how it should be managed |
| ## 4. Dokümantasyon & Test <br> API dokümanı okuma <br> Swagger / OpenAPI <br> Postman <br> 🎯 Amaç: Backend hazır mı anlamak | ## 4. Documentation & Testing <br> Reading API documentation <br> Swagger / OpenAPI <br> Postman <br> 🎯 Goal: Understand how to consume an API before writing UI code |
| ## 5. WebSocket (Gerçek Zamanlı) <br> Sürekli açık bağlantı <br> Anlık veri akışı <br> Kullanım: Chat, Live bildirim, Dashboard <br> 🎯 Amaç: UI’yi anlık güncellemek | ## 5. WebSocket (Real-Time Communication) <br> Persistent connection <br> Real-time data flow <br> Use: Chat, Live notifications, Dashboard <br> 🎯 Goal: Build UIs that update instantly |
| ## 6. Webhook (Kavram) <br> Backend → Backend <br> Örnek: Ödeme, Sipariş <br> Frontend değişimi REST veya WS ile alır <br> 🎯 Amaç: UI neden kendiliğinden güncellendiğini anlamak | ## 6. Webhook (Conceptual) <br> Backend → Backend <br> Example: Payment, Order <br> Frontend gets changes via REST or WS <br> 🎯 Goal: Understand why the UI updates automatically |
| ## 7. GraphQL (Opsiyonel) <br> Query / Mutation <br> Tek endpoint <br> 🎯 Amaç: REST yetmediğinde alternatif bilmek | ## 7. GraphQL (Optional) <br> Query / Mutation <br> Single endpoint <br> 🎯 Goal: Know when REST is not enough |
| ## 8. gRPC & SOAP (Sadece Tanı) <br> gRPC = backend ağırlıklı <br> SOAP = legacy <br> 🎯 Amaç: Enterprise projelerde yabancı kalmamak | ## 8. gRPC & SOAP (Awareness) <br> gRPC = backend-oriented <br> SOAP = legacy <br> 🎯 Goal: Avoid confusion in enterprise projects |
| ## 9. Mimariler <br> Monolith <br> Microservices <br> BFF <br> 🎯 Amaç: Frontend neden böyle API alıyor anlamak | ## 9. Architectures <br> Monolith <br> Microservices <br> BFF <br> 🎯 Goal: Understand why frontend receives APIs in certain shapes |

---

## 🔑 Kısa Özet / Quick Summary

- REST API → Sen sorarsın / You request data  
- WebSocket → Sürekli konuşursun / You keep talking  
- Webhook → Sana haber gelir / You get notified  

---

## 🧭 Öğrenme Sırası / Learning Order

```text
Advanced JavaScript
→ Web (HTTP)
→ REST API
→ State Management
→ Docs & Testing
→ WebSocket
→ Webhook (Concept)
→ GraphQL
→ gRPC / SOAP
→ Architecture



# Frontend Web Yol Haritası (Advanced JS Sonrası)

Bu doküman, **ileri seviye JavaScript** bilgisine sahip bir frontend geliştiricinin  
web tarafında **hangi konuyu ne zaman öğrenmesi gerektiğini** sade bir şekilde açıklar.

---

## 1. Web Temelleri (HTTP & Browser)
**Önce bunu öğrenmeden hiçbir yere geçme.**

- HTTP / HTTPS
- Request / Response
- Status Codes
- Headers
- Cookies
- CORS
- Browser DevTools (Network tab)

🎯 Amaç:  
Tarayıcı → Backend iletişimini okuyabilmek.

---

## 2. REST API (EN ÖNEMLİ)
**Frontend’in ana işi budur.**

- GET / POST / PUT / DELETE
- JSON veri yapısı
- Auth (Token / Cookie)
- Error handling
- Pagination & filtering

🎯 Amaç:  
Backend’den gelen veriyi alıp UI’da doğru yönetmek.

> Frontend projelerinin %70–80’i REST API ile çalışır.

---

## 3. State Management
**REST’ten hemen sonra gelir.**

- Local state
- Global state
- Server state (cache vs state farkı)

🎯 Amaç:  
“Bu veri nerede durmalı?” sorusuna doğru cevap verebilmek.

---

## 4. Dokümantasyon & Test
**Gerçek projelerde zorunlu.**

- API dokümanı okuma
- Swagger / OpenAPI
- Postman

🎯 Amaç:  
Backend hazır mı, nasıl kullanılmalı anlayabilmek.

---

## 5. WebSocket (Gerçek Zamanlı İletişim)
**REST yetmediğinde öğrenilir.**

- Sürekli açık bağlantı
- Anlık veri akışı

Kullanım alanları:
- Chat
- Canlı bildirim
- Canlı dashboard

🎯 Amaç:  
“Anlık güncellenen UI” kurabilmek.

---

## 6. Webhook (KAVRAM OLARAK)
**Frontend yazmaz, ama bilmelidir.**

- Backend → Backend tetikleme
- Ödeme alındı
- Sipariş tamamlandı

Frontend bu değişimi:
- REST ile çeker
- veya WebSocket ile anında görür

🎯 Amaç:  
UI neden kendiliğinden güncellendiğini anlamak.

---

## 7. GraphQL (Opsiyonel)
**REST alternatifidir.**

- Query / Mutation
- Tek endpoint mantığı

🎯 Amaç:  
REST yetersiz kaldığında alternatif bilmek.

---

## 8. gRPC & SOAP (Sadece Tanı)
- gRPC: Backend ağırlıklı
- SOAP: Eski sistemler

🎯 Amaç:  
Kurumsal projelerde yabancı kalmamak.

---

## 9. Mimariler (En Son)
- Monolith
- Microservices
- BFF (Backend for Frontend)

🎯 Amaç:  
Frontend’in neden böyle API’ler aldığını anlayabilmek.

---

## 🔑 Kısa Özet

- REST API → **Sen sorarsın**
- WebSocket → **Sürekli konuşursun**
- Webhook → **Sana haber gelir**

---

## 🧭 Net Öğrenme Sırası

```text
Advanced JavaScript
→ Web (HTTP)
→ REST API
→ State Management
→ Docs & Test
→ WebSocket
→ Webhook (mantık)
→ GraphQL
→ gRPC / SOAP
→ Architecture
