# FINAL PROJECT_MACHINE LEARNING

SV1: Nguyễn Tấn Phát - 52000583

SV2: Võ Quốc Thái - 52000398

SV3: Trương Thị Bích Trinh - 52000424

## Bài 1 (3 điểm): làm riêng từng người

Trình bày một bài nghiên cứu, đánh giá của em về các vấn đề sau:
  1)	Tìm hiểu, so sánh các phương pháp Optimizer trong huấn luyện mô hình học máy;
  2)	Tìm hiểu về Continual Learning và Test Production khi xây dựng một giải pháp học máy để giải quyết một bài toán nào đó.

## Bài 2: (7 điểm): làm chung trong nhóm
Đưa ra một bài toán dự đoán có thể giải quyết bằng học máy (machine leanring) với các yêu cầu sau:
  -	Số Feature/Attribute gồm nhiều kiểu: categorial và numerical;
  -	Dữ liệu phải chưa được học, thực tập trên lớp và trong bài tập về nhà;

  1)	Phân tích thống kê trên dữ liệu, vẽ các đồ thị để hiểu bài toán, hiểu dữ liệu. Tìm hiểu các đặc trưng và đánh gía vai trò của các đặc trưng đối với mục tiêu bài toán;
  2)	Ứng dụng các mô hình học máy cơ bản để giải quyết bài toán, bao gồm cả các mô hình thuộc Ensemble Learing;
  3)	Sử dụng Feed Forward Neural Network và Reccurent Neural Network (hoặc mô thuộc loại này) để giải quyết bài toán;
  4)	Áp dụng các kỹ thuật tránh Overfiting trên các mô hình của câu (2) và câu (3) để giải quyết bài toán;
  5)	Sau khi huấn luyện xong mô hình thì muốn cải thiện độ chính xác, ta sẽ làm gì để giải quyết nó? Phân tích các trường hợp sai, đề ra giải pháp và thực hiện nó, sau đó đánh giá xem có cải tiến so với trước không. 
  
### Giới thiệu bộ dữ liệu:
  - Mỗi hàng đại diện cho một khách hàng, mỗi cột chứa các thuộc tính của khách hàng được mô tả trên cột Metadata.
  - Bộ dữ liệu bao gồm 21 feature: Customer ID, Gender, Senior Citizen, Partner, Dependents, Tenure, Phone Service, Multiple Lines, Internet Service, Online     Security, Online Backup, Device Protection, Tech Support, Streaming TV, Streaming Movies, Contract, Paperless Billing, Payment Method, Monthly Charges, Total Charges, Churn.
  - Bộ dữ liệu bao gồm thông tin về:
    + Khách hàng đã rời đi trong tháng trước – cột có tên là Churn
    + Các dịch vụ mà mỗi khách hàng đã đăng ký – điện thoại, nhiều đường dây, internet, bảo mật trực tuyến, sao lưu trực tuyến, bảo vệ thiết bị, hỗ trợ kỹ thuật và truyền phát trực tuyến TV và phim
    + Thông tin tài khoản khách hàng – họ đã là khách hàng trong bao lâu, hợp đồng, phương thức thanh toán, thanh toán không cần giấy tờ, phí hàng tháng và tổng phí
    + Thông tin nhân khẩu học về khách hàng – giới tính, độ tuổi và liệu họ có đối tác và người phụ thuộc hay không
### Các kĩ thuật sử dụng để tiền xử lý dữ liệu:
  - Kết hợp tất cả dữ liệu với nhau theo một định dạng thống nhất
  - Cân bằng dữ liệu
  - Chuẩn hóa dữ liệu
  - Loại bỏ các giá trị ngoại lai
  - Điền giá trị trung bình cho các cột bị thiếu
  - Xóa các feature có phương sai thấp
### Các mô hình cơ bản được huấn luyện
  - Linear Regression
  - K Neighbors Classifier
  - GaussianNB
  - MultinomialNB
  - Decision Tree Classifier
  - Decision Tree Regressor
### Các mô hình Ensemble Learning được sử dụng
  - AdaBoost Classifier
  - AdaBoost Regressor
  - Gradient Boosting Classifier
  - Gradient Boosting Regressor
  - XGboost
### Các mô hình Neural Network được sử dụng
  - Feed Forward Neural Network
  - Reccurent Neural Network
### Các kĩ thuật được dùng để tránh Overfitting
  - Cross-validation để chọn giá trị tham số đầu vào tốt nhất để tránh overfitting
  - Sử dụng regularization L2 để giảm trọng số để tránh overfitting
  - Sử dụng phương pháp giới hạn Độ Sâu (Max Depth) để tránh overfitting
  - Sử dụng kiểm soát Learning Rate để tránh overfitting
  - Sử dụng lớp Dropout và EarlyStopping callback để tránh overfitting
  - Sử dụng Gradient Clipping để tránh overfitting
### Các kĩ thuật để đánh giá các giá trị sai trong việc huấn luyện mô hình
  - Đánh giá độ chính xác, precision, recall, F1-score, và các độ đo hiệu suất khác trên tập kiểm thử.
  - Tạo ma trận nhầm lẫn để xem xét cụ thể là mô hình của bạn đang làm gì sai.
  - Xem xét một số mẫu mà mô hình dự đoán sai để hiểu tại sao chúng được phân loại sai.
  - Kiểm tra phân phối của các đặc trưng trong tập huấn luyện và kiểm thử để xem xét sự tương đồng.
### Các kĩ thuật được dùng để cải thiện độ chính xác:
  - Sử dụng kỹ thuật cross-validation để đánh giá hiệu suất của mô hình trên nhiều tập dữ liệu khác nhau.
  - Sử dụng kỹ thuật tinh chỉnh siêu tham số bằng cách sử dụng tìm kiếm lưới (Grid Search) hoặc tìm kiếm ngẫu nhiên (Random Search).
  - Sử dụng các kỹ thuật như L1 hoặc L2 regularization để kiểm soát overfitting và cải thiện tổng quát hóa.
  - Thêm các lớp vào các mô hình
  - Kết hợp nhiều mô hình để cung cấp dự đoán tốt hơn.
