# Training Model for Predictive Task
## Hướng dẫn thực thi notebook

### Bước 1: Mở [Google Colab](https://colab.research.google.com/)
### Bước 2: Chọn mục `Upload` > `Browse` > Chọn file `train.ipynb`.
### Bước 3: Ở phần upload dữ liệu, 2 file `new_train.csv` và `new_test.csv` hoàn toàn giống nhau ở 2 lựa chọn:
- Lựa chọn 1 (tiết kiệm thời gian): Chạy mặc định sử dụng 2 file `new_train.csv` và `new_test.csv` có được khi thực thi `Preprocess.ipynb` và được lưu trữ sẵn từ trước.
- Lựa chọn 2 (khi cần xác thực): Mở comment ở cell upload để tải lên thủ công 2 file `new_train.csv` và `new_test.csv` có được khi thực thi `Preprocess.ipynb` trước đó.
### Bước 4: Ở phần tải model pretrained, do quá trình huấn luyện model tương đối lâu nên nhóm đã chuẩn bị các lựa chọn:
- Lựa chọn 1 (tiết kiệm thời gian): Chạy mặc định cell để load model pretrained và tiến hành dự đoán tập test dựa trên model đó
- Lựa chọn 2 (khi cần xác thực): Comment toàn bộ đoạn code có trong cell để tiến hành quá trình huấn luyện lại từ đầu.
### Bước 5: Kết quả dự đoán sẽ được lưu ở dạng `.csv`, và mô hình mới (nếu có) sẽ được lưu dưới dạng `.pkl`.
## Mô tả dự án

Notebook này được xây dựng nhằm mục đích huấn luyện một mô hình học máy cho bài toán dự đoán từ một tập dữ liệu đầu vào. Mục tiêu là đạt được hiệu suất dự đoán tốt nhất thông qua các bước xử lý dữ liệu, xây dựng mô hình và đánh giá chất lượng.

## Các bước thực hiện

1. **Tiền xử lý dữ liệu**
   - Làm sạch dữ liệu
   - Tạo các đặc trưng mới phù hợp với bài toán

2. **Biến đổi dữ liệu**
   - Chuẩn hóa các đặc trưng số
   - Mã hóa các đặc trưng dạng phân loại (categorical features)

3. **Chia dữ liệu**
   - Chia dữ liệu thành tập huấn luyện và tập kiểm tra

4. **Huấn luyện mô hình**
   - Xây dựng pipeline mô hình
   - Sử dụng thuật toán học máy **2-Stage Model: XGBoost**
   - Tinh chỉnh các siêu tham số 

5. **Đánh giá mô hình**
   - Sử dụng chỉ số Winkler do cuộc thi cung cấp
   - Kiểm tra hiệu quả mô hình trên tập test

6. **Lưu và xuất kết quả**
   - Lưu mô hình đã huấn luyện
   - Xuất kết quả dự đoán phục vụ cho bước nộp bài

## Công nghệ sử dụng

- Python
- scikit-learn
- pandas
- numpy
- matplotlib / seaborn
- Jupyter Notebook
- XGBoost

## Cấu trúc thư mục
```
.
├── train.ipynb
├── Dataset
│   ├── new_train.csv
│   └── new_test.csv
├── Model
│   ├── model0.pkl
│   └── model1.pkl
└── Submission
    └── submission_twostage_grid.csv
```
