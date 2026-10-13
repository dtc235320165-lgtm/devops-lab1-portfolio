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

---

---

## 4.2 SƠ ĐỒ QUY TRÌNH DEVOPS WORKFLOW: TRẢI NGHIỆM ĐẦU TIÊN CỦA SINH VIÊN

```mermaid
graph LR
    A["1. PLAN<br/>Lên kế hoạch làm Lab 1"] --> B["2. CODE<br/>Viết HTML & dùng Git"]
    B --> C["3. PUSH CODE<br/>Gõ git push lên GitHub"]
    C --> D{"4. KIỂM TRA<br/>GitHub Actions running..."}
    D -- "Lỗi ❌" --> B
    D -- "Thành công ✅" --> E["5. BUILD & TEST<br/>Validate thành công"]
    E --> F["6. DEPLOY<br/>Triển khai lên GitHub Pages"]
    F --> G["7. MONITOR<br/>Xem log xanh ở tab Actions"]
    G -. "Tự động lặp" .-> A
    G -. Tự động lặp .-> A

---

## **4.3 TRẢ LỜI CÂU HỎI THU HOẠCH**

1. **DevOps workflow tự động hóa những bước nào mà cách thủ công phải làm bằng tay?**
   - Tự động hóa toàn bộ quy trình kiểm tra mã nguồn (Test/Validate HTML), đóng gói (Build) và triển khai (Deploy) trang web lên GitHub Pages ngay lập tức mỗi khi gõ lệnh `git push`.

2. **Nếu bạn deploy sai (website bị lỗi), làm sao để quay lại phiên bản cũ?**
   - Sử dụng lệnh `git revert <commit-id>` (hoặc `git reset --hard <commit-id>`) rồi `git push` lại. Pipeline CI/CD của GitHub Actions sẽ tự động kích hoạt và deploy bản chạy ổn định cũ lên lại trang web (quy trình Rollback tự động).

3. **GitHub Actions pipeline đã giúp bạn tiết kiệm bao nhiêu thời gian so với cách thủ công?**
   - **Cách thủ công:** Phải tải file, kết nối server qua FTP/SSH, upload file đè lên server rồi cấu hình và mở web test thủ công (mất khoảng 15 – 30 phút).
   - **Cách DevOps:** Chỉ cần gõ lệnh `git push` mất khoảng 10 giây, máy tự động làm hết mọi bước còn lại.
   - $\rightarrow$ **Kết quả:** Tiết kiệm hơn 90% thời gian làm việc.
