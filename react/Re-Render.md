| Concept          | React                                                | jQuery / Vanilla JS                                |
| ---------------- | ---------------------------------------------------- | -------------------------------------------------- |
| State Management | Built-in (`useState`, `useReducer`)                  | None, manual variables                             |
| DOM Update       | Virtual DOM → minimal, efficient updates             | Direct DOM → manual updates                        |
| Re-render        | Automatic at component level when state/props change | No automatic re-render, developer updates manually |
| Performance      | Optimized for large apps                             | Can be slow with large DOM manipulations           |
| Predictability   | More predictable, single source of truth (state)     | Less predictable, prone to event-handling bugs     |
| UI Logic         | UI = function(state, props)                          | UI = developer responsibility                      |


| Kavram           | React                                                   | jQuery / Vanilla JS                                     |
| ---------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| State Yönetimi   | Dahili (`useState`, `useReducer`)                       | Yok, manuel değişkenler                                 |
| DOM Güncelleme   | Virtual DOM → minimal ve hızlı güncellemeler            | Direkt DOM → manuel güncelleme                          |
| Re-render        | State veya props değişince otomatik component re-render | Otomatik yok, developer manuel update yapar             |
| Performans       | Büyük uygulamalarda optimize                            | Büyük DOM manipülasyonlarında yavaşlayabilir            |
| Öngörülebilirlik | Daha öngörülebilir, tek kaynak: state                   | Daha az öngörülebilir, eventlere bağlı hatalar olabilir |
| UI Mantığı       | UI = function(state, props)                             | UI = developer sorumluluğu                              |
