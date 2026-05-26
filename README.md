# Họ và tên: Lương Văn Học - MSSV:K225480106025
# Lớp K58KTP
# Môn: Khoa học dữ liệu
# Bài tập 1: Phân cụm lớp thành 3 nhóm, phân cụm sinh viên bằng thuật toán K-means

Linkyoutube:

## Giới thiệu bài tập

Bài tập thực hiện phân cụm sinh viên trong lớp thành 3 nhóm dựa trên điểm hệ số 4 của các môn học.

Dữ liệu đầu vào là file Excel `input.xlsx`, chứa bảng điểm của sinh viên ngành Kỹ thuật máy tính, chuyên ngành Kỹ thuật phần mềm. Chương trình sử dụng thuật toán K-means để phân cụm sinh viên dựa trên điểm trung bình của 3 nhóm năng lực:

1. Nhóm Phát triển phần mềm  
2. Nhóm AI - Dữ liệu - Thuật toán  
3. Nhóm Hệ thống - Mạng - Nhúng  

Kết quả sau khi chạy chương trình sẽ xuất ra file Excel `ket_qua_phan_cum_kmeans.xlsx`, trong đó có danh sách sinh viên, điểm trung bình từng nhóm năng lực, số môn có điểm, mã cụm, tên cụm và nhóm năng lực mạnh nhất.

## Ý tưởng thực hiện

Thay vì chỉ phân loại sinh viên theo điểm trung bình chung, chương trình chia các môn học thành 3 nhóm năng lực phù hợp với chuyên ngành Kỹ thuật phần mềm.

Với mỗi sinh viên, chương trình tính điểm trung bình của từng nhóm môn học. Ba điểm trung bình này được dùng làm dữ liệu đầu vào cho thuật toán K-means.

Sau khi chạy K-means với `K = 3`, sinh viên được chia thành 3 cụm:

- Cụm 1: Nhóm học lực tốt, nền tảng chuyên môn mạnh
- Cụm 2: Nhóm học lực khá, năng lực tương đối cân bằng
- Cụm 3: Nhóm cần cải thiện thêm kiến thức chuyên môn

Những sinh viên không đủ dữ liệu điểm sẽ được đưa vào nhóm riêng là `Không đủ dữ liệu để phân cụm`.


## Hướng dẫn chạy chương trình

### 1. Chuẩn bị file

Đặt các file trong cùng một thư mục:

```text
KMeans_PhanCum_Lop/
├── input.xlsx
├── phan_cum_kmeans.ipynb
└── README.md
```
Trong đó input.xlsx là file điểm đầu vào.

### 2. Cài thư viện

Mở Terminal trong thư mục dự án và chạy:

```
pip install pandas openpyxl scikit-learn matplotlib
```
### 3. Chạy chương trình

Mở file phan_cum_kmeans.ipynb bằng VS Code hoặc Jupyter Notebook.

Sau đó chạy lần lượt từng cell từ trên xuống dưới, hoặc bấm:
```
Run All
```
### 4. Kết quả

Sau khi chạy xong, chương trình tạo file:```ket_qua_phan_cum_kmeans.xlsx```

File kết quả gồm danh sách sinh viên, điểm trung bình theo 3 nhóm năng lực, mã cụm, tên cụm và thống kê số lượng sinh viên theo từng cụm.
