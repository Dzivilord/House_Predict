# House Price Prediction with Prediction Intervals

## 1. Mô tả Đồ án

Đây là một đồ án học thuật dựa trên cuộc thi **Prediction Interval Competition II - House Price**. Nhóm thực hiện sẽ xây dựng một mô hình dự đoán **khoảng giá nhà có độ tin cậy cao**, thay vì chỉ dự đoán giá trị trung bình như các bài toán hồi quy truyền thống.

Mục tiêu cuối cùng là giúp mô hình có thể đưa ra các khoảng giá dự đoán (gồm **giới hạn dưới** và **giới hạn trên**) với độ tin cậy cao, phục vụ các ứng dụng thực tiễn như:

- Tư vấn tài chính và đầu tư bất động sản
- Định giá nhà ở, đất đai
- Tính toán bảo hiểm và rủi ro tài sản

---

## 2. Công việc chính

### 2.1 EDA và Xử lý Dữ liệu (`Q1/`)

📊 Trong bước này, nhóm tiến hành:

- Phân tích sơ bộ dữ liệu (EDA) để hiểu rõ đặc trưng của tập dữ liệu
- Thực hiện các bước tiền xử lý để chuẩn bị cho mô hình như:
  - Loại bỏ ngoại lệ
  - Điền giá trị thiếu
  - Biến đổi các đặc trưng
  - Chuẩn hóa các cột dạng số
  - One-hot encoding các biến phân loại

🔗 Chi tiết hướng dẫn chạy notebook: xem file `Q1/README.md`

---

### 2.2 Huấn luyện Mô hình Dự đoán Khoảng giá (`Q2/`)

- Ở bước này, nhóm xây dựng mô hình học máy để dự đoán **hai giá trị: Lower Bound và Upper Bound** cho `sale_price`. Kết quả được đánh giá thông qua điểm số trên hệ thống **Kaggle**.

📤 Nhóm submit file kết quả dự đoán (`submission.csv`) gồm 3 cột: `id`, `pi_lower`, `pi_upper`  


🔗 Chi tiết cách huấn luyện và chạy thử mô hình: xem file `Q2/README.md`

---

## 3. Yêu cầu Nộp bài

### 3.1. Source Code

- Thư mục `Q1/`: EDA và xử lý dữ liệu
- Thư mục `Q2/`: Huấn luyện và đánh giá mô hình
- Mỗi thư mục có `README.md` riêng, đảm bảo có thể chạy được trên **Google Colab**

### 3.2. Báo cáo

Bao gồm các nội dung:

...  

### 3.3. Video thuyết trình

- Thời lượng: ... phút
- (link Youtube or Gooogle Drive)

### 3.4. Slide trình bày

...  
