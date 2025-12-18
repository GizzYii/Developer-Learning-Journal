# HTTP Methods – Detailed Explanation

HTTP methods describe **what the client (browser, frontend, Postman)** wants to do on the server.  
They form the foundation of **REST APIs** and **web services**.

---

## GET – Retrieve Data
**Purpose:** Retrieve data from the server  
- Does not modify data  
- Read-only operation  

**Example:**
GET /users

**Characteristics:**
- No request body  
- Parameters are sent via URL  
- Cacheable  

**Use Cases:**
- Listing resources  
- Viewing details  
- Search operations  

---

## POST – Create New Data
**Purpose:** Create a new resource on the server  

**Example:**
POST /users

**Body (JSON):**
```json
{
  "name": "Ahmet",
  "email": "ahmet@mail.com"
}
