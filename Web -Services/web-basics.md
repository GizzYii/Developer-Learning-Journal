# 🌐 WEB BASICS (EN)

## What Is a Protocol?

A **protocol** is a set of rules that defines how computers communicate with each other over a network.

Common protocols:

* HTTP / HTTPS
* FTP
* SMTP
* TCP/IP

> You can find more details about this topic on
> [MDN Web Docs](https://developer.mozilla.org/).

---

## What Is HTTP?

**HTTP (HyperText Transfer Protocol)** is the protocol used for communication between a web browser and a server.

Key characteristics:

* Stateless
* Request / Response based

**HTTPS** is the secure version of HTTP and uses SSL/TLS encryption.

> For more details, see:
> [MDN – HTTP Overview](https://developer.mozilla.org/en-US/docs/Web/HTTP)

---

## What Is HyperText?

**HyperText** is text that contains links, allowing users to navigate between documents on the web.

> Learn more on MDN:
> [MDN – Hypertext](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP)

---

## HTTP Request Structure

An HTTP request typically includes:

* URL
* Request Method
* Headers
* Body (optional)

## HTTP Response Structure

An HTTP response typically includes:

* Status Code
* Headers
* Body

---

## HTTP Methods

Common HTTP request methods:

* **GET** – Retrieve data
* **POST** – Send data
* **PUT** – Update existing data
* **PATCH** – Partially update data
* **DELETE** – Remove data
* **OPTIONS** – Check allowed methods

> Reference:
> [MDN – HTTP Methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)

---

## HTTP Status Codes

HTTP status codes indicate the result of a request.

### Status Code Categories

* **1xx** – Informational
* **2xx** – Success
* **3xx** – Redirection
* **4xx** – Client Errors
* **5xx** – Server Errors

Common examples:

* 200 OK
* 201 Created
* 301 Moved Permanently
* 401 Unauthorized
* 403 Forbidden
* 404 Not Found
* 500 Internal Server Error

> Detailed list:
> [MDN – HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

---

## What Is a MIME Type?

A **MIME type** tells the browser what kind of data the server is sending.

Examples:

* text/html
* application/json
* image/png

> More information:
> [MDN – MIME Types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)

---

## Referer & Referrer Policy

The **Referer** header indicates the page where the request originated.

**Referrer Policy** controls how much referrer information is shared.

Common policies:

* no-referrer
* same-origin
* strict-origin

> Learn more:
> [MDN – Referrer Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy)

---

## What Is a User Agent?

A **User Agent** identifies the browser, operating system, and device making the request.

> Reference:
> [MDN – User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent)

---

## Browser Developer Tools

Modern browsers provide developer tools to inspect web applications.

### Console

* JavaScript errors
* Debug logs

### Network

* HTTP requests and responses
* Status codes
* Headers
* Cookies

### Application / Storage

* Cookies
* LocalStorage
* SessionStorage
* IndexedDB

---

## What Is a Cookie?

A **cookie** is a small piece of data stored in the browser and sent with HTTP requests.

Common uses:

* Authentication
* Session management
* User preferences

> More details:
> [MDN – HTTP Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)

---

## Cookie Lifetime

* **Session Cookie** – Deleted when the browser is closed
* **Persistent Cookie** – Stored until its expiration date

---

## Where Are Cookies Managed?

* Server-side via the `Set-Cookie` response header
* Browser DevTools → Application → Cookies

---

## Cookie Attributes

Important cookie attributes:

* **Secure** – Sent only over HTTPS
* **HttpOnly** – Not accessible via JavaScript
* **Domain** – Specifies the valid domain
* **Path** – Specifies the valid URL path
* **SameSite** – Helps prevent CSRF attacks

---

## What Is IndexedDB?

**IndexedDB** is a low-level API for storing large amounts of structured data in the browser.

Features:

* Asynchronous
* Supports offline usage
* More powerful than LocalStorage

> Reference:
> [MDN – IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)

---

## What Is Chromium?

**Chromium** is an open-source browser engine.

Browsers based on Chromium:

* Google Chrome
* Microsoft Edge
* Brave
* Opera

> Learn more:
> [Chromium Project](https://www.chromium.org/)

