# Thiết Lập Trình Duyệt Chuyên Nghiệp

## 1. Nguyên lý Data Isolation
- Thiết lập tối thiểu **2 Browser Profile** độc lập:
  1. `Personal`: Dành cho giải trí, mạng xã hội cá nhân.
  2. `TechNova_Work`: Dành riêng cho công việc, email công ty, dự án.
> **Bẫy Trình Duyệt:** KHÔNG dùng chung 1 Profile cho cá nhân và công việc. Việc này giúp tránh nhầm lẫn tài khoản, lọt rò rỉ lịch sử duyệt web và tách biệt Cookies/Session.

## 2. Quản lý Bookmark Manager
Tổ chức thanh dấu trang gọn gàng theo 3 thư mục:
- `01_Work_Dev`: Các tài liệu kỹ thuật, API docs, GitHub Repo.
- `02_Onboarding_Docs`: Sổ tay nhân viên, chính sách, tài liệu đào tạo.
- `03_Tools`: Jira, Figma, Lark, AWS Console.

## 3. Bộ Extension Khuyên Dùng
Giới hạn quyền Site Access ở chế độ **On click** (chỉ cấp quyền khi click vào tiện ích).
- **Dev Suite:** React Developer Tools, Wappalyzer.
- **Productivity Suite:** Grammarly, Todoist.
- **Security Suite:** Bitwarden, uBlock Origin.

## 4. Thao tác DevTools (F12) Cơ Bản
- Dùng `Inspect Element` để kiểm tra CSS/HTML.
- Tab `Application` để phân biệt và quản lý **Cache** và **Cookies**.
- **Lưu ý:** Luôn thực hiện **Hard Reload** (`Ctrl + Shift + R` hoặc click chuột phải vào nút Refresh chọn *Empty Cache and Hard Reload* khi bật F12) trước khi kết luận giao diện bị lỗi để đảm bảo kiểm tra trên bản mã mới nhất.
