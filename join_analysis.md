# Giải trình lựa chọn hàm COUNT trong LEFT JOIN

Trong báo cáo của Marketing, việc sử dụng `COUNT(o.order_id)` thay vì `COUNT(*)` là bắt buộc để tính chính xác số lượng đơn hàng của từng khách hàng:

- **`COUNT(o.order_id)`**: Chỉ đếm các giá trị không phải `NULL`. Khi kết hợp với `LEFT JOIN`, những khách hàng chưa mua hàng như Charlie sẽ nhận giá trị `NULL` ở cột `o.order_id`, hàm sẽ trả về kết quả chính xác là `0`.
- **`COUNT(*)`**: Đếm toàn bộ dòng trong nhóm (bao gồm cả dòng chứa giá trị `NULL` được sinh ra từ bảng phụ). Điều này sẽ làm cho khách hàng chưa mua hàng bị tính thành `1` đơn hàng do lỗi đếm dòng, gây sai lệch báo cáo kích cầu.
