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
