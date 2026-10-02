# Nhật ký tương tác AI (AI Prompt Log)

1. **Lý thuyết tập hợp (Set Theory) về JOIN:**
   - *Prompt:* "Trong cơ sở dữ liệu MySQL, mặc định từ khóa JOIN (khi không ghi rõ LEFT hay RIGHT) sẽ hoạt động như thế nào?"
   - *Kết quả học tập:* Phân biệt được `JOIN` mặc định là `INNER JOIN` (chỉ lấy phần giao nhau của hai tập hợp), từ đó hiểu nguyên nhân vì sao khách hàng chưa mua hàng và sản phẩm chưa bán bị loại bỏ.

2. **Hàm COUNT kết hợp LEFT JOIN:**
   - *Prompt:* "Khi tôi sử dụng LEFT JOIN và đếm số lượng đơn hàng bằng hàm COUNT, tôi nên dùng COUNT() hay COUNT(tên_cột_khóa_chính_bảng_order)? Sự khác biệt khi kết quả trả về NULL là gì?"
   - *Kết quả học tập:* Nắm vững cách hàm `COUNT(column)` bỏ qua giá trị `NULL` để trả về số 0, tránh việc dùng `COUNT(*)` đếm nhầm dòng `NULL`.

3. **Tối ưu hiệu năng Anti-Join:**
   - *Prompt:* "Hãy phân tích hiệu năng của việc dùng LEFT JOIN kết hợp IS NULL so với việc dùng subquery NOT IN khi muốn tìm kiếm các bản ghi không tồn tại trong bảng khác."
   - *Kết quả học tập:* Hiểu cách MySQL tối ưu hóa bằng thuật toán `Left Outer Join / Anti-Join` thông qua cơ chế `Nested-Loop Join` hiệu quả hơn so với xử lý `NOT IN` khi gặp giá trị `NULL`.
