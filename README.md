
---

# AI Code Analyzer & Flowchart Generator

Dự án này là một công cụ phân tích mã nguồn sử dụng AI (Llama 3.3 qua Groq hoặc Qwen 2.5 chạy offline qua Ollama) để tự động tạo Flowchart, giải thích logic và phân tích độ phức tạp thuật toán.

## 👤 Tác giả
* **Nguyễn Đức Minh** - 25521111 - UIT - K20

## 🚀 Tính năng chính
Công cụ cung cấp 3 chế độ phân tích chuyên sâu:
1. **Tạo Mermaid Flowchart:** Chuyển đổi đoạn code của bạn thành sơ đồ quy trình trực quan (định dạng Mermaid).
2. **Phân tích Logic:** Mô tả chi tiết trình tự thực thi, các điều kiện rẽ nhánh và vòng lặp trong code.
3. **Độ phức tạp thuật toán:** Phân tích độ phức tạp về thời gian (Time Complexity - Big O) và không gian (Space Complexity).

## 🛠 Cấu trúc dự án
Dự án bao gồm các thành phần chính sau:
* `Alltools.py`: File xử lý logic AI chính, chứa các Prompt chuyên dụng và trình xử lý kết quả.
* `main.py`: Backend API được xây dựng bằng FastAPI.
* `index.html`: Giao diện người dùng (Frontend) để tương tác trực quan.
* `.env`: Nơi lưu trữ khóa bảo mật API.

## ⚙️ Cài đặt & Sử dụng

### 1. Yêu cầu hệ thống
* Python 3.x
* Ollama (nếu dùng chế độ offline với `qwen2.5-coder:7b`)
* Tài khoản Groq (nếu dùng chế độ online với `llama-3.3-70b-versatile`)

### 2. Cài đặt thư viện
```
pip install requests python-dotenv fastapi uvicorn
```

### 3. Cấu hình API Key
Tạo file `.env` trong thư mục gốc và thêm khóa API của bạn:
```env
GROQ_API_KEY=your_api_key_here
```

### 4. Chạy ứng dụng
Bạn có thể chạy trực tiếp qua Terminal để test logic:
```bash
python Alltools.py
```
Hoặc khởi chạy Backend API:
```bash
python main.py
```

## 🤖 AI Models hỗ trợ
Dự án hỗ trợ linh hoạt giữa hai chế độ:
* **Offline:** Sử dụng `qwen2.5-coder:14b` qua Ollama tại `http://localhost:11434`.
* **Online:** Sử dụng `llama-3.3-70b-versatile` qua Groq Cloud API.

---
