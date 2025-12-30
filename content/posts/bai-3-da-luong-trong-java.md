---
title: "Bài 3: Đa luồng (Multithreading) trong Java"
date: 2025-12-29
draft: false
summary: "Tìm hiểu cách Java xử lý nhiều công việc cùng lúc, một kiến thức quan trọng trong lập trình mạng."
tags: ["Java", "Multithreading"]
---

### 1. Đa luồng là gì?
Đa luồng (Multithreading) là một tính năng của Java cho phép thực hiện đồng thời nhiều phần của một chương trình để tối đa hóa việc sử dụng CPU.

### 2. Tại sao lập trình mạng cần đa luồng?
Trong lập trình Server-Client, Server cần xử lý nhiều kết nối từ nhiều Client cùng một lúc. Nếu không có đa luồng, Server chỉ có thể phục vụ một người dùng tại một thời điểm.

### 3. Cách tạo luồng trong Java
Có hai cách chính để tạo một luồng:
* **Cách 1:** Kế thừa lớp `Thread`.
* **Cách 2:** Triển khai interface `Runnable` (khuyên dùng).

```java
class MyThread implements Runnable {
    public void run() {
        System.out.println("Luồng đang chạy...");
    }
}