# 📈 Dự đoán giá Bitcoin dựa trên dữ liệu lịch sử giá Bitcoin

**Sinh viên thực hiện:** Trương Công Duy ,Trần Quốc Huy
**Trường:** Đại học Công nghiệp TP. Hồ Chí Minh – Khoa Công Nghệ Thông Tin

---

## 📌 Bối cảnh

Do giá **Bitcoin** có sự biến động lớn, nhà đầu tư cần một công cụ hỗ trợ dự đoán giá để tối ưu hóa quyết định giao dịch và giảm thiểu rủi ro. Tuy nhiên, các mô hình truyền thống thường gặp hạn chế trong việc nhận diện xu hướng dài hạn, đặc biệt là khi có **các biến động bất thường trên thị trường**.

---

## 🎯 Mục tiêu

1. Phân tích và tiền xử lý dữ liệu Bitcoin (giá, khối lượng, tỷ lệ thay đổi…).
2. Ứng dụng mô hình **LSTM** để dự đoán giá dựa trên dữ liệu 30 ngày trước đó.
3. Đánh giá hiệu suất mô hình bằng các chỉ số như RMSE, MAE.
4. Ứng dụng thực tế, hỗ trợ nhà đầu tư tối ưu quyết định và giảm rủi ro.

---

## 🗃️ Mô tả dữ liệu

- Dữ liệu được lấy từ **Kaggle**, gồm **3.669 hàng × 7 cột**:
  1. `Date`: Ngày giao dịch
  2. `Price`: Giá đóng cửa
  3. `Open`: Giá mở cửa
  4. `High/Low`: Giá cao nhất và thấp nhất trong ngày
  5. `Vol.`: Khối lượng giao dịch
  6. `Change %`: Tỷ lệ thay đổi giá

> Dữ liệu được tiền xử lý (loại bỏ giá trị thiếu, chuẩn hóa) và dùng làm đầu vào cho mô hình **LSTM** để dự đoán xu hướng giá Bitcoin.

---

## 🔁 Mô hình đề xuất

```text
Input → Data Processing → Feature Selection → Tạo dữ liệu sinh → LSTM → Dự đoán giá
