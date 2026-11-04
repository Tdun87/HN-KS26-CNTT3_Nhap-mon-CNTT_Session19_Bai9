

# Session 19 - Bài 9: Két Sắt Số Bitwarden & Chính Sách Mật Khẩu

### PHẦN 1: BÁO CÁO PHÂN TÍCH

**1. Hiểm họa lưu mật khẩu trên Chrome:**
- Chrome lưu mật khẩu ở tệp `Login Data`.
- Khi dính mã độc Infostealer, nó trích xuất tệp này kèm chốt giải mã, gửi toàn bộ tài khoản/mật khẩu về hacker trong vài giây.

**2. Kiến trúc Zero-Knowledge:**
- Mã hóa/giải mã trực tiếp trên máy cá nhân bằng AES-256.
- Server Bitwarden bị hack cũng chỉ thu được bản mã vô nghĩa. Vì Bitwarden không giữ Master Passphrase nên không thể giải mã dữ liệu của PixelForge Studio.

---

### PHẦN 2: CHÍNH SÁCH & CHUYỂN ĐỔI

**3. Master Passphrase chuẩn:**
- Ghép 4-5 từ ngẫu nhiên + ký tự đặc biệt/số.
- Ví dụ: `PixelForge#2026@Dragon#Coffee` (27 ký tự).

**4. Bảng cấu hình Bitwarden Generator:**
- Độ dài: 24 ký tự.
- Bật đủ: Chữ hoa, chữ thường, chữ số, ký tự đặc biệt.
- Tích chọn: *Avoid ambiguous characters* (tránh ký tự dễ nhầm như `1`, `l`, `I`, `0`, `O`).

**5. Cơ chế Auto-fill chống Phishing:**
- Bitwarden đối chiếu chính xác Domain trên URL.
- Nếu vào trang giả mạo (`githúb.com`, `steampowered.xyz`), Bitwarden **không tự động điền**, chặn đứng lừa đảo.

**6. Quy trình lưu Khóa Cấp cứu (Emergency Kit):**
- Xuất file/in bản giấy mã khôi phục (Recovery Code).
- Lưu trong USB bảo mật hoặc két an toàn công ty, chỉ Trưởng nhóm và Trưởng phòng Kỹ thuật nắm quyền mở.
