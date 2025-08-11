# Seminar_DifferentialPrivacy
## Giới Thiệu
Dự án này là đồ án cuối kỳ cho môn Phân Tích Dữ Liệu Bảo Toàn Tính Riêng Tư, thuộc Bộ Môn Công Nghệ Tri Thức. Mục tiêu chính là xây dựng mô hình hồi quy tuyến tính để dự đoán giá bán xe hơi cũ dựa trên tập dữ liệu được cung cấp, đồng thời áp dụng Differential Privacy (DP) để bảo vệ tính riêng tư của dữ liệu.
Tập dữ liệu bao gồm các thông tin về xe hơi cũ (như thương hiệu, năm sản xuất, số km đã chạy, công suất tối đa, dung lượng bình xăng, v.v.) và giá bán. Dự án bao gồm các phần chính:

- Phần 1: Tải và khám phá dữ liệu (train.csv và test.csv).
- Phần 2: Tiền xử lý dữ liệu (xử lý giá trị thiếu, chuyển đổi categorical sang numerical, trích xuất số từ chuỗi, chuẩn hóa dữ liệu).
- Phần 3: Xây dựng và huấn luyện mô hình hồi quy tuyến tính với ít nhất 4 công thức khác nhau (không sử dụng sklearn cho huấn luyện, sử dụng gradient descent thủ công). Đánh giá bằng Mean Squared Error (MSE) trên log scale.
- Phần 3.3: Áp dụng Differential Privacy ở mức server-level sử dụng Laplace Mechanism trên tham số mô hình. Đánh giá với các mức epsilon: <1, 1-10, >10. Chọn công thức tốt nhất (công thức 4) để áp dụng DP.
- Bonus: Triển khai Federated Learning với DP để bảo vệ dữ liệu cục bộ của client, sử dụng Federated Averaging để tổng hợp mô hình.

Dự án được thực hiện bằng Python và Jupyter Notebook. Lý do chọn các công thức: Dựa trên quan sát dữ liệu (tương quan giữa các đặc trưng như Year, Kilometer, Max Power, Fuel Tank Capacity, Seating Capacity), các công thức đa dạng để kiểm tra sự kết hợp tuyến tính, bậc cao, và tương tác giữa biến.
## Yêu Cầu Hệ Thống

- Ngôn ngữ: Python 3.13.2 (hoặc tương đương).
- Thư viện cho phép: pandas, numpy, matplotlib, seaborn, re (và các thư viện cơ bản khác cho xử lý dữ liệu; không dùng sklearn cho huấn luyện mô hình).
- Môi trường: Jupyter Notebook (khuyến nghị sử dụng Anaconda, VS Code với extension Jupyter, hoặc Google Colab để dễ dàng cài đặt và chạy).
- Dữ liệu: Tải từ Moodle (train.csv và test.csv). Đặt các file dữ liệu vào thư mục data/ trong repository.

Lưu ý: Không sử dụng các thư viện chuyên dụng cho machine learning như sklearn cho phần huấn luyện mô hình. Chỉ dùng cho các tác vụ phụ như đọc dữ liệu. Code được kiểm tra để đảm bảo chạy mà không lỗi.

## Cài Đặt
Clone repository về máy:
        https://github.com/BeanCole/Seminar_DifferentialPrivacy.git
Cài đặt các thư viện cần thiết (nếu chưa có):
        pip install -r requirements.txt

## Thành Viên Nhóm

Trần Anh Tú - 22120400
Hoàng Ngọc Tuệ - 22120407
