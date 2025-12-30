---
title: "Bài 5: Lập trình mạng UDP với Java"
date: 2025-12-29
draft: false
tags: ["Java", "Network"]
---

### 1. Giao thức UDP là gì?
UDP (User Datagram Protocol) là giao thức không hướng kết nối. Nó gửi dữ liệu nhanh hơn TCP vì không cần bắt tay 3 bước.

### 2. Các lớp chính trong Java
* **DatagramSocket:** Dùng để gửi và nhận gói tin.
* **DatagramPacket:** Là "bao thư" chứa dữ liệu và địa chỉ người nhận.

### 3. Khi nào dùng UDP?
Dùng cho livestream, gọi VoIP hoặc game online nơi mà tốc độ quan trọng hơn việc mất mát một vài gói tin nhỏ.