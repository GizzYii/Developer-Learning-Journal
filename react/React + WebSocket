# React + WebSocket – README

Bu doküman **yalnızca React tarafında WebSocket kullanımını** anlatır. Backend, protokol veya genel network detayları bu dokümana dahil değildir.

---

## 📌 React’te WebSocket Ne İşe Yarar?

React uygulamalarında WebSocket, **UI’ın anlık (real-time) güncellenmesi** gereken durumlarda kullanılır.

Örnek senaryolar:

* Chat mesajlarının anında ekrana düşmesi
* Canlı bildirimler
* Gerçek zamanlı sayaçlar / skorlar
* Canlı veri akışı (fiyat, durum, konum vb.)

---

## 🧠 React Mantığıyla WebSocket

React’te WebSocket kullanırken temel prensipler:

* WebSocket bağlantısı **component mount olduğunda** açılır
* Gelen veriler **useState** ile tutulur
* Bağlantı **component unmount olduğunda** kapatılır
* Yan etkiler için **useEffect** kullanılır

---

## 🔧 Temel React WebSocket Örneği

```jsx
import { useEffect, useState } from "react";

function Chat() {
  const [messages, setMessages] = useState([]);

  useEffect(() => {
    const socket = new WebSocket("ws://localhost:8080");

    socket.onmessage = (event) => {
      setMessages(prev => [...prev, event.data]);
    };

    return () => {
      socket.close();
    };
  }, []);

  return (
    <ul>
      {messages.map((msg, index) => (
        <li key={index}>{msg}</li>
      ))}
    </ul>
  );
}

export default Chat;
```

---

## 🧩 React Hooks Kullanımı

### useEffect

* WebSocket bir **side-effect** olduğu için burada açılır
* Dependency array boş (`[]`) ise sadece bir kez çalışır

### useState

* Sunucudan gelen veriler UI’da gösterilmek için state’te tutulur

---

## 🔑 React’te `key` Kullanımı

WebSocket’ten gelen mesajlar genellikle liste halinde render edilir.

```jsx
{messages.map((msg, index) => (
  <li key={index}>{msg}</li>
))}
```

* `key` React’in listeyi doğru güncellemesi için gereklidir
* Mesaj ID varsa `index` yerine **benzersiz id** kullanılmalıdır

---

## ⚠️ Dikkat Edilmesi Gerekenler (React)

* Component unmount olurken `socket.close()` çağrılmazsa **memory leak** oluşur
* Her render’da yeni WebSocket açılmamalıdır
* State güncellerken önceki state korunmalıdır (`prev => ...`)

---

## ✅ Özet

* WebSocket React’te **gerçek zamanlı UI** için kullanılır
* useEffect → bağlantı yönetimi
* useState → gelen veriyi saklama
* key → liste render optimizasyonu
* Temiz kapatma → performans ve stabilite için şart
