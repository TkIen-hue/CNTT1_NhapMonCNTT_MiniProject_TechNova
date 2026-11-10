# Module 3: Củng cố An toàn Thông tin Cá nhân — Giải thích & Hướng giải quyết

> `security/` — TechNova Onboarding Kit

---

## 1. Password Manager (Bitwarden) làm Digital Vault trung tâm

**Giải thích:** Mỗi tài khoản cần một mật khẩu riêng biệt, vì nếu dùng chung 1 mật khẩu mà một dịch vụ bị lộ dữ liệu, hacker có thể dùng mật khẩu đó để đăng nhập vào toàn bộ tài khoản khác của bạn.Nhớ hàng chục mật khẩu phức tạp rất khó khắn với con người, nên cần công cụ quản lý.

**Hướng giải quyết:** Dùng Bitwarden làm trung tâm - chỉ cần nhớ 1 Master Password mạnh.Với mỗi tài khoản mới, dùng tính năng Generator của Bitwarden để sinh mật khẩu ngẫu nhiên 16–32 ký tự, lưu thẳng vào vault, dùng Autofill để điền thay vì gõ tay hay copy-paste.

---

## 2. Xác thực 2 yếu tố (2FA/TOTP)

**Giải thích:** Mật khẩu dù mạnh vẫn có thể bị lộ.2FA thêm một lớp bảo vệ thứ hai,kể cả khi mật khẩu bị lộ, kẻ gian vẫn cần mã từ thiết bị vật lý của bạn mới đăng nhập được.

**Hướng giải quyết:** Bật 2FA qua Authenticator App cho GitHub và Email công ty,ưu tiên hơn SMS OTP vì SMS có thể bị chiếm đoạt qua SIM swapping. Khi bật xong, hệ thống cấp Backup Codes,lưu ngay vào Bitwarden để phòng khi mất điện thoại.

---

## 3. Nhận diện Phishing, Typosquatting, mã độc Crack

**Giải thích:** Đây là 3 con đường phổ biến nhất khiến tài khoản/máy tính bị xâm nhập: email giả mạo dụ nhập mật khẩu, domain giả gần giống thật,và phần mềm crack/keygen tải lậu thường đi kèm malware.

**Hướng giải quyết:** Luôn kiểm tra kỹ URL trên thanh địa chỉ trước khi đăng nhập, không click link lạ trong email, xác minh qua kênh khác nếu email có vẻ bất thường dù từ người quen, và tuyệt đối không cài phần mềm crack trên máy dùng để làm việc.

---

## 4. Bảo vệ Secrets bằng `.env` + `.gitignore`

**Giải thích:** Nếu API Key/mật khẩu được viết thẳng (hardcode) trong code rồi commit lên GitHub, bất kỳ ai xem được repo (kể cả khi repo bị leak sau này) đều lấy được secrets đó.

**Hướng giải quyết:** Giá trị thật để trong file `.env` (không commit), thêm `.env` vào `.gitignore` **ngay từ commit đầu tiên**, và tạo `.env.example` chỉ liệt kê tên biến để commit cho đồng đội biết cần khai báo gì khi setup dự án.

---

## Quy tắc 5 KHÔNG

1. **KHÔNG** dùng chung 1 mật khẩu cho nhiều tài khoản.
2. **KHÔNG** chọn SMS OTP làm phương thức 2FA chính khi dịch vụ hỗ trợ Authenticator App.
3. **KHÔNG** click link hoặc nhập thông tin đăng nhập từ email/tin nhắn không xác minh được nguồn gốc.
4. **KHÔNG** tải và cài phần mềm crack, keygen, hoặc bản bẻ khoá từ nguồn không chính thức.
5. **KHÔNG** hardcode API Key/mật khẩu trong mã nguồn hoặc commit file `.env` thật lên Git.
