| English                                                          | Türkçe                                                                     |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Array State is a state value that stores a list of items.        | Array State, bir liste (dizi) tutan state türüdür.                         |
| React tracks array state changes using **reference comparison**. | React, array state değişimini **referans karşılaştırması** ile takip eder. |
| Mutating an array directly does **not trigger a re-render**.     | Bir array’i doğrudan değiştirmek **render tetiklemez**.                    |
| A new array reference must be created to update state.           | State güncellemek için **yeni bir array referansı** oluşturulmalıdır.      |
| Common operations include add, remove, update, and filter.       | Yaygın işlemler: ekleme, silme, güncelleme, filtreleme.                    |
| Array state is commonly used for lists, tables, and dynamic UI.  | Array state; listeler, tablolar ve dinamik UI için kullanılır.             |
| Keys are required when rendering array state elements.           | Array state render edilirken `key` kullanılması zorunludur.                |
| Incorrect updates cause diff algorithm inefficiency.             | Yanlış güncellemeler diff algoritmasını verimsizleştirir.                  |

#⚙️ Table 2: Array State Usage & Patterns (EN / TR + Code)
| English Explanation                                                                         | Türkçe Açıklama ve Kod                                                                                                                      |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Creating Array State**                                                                    | **Array State Oluşturma**                                                                                                                   |
| `jsx\nconst [items, setItems] = useState([]);\n`                                            | `jsx\n// Boş bir dizi ile state oluşturulur\nconst [items, setItems] = useState([]);\n`                                                     |
| **Adding an Item (Immutable)**                                                              | **Eleman Ekleme (Immutable)**                                                                                                               |
| `jsx\nsetItems([...items, newItem]);\n`                                                     | `jsx\n// Yeni bir array oluşturulur\nsetItems([...items, newItem]);\n`                                                                      |
| **Removing an Item**                                                                        | **Eleman Silme**                                                                                                                            |
| `jsx\nsetItems(items.filter(item => item.id !== id));\n`                                    | `jsx\n// Belirli id’ye sahip eleman çıkarılır\nsetItems(items.filter(item => item.id !== id));\n`                                           |
| **Updating an Item**                                                                        | **Eleman Güncelleme**                                                                                                                       |
| `jsx\nsetItems(items.map(item =>\n  item.id === id ? { ...item, done: true } : item\n));\n` | `jsx\n// Sadece ilgili obje kopyalanarak güncellenir\nsetItems(items.map(item =>\n  item.id === id ? { ...item, done: true } : item\n));\n` |
| **Incorrect Mutation (Do Not Do This)**                                                     | **Yanlış Kullanım (Yapma)**                                                                                                                 |
| `jsx\nitems.push(newItem);\nsetItems(items);\n`                                             | `jsx\n// Aynı referans kullanıldığı için React değişimi algılamaz\nitems.push(newItem);\nsetItems(items);\n`                                |
| **Rendering Array State with key**                                                          | **Array State Render Etme**                                                                                                                 |
| `jsx\nitems.map(item => (\n  <Item key={item.id} {...item} />\n));\n`                       | `jsx\n// key benzersiz olmalıdır\nitems.map(item => (\n  <Item key={item.id} {...item} />\n));\n`                                           |
