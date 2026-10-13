[Vẽ sơ đồ workflow .drawio](https://github.com/user-attachments/files/33396895/V.s.d.workflow.drawio)# devops-lab1-portfolio
Lab 1 – DevOps Course: My First CI/CD Pipeline

- **Họ và tên:** Lang Thị Khánh Ly
- **Mã sinh viên:** dtc235320165
- **Lớp:** KTPM K22C



## 4.1 BẢNG SO SÁNH CÁCH LÀM THỦ CÔNG VS DEVOPS

| Tiêu chí | Cách THỦ CÔNG (Traditional) | Cách DEVOPS (CI/CD Pipeline) |
| :--- | :--- | :--- |
| **Làm sao để deploy?** | Upload/copy file thủ công lên server (dùng FTP/SSH) | Push code lên GitHub → pipeline tự chạy |
| **Mất bao lâu?** | 15 – 30 phút | ~10 giây |
| **Ai làm deploy?** | Con người tự làm bằng tay | GitHub Actions (máy tự làm) |
| **Có bị sai sót không?** | Có — sai sót, dễ nhầm file, thiếu bước | Không — pipeline nhất quán 100% |
| **Rollback nếu lỗi?** | Tìm file cũ rồi upload đè lại bằng tay | `git revert` + push → tự động rollback |
| **Làm sao biết deploy thành công?** | Tự mở trình duyệt F5 kiểm tra xem có hiển thị lên không | GitHub Actions gửi notification ✅/❌ |





## 4.2 SƠ ĐỒ QUY TRÌNH DEVOPS WORKFLOW: TRẢI NGHIỆM ĐẦU TIÊN CỦA SINH VIÊN
[Vẽ sơ đồ workflow .drawio](https://github.com/user-attachments/files/33396995/V.s.d.workflow.drawio)

<mxfile host="app.diagrams.net">
  <diagram name="Trang-1" id="rS6wnoyNf9HwqfumCGjX">
    <mxGraphModel dx="715" dy="396" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-13" edge="1" parent="1" source="XRAg8oFN_3pxmKIKu4ri-1" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=1;entryY=0.5;entryDx=0;entryDy=0;" target="XRAg8oFN_3pxmKIKu4ri-2">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-1" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;" value="&lt;br&gt; 4. TEST&lt;br&gt;• Runner chạy&amp;nbsp;step kiểm tra&amp;nbsp;index.html&amp;nbsp;" vertex="1">
          <mxGeometry height="80" width="80" x="460" y="250" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-17" edge="1" parent="1" source="XRAg8oFN_3pxmKIKu4ri-2" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=1;entryY=0.5;entryDx=0;entryDy=0;" target="XRAg8oFN_3pxmKIKu4ri-15" value="">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="100" y="360" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-2" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;" value="&lt;br&gt;5. DEPLOY&lt;br&gt;• Action gh-pages&amp;nbsp;đẩy lên nhánh&amp;nbsp;gh-pages&lt;div&gt;&lt;br&gt;&lt;/div&gt;" vertex="1">
          <mxGeometry height="80" width="80" x="280" y="240" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-12" edge="1" parent="1" source="XRAg8oFN_3pxmKIKu4ri-3" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0.5;exitY=1;exitDx=0;exitDy=0;" target="XRAg8oFN_3pxmKIKu4ri-1">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-3" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;" value="&lt;br&gt;3. BUILD&lt;br&gt;• Git add/commit&lt;div&gt;&amp;amp; push main&lt;/div&gt;&lt;div&gt;• Trigger GitHub&lt;/div&gt;&lt;div&gt;Actions tự động&lt;/div&gt;" vertex="1">
          <mxGeometry height="90" width="90" x="450" y="80" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-4" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;" value="&lt;br&gt;2. CODE&lt;br&gt;• index.html&lt;br&gt;&lt;div&gt;&lt;span style=&quot;background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));&quot;&gt;•&lt;/span&gt;&lt;span style=&quot;background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));&quot;&gt; &lt;/span&gt;file&amp;nbsp;pipeline ,deploy.yml&lt;/div&gt;" vertex="1">
          <mxGeometry height="80" width="80" x="250" y="90" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-20" edge="1" parent="1" source="XRAg8oFN_3pxmKIKu4ri-5" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=0;entryY=0.5;entryDx=0;entryDy=0;" target="XRAg8oFN_3pxmKIKu4ri-4">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-5" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;" value="1. PLAN&lt;div&gt;làm web&amp;nbsp;portfolio&amp;nbsp;&lt;/div&gt;" vertex="1">
          <mxGeometry height="80" width="80" x="50" y="90" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-15" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;" value="" vertex="1">
          <mxGeometry height="80" width="80" x="80" y="250" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-18" edge="1" parent="1" source="XRAg8oFN_3pxmKIKu4ri-4" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=0.007;entryY=0.617;entryDx=0;entryDy=0;entryPerimeter=0;" target="XRAg8oFN_3pxmKIKu4ri-3">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="XRAg8oFN_3pxmKIKu4ri-19" parent="1" style="text;whiteSpace=wrap;html=1;" value="6. MONITOR&amp;nbsp;&lt;div&gt;• Kiểm tra URL&amp;nbsp;github.io hoạt động&lt;/div&gt;" vertex="1">
          <mxGeometry height="40" width="100" x="80" y="250" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>



## **4.3 TRẢ LỜI CÂU HỎI THU HOẠCH**

1. **DevOps workflow tự động hóa những bước nào mà cách thủ công phải làm bằng tay?**
   - Tự động hóa toàn bộ quy trình kiểm tra mã nguồn (Test/Validate HTML), đóng gói (Build) và triển khai (Deploy) trang web lên GitHub Pages ngay lập tức mỗi khi gõ lệnh `git push`.

2. **Nếu bạn deploy sai (website bị lỗi), làm sao để quay lại phiên bản cũ?**
   - Sử dụng lệnh `git revert <commit-id>` (hoặc `git reset --hard <commit-id>`) rồi `git push` lại. Pipeline CI/CD của GitHub Actions sẽ tự động kích hoạt và deploy bản chạy ổn định cũ lên lại trang web (quy trình Rollback tự động).

3. **GitHub Actions pipeline đã giúp bạn tiết kiệm bao nhiêu thời gian so với cách thủ công?**
   - **Cách thủ công:** Phải tải file, kết nối server qua FTP/SSH, upload file đè lên server rồi cấu hình và mở web test thủ công (mất khoảng 15 – 30 phút).
   - **Cách DevOps:** Chỉ cần gõ lệnh `git push` mất khoảng 10 giây, máy tự động làm hết mọi bước còn lại.
   - $\rightarrow$ **Kết quả:** Tiết kiệm hơn 90% thời gian làm việc.



   
