# 📌 Props Nedir?

**Props (Properties)**, React’te **bileşenler (components) arasında veri taşımak** için kullanılır.  
Bir bileşene **dışarıdan gönderilen**, **salt okunur (read-only)** verilerdir.

> 🔑 Props = “Bileşenin dışarıdan aldığı bilgiler”

---

## 🧠 Props’un Temel Mantığı

- Parent (üst) component → Child (alt) component’e veri gönderir
- Child component props’u **değiştiremez**
- Tek yönlü veri akışı vardır (one-way data flow)

---

## 🧩 Props Nasıl Kullanılır?

### 1️⃣ Parent Component’ten Props Gönderme

```jsx
<User name="Ahmet" age={25} />
