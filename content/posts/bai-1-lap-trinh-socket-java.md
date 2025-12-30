---
title: "Bài 1: Lập trình Socket TCP với Java"
date: '2025-12-29T16:54:28+07:00'
draft: false
summary: "Hướng dẫn cơ bản về cách kết nối Client-Server sử dụng Socket trong ngôn ngữ Java."
tags: ["Java", "Network"]
---

### 1. Khái niệm về Socket
Socket là một phương thức để thiết lập kết nối truyền thông giữa các máy tính với nhau thông qua mạng Internet. Trong Java, Socket giúp chúng ta truyền tải dữ liệu giữa Client và Server một cách dễ dàng.

### 2. Các lớp quan trọng trong Java
Để lập trình mạng, Java cung cấp gói `java.net` với hai lớp chính:
* **ServerSocket:** Dùng cho phía máy chủ (Server) để lắng nghe yêu cầu.
* **Socket:** Dùng cho phía máy khách (Client) để gửi yêu cầu kết nối.

### 3. Ví dụ mã nguồn đơn giản (Server)
```java
import java.net.*;
import java.io.*;

public class SimpleServer {
    public static void main(String[] args) throws IOException {
        ServerSocket server = new ServerSocket(5000);
        System.out.println("Server đang chờ kết nối...");
        Socket socket = server.accept();
        System.out.println("Đã có Client kết nối!");
    }
}