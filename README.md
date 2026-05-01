# Bánh Gà Phô Mai - Datathon Project

Repository này lưu trữ toàn bộ notebook, báo cáo và file kết quả của team **Bánh Gà Phô Mai** trong bài toán phân tích chẩn đoán và dự báo doanh thu cho một doanh nghiệp thương mại điện tử thời trang.

Project được chia thành ba phần chính:

1. Xử lý câu hỏi và khám phá dữ liệu ban đầu.
2. Phân tích dữ liệu khám phá để tìm vấn đề kinh doanh.
3. Xây dựng mô hình Machine Learning để dự báo Revenue và COGS.

---

## 1. Cấu trúc repository

```text
.
├── Bánh Gà Phô Mai - Report.pdf
├── Bánh_Gà_Phô_Mai_Part_1_MCQ.ipynb
├── Bánh_Gà_Phô_Mai_Part_2_EDA.ipynb
├── Bánh_Gà_Phô_Mai_Part_3_Machine_Learning.ipynb
├── README.md
└── submission.csv
```

---

## 2. Mô tả các file

| File | Mô tả |
|---|---|
| `Bánh Gà Phô Mai - Report.pdf` | Báo cáo cuối cùng của team, bao gồm các phần Business Understanding, Business Issue, Root Cause Analysis, Recommendations và mô hình dự báo doanh thu/COGS. |
| `Bánh_Gà_Phô_Mai_Part_1_MCQ.ipynb` | Notebook xử lý phần câu hỏi trắc nghiệm và các phân tích ban đầu theo yêu cầu của đề bài. |
| `Bánh_Gà_Phô_Mai_Part_2_EDA.ipynb` | Notebook phân tích dữ liệu khám phá, bao gồm phân tích doanh thu, đơn hàng, khách hàng, sản phẩm, tồn kho, rating, hoàn/hủy hàng và các nguyên nhân dẫn đến sự suy giảm hiệu quả kinh doanh. |
| `Bánh_Gà_Phô_Mai_Part_3_Machine_Learning.ipynb` | Notebook xây dựng mô hình dự báo Revenue và COGS bằng các mô hình Gradient Boosting như XGBoost, LightGBM và CatBoost. |
| `submission.csv` | File kết quả dự báo cuối cùng dùng để submit theo đúng format của cuộc thi. |
| `README.md` | File mô tả cấu trúc repository, vai trò của từng file và hướng dẫn chạy notebook. |

---

## 3. Mục tiêu project

Project tập trung vào việc sử dụng dữ liệu để trả lời hai nhóm câu hỏi chính:

### 3.1. Doanh nghiệp đang gặp vấn đề gì?

Thông qua phần EDA, team phân tích các khía cạnh chính của hoạt động kinh doanh như:

- Quy mô doanh thu và đơn hàng qua thời gian.
- Sự thay đổi của lượng khách hàng mới và khách hàng quay lại.
- Hiệu quả giữ chân khách hàng theo cohort.
- Cấu trúc danh mục sản phẩm.
- Tình trạng stockout, overstock và zombie products.
- Hiệu quả khuyến mãi.
- Biên lợi nhuận gộp và áp lực từ COGS.

Từ đó, team xác định vấn đề cốt lõi của doanh nghiệp là sự suy giảm nhu cầu, xói mòn product-market fit và mất cân đối giữa danh mục hàng hóa với nhu cầu thực tế của thị trường.

### 3.2. Có thể dự báo Revenue và COGS như thế nào?

Sau khi hiểu được vấn đề kinh doanh, team xây dựng mô hình dự báo Revenue và COGS nhằm hỗ trợ doanh nghiệp:

- Lập kế hoạch sản phẩm.
- Quản trị tồn kho.
- Kiểm soát khuyến mãi.
- Ước lượng áp lực giá vốn.
- Theo dõi rủi ro biên lợi nhuận gộp.
- Ra quyết định nhanh hơn dựa trên dữ liệu.

---

## 4. Môi trường chạy code

Team sử dụng **Google Colab** làm môi trường chính để chạy notebook. Vì vậy, các file `.ipynb` trong repository được thiết kế để có thể chạy trực tiếp trên Colab.

Một số thư viện phổ biến như:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

thường đã được Google Colab cài đặt sẵn.

Với các thư viện chưa có sẵn, notebook sẽ có cell cài đặt riêng ở phần đầu, ví dụ:

```python
!pip install xgboost lightgbm catboost shap
```

Người dùng cũng có thể chạy notebook bằng **Jupyter Notebook** hoặc **JupyterLab** trên máy cá nhân, nhưng cần tự cài đặt đầy đủ các thư viện cần thiết trước khi chạy.

---

## 5. Cách chạy bằng Google Colab

Đây là cách chạy được khuyến nghị vì project được team phát triển chủ yếu trên Google Colab.

### Bước 1: Mở Google Colab

Truy cập:

```text
https://colab.research.google.com/
```

### Bước 2: Upload notebook

Có thể mở notebook theo một trong hai cách:

- Chọn `File > Upload notebook`, sau đó upload file `.ipynb` từ máy.
- Hoặc chọn `File > Open notebook > GitHub`, sau đó dán link repository GitHub.

### Bước 3: Upload dữ liệu

Nếu notebook yêu cầu file dữ liệu đầu vào, hãy upload các file dữ liệu theo hướng dẫn trong từng notebook.

Một số notebook có thể sử dụng cú pháp riêng của Colab như:

```python
from google.colab import files
uploaded = files.upload()
```

hoặc mount Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

### Bước 4: Chạy notebook

Chạy lần lượt các cell từ trên xuống dưới bằng một trong hai cách:

```text
Runtime > Run all
```

hoặc nhấn:

```text
Shift + Enter
```

cho từng cell.

### Bước 5: Xuất file kết quả

Sau khi chạy notebook Machine Learning, file dự báo cuối cùng sẽ được xuất ra dưới dạng:

```text
submission.csv
```

File này là kết quả dùng để submit theo format yêu cầu của đề bài.

---

## 6. Cách chạy bằng Jupyter Notebook local

Nếu muốn chạy project trên máy cá nhân, cần cài đặt Python và các thư viện cần thiết.

### Bước 1: Cài đặt thư viện

Chạy lệnh sau trong terminal hoặc command prompt:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm catboost shap
```

Nếu sử dụng Jupyter Notebook:

```bash
pip install notebook
```

Nếu sử dụng JupyterLab:

```bash
pip install jupyterlab
```

### Bước 2: Mở notebook

Mở Jupyter Notebook:

```bash
jupyter notebook
```

hoặc JupyterLab:

```bash
jupyter lab
```

Sau đó mở lần lượt các file `.ipynb` trong repository.

### Bước 3: Chạy các cell

Chạy các cell theo thứ tự từ trên xuống dưới để tránh lỗi biến chưa được khởi tạo.

---

## 7. Thứ tự khuyến nghị khi chạy notebook

Nên chạy các notebook theo đúng thứ tự sau:

```text
1. Bánh_Gà_Phô_Mai_Part_1_MCQ.ipynb
2. Bánh_Gà_Phô_Mai_Part_2_EDA.ipynb
3. Bánh_Gà_Phô_Mai_Part_3_Machine_Learning.ipynb
```

Trong đó:

### Part 1 - MCQ

Notebook này xử lý các câu hỏi ban đầu và một số bước kiểm tra dữ liệu cơ bản.

### Part 2 - EDA

Notebook này là phần phân tích dữ liệu khám phá. Đây là phần quan trọng để hiểu bối cảnh kinh doanh và tìm ra nguyên nhân khiến doanh nghiệp suy giảm.

Các phân tích chính bao gồm:

- Business performance.
- Customer analysis.
- Order volume and AOV trend.
- Conversion analysis.
- Cohort retention.
- Product portfolio.
- Hero products.
- Stockout and overstock.
- Sell-through rate.
- Reorder flag.
- Gross profit margin.
- Return reason.

### Part 3 - Machine Learning

Notebook này xây dựng mô hình dự báo Revenue và COGS.

Quy trình chính bao gồm:

- Feature engineering cho dữ liệu chuỗi thời gian.
- Tạo các biến calendar, lag, rolling, momentum và Fourier.
- Huấn luyện các mô hình XGBoost, LightGBM và CatBoost.
- Tối ưu tham số bằng grid search.
- Đánh giá mô hình bằng RMSE và MAE.
- Chọn mô hình tốt nhất.
- Dự báo Revenue và COGS.
- Xuất file `submission.csv`.

---

## 8. Output của project

Project tạo ra hai nhóm output chính:

### 8.1. Báo cáo phân tích

File:

```text
Bánh Gà Phô Mai - Report.pdf
```

Báo cáo này tổng hợp toàn bộ logic phân tích, phát hiện chính, nguyên nhân gốc rễ và khuyến nghị cho doanh nghiệp.

### 8.2. File dự báo

File:

```text
submission.csv
```

Đây là file kết quả dự báo cuối cùng được tạo ra từ notebook Machine Learning.

---

## 9. Lưu ý khi chạy project

- Notebook được tối ưu để chạy trên Google Colab.
- Một số cell có thể sử dụng cú pháp đặc thù của Colab như `!pip install`, `files.upload()` hoặc `drive.mount()`.
- Nếu chạy bằng Jupyter Notebook local, cần đảm bảo tất cả thư viện đã được cài đặt đầy đủ.
- Nên chạy các cell theo đúng thứ tự từ trên xuống dưới.
- Kết quả có thể thay đổi nhẹ tùy theo phiên bản thư viện và môi trường chạy.
- Nếu gặp lỗi thiếu thư viện, hãy cài đặt thư viện đó bằng `pip install`.
- Nếu gặp lỗi đường dẫn dữ liệu, hãy kiểm tra lại vị trí file dữ liệu đầu vào.

---

## 10. Công nghệ và thư viện sử dụng

Project sử dụng các công cụ và thư viện chính sau:

```text
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
XGBoost
LightGBM
CatBoost
SHAP
Google Colab
Jupyter Notebook
```

---

## 11. Tác giả

Project được thực hiện bởi team **Bánh Gà Phô Mai**.

```text
National Economics University - NEU
Datathon / Vintelligence Project
```
