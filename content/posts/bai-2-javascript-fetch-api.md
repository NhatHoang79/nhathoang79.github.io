---
title: "Bài 2: Làm việc với Fetch API trong JavaScript"
date: 2025-12-29
draft: false
summary: "Hướng dẫn cách sử dụng Fetch API để gọi dữ liệu từ Server trong lập trình mạng với JS."
tags: ["JavaScript", "Network"]
---

### 1. Fetch API là gì?
Fetch API là một giao diện hiện đại trong JavaScript dùng để thực hiện các yêu cầu mạng (gọi API) từ phía Client tới Server.

### 2. Ví dụ Code thực tế
```javascript
// Lấy dữ liệu từ một đường dẫn API
fetch('[https://jsonplaceholder.typicode.com/posts/1](https://jsonplaceholder.typicode.com/posts/1)')
  .then(response => response.json())
  .then(json => console.log('Dữ liệu nhận được:', json))
  .catch(err => console.log('Lỗi kết nối:', err));