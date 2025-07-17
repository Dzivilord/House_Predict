# Training Model for Predictive Task

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

## Hướng dẫn chạy notebook

1. Chạy train.ipynb trong Jupyter Notebook từ đầu đến cuối.

- (Optional) Mở comment ở chỗ upload để tải lên 2 file new_train.csv và new_test.csv có được từ Preprocess.ipynb

2. Kết quả dự đoán sẽ được lưu ở dạng .csv, và mô hình mới (nếu có) sẽ được lưu dưới dạng .pkl.
