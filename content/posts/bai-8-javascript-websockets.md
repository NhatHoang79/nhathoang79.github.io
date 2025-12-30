---
title: "Bài 8: Kết nối thời gian thực với WebSockets"
date: 2025-12-29
draft: false
tags: ["JavaScript", "Network"]
---

### 1. WebSocket là gì?
Khác với HTTP (Client hỏi - Server trả lời), WebSocket giữ cho kết nối luôn mở. Cả hai bên có thể gửi tin nhắn cho nhau bất cứ lúc nào.

### 2. Ví dụ tạo kết nối WebSocket
```javascript
const socket = new WebSocket('ws://localhost:8080');

// Khi kết nối thành công
socket.onopen = () => {
    socket.send('Chào Server, mình là Client!');
};

// Khi nhận tin nhắn từ Server
socket.onmessage = (event) => {
    console.log('Server nói:', event.data);
};