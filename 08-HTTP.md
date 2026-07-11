# Hypertext Transfer Protocol (HTTP)

## Introduction

The **Hypertext Transfer Protocol (HTTP)** is an application-layer protocol used for communication between web browsers (clients) and web servers. It enables users to access websites, retrieve web pages, submit forms, and interact with web applications.

HTTP follows a **client-server model**, where the client sends a request to the server, and the server processes the request and returns a response.

Although HTTP is fast and widely supported, it does **not encrypt data**, making it vulnerable to interception. This limitation led to the development of **HTTPS (Hypertext Transfer Protocol Secure)**, which encrypts communication using SSL/TLS.

---

# Why is HTTP Important?

HTTP is the foundation of the World Wide Web. It enables:

- Loading web pages
- Downloading files
- Uploading data
- Accessing web applications
- Communication between browsers and web servers
- API communication

Without HTTP, modern websites and web applications would not function.

---

# How HTTP Works

When a user enters a website address in a browser, the following process occurs:

1. The browser sends an HTTP request to the web server.
2. The server processes the request.
3. The server sends an HTTP response back.
4. The browser displays the webpage.

Example:

```
Browser
    │
HTTP Request
    │
    ▼
Web Server
    │
HTTP Response
    │
    ▼
Browser Displays Website
```

---

# HTTP Communication Process

Suppose you visit:

```
http://example.com
```

The communication process is:

1. Browser checks the DNS cache.
2. DNS resolves the domain name to an IP address.
3. Browser establishes a TCP connection to **Port 80**.
4. Browser sends an HTTP request.
5. Server processes the request.
6. Server returns an HTTP response.
7. Browser displays the webpage.

---

# HTTP Components

Every HTTP communication consists of two main parts:

## HTTP Request

A request is sent from the client to the server.

Example:

```http
GET /index.html HTTP/1.1
Host: example.com
User-Agent: Chrome
Accept: text/html
```

The request contains:

- Request Method
- URL
- HTTP Version
- Headers
- Optional Body

---

## HTTP Response

A response is returned by the server.

Example:

```http
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1500

<html>
...
</html>
```

The response contains:

- Status Code
- Status Message
- Headers
- Response Body

---

# HTTP Methods

HTTP methods define the action that the client wants the server to perform.

| Method | Purpose |
|----------|----------|
| GET | Retrieve data |
| POST | Submit new data |
| PUT | Update existing data |
| DELETE | Remove data |
| PATCH | Partially update data |
| HEAD | Retrieve headers only |
| OPTIONS | Display supported methods |

---

## GET

Retrieves information from the server.

Example:

```
GET /products
```

---

## POST

Sends data to the server.

Example:

```
POST /login
```

Common uses:

- Login forms
- Registration
- File uploads

---

## PUT

Replaces an existing resource.

Example:

```
PUT /users/10
```

---

## PATCH

Updates part of an existing resource.

Example:

```
PATCH /users/10
```

---

## DELETE

Removes a resource.

Example:

```
DELETE /users/10
```

---

# HTTP Status Codes

Status codes indicate the result of a request.

---

## 1xx – Informational

| Code | Meaning |
|------|---------|
|100|Continue|

---

## 2xx – Success

| Code | Meaning |
|------|---------|
|200|OK|
|201|Created|
|204|No Content|

---

## 3xx – Redirection

| Code | Meaning |
|------|---------|
|301|Moved Permanently|
|302|Found|
|304|Not Modified|

---

## 4xx – Client Errors

| Code | Meaning |
|------|---------|
|400|Bad Request|
|401|Unauthorized|
|403|Forbidden|
|404|Not Found|
|405|Method Not Allowed|

---

## 5xx – Server Errors

| Code | Meaning |
|------|---------|
|500|Internal Server Error|
|502|Bad Gateway|
|503|Service Unavailable|
|504|Gateway Timeout|

---

# HTTP Headers

Headers provide additional information about the request or response.

Common request headers:

- Host
- User-Agent
- Accept
- Authorization
- Cookie

Common response headers:

- Content-Type
- Content-Length
- Server
- Cache-Control
- Set-Cookie

---

# Cookies

Cookies are small pieces of data stored by the browser.

They are used for:

- User authentication
- Session management
- Preferences
- Shopping carts

Example:

```
Set-Cookie: SessionID=ABC123
```

---

# HTTP Sessions

HTTP is a **stateless protocol**, meaning each request is treated independently.

To maintain user sessions, websites use:

- Cookies
- Session IDs
- Authentication Tokens

---

# Advantages of HTTP

- Simple
- Fast
- Lightweight
- Widely supported
- Platform independent

---

# Limitations of HTTP

- No encryption
- Vulnerable to eavesdropping
- Data can be modified during transmission
- Does not verify server identity

Because of these limitations, HTTPS is preferred for secure communication.

---

# HTTP vs HTTPS

| Feature | HTTP | HTTPS |
|----------|-------|--------|
|Port|80|443|
|Encryption|No|Yes|
|Security|Low|High|
|SSL/TLS|No|Yes|
|Data Integrity|No|Yes|

---

# Cybersecurity Relevance

HTTP traffic can be intercepted because it is transmitted in plain text.

Common security risks include:

- Packet sniffing
- Session hijacking
- Man-in-the-Middle (MITM) attacks
- Cookie theft
- Credential interception

Security professionals monitor HTTP traffic to:

- Analyze web requests
- Detect malicious activity
- Investigate attacks
- Test web applications
- Identify insecure communications

---

# Real-World Example

Suppose you open:

```
http://example.com
```

Your browser:

1. Resolves the domain using DNS.
2. Opens a TCP connection on Port 80.
3. Sends an HTTP GET request.
4. Receives an HTTP response.
5. Displays the webpage.

If the website uses HTTPS instead, the communication is encrypted before any data is exchanged.

---

# Key Takeaways

- HTTP stands for Hypertext Transfer Protocol.
- It operates at the Application Layer.
- It follows a client-server communication model.
- HTTP uses Port 80 by default.
- It is a stateless protocol.
- Common HTTP methods include GET, POST, PUT, PATCH, and DELETE.
- HTTP does not encrypt data, making it insecure for transmitting sensitive information.

---

# Interview Questions

1. What is HTTP?
2. Which OSI layer does HTTP operate on?
3. What is the default port for HTTP?
4. What is the difference between an HTTP request and an HTTP response?
5. Why is HTTP considered stateless?
6. What are HTTP methods?
7. What is the purpose of cookies?
8. What do HTTP status codes indicate?
9. Why is HTTP considered insecure?
10. What is the difference between HTTP and HTTPS?

---

# Next Topic

➡️ **09-HTTPS.md** – Learn how HTTPS secures web communication using SSL/TLS encryption, digital certificates, and the TLS handshake to protect data from interception and tampering.
