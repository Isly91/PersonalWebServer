# 🌐 webserv — 42 Codam HTTP Server

Welcome to `webserv`, a custom-built HTTP server developed as part of the 42 Codam curriculum.  
This project dives into the fundamentals of web protocols, socket programming, and server behavior by implementing a simplified, NGINX-like web server **from scratch** in C++.

---

## 📜 Subject Summary

> Implement a fully functional HTTP/1.1 server in C++, capable of handling multiple clients concurrently, parsing requests, responding with correct status codes, serving static files, executing CGI scripts, and reading from a configuration file.

---

## ⚙️ Features

- 🧠 **From-scratch HTTP server in C++**
- 🧵 **Non-blocking I/O** and **multiplexing** (via `poll`)
- 📄 Config file parser (similar to `nginx.conf`)
- 📂 Serving static files and directory listings
- 🔄 Chunked transfer encoding support
- 🖥️ Support for multiple virtual servers & ports
- 🔧 CGI support (e.g., PHP/Python scripts)
- 📥 Methods supported: `GET`, `POST`, `DELETE`
- 🚫 Error pages & status codes (`404`, `403`, etc.)

---

## 🔁 I/O Multiplexing

This project uses the `poll()` system call to handle multiple simultaneous connections in a single-threaded environment. This allows efficient I/O without blocking, providing scalability and responsiveness.

---

## 📂 Configuration File
The server configuration is defined in a custom file format, similar to `nginx.conf`. It allows for defining multiple server blocks, each with its own settings, including:
- Server name
- Listening port
- Root directory
- Index files
- Error pages
- CGI settings
- Location blocks for URL routing
- Access and error logs
- Client body size limits