
#(EN)
| Concept                   | Explanation                                                      | Example                                                             |
| ------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------- |
| Object State              | State can be an object to hold multiple related values in React. | `const [user, setUser] = useState({ name: "Gizem", age: 25 });`     |
| Updating Object State     | Must preserve old fields with the spread operator.               | `setUser({ ...user, name: "Ahmet" });`                              |
| Simple Counter            | State can be a number for basic increment/decrement.             | `<button onClick={() => setCount(count + 1)}>+</button>`            |
| Counter with Object State | Store `value` and `step` in one object.                          | `const [counter, setCounter] = useState({ value: 0, step: 1 });`    |
| Increment / Decrement     | Use spread operator to update only `value`.                      | `setCounter({ ...counter, value: counter.value + counter.step });`  |
| Functional Update         | Safe way to update state based on previous value.                | `setCounter(prev => ({ ...prev, value: prev.value + prev.step }));` |


#(TR)
| Kavram                  | Açıklama                                                                            | Örnek                                                               |
| ----------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Object State            | React’te birden fazla ilişkili veriyi tek bir object içinde tutmak için kullanılır. | `const [user, setUser] = useState({ name: "Gizem", age: 25 });`     |
| Object State Güncelleme | Eski alanları korumak için spread operator kullanmak gerekir.                       | `setUser({ ...user, name: "Ahmet" });`                              |
| Basit Sayaç             | Tek bir sayı ile artırma/azaltma yapılabilir.                                       | `<button onClick={() => setCount(count + 1)}>+</button>`            |
| Object State ile Sayaç  | `value` ve `step` değerlerini tek obje içinde tutar.                                | `const [counter, setCounter] = useState({ value: 0, step: 1 });`    |
| Arttırma / Azaltma      | Sadece `value` alanı güncellenir, spread operator kullanılır.                       | `setCounter({ ...counter, value: counter.value + counter.step });`  |
| Functional Update       | Önceki state’e bağlı güncellemeler için güvenli yöntem.                             | `setCounter(prev => ({ ...prev, value: prev.value + prev.step }));` |
