# 🚚 TỐI ƯU TUYẾN GIAO HÀNG
## So sánh Greedy Algorithm, Genetic Algorithm và Dynamic Programming

## 📖 Giới thiệu

Đây là đồ án môn **Phân tích và Thiết kế Giải thuật**.

Đề tài hướng đến việc xây dựng chương trình mô phỏng bài toán **Tối ưu tuyến giao hàng (Delivery Route Optimization)**, đồng thời so sánh hiệu quả của ba thuật toán:

- Greedy Algorithm
- Genetic Algorithm
- Dynamic Programming

Chương trình được xây dựng bằng **C++**, hoạt động trên **Console**, cho phép người dùng nhập các điểm giao hàng và lựa chọn thuật toán để tìm tuyến đường tối ưu.

---

# 🎯 Mục tiêu đề tài

- Tìm hiểu nguyên lý hoạt động của từng thuật toán.
- Áp dụng các thuật toán vào bài toán tối ưu tuyến giao hàng.
- So sánh kết quả giữa các thuật toán dựa trên:
  - Tổng quãng đường.
  - Thời gian thực thi (Execution Time).
  - Chất lượng lời giải.
  - Độ phức tạp thuật toán (Time Complexity).

---

# 👨‍💻 Thành viên nhóm

| MSSV | Họ và tên | Công việc |
|------|-----------|-----------|
| | | Phân tích yêu cầu & Thiết kế |
| | | Greedy Algorithm |
| | | Genetic Algorithm |
| | | Dynamic Programming & Tổng hợp |

---

# 📚 Mô tả bài toán

Một xe giao hàng xuất phát từ **KHO**, cần giao hàng đến nhiều địa điểm khác nhau.

Yêu cầu:

- Đi qua tất cả các điểm giao đúng một lần.
- Quay trở về KHO sau khi hoàn thành.
- Tìm tuyến đường có tổng khoảng cách nhỏ nhất.

Đây là một biến thể của bài toán nổi tiếng:

> **Travelling Salesman Problem (TSP)**

---

# 💻 Công nghệ sử dụng

- Ngôn ngữ: C++
- IDE: Visual Studio / Visual Studio Code
- Compiler: GCC / MinGW
- Console Application

---

# 📂 Cấu trúc thư mục

```
DeliveryRouteOptimization
│
├── README.md
├── main.cpp
│
├── include
│   ├── DeliveryPoint.h
│   ├── Menu.h
│   ├── Greedy.h
│   ├── Genetic.h
│   └── Dynamic.h
│
├── src
│   ├── Menu.cpp
│   ├── DeliveryPoint.cpp
│   ├── Greedy.cpp
│   ├── Genetic.cpp
│   └── Dynamic.cpp
│
└── data
```

---

# ⚙️ Chức năng chương trình

```
=========================================
      GIẢI BÀI TOÁN GIAO HÀNG
=========================================

1. Thêm các điểm giao
2. Greedy Algorithm
3. Genetic Algorithm
4. Dynamic Programming
5. Thoát

Lựa chọn:
```

---

# 📌 Chức năng 1 - Thêm các điểm giao

Người dùng nhập số lượng điểm giao.

Giới hạn:

- Tối thiểu: 1 điểm
- Tối đa: 20 điểm

Ví dụ

```
Nhập số lượng điểm giao: 3

Điểm giao thứ 1

Tên điểm:
A

Khoảng cách từ KHO:
12

------------------------

Điểm giao thứ 2

Tên điểm:
B

Khoảng cách từ KHO:
8

------------------------

Điểm giao thứ 3

Tên điểm:
C

Khoảng cách từ KHO:
20

Lưu dữ liệu thành công!
```

---

# 📌 Chức năng 2 - Greedy Algorithm

Thuật toán sẽ luôn chọn điểm giao gần nhất chưa được ghé.

Sau khi thực hiện sẽ hiển thị:

- Tuyến đường
- Tổng quãng đường
- Execution Time

Ví dụ

```
========== GREEDY ALGORITHM ==========

KHO

↓

B

↓

A

↓

C

↓

KHO

Tổng quãng đường: 45 km

Execution Time: 0.00012 s
```

---

# 📌 Chức năng 3 - Genetic Algorithm

Thuật toán sử dụng cơ chế tiến hóa để tìm lời giải gần tối ưu.

Chương trình sẽ hiển thị:

- Tuyến đường tốt nhất
- Tổng quãng đường
- Số thế hệ (Generation)
- Execution Time

---

# 📌 Chức năng 4 - Dynamic Programming

Áp dụng thuật toán **Held-Karp Algorithm** để tìm lời giải tối ưu.

Kết quả hiển thị:

- Tuyến đường tối ưu
- Tổng quãng đường nhỏ nhất
- Execution Time

---

# 📊 Tiêu chí so sánh

| Tiêu chí | Greedy | Genetic | Dynamic Programming |
|----------|---------|----------|---------------------|
| Chất lượng lời giải | Trung bình | Gần tối ưu | Tối ưu |
| Execution Time | Nhanh | Trung bình | Chậm |
| Time Complexity | O(n²) | O(P × G × n) | O(n² × 2ⁿ) |
| Memory Usage | Thấp | Trung bình | Cao |
| Khả năng mở rộng | Tốt | Rất tốt | Kém |

Trong đó:

- n: Số điểm giao.
- P: Population Size.
- G: Generation.

---

# 🔄 Quy trình hoạt động

```
Khởi động chương trình

↓

Thêm các điểm giao

↓

Lưu dữ liệu

↓

Chọn thuật toán

↓

Thực hiện tính toán

↓

Hiển thị tuyến đường

↓

Hiển thị tổng khoảng cách

↓

Hiển thị Execution Time

↓

So sánh kết quả

↓

Kết thúc
```

---

# 📸 Ví dụ giao diện Console

```
=========================================
      GIẢI BÀI TOÁN GIAO HÀNG
=========================================

1. Thêm các điểm giao
2. Greedy Algorithm
3. Genetic Algorithm
4. Dynamic Programming
5. Thoát

Lựa chọn:
```

---

# 📖 Thuật toán sử dụng

## 1. Greedy Algorithm

- Luôn chọn điểm gần nhất.
- Tốc độ xử lý nhanh.
- Không đảm bảo lời giải tối ưu.

### Ưu điểm

- Đơn giản.
- Dễ cài đặt.
- Execution Time thấp.

### Nhược điểm

- Có thể bỏ lỡ lời giải tối ưu.

---

## 2. Genetic Algorithm

- Mô phỏng quá trình tiến hóa tự nhiên.
- Sử dụng Population, Selection, Crossover và Mutation.
- Có khả năng tìm lời giải gần tối ưu.

### Ưu điểm

- Phù hợp với dữ liệu lớn.
- Chất lượng lời giải cao.

### Nhược điểm

- Cần điều chỉnh nhiều tham số.
- Không đảm bảo luôn tối ưu.

---

## 3. Dynamic Programming

Áp dụng thuật toán Held-Karp.

### Ưu điểm

- Luôn tìm được lời giải tối ưu.

### Nhược điểm

- Time Complexity rất lớn.
- Không phù hợp với số lượng điểm giao lớn.

---

# 📈 Kết quả mong đợi

Sau khi chạy mỗi thuật toán, chương trình sẽ hiển thị:

- Tuyến đường giao hàng.
- Tổng quãng đường.
- Execution Time.

Từ đó người dùng có thể dễ dàng so sánh hiệu quả giữa ba thuật toán.

---

# 🎓 Mục đích học tập

Đồ án được thực hiện nhằm phục vụ môn học **Phân tích và Thiết kế Giải thuật**, giúp sinh viên hiểu rõ nguyên lý hoạt động, ưu điểm, nhược điểm và khả năng ứng dụng của các thuật toán tối ưu trong thực tế.

---

# 📄 License

Project được phát triển cho mục đích học tập và nghiên cứu.
