# EC335.P21
Machine Learning for IoT 

🛡️ Phát hiện xâm nhập trong hệ thống IoT bằng các thuật toán học máy
Đây là đồ án áp dụng các thuật toán học máy để xây dựng hệ thống phát hiện xâm nhập (IDS) trong mạng IoT, sử dụng dữ liệu mạng và hành vi truy cập. Các mô hình được so sánh bao gồm: Decision Tree, Random Forest, LightGBM và XGBoost.

📂 Dữ liệu sử dụng: Do dung lượng lớn, dữ liệu không được đính kèm trực tiếp trong repo.

👉 Vui lòng tải bộ dữ liệu gốc tại đây: https://www.kaggle.com/datasets/hemachandiranmurugan/intrusion-in-iot/data
Sau khi tải xong, đặt file .csv vào thư mục data/:

data/
└── cleaned_iot.csv

🎯 Mục tiêu đề tài
+ Xây dựng hệ thống phát hiện và phân loại các cuộc tấn công vào hệ thống IoT.
+ So sánh hiệu quả giữa các thuật toán học máy phổ biến.
+ Hiển thị kết quả trực quan như: biểu đồ ROC, confusion matrix, feature importance.

📊 Các thuật toán sử dụng
+ Decision Tree
+ Random Forest
+ LightGBM
+ XGBoost
Mỗi mô hình được tối ưu bằng GridSearchCV và đánh giá qua:
+ Accuracy
+ Precision / Recall
+ F1-score (macro)
+ Thời gian dự đoán theo lô (batch)
+ ROC-AUC
+ Tầm quan trọng của đặc trưng (Feature Importance)

🛠️ Tiền xử lý dữ liệu
+ Xoá dữ liệu trùng lặp (65.556 dòng)
+ Mã hóa nhãn (Label Encoding)
+ Gộp các nhãn xuất hiện ít thành nhãn other
+ Chuẩn hóa đặc trưng với StandardScaler
+ Xử lý mất cân bằng lớp bằng tham số class_weight và sample_weight

📈 Kết quả nổi bật
+ XGBoost và LightGBM đạt F1-macro ~ 0.992
+ Random Forest cho kết quả ổn định, dễ huấn luyện
+ LightGBM huấn luyện rất nhanh, phù hợp dữ liệu lớn

📁 Cấu trúc thư mục

📁 intrusion-in-iot-classification
├── intrusion-in-iot-classification-algorithms.ipynb  # Notebook chính
├── README.md
└── data/
    └── cleaned_iot.csv  # (Dữ liệu tải từ Kaggle)

▶️ Cách chạy project
1. Clone repo
2. Cài đặt thư viện: pip install -r requirements.txt
3. Tải dữ liệu từ Kaggle và đặt vào thư mục data/.
4. Mở Jupyter Notebook và chạy: jupyter notebook intrusion-in-iot-classification-algorithms.ipynb

👥 Thành viên thực hiện
+ Nguyễn Thị Mỹ Dung – 22520288
+ Nguyễn Thị Kim Ngọc – 22520959
+ Lê Nguyễn Thục Nhi – 22521036
+ Đỗ Nhật Quỳnh – 22521229



