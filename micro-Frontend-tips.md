# How to Build Micro Frontends in React with Vite and Module Federation

## 🧭 Bu Repo Neyi Temsil Ediyor?

Bu repository:

* Bir **merak yolculuğunu**
* Bir **mimari farkındalık egzersizini**
* İleride daha derin çalışmalara zemin hazırlayan bir **not defterini** temsil eder.

Mikro frontend burada bir hedef değil;
**ileride doğru yerde kullanabilmek için öğrenilen bir araçtır.**

---

> Amaç: "Bunu her yerde kullanmalıyım" demek değil,
> "Bunun neden zor ve güçlü olduğunu anlamak".


> **Alıntı / Quote:** *"How to Build Micro Frontends in React with Vite and Module Federation"*
>
> Bu doküman, yukarıdaki başlık referans alınarak hazırlanmış özet ve uygulama rehberidir.

---

## 📌 What is Micro Frontend?

Micro Frontend, büyük frontend uygulamalarını **bağımsız, küçük ve yönetilebilir parçalara** ayırma mimarisidir.
**(EN:** Micro Frontend is an architectural approach that breaks large frontend applications into **independent, small, and manageable pieces**.)

Her parça (micro app) kendi başına geliştirilebilir, test edilebilir ve deploy edilebilir.
**(EN:** Each micro app can be developed, tested, and deployed independently.)

**Avantajlar / Advantages:**

* Bağımsız deploy 🚀 *(EN: Independent deployment)*
* Takım bazlı geliştirme 👥 *(EN: Team-based development)*
* Ölçeklenebilir mimari 📈 *(EN: Scalable architecture)*
* Teknoloji esnekliği *(EN: Technology flexibility)*

---

## ⚙️ Why Vite + Module Federation?

### Vite

* Çok hızlı development server *(EN: Very fast development server)*
* ES module tabanlı *(EN: Built on native ES modules)*
* Modern frontend için ideal *(EN: Ideal for modern frontend development)*

### Module Federation

* Runtime’da modül paylaşımı *(EN: Module sharing at runtime)*
* Uygulamalar arası bağımlılık paylaşımı *(EN: Sharing dependencies between applications)*
* Micro frontend mimarisinin temel taşı *(EN: Core building block of micro frontend architecture)*

---

## 🧱 Architecture Overview

```
Host App (Shell)
 ├── Remote App 1 (Header)
 ├── Remote App 2 (Products)
 └── Remote App 3 (Cart)
```

* **Host (Shell):** Ana uygulama
* **Remote:** Bağımsız micro frontend uygulamaları

---

## 🛠️ Setup: Host Application

### 1️⃣ Create Vite React App

```bash
npm create vite@latest host-app -- --template react
cd host-app
npm install
```

### 2️⃣ Install Module Federation Plugin

```bash
npm install @originjs/vite-plugin-federation
```

### 3️⃣ vite.config.js

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import federation from '@originjs/vite-plugin-federation'

export default defineConfig({
  plugins: [
    react(),
    federation({
      name: 'host',
      remotes: {
        products: 'http://localhost:5001/assets/remoteEntry.js'
      },
      shared: ['react', 'react-dom']
    })
  ]
})
```

---

## 🧩 Setup: Remote Application

### 1️⃣ Create Remote App

```bash
npm create vite@latest products-app -- --template react
cd products-app
npm install
```

### 2️⃣ vite.config.js (Remote)

```js
export default defineConfig({
  plugins: [
    react(),
    federation({
      name: 'products',
      filename: 'remoteEntry.js',
      exposes: {
        './ProductList': './src/ProductList.jsx'
      },
      shared: ['react', 'react-dom']
    })
  ]
})
```

---

## 🔗 Using Remote Component in Host

```js
const ProductList = React.lazy(() => import('products/ProductList'))
```

```jsx
<Suspense fallback={<div>Loading...</div>}>
  <ProductList />
</Suspense>
```

---

## ⚠️ Common Challenges

* Version mismatch (React)
* Shared state management
* Routing (Shell vs Remote)
* Build & deployment uyumu

---

## 🧠 Best Practices

* Shared dependencies’i dikkatli yönetin
* UI/UX tutarlılığı için design system kullanın
* Error Boundary ekleyin
* CI/CD süreçlerini ayırın

---

## 🎯 Conclusion

Micro Frontend mimarisi, özellikle **büyük ve ölçeklenen React projelerinde** güçlü bir çözümdür.
**(EN:** Micro Frontend architecture is a powerful solution, especially for **large and scalable React projects**.)

Vite + Module Federation kombinasyonu, bu yapıyı **modern, hızlı ve sürdürülebilir** hale getirir.
**(EN:** The combination of Vite and Module Federation makes this architecture **modern, fast, and sustainable**.)

---

> **Source / Reference**
>
> This summary is based on the following article from freeCodeCamp:
> *How to Build Micro Frontends in React with Vite and Module Federation*
> [https://www.freecodecamp.org/news/how-to-build-micro-frontends-in-react-with-vite-and-module-federation/](https://www.freecodecamp.org/news/how-to-build-micro-frontends-in-react-with-vite-and-module-federation/)
>
> **Short Summary:**
> This article explains how to build a micro frontend architecture in React using Vite and Module Federation. It demonstrates how a host application can dynamically load remote applications at runtime while sharing dependencies like React. The guide highlights the benefits of independent deployment, better scalability, and faster development through modular frontend design.

---

## 📘 Mikro Frontend Nedir? (Öğrenme Amaçlı Dokümantasyon)

Bu repository, **mikro frontend mimarisine merak duyan ve öğrenme aşamasında olan** geliştiriciler için hazırlanmış bir keşif ve farkındalık dokümantasyonudur. Amaç, mikro frontend’i derin teknik detaylara boğulmadan; **neden var, ne zaman gerekir ve ne zaman gerekmez** sorularına cevap verecek şekilde tanımaktır.

Bu repo, "mikro frontend’i uygulamak"tan çok, **mikro frontend’i anlamaya başlama noktası** olarak konumlandırılmıştır.

---

## 🧠 Mikro Frontend Kısaca Nedir?

Mikro frontend, büyük bir frontend uygulamasını; **bağımsız geliştirilebilen, ayrı ayrı deploy edilebilen ve gerektiğinde runtime’da bir araya gelen** küçük frontend uygulamalarına bölme yaklaşımıdır.

Buradaki temel fikir, klasik modüllendirmeden farklı olarak:

* Sadece kodu değil,
* **Uygulamanın kendisini** modüllere ayırmaktır.

---

## 🧩 Host ve Remote Mantığı (Temel Kavrayış)

* **Host uygulama**: Ana uygulamadır ve diğer uygulamalardan gelen bileşenleri kullanır.
* **Remote uygulama**: Kendi bileşenlerini dışarı açan bağımsız uygulamadır.

En kritik nokta şudur:

> Host, remote uygulamalardan gelen kodları **build time’da değil, runtime’da** yükler.

Bu yaklaşım, uygulamaların birbirinden bağımsız geliştirilmesini ve dağıtılmasını mümkün kılar.

---

## 🎯 Öğrenme Aşamasında Mikro Frontend (%20 Kuralı)

Bu repo, mikro frontend’in **%20’lik öğrenme kısmına** odaklanır.

### Şimdilik Bilmen Yeterli Olanlar:

* Mikro frontend **nedir / ne değildir**
* Monolith vs Micro farkı
* Host / Remote kavramı
* Runtime import fikri
* Neden her projede kullanılmaz

### Şimdilik Derinleşmene Gerek Olmayanlar:

* Karmaşık state paylaşımı
* Production ölçekli konfigürasyonlar
* CI/CD senaryoları
* Versiyon çatışması stratejileri

---


## 📌 Son Not

Mikro frontend öğrenmek, erken aşamada bir zorunluluk değildir.
Ancak bu mimariyi tanımak, geliştiriciyi sadece kod yazan değil;
**neden ve ne zaman karar verileceğini bilen** bir noktaya taşır.

Bu repo da tam olarak bu bakış açısıyla hazırlanmıştır.

