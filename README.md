# Phân Tích và Dự Đoán Nguy Cơ Mắc Bệnh Alzheimer

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-yellowgreen)
![XGBoost](https://img.shields.io/badge/XGBoost-Classification-red)

## 1. Tổng quan dự án (About The Project)
Bệnh Alzheimer là một chứng rối loạn thoái hóa thần kinh tiến triển gây ảnh hưởng nghiêm trọng đến trí nhớ và các chức năng nhận thức. Việc phát hiện sớm nguy cơ mắc bệnh đóng vai trò vô cùng quan trọng trong việc can thiệp và điều trị y tế kịp thời.

Dự án này thực hiện phân tích một bộ dữ liệu y tế đa chiều và áp dụng các thuật toán Machine Learning để giải quyết hai bài toán chính:
1. **Khám phá và phân cụm (Unsupervised Learning):** Tìm ra các nhóm bệnh nhân có cấu trúc đặc điểm tương đồng ẩn sâu trong dữ liệu.
2. **Dự đoán và phân loại (Supervised Learning):** Xây dựng các mô hình có khả năng phân loại, dự đoán rủi ro mắc bệnh Alzheimer dựa trên hồ sơ bệnh án, lối sống và các chỉ số lâm sàng.

## 2. Mô tả dữ liệu (Dataset)
Tập dữ liệu sử dụng là `alzheimers_disease_data.csv` bao gồm **2149 quan sát (bệnh nhân)** và **35 thuộc tính**. Trong quá trình tiền xử lý, các cột định danh (`PatientID`, `DoctorInCharge`) được loại bỏ. Các nhóm biến chính bao gồm:
* **Nhân khẩu học & Thói quen:** Tuổi, Giới tính, Dân tộc, Học vấn, BMI, Hút thuốc, Tiêu thụ rượu, Hoạt động thể chất...
* **Tiền sử y khoa & Chỉ số lâm sàng:** Tiền sử gia đình, Bệnh tim mạch, Tiểu đường, Huyết áp, Cholesterol (Total, LDL, HDL, Triglycerides)...
* **Thang điểm nhận thức/chức năng:** MMSE, Đánh giá chức năng, Vấn đề hành vi, ADL...
* **Triệu chứng lâm sàng:** Nhầm lẫn, Mất phương hướng, Thay đổi tính cách, Hay quên...
* **Biến mục tiêu (Target Variable):** `Diagnosis` (0: Không mắc bệnh, 1: Mắc bệnh).

## 3. Công nghệ và Phương pháp áp dụng (Tech Stack & Methodology)
* **Ngôn ngữ & Thư viện:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost.
* **Tiền xử lý dữ liệu:** Xử lý missing values, Scaling (`MinMaxScaler`, `StandardScaler`, `RobustScaler`).
* **Học Không Giám Sát (Phân cụm):** * Giảm chiều dữ liệu: PCA, t-SNE.
  * Thuật toán: K-Means.
  * Đánh giá: Silhouette score, Davies-Bouldin score, Calinski-Harabasz score.
* **Học Có Giám Sát (Phân loại):**
  * Thuật toán: Logistic Regression, Decision Tree, Random Forest, KNN, SVC, XGBoost.
  * Tối ưu hóa: `GridSearchCV` để tinh chỉnh siêu tham số.
  * Đánh giá: Confusion Matrix, Classification Report (Accuracy, Precision, Recall, F1-Score).

## 4. Cấu trúc thư mục (Folder Structure)

```text
├── alzheimers_disease_data.csv              # File dữ liệu y tế gốc
├── Tranthimaianh_Nhom5_Alzheimer.ipynb      # Notebook Tiền xử lý, EDA và Phân cụm (K-Means, PCA)
├── Demo_Alzheimers_nhom5.ipynb              # Notebook Huấn luyện mô hình Phân loại dự đoán (XGBoost, RF, SVC...)
└── README.md                                # Thông tin tổng quan về dự án