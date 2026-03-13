# Nhận Diện Chữ Số Viết Tay MNIST Với Kiến Trúc CNN

## Tổng quan dự án
Dự án này tập trung vào việc xây dựng, huấn luyện và tối ưu hóa mạng nơ-ron tích chập (**Convolutional Neural Network - CNN**) để phân loại chữ số viết tay từ bộ dữ liệu **MNIST**. Mục tiêu chính là khảo sát sự ảnh hưởng của cấu trúc mạng và các siêu tham số đến hiệu suất mô hình.



## 🛠 Công nghệ sử dụng
* **Framework:** PyTorch
* **Xử lý dữ liệu:** Torchvision
* **Trực quan hóa:** Matplotlib
* **Tính toán số học:** NumPy

## Kiến trúc và Cơ chế hoạt động
Mô hình CNN được thiết kế theo cấu trúc phân tầng để hiểu hình ảnh theo cách con người nhìn nhận:
1.  **Convolutional Layer:** Sử dụng các bộ lọc để trích xuất đặc trưng (cạnh, nét, góc).
2.  **Activation (ReLU):** Áp dụng hàm phi tuyến tính để loại bỏ các giá trị âm, giúp mạng học các mẫu phức tạp.

3.  **Pooling (Max Pooling):** Giảm kích thước ảnh nhưng vẫn giữ lại các thông tin quan trọng nhất, giúp giảm khối lượng tính toán.

4.  **Fully Connected Layer:** Tổng hợp các đặc trưng đã trích xuất để đưa ra dự đoán cuối cùng (0-9).

---

## Nội dung thực nghiệm và Phân tích

### 1. Thay đổi số lượng Epoch (Chu kỳ huấn luyện)
* **Thực hiện:** Tăng số epoch từ 5 lên 10.
* **Kết quả:** Độ chính xác trên tập kiểm tra tăng lên và ổn định hơn.
* **Phân tích:** Việc tăng epoch giúp mô hình có thêm thời gian để tối ưu hóa trọng số. Tuy nhiên, nếu tăng quá mức có thể dẫn đến hiện tượng **Overfitting** (quá khớp).

### 2. Nâng cấp cấu trúc mạng (Thêm tầng Conv3)
* **Thực hiện:** Tích hợp thêm tầng tích chập thứ ba (`conv3`) với 64 bộ lọc.
* **Kết quả:** Mô hình có khả năng học được các đặc trưng trừu tượng và phức tạp hơn.
* **Phân tích:** Việc thêm tầng giúp tăng độ sâu cho mạng, nhưng đòi hỏi phải tính toán lại kích thước tensor ở tầng kết nối đầy đủ (Fully Connected).

### 3. Khảo sát Learning Rate (Tốc độ học)
* **LR = 0.001:** Mô hình học rất chậm, Loss giảm mịn nhưng cần nhiều thời gian để hội tụ.
* **LR = 0.1:** Tốc độ học nhanh nhưng Loss thường xuyên dao động mạnh, dễ vượt qua điểm tối ưu toàn cục.
* **Kết luận:** Learning rate cần được chọn lựa cẩn thận để cân bằng giữa tốc độ và độ ổn định của quá trình huấn luyện.

### 4. Trực quan hóa Feature Maps (Tầng Conv2)
* **Thực hiện:** Trích xuất và hiển thị bản đồ đặc trưng từ tầng tích chập thứ 2.
* **So sánh:**
    * **Conv1:** Thường giữ lại các đường nét cơ bản của chữ số.
    * **Conv2:** Hình ảnh trở nên trừu tượng hơn, tập trung vào các vùng hình khối thay vì các pixel thô.
* **Giải thích:** Điều này minh chứng cho cơ chế học phân tầng của CNN: từ nét vẽ đơn giản đến các hình thái phức tạp.


---

## Kết luận
Qua Lab 5, chúng ta thấy rõ tầm quan trọng của việc tinh chỉnh các siêu tham số. Một mạng CNN tốt không chỉ cần cấu trúc sâu mà còn cần sự cân bằng giữa số lượng vòng lặp huấn luyện và tốc độ cập nhật trọng số phù hợp.

---