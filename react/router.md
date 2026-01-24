# React Router – README (EN / TR)

> Two-column explanation for quick reference.
> Hızlı referans için iki sütunlu anlatım.

---

## What is React Router?

| English                                                                                                                                       | Türkçe                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| React Router is a library that enables navigation in single-page React applications by mapping URLs to components without reloading the page. | React Router, tek sayfalı React uygulamalarında sayfa yenilemeden URL’leri component’lerle eşleştiren bir kütüphanedir. |

---

## Exact Prop

| English                                                                                         | Türkçe                                                                                         |
| ----------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| In React Router v5, `exact` ensures that a route only matches when the URL is exactly the same. | React Router v5’te `exact`, route’un sadece tam URL eşleştiğinde çalışmasını sağlar.           |
| In React Router v6, `exact` is removed because all routes are exact by default.                 | React Router v6’da `exact` kaldırılmıştır çünkü tüm route’lar varsayılan olarak exact çalışır. |

---

## URL Parameters

| English                                                          | Türkçe                                                                       |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| URL parameters allow passing dynamic values through the URL.     | URL parametreleri, URL üzerinden dinamik veri taşımayı sağlar.               |
| Commonly used for user profiles, product details, or blog posts. | Kullanıcı profilleri, ürün detayları ve blog yazıları için sıkça kullanılır. |
| Example: `/user/:id`                                             | Örnek: `/user/:id`                                                           |

---

## Nesting (Nested Routes)

| English                                                          | Türkçe                                                                          |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Nested routes allow rendering child routes inside parent routes. | Nested route’lar, bir route’un içinde alt route’ların render edilmesini sağlar. |
| Useful for dashboards, admin panels, and layouts.                | Dashboard, admin panel ve layout yapıları için kullanılır.                      |
| `<Outlet />` is used to render child routes.                     | Alt route’ları göstermek için `<Outlet />` kullanılır.                          |

---

## NavLink

| English                                                          | Türkçe                                                     |
| ---------------------------------------------------------------- | ---------------------------------------------------------- |
| `NavLink` works like `Link` but knows when it is active.         | `NavLink`, `Link` gibidir ama aktif olup olmadığını bilir. |
| It automatically applies an active class when the route matches. | Route eşleştiğinde otomatik olarak aktif class ekler.      |
| Commonly used in navigation menus.                               | Genellikle menü ve navbar’larda kullanılır.                |

---

## No Match (404 Page)

| English                                          | Türkçe                                                   |
| ------------------------------------------------ | -------------------------------------------------------- |
| A No Match route handles URLs that do not exist. | No Match route, tanımlı olmayan URL’leri yakalar.        |
| Implemented using `path="*"` in React Router v6. | React Router v6’da `path="*"` ile uygulanır.             |
| Improves user experience by showing a 404 page.  | 404 sayfası göstererek kullanıcı deneyimini iyileştirir. |

---

## Summary

| English                                                      | Türkçe                                                     |
| ------------------------------------------------------------ | ---------------------------------------------------------- |
| React Router manages navigation in React apps.               | React Router, React uygulamalarında yönlendirmeyi yönetir. |
| It supports dynamic routes, nested routes, and 404 handling. | Dinamik route, nested route ve 404 yönetimini destekler.   |
| Essential for modern single-page applications.               | Modern tek sayfalı uygulamalar için vazgeçilmezdir.        |
