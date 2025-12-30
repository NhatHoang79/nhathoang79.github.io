---
title: "Bài 4: Xử lý bất đồng bộ với Async/Await trong JS"
date: 2025-12-29
draft: false
tags: ["JavaScript", "Network"]
---

### 1. Tại sao cần Async/Await?
Khi làm việc với mạng, dữ liệu không trả về ngay lập tức. Async/Await giúp chúng ta viết code đợi dữ liệu về mà không làm "đóng băng" trình duyệt.

### 2. Ví dụ Code
```javascript
async function getStudentData() {
    try {
        let response = await fetch('[https://api.example.com/students](https://api.example.com/students)');
        let data = await response.json();
        console.log(data);
    } catch (error) {
        console.error("Lỗi lấy dữ liệu:", error);
    }
}