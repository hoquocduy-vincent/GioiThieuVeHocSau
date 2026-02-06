# Pandas

Notebook này cung cấp giới thiệu toàn diện về thư viện pandas - một công cụ mạnh mẽ để xử lý và phân tích dữ liệu trong Python.

## Nội Dung

### 1. **Series (Chuỗi Dữ Liệu)**
   - Tạo Series từ danh sách và mảng NumPy
   - Thuộc tính của Series: `values`, `index`
   - Truy cập và cắt lát với chỉ số rõ ràng và ngầm định
   - Làm việc với chỉ số kiểu từ điển
   - Tạo Series từ từ điển và giá trị vô hướng

### 2. **DataFrames (Bảng Dữ Liệu)**
   - Tạo DataFrame từ từ điển
   - Cấu trúc và thuộc tính của DataFrame
   - Các cách khác nhau để tạo DataFrame (từ Series, danh sách từ điển, mảng NumPy)
   - Quy ước đặt tên cột và hàng

### 3. **Truy Cập, Cắt Lát và Fancy Indexing cho Series**
   - So sánh chỉ số rõ ràng vs. ngầm định
   - Thêm giá trị mới vào Series
   - Sử dụng toán tử `in` và phương thức `.keys()`
   - Mặt nạ (masking) với điều kiện boolean
   - Fancy indexing với nhiều chỉ số
   - Các bộ truy cập `.loc` vs `.iloc`

### 4. **Truy Cập, Cắt Lát và Fancy Indexing cho DataFrame**
   - Truy cập kiểu từ điển và kiểu thuộc tính
   - Kỹ thuật xây dựng tính năng (tạo cột mới)
   - `.iloc` và `.loc` cho truy cập chính xác
   - Kết hợp `.loc` và `.iloc` cho các truy vấn phức tạp
   - Mặt nạ và lọc hàng

### 5. **Broadcasting (Phát Sóng)**
   - Các phép toán broadcasting cơ bản
   - Căn chỉnh chỉ số khi thực hiện phép toán
   - Phép toán giữa DataFrame và Series
   - Sử dụng tham số `fill_value` cho chỉ số bị thiếu

### 6. **Xử Lý Dữ Liệu Bị Thiếu**
   - Hiểu về `np.nan` và `None`
   - Các phương thức: `.isnull()`, `.notnull()`, `.dropna()`, `.fillna()`
   - Xóa cột hoặc hàng với giá trị thiếu
   - Thay thế giá trị thiếu bằng trung bình, trung vị hoặc nội suy
   - Nối DataFrame với tham số axis

### 7. **Gộp Hợp Datasets**
   - Nối các DataFrame với `.concat()`
   - Inner và outer joins
   - Gộp các datasets bằng `.merge()` với cột ID
   - Các loại join khác nhau: inner, outer, left, right

### 8. **Tổng Hợp và GroupBy**
   - Nhóm dữ liệu theo một hoặc nhiều cột
   - Các hàm tổng hợp: `.sum()`, `.mean()`, `.median()`
   - Sử dụng `.aggregate()` cho nhiều phép toán
   - `.filter()` để chọn nhóm theo tiêu chí
   - `.apply()` cho các phép toán tùy chỉnh trên nhóm
   - Lặp lại các đối tượng nhóm

## Bài Tập Thực Hành

### Bài Tập 1: Tải Dữ Liệu và Xử Lý Trước
- Tải dataset `howlongwelive.csv`
- Hiển thị các dòng đầu/cuối và kích thước dataset
- Xóa các cột có nhiều giá trị thiếu
- Mã hóa các biến phân loại (Status)
- Chuẩn bị features (X) và target (y) cho machine learning

### Bài Tập 2: Khám Phá Dữ Liệu và Gộp Hợp
- Xác định và xử lý dữ liệu bị thiếu
- Nhóm dữ liệu theo Quốc gia và Trạng thái
- Phân tích sự khác biệt về tuổi thọ
- Tạo các datasets bổ sung và gộp chúng lại

## Các Tệp
- `Pandas.ipynb` - Code
- `howlongwelive.csv` - Dataset 
- `README.md` - Readme

## Những Điểm Chính
- Pandas Series là mảng 1 chiều có nhãn với truy cập linh hoạt
- DataFrame là bảng 2 chiều với chỉ số hàng và cột linh hoạt
- Sử dụng `.loc` cho truy cập dựa trên nhãn và `.iloc` cho truy cập dựa trên vị trí
- Xử lý dữ liệu bị thiếu một cách thích hợp (xóa, điền hoặc nội suy)
- Nhóm và tổng hợp dữ liệu để có được thông tin chi tiết từ các datasets
- Gộp các datasets để kết hợp thông tin từ nhiều nguồn

## Các Thư Viện Cần Thiết
- Python 3.x
- pandas
- NumPy
- seaborn (cho các datasets ví dụ)
