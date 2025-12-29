![React Diff Algorithm Diagram](https://media.geeksforgeeks.org/wp-content/uploads/20241228111254637293/Diffing-Algorithm.jpg)

#Table 1: Conceptual Explanation
| English                                                                   | Türkçe                                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| The Diff Algorithm is part of React’s **reconciliation process**.         | Diff algoritması, React’in **reconciliation (uzlaştırma)** sürecinin bir parçasıdır. |
| React compares the **previous Virtual DOM** with the **new Virtual DOM**. | React, önceki Virtual DOM ile yeni Virtual DOM’u karşılaştırır.                      |
| Only the **minimum number of changes** are applied to the real DOM.       | Gerçek DOM’a sadece **en az gerekli değişiklikler** uygulanır.                       |
| This process improves **performance** significantly.                      | Bu süreç **performansı ciddi şekilde artırır**.                                      |
| Elements are compared **level by level** in the component tree.           | Elemanlar component ağacında **aynı seviyede** karşılaştırılır.                      |
| If an element type changes, React **destroys and recreates** the subtree. | Bir elemanın tipi değişirse React **tüm alt ağacı silip yeniden oluşturur**.         |
| The `key` prop helps React identify elements between renders.             | `key` prop, React’in render’lar arasında elemanları tanımasını sağlar.               |
| Without keys, React may re-render more elements than necessary.           | Key yoksa React gerekenden fazla render yapabilir.                                   |
| Diffing is **automatic**; developers guide it using best practices.       | Diff işlemi **otomatik**tir; geliştirici sadece doğru yönlendirir.                   |


#Table 2: How React Uses Diff Algorithm
| English Explanation                                                 | Türkçe Açıklama ve Kod                                                                                                        |
| ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **State change triggers diffing**                                   | **State değişimi diff sürecini başlatır**                                                                                     |
| `jsx\nsetCount(count + 1);\n`                                       | `jsx\n// setState çağrıldığında React yeni Virtual DOM oluşturur\nsetCount(count + 1);\n`                                     |
| **Virtual DOM is re-created on each render**                        | **Her render’da yeni Virtual DOM oluşturulur**                                                                                |
| `jsx\nfunction Counter({ count }) {\n  return <p>{count}</p>;\n}\n` | `jsx\n// Bu JSX her render’da yeni bir Virtual DOM node üretir\nfunction Counter({ count }) {\n  return <p>{count}</p>;\n}\n` |
| **Diff compares old and new trees**                                 | **Diff eski ve yeni ağaçları karşılaştırır**                                                                                  |
| `txt\nOld: <p>1</p>\nNew: <p>2</p>\n`                               | `txt\n// Sadece text node değiştiği tespit edilir\nEski: <p>1</p>\nYeni: <p>2</p>\n`                                          |
| **Only changed DOM nodes are updated**                              | **Sadece değişen DOM node’ları güncellenir**                                                                                  |
| `txt\nText updated, element preserved\n`                            | `txt\n// <p> silinmez, sadece içeriği güncellenir\n`                                                                          |
| **Keys optimize list diffing**                                      | **Key’ler liste diff’ini optimize eder**                                                                                      |
| `jsx\nitems.map(item => (\n  <Item key={item.id} />\n))\n`          | `jsx\n// React aynı elemanı tanır, yeniden yaratmaz\nitems.map(item => (\n  <Item key={item.id} />\n))\n`                     |
| **Without key, React reorders by index**                            | **Key yoksa React index’e göre karşılaştırır**                                                                                |
| `jsx\nitems.map((item, i) => (\n  <Item key={i} />\n))\n`           | `jsx\n// Elemanlar kayarsa yanlış DOM güncellenir\nitems.map((item, i) => (\n  <Item key={i} />\n))\n`                        |
| **Type change causes full subtree replacement**                     | **Tip değişirse tüm subtree yenilenir**                                                                                       |
| `jsx\n<div /> → <span />\n`                                         | `txt\n// div yerine span gelirse React tüm alt yapıyı siler\n`                                                                |
