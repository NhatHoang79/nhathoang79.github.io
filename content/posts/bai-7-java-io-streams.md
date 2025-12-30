---
title: "Bài 7: Sử dụng I/O Streams để truyền dữ liệu mạng"
date: 2025-12-29
draft: false
tags: ["Java", "Network"]
---

### 1. Luồng dữ liệu (Stream) là gì?
Trong Java, dữ liệu di chuyển qua mạng theo dạng luồng (Stream). Để gửi dữ liệu đi, ta dùng **OutputStream**, để nhận dữ liệu về, ta dùng **InputStream**.

### 2. Cách dùng BufferedReader và PrintWriter
Đây là hai bộ đệm giúp việc truyền tin nhắn văn bản qua Socket hiệu quả hơn:

```java
// Gửi tin nhắn
PrintWriter out = new PrintWriter(socket.getOutputStream(), true);
out.println("Chào Server!");

// Nhận tin nhắn
BufferedReader in = new BufferedReader(new InputStreamReader(socket.getInputStream()));
String response = in.readLine();