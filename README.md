# devops-lab1-portfolio
Lab 1 – DevOps Course: My First CI/CD Pipeline

- **Họ và tên:** Lang Thị Khánh Ly
- **Mã sinh viên:** dtc235320165
- **Lớp:** KTPM K22C

---

## 4.1 BẢNG SO SÁNH CÁCH LÀM THỦ CÔNG VS DEVOPS

| Tiêu chí | Cách THỦ CÔNG (Traditional) | Cách DEVOPS (CI/CD Pipeline) |
| :--- | :--- | :--- |
| **Làm sao để deploy?** | Upload/copy file thủ công lên server (dùng FTP/SSH) | Push code lên GitHub → pipeline tự chạy |
| **Mất bao lâu?** | 15 – 30 phút | ~10 giây |
| **Ai làm deploy?** | Con người tự làm bằng tay | GitHub Actions (máy tự làm) |
| **Có bị sai sót không?** | Có — sai sót, dễ nhầm file, thiếu bước | Không — pipeline nhất quán 100% |
| **Rollback nếu lỗi?** | Tìm file cũ rồi upload đè lại bằng tay | `git revert` + push → tự động rollback |
| **Làm sao biết deploy thành công?** | Tự mở trình duyệt F5 kiểm tra xem có hiển thị lên không | GitHub Actions gửi notification ✅/❌ |
