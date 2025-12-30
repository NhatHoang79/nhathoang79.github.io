---
title: "Bài 6: Kỹ thuật Destructuring trong JavaScript ES6"
date: 2025-12-29
draft: false
tags: ["JavaScript"]
---

### 1. Khái niệm
Destructuring cho phép chúng ta "phá vỡ" cấu trúc của Array hoặc Object để lấy giá trị ra một cách nhanh nhất.

### 2. Ứng dụng khi nhận dữ liệu API
Thay vì viết: `let name = user.name; let age = user.age;`
Chúng ta chỉ cần: `const { name, age } = user;`

Điều này giúp code xử lý dữ liệu mạng gọn gàng hơn rất nhiều.