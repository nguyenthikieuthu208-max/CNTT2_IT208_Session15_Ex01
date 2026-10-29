## **Bài 1: Loại bỏ rủi ro lưu trữ cục bộ**

### **Phần 1: Phân tích – Hậu quả của “Thảm họa dữ liệu truyền thống”**

1. **Mất dữ liệu không thể khôi phục:** Ctrl+S ghi đè lên file cũ, không còn bản lịch sử. Máy hỏng, mất hoặc xóa nhầm thì code chỉ nằm trên máy nên mất luôn (single point of failure)  
2. **Xung đột và nhầm lẫn phiên bản:** Các file `code_v1.py`, `main_v2_final.py`... không cho biết bản nào mới nhất, ai sửa gì, sửa lúc nào. Nhiều người cùng sửa dễ ghi đè lên nhau  
3. **Cộng tác kém hiệu quả:** Gửi file qua Zalo thủ công nên mỗi thành viên giữ một bản khác nhau, không đồng bộ, mất thời gian ghép code và dễ phát sinh lỗi.  
4. **Lập luận sai của Nam:** Lưu nhiều bản trên cùng một ổ đĩa không phải là sao lưu (backup). Các bản này vẫn cùng chịu một rủi ro (hỏng ổ, mất máy), và bản “final” bị lưu đè vẫn mất nội dung

### **Phần 2: Quy trình Hybrid Workflow**

1. **Tạo thư mục dùng chung trên Cloud** (Google Drive / OneDrive), chia sẻ cho cả nhóm, đặt tên chuẩn, ví dụ `SmartFood_Code`  
2. **Cài ứng dụng đồng bộ** (Drive for Desktop / OneDrive) và chuyển thư mục `D:\Project` vào thư mục đồng bộ  
3. **Làm việc trên máy cá nhân (Local)** để tốc độ nhanh, không bị chậm máy. Mỗi lần lưu file, Cloud tự động đồng bộ và lưu thành một phiên bản mới  
4. **Chỉ giữ một file duy nhất** là `main.py`, bỏ các file `v1`, `final`. Lịch sử phiên bản do hệ thống quản lý  
5. **Khôi phục bằng 1-click khi lỡ xóa:** Chuột phải vào file → **Version history / Manage versions** → chọn phiên bản trước lúc xóa → **Restore**  
6. **Tạo thói quen:** Đặt tên cho các mốc quan trọng và chia sẻ link thay vì gửi file qua Zalo

