## Hướng dẫn thực thi các file có trong thư mục

### Bước 1: Mở [Google Colab](https://colab.research.google.com/)
### Bước 2: Chọn mục `Upload` > `Browse` > Chọn file cần thực thi
### Bước 3: Chọn `Run all` để thực thi toàn bộ file notebook.
- Đối với file `Overview.ipynb`: file chứa góc nhìn khái quát về tập dữ liệu.
- Đối với file `EDA.ipynb`: file chứa những phân tích, khám phá, trực quan hóa chuyên sâu hơn về tập dữ liệu.
- Đối với file `Preprocess.ipynb`: file chứa những thao tác tiền xử lý tập dữ liệu, chọn lọc những đặc trưng dựa trên những phân tích trước đó.
### <u>Lưu ý</u>:
- Dữ liệu sau khi được tiền xử lý trong file `Preprocess.ipynb` sẽ được tự động xuất ra file .csv ở trong đường dẫn của phiên runtime hiện hành, đồng thời cũng sẽ được tải về local của người chạy notebook.
- Trong quá trình thực thi, khi notebook thực thi đến cell để tải về local thì trình duyệt có thể yêu cầu người dùng cho phép tải nhiều file cùng lúc. Lúc này hãy nhấn `Cho phép`
- Các tập dữ liệu đầu ra của file `Preprocess.ipynb` sẽ là dữ liệu đầu vào cho mô hình huấn luyện và dự đoán trong file `Q2-Predict_Model/train.ipynb`
## Q1. EDA và Xử lý Dữ liệu (Exploratory Data Analysis & Data Preprocessing)

### Mục tiêu

Trong bước này, nhóm tiến hành:

- Hiểu rõ hơn về tập dữ liệu thông qua các phân tích thống kê và trực quan hóa.
- Thực hiện các bước xử lý dữ liệu ban đầu nhằm chuẩn bị cho quá trình huấn luyện mô hình dự đoán giá nhà.

---

### 1. Tổng quan Dữ liệu (`Overview.ipynb`)

- **Đọc dữ liệu** từ tập tin `dataset.csv` và hiển thị thông tin cơ bản như:
  - Kích thước dataset
  - Kiểu dữ liệu từng cột
  - Số lượng giá trị thiếu
- **Thống kê mô tả**: sử dụng `.describe()` để xem các chỉ số như mean, std, min, max,...
- **Phân nhóm thuộc tính**:
  - Tách các thuộc tính thành dạng số (numerical) và dạng phân loại (categorical)

---

### 2. Phân tích Dữ liệu Khám phá (EDA) (`EDA.ipynb`)

- **Phân tích phân phối giá nhà**:
  - Vẽ biểu đồ histogram và boxplot của `sale_price`
  - Log-transform `sale_price` để kiểm tra phân phối chuẩn
- **Tương quan với giá nhà**:
  - Tính hệ số tương quan Pearson
  - Vẽ heatmap các đặc trưng tương quan cao với `sale_price`
- **Phân tích biến phân loại**:
  - So sánh giá nhà giữa các nhóm như `grade`, `condition`, `waterfront`,...
- **Đặc trưng địa lý**:
  - Phân tích ảnh hưởng của `latitude`, `longitude` tới `sale_price` bằng biểu đồ scatter

---

### 3. Tiền xử lý Dữ liệu (`Preprocess.ipynb`)

- **Xử lý missing values**:
  - Với numerical: điền bằng giá trị trung bình hoặc median
  - Với categorical: điền bằng `"Unknown"` hoặc mode
- **Xử lý ngoại lệ**:
  - Dựa vào boxplot, z-score để loại bỏ các mẫu bất thường
- **Biến đổi dữ liệu**:
  - Áp dụng `np.log1p()` lên `sale_price` để chuẩn hóa
- **Chuẩn hóa dữ liệu số**:
  - Sử dụng `StandardScaler` hoặc `MinMaxScaler`
- **One-hot encoding**:
  - Biến đổi các cột phân loại thành dạng số để đưa vào mô hình
- **Tải tập train và test mới về máy**
  - Tải tập train và test mới về máy để chuẩn bị cho việc huấn luyện mô hình.

---

### Ghi chú

- Các bước trên đảm bảo dữ liệu đầu vào sạch, đồng nhất và có tính biểu diễn tốt.
- Việc phân tích kỹ càng giúp lựa chọn đặc trưng đầu vào hợp lý, từ đó tăng độ chính xác của mô hình học máy.
