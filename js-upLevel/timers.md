# JavaScript Zamanlayıcılar (Timers)

Bu doküman, JavaScript’te sık kullanılan **zamanlayıcı (timer)** konularını özetlemek için hazırlanmıştır.

---

## ⏱️ setTimeout

### Nedir?

Belirli bir süre sonra **yalnızca 1 kez** çalışan bir zamanlayıcı metodudur.

### Temel Kullanım

```js
setTimeout(() => {
  console.log("1 saniye sonra çalıştım");
}, 1000);
```

### Özellikler

* Tek seferlik çalışır
* Gecikmeli işlem yapmak için kullanılır
* Web API tarafından sağlanır

### Durdurma

```js
const timeoutId = setTimeout(() => {}, 1000);
clearTimeout(timeoutId);
```

---

## 🔁 setInterval

### Nedir?

Belirlenen süre aralığında **tekrar tekrar** çalışan zamanlayıcı metodudur.

### Temel Kullanım

```js
setInterval(() => {
  console.log("Her 1 saniyede bir çalışıyorum");
}, 1000);
```

### Özellikler

* Sürekli çalışır
* Manuel olarak durdurulmazsa devam eder
* Sayaç, canlı veri yenileme gibi yerlerde kullanılır

### Durdurma

```js
const intervalId = setInterval(() => {}, 1000);
clearInterval(intervalId);
```

---

## 🆕 Güncellik Durumu

* `setTimeout` ve `setInterval` **günceldir**
* Modern tarayıcıların tamamında desteklenir
* Node.js ortamında da kullanılabilir
* Deprecated değildir

---

## ⚙️ Bunlar Nedir? (Metot mu?)

* Evet, bunlar **metot / fonksiyon** olarak kullanılır
* JavaScript çekirdeğinin değil, **Web API**’nin parçasıdır
* Tarayıcı tarafından sağlanır ve Event Loop ile çalışır

---

## ⚠️ Alternatif ve İyi Pratikler

### setTimeout Chain (Daha güvenilir tekrar)

```js
function tick() {
  console.log("Zaman kayması daha az");
  setTimeout(tick, 1000);
}
tick();
```

### requestAnimationFrame

* Animasyonlarda `setInterval` yerine tercih edilir

---

## 🧠 Event Loop ile İlişkisi

* `setTimeout` ve `setInterval` **call stack** içinde çalışmaz
* Tarayıcı tarafından **Web API** alanına gönderilir
* Süre dolunca **callback queue**'ya alınır
* Call stack boşsa çalıştırılır

Bu yüzden süre dolsa bile, JavaScript meşgulse çalışması gecikebilir.

---

## ⚛️ React'te Kullanım Örnekleri

### setTimeout (Component içinde)

```js
useEffect(() => {
  const id = setTimeout(() => {
    console.log("Component mount olduktan 1 sn sonra");
  }, 1000);

  return () => clearTimeout(id);
}, []);
```

### setInterval (Sayaç örneği)

```js
useEffect(() => {
  const id = setInterval(() => {
    console.log("Her saniye çalışır");
  }, 1000);

  return () => clearInterval(id);
}, []);
```

> ⚠️ React'te mutlaka **cleanup** yapılmalıdır.

---

## 📌 Özet

* `setTimeout` → Tek seferlik gecikmeli işlem
* `setInterval` → Sürekli tekrar eden işlem
* İkisi de güncel ve Web API tabanlıdır
* Event Loop ile çalışır
* React'te kullanırken temizleme (cleanup) şarttır
