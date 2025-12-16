# HTTP Request & Response / HTTP İstek ve Yanıt

| **English** | **Türkçe** |
|------------|------------|
| **1. HTTP Request (Client → Server)** | **1. HTTP İsteği (İstemci → Sunucu)** |
| ![HTTP Request](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS9H7KRcmJwkAcDCb2b7zWtC9OqiGR7Ud7SHA&s) | ![HTTP Request](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSzTVHpYrZxQA8cDwycR0YnMDCtCRKlpG9zBw&s) |
| A **Request** is sent by the client (browser, app) to ask the server for some data or action. It includes: <br>• **Method**: GET, POST, PUT, DELETE… <br>• **URL**: The address of the resource <br>• **Headers**: Extra info (like authentication, content-type) <br>• **Body**: Optional data (like form submission) | **İstek (Request)**, istemci (tarayıcı, uygulama) tarafından sunucuya veri almak veya işlem yapmak için gönderilir. İçeriği: <br>• **Method (Metot)**: GET, POST, PUT, DELETE… <br>• **URL**: Kaynağın adresi <br>• **Headers (Başlıklar)**: Ek bilgiler (ör. kimlik doğrulama, içerik tipi) <br>• **Body (Gövde)**: Opsiyonel veri (ör. form gönderimi) |

| **English** | **Türkçe** |
|------------|------------|
| **2. HTTP Response (Server → Client)** | **2. HTTP Yanıtı (Sunucu → İstemci)** |
| ![HTTP Response](https://media.geeksforgeeks.org/wp-content/uploads/20210905094321/StructureOfAHTTPResponse-660x374.png)) | ![HTTP Response](https://media.geeksforgeeks.org/wp-content/uploads/20210905094321/StructureOfAHTTPResponse-660x374.png) |
| A **Response** is what the server sends back to the client after processing the request. It includes: <br>• **Status Code**: 200 OK, 404 Not Found… <br>• **Headers**: Info about the response (content-type, cookies…) <br>• **Body**: The actual data (HTML, JSON, image…) | **Yanıt (Response)**, sunucunun isteği işledikten sonra istemciye gönderdiği bilgidir. İçeriği: <br>• **Durum Kodu (Status Code)**: 200 OK, 404 Not Found… <br>• **Başlıklar (Headers)**: Yanıt hakkında bilgiler (ör. içerik tipi, çerezler…) <br>• **Gövde (Body)**: Asıl veri (HTML, JSON, resim…) |

| **English** | **Türkçe** |
|------------|------------|
| **3. Full Example** | **3. Tam Örnek** |
| **Request:** <br>GET /api/users HTTP/1.1 <br>Host: example.com <br>Authorization: Bearer token123 | **İstek:** <br>GET /api/users HTTP/1.1 <br>Host: example.com <br>Authorization: Bearer token123 |
| **Response:** <br>HTTP/1.1 200 OK <br>Content-Type: application/json <br>Body: { "users": ["Alice","Bob"] } | **Yanıt:** <br>HTTP/1.1 200 OK <br>Content-Type: application/json <br>Gövde: { "users": ["Alice","Bob"] } |

---



**Summary / Özet:**  
- **Request:** The client asks the server for data or action.  
- **Response:** The server sends back the requested data.  

