
## 🧩 Components

Component’ler, React uygulamasının **en temel yapı taşlarıdır**. Her component, ekranın belirli bir bölümünü temsil eder.

Örnekler:

* Button
* Header
* Card
* Form

Bir React uygulaması, birçok component’in birleşmesinden oluşur.

---

## 🚀 Bir React Projesini Ayağa Kaldırmak (create-react-app)

React ile çalışmaya başlamak için hazır bir proje yapısı oluşturmamız gerekir.

```bash
npx create-react-app my-app
cd my-app
npm start
```

Bu komutlar:

* Gerekli React yapılandırmasını otomatik kurar
* Geliştirme sunucusunu başlatır
* Seni React dünyasına hazır hale getirir

---

## 🧠 Component Nedir?

Component, **bir JavaScript fonksiyonudur** ve JSX döndürür.

```jsx
function Hello() {
  return <h1>Merhaba React</h1>
}
```

Her component:

* Kendi sorumluluğuna sahiptir
* Tek bir işi yapmaya odaklanır
* Tekrar kullanılabilir yapıdadır

---

## 🛠️ Component Oluşturmak ve Kullanmak

### Component Oluşturma

```jsx
function Button() {
  return <button>Tıkla</button>
}
```

### Component Kullanma

```jsx
function App() {
  return (
    <div>
      <Button />
    </div>
  )
}
```

---

## 🧾 JSX ve Temel Kuralları

JSX, JavaScript içinde HTML benzeri yazım kullanmamızı sağlar.

Temel kurallar:

* Tek bir kapsayıcı element olmalı
* class yerine **className** kullanılır
* JavaScript ifadeleri `{}` içine yazılır

```jsx
const name = "React"
<h1>Merhaba {name}</h1>
```

---

## 🔢 Component’lerde Değişken Render Etmek

```jsx
function User() {
  const username = "Gizem"
  return <p>Kullanıcı: {username}</p>
}
```

Değişkenler JSX içinde `{}` ile gösterilir.

---

## 🔀 Koşullu Render İşlemi

Koşula göre farklı içerik göstermek mümkündür.

```jsx
function LoginStatus({ isLoggedIn }) {
  return (
    <div>
      {isLoggedIn ? <p>Hoş geldin</p> : <p>Lütfen giriş yap</p>}
    </div>
  )
}
```

---

## ✅ Components – Bölüm Sonu Kazanımları

Bu bölüm sonunda:

* React’in ne olduğunu ve mantığını öğrendin
* Component kavramını anladın
* Component oluşturmayı ve kullanmayı öğrendin
* JSX yazım kurallarını kavradın
* Değişken ve koşullu render işlemlerini uyguladın

> Bu kazanımlar, React öğrenme yolculuğunun **temelini** oluşturur.

---

✨ Bu doküman, React öğrenme sürecinde referans alınmak üzere hazırlanmıştır.
