# 🧼 SOAP & SoapUI – Detailed README

This document explains SOAP and SoapUI in detail.  
Bu doküman SOAP ve SoapUI konularını detaylı şekilde açıklar.

---

## 🧼 SOAP (DETAILED)  
## 🧼 SOAP (DETAYLI ANLATIM)

---

## 📜 SOAP Protocol Explained  
## 📜 SOAP Protokolü Açıklaması

### 🌍 English

| Topic | Explanation |
|------|------------|
| SOAP | Simple Object Access Protocol |
| Data Format | XML only |
| Rules | Very strict and standardized |
| Transport | HTTP, HTTPS, SMTP |
| Security | WS-Security supported |
| Usage Area | Banking, Government, Enterprise |

### 🇹🇷 Türkçe

| Başlık | Açıklama |
|------|----------|
| SOAP | Simple Object Access Protocol |
| Veri Formatı | Sadece XML |
| Kurallar | Çok katı ve standartlı |
| Taşıma | HTTP, HTTPS, SMTP |
| Güvenlik | WS-Security destekler |
| Kullanım Alanı | Bankalar, Devlet, Kurumsal |

---

## 📄 SOAP Message Structure  
## 📄 SOAP Mesaj Yapısı

### 🌍 English

| Element | Description |
|------|------------|
| Envelope | Root element |
| Header | Security & metadata |
| Body | Actual request/response |
| Fault | Error handling |

### 🇹🇷 Türkçe

| Eleman | Açıklama |
|------|----------|
| Envelope | Ana kapsayıcı |
| Header | Güvenlik ve ek bilgiler |
| Body | Asıl istek/cevap |
| Fault | Hata yönetimi |

---

## 🧪 SOAP UI (VERY DETAILED)  
## 🧪 SOAP UI (ÇOK DETAYLI)

---

## 🔧 What is SoapUI?  
## 🔧 SoapUI Nedir?

### 🌍 English

| Feature | Description |
|------|------------|
| Purpose | Testing SOAP & REST APIs |
| WSDL Support | Auto-generate requests |
| Assertions | Validate responses |
| Security Tests | WS-Security, Auth |
| Automation | Test suites & cases |
| Mock Services | Simulate APIs |

### 🇹🇷 Türkçe

| Özellik | Açıklama |
|------|----------|
| Amaç | SOAP & REST API test etmek |
| WSDL Desteği | Otomatik istek oluşturma |
| Assertions | Yanıt doğrulama |
| Güvenlik Testleri | WS-Security, Auth |
| Otomasyon | Test senaryoları |
| Mock Servisler | Sahte API oluşturma |

---

## 🛠 What Can You Do with SoapUI?  
## 🛠 SoapUI ile Neler Yapılır?

### 🌍 English

| Action | Explanation |
|------|-------------|
| Import WSDL | Load service definition |
| Create Request | XML auto-created |
| Add Assertions | Check response correctness |
| Security Test | Add authentication |
| Load Test | Performance testing |

### 🇹🇷 Türkçe

| İşlem | Açıklama |
|------|----------|
| WSDL İçe Aktar | Servis tanımını yükler |
| Request Oluştur | XML otomatik oluşur |
| Assertion Ekle | Yanıt kontrolü |
| Güvenlik Testi | Kimlik doğrulama |
| Yük Testi | Performans ölçümü |

## 📜 WSDL & 🔁 RPC – Detailed Explanation

This section explains WSDL and RPC concepts used in SOAP and distributed systems.  
Bu bölüm SOAP ve dağıtık sistemlerde kullanılan WSDL ve RPC kavramlarını açıklar.

---

## 📜 WSDL (Web Services Description Language)  
## 📜 WSDL (Web Servis Tanımlama Dili)

---

### 🌍 English

| Topic | Explanation |
|------|------------|
| WSDL | XML-based language describing a SOAP service |
| Purpose | Defines how to call a web service |
| File Type | `.wsdl` |
| Contains | Operations, messages, data types |
| Used By | Clients & tools (SoapUI, Postman) |
| Role | Service contract |

---

### 🇹🇷 Türkçe

| Başlık | Açıklama |
|------|----------|
| WSDL | SOAP servisini tanımlayan XML tabanlı dil |
| Amaç | Web servisinin nasıl çağrılacağını tanımlar |
| Dosya Türü | `.wsdl` |
| İçerik | Operasyonlar, mesajlar, veri tipleri |
| Kim Kullanır | Client’lar ve test araçları |
| Rol | Servis sözleşmesi |

---

## 🧩 WSDL İçeriği / WSDL Structure

---

### 🌍 English

| Element | Description |
|------|-------------|
| Types | Data types (XSD) |
| Message | Request & response definitions |
| PortType | Operations (methods) |
| Binding | Protocol & format (SOAP/HTTP) |
| Service | Endpoint URL |

---

### 🇹🇷 Türkçe

| Eleman | Açıklama |
|------|----------|
| Types | Veri tipleri (XSD) |
| Message | Request & response tanımı |
| PortType | Operasyonlar (metotlar) |
| Binding | Protokol ve format |
| Service | Servis adresi (URL) |

---

## 📌 Why WSDL is Important  
## 📌 WSDL Neden Önemlidir?

---

### 🌍 English

| Reason | Explanation |
|------|-------------|
| Auto Generation | Clients can be auto-generated |
| Standardization | Clear service contract |
| Interoperability | Language-independent |
| Tool Support | SoapUI, Java, .NET |

---

### 🇹🇷 Türkçe

| Sebep | Açıklama |
|------|----------|
| Otomatik Kod | Client otomatik üretilir |
| Standart | Net servis sözleşmesi |
| Uyumluluk | Dilden bağımsız |
| Araç Desteği | SoapUI, Java, .NET |

---

## 🔁 RPC (Remote Procedure Call)  
## 🔁 RPC (Uzak Prosedür Çağrısı)

---

### 🌍 English

| Topic | Explanation |
|------|------------|
| RPC | Calling a method on a remote server |
| Logic | Function call over network |
| Focus | Action / method-based |
| Data Style | Parameters & return values |
| Common Use | SOAP RPC style |

---

### 🇹🇷 Türkçe

| Başlık | Açıklama |
|------|----------|
| RPC | Uzak sunucudaki metodu çağırma |
| Mantık | Ağ üzerinden fonksiyon çağrısı |
| Odak | Metot / işlem |
| Veri Yapısı | Parametre ve dönüş değeri |
| Kullanım | SOAP RPC stili |

---

## 🧠 RPC Nasıl Çalışır? / How RPC Works

---

### 🌍 English

| Step | Description |
|------|-------------|
| Client Call | Client calls a function |
| Serialization | Parameters converted to XML |
| Transport | Sent via HTTP |
| Execution | Server executes function |
| Response | Result returned |

---

### 🇹🇷 Türkçe

| Adım | Açıklama |
|------|----------|
| Client Çağrı | Metot çağrılır |
| Serileştirme | Parametreler XML’e çevrilir |
| Taşıma | HTTP ile gönderilir |
| Çalıştırma | Sunucu metodu çalıştırır |
| Yanıt | Sonuç döner |

---

## ⚖️ RPC vs Document Style (SOAP)  
## ⚖️ RPC vs Document Stili (SOAP)

---

### 🌍 English

| Feature | RPC Style | Document Style |
|------|-----------|----------------|
| Focus | Method call | Message |
| Structure | Function-based | XML document |
| Flexibility | Low | High |
| Usage Today | Rare | Recommended |

---

### 🇹🇷 Türkçe

| Özellik | RPC Stili | Document Stili |
|------|-----------|----------------|
| Odak | Metot çağrısı | Mesaj |
| Yapı | Fonksiyon tabanlı | XML belge |
| Esneklik | Düşük | Yüksek |
| Güncel Kullanım | Nadir | Önerilen |

---

## 🎯 Summary / Özet

- **WSDL** → SOAP servisinin sözleşmesidir  
- **RPC** → Uzak metot çağırma yaklaşımıdır  
- **Modern SOAP** → Document-style + WSDL  

- **WSDL** → Ne var, nasıl çağrılır söyler  
- **RPC** → Metot çağırır gibi çalışır  

---

📌 Suitable for SOAP learning & interviews  
📌 SOAP öğrenimi ve mülakatlar için uygundur

---

## 🎯 Summary / Özet

- **SOAP** → Secure, strict, enterprise-level protocol  
- **SoapUI** → Professional SOAP testing tool  
- Commonly used in **banking, government, and corporate systems**

- **SOAP** → Güvenli, katı, kurumsal protokol  
- **SoapUI** → Profesyonel SOAP test aracı  
- **Bankacılık, devlet ve kurumsal sistemlerde yaygın**
- 
