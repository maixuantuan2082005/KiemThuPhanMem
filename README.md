# Kiểm thử hiệu năng website bằng Apache JMeter

## 1. Giới thiệu

Kiểm thử hiệu năng (Performance Testing) là một hoạt động quan trọng trong kiểm thử phần mềm nhằm đánh giá khả năng hoạt động của hệ thống khi có nhiều người dùng truy cập cùng lúc. Thông qua kiểm thử hiệu năng, chúng ta có thể xác định được thời gian phản hồi của hệ thống, khả năng xử lý yêu cầu cũng như phát hiện các điểm nghẽn về hiệu năng.

Trong bài thực hành này, công cụ **Apache JMeter** được sử dụng để mô phỏng nhiều người dùng truy cập vào một website và đo lường hiệu năng của hệ thống.

Website được lựa chọn để kiểm thử:

https://www.wikipedia.org

---

# 2. Mục tiêu

Mục tiêu của bài thực hành kiểm thử hiệu năng bao gồm:

- Hiểu cách sử dụng **Apache JMeter** để kiểm thử hiệu năng của website.
- Thiết kế các kịch bản kiểm thử với số lượng người dùng khác nhau.
- Mô phỏng hành vi truy cập của người dùng bằng cách gửi các HTTP Request.
- Thu thập và phân tích các chỉ số hiệu năng như:

  - Thời gian phản hồi (Response Time)
  - Thông lượng (Throughput)
  - Tỷ lệ lỗi (Error Rate)

- Viết báo cáo và lưu trữ kết quả kiểm thử trên GitHub.

---

# 3. Môi trường kiểm thử

| Thành phần       | Mô tả                     |
| ---------------- | ------------------------- |
| Công cụ          | Apache JMeter 5.6         |
| Giao thức        | HTTP / HTTPS              |
| Loại kiểm thử    | Load Testing              |
| Hệ điều hành     | Windows                   |
| Website kiểm thử | https://www.wikipedia.org |

---

# 4. Thiết kế Test Plan

Test Plan được thiết kế với **3 Thread Group**, mỗi Thread Group mô phỏng một kịch bản tải khác nhau của người dùng.

---

# 4.1 Kịch bản 1 – Tải cơ bản (Basic Load Test)

Kịch bản này mô phỏng một số lượng nhỏ người dùng truy cập vào trang chủ của website.

Cấu hình:

- Số lượng người dùng (Threads): **10**
- Ramp-up Period: **5 giây**
- Loop Count: **5 lần**

Request gửi đi:

- Phương thức: **GET**
- URL: `/`

Mục đích:

Đánh giá hiệu năng cơ bản của website khi có số lượng người dùng truy cập thấp.

---

# 4.2 Kịch bản 2 – Tải nặng (Heavy Load Test)

Kịch bản này mô phỏng nhiều người dùng truy cập đồng thời vào website và mở nhiều trang khác nhau.

Cấu hình:

- Số lượng người dùng: **50**
- Ramp-up Period: **30 giây**
- Loop Count: **5**

Các request được gửi:

1. GET `/`
2. GET `/wiki/Main_Page`

Mục đích:

Đánh giá khả năng xử lý của website khi có nhiều người dùng truy cập cùng lúc.

---

# Kiểm thử hiệu năng website bằng Apache JMeter

## 1. Giới thiệu

Kiểm thử hiệu năng (Performance Testing) là một hoạt động quan trọng trong kiểm thử phần mềm nhằm đánh giá khả năng hoạt động của hệ thống khi có nhiều người dùng truy cập cùng lúc. Thông qua kiểm thử hiệu năng, chúng ta có thể xác định được thời gian phản hồi của hệ thống, khả năng xử lý yêu cầu cũng như phát hiện các điểm nghẽn về hiệu năng.

Trong bài thực hành này, công cụ **Apache JMeter** được sử dụng để mô phỏng nhiều người dùng truy cập vào một website và đo lường hiệu năng của hệ thống.

Website được lựa chọn để kiểm thử:

https://www.wikipedia.org

---

# 2. Mục tiêu

Mục tiêu của bài thực hành kiểm thử hiệu năng bao gồm:

- Hiểu cách sử dụng **Apache JMeter** để kiểm thử hiệu năng của website.
- Thiết kế các kịch bản kiểm thử với số lượng người dùng khác nhau.
- Mô phỏng hành vi truy cập của người dùng bằng cách gửi các HTTP Request.
- Thu thập và phân tích các chỉ số hiệu năng như:

  - Thời gian phản hồi (Response Time)
  - Thông lượng (Throughput)
  - Tỷ lệ lỗi (Error Rate)

- Viết báo cáo và lưu trữ kết quả kiểm thử trên GitHub.

---

# 3. Môi trường kiểm thử

| Thành phần       | Mô tả                     |
| ---------------- | ------------------------- |
| Công cụ          | Apache JMeter 5.6         |
| Giao thức        | HTTP / HTTPS              |
| Loại kiểm thử    | Load Testing              |
| Hệ điều hành     | Windows                   |
| Website kiểm thử | https://www.wikipedia.org |

---

# 4. Thiết kế Test Plan

Test Plan được thiết kế với **3 Thread Group**, mỗi Thread Group mô phỏng một kịch bản tải khác nhau của người dùng.

---

# 4.1 Kịch bản 1 – Tải cơ bản (Basic Load Test)

Kịch bản này mô phỏng một số lượng nhỏ người dùng truy cập vào trang chủ của website.

Cấu hình:

- Số lượng người dùng (Threads): **10**
- Ramp-up Period: **5 giây**
- Loop Count: **5 lần**

Request gửi đi:

- Phương thức: **GET**
- URL: `/`

Mục đích:

Đánh giá hiệu năng cơ bản của website khi có số lượng người dùng truy cập thấp.

---

# 4.2 Kịch bản 2 – Tải nặng (Heavy Load Test)

Kịch bản này mô phỏng nhiều người dùng truy cập đồng thời vào website và mở nhiều trang khác nhau.

Cấu hình:

- Số lượng người dùng: **50**
- Ramp-up Period: **30 giây**
- Loop Count: **5**

Các request được gửi:

1. GET `/`
2. GET `/wiki/Main_Page`

Mục đích:

Đánh giá khả năng xử lý của website khi có nhiều người dùng truy cập cùng lúc.

---

# 4.3 Kịch bản 3 – Hành vi người dùng tùy chỉnh (Custom Scenario)

Kịch bản này mô phỏng hành vi thực tế của người dùng khi họ truy cập và xem nhiều trang khác nhau.

Cấu hình:

- Số lượng người dùng: **20**
- Ramp-up Period: **10 giây**
- Thời gian chạy: **60 giây**

Các request:

1. GET `/wiki/Technology`
2. GET `/wiki/Computer`

Mục đích:

Mô phỏng hành vi người dùng khi duyệt nhiều nội dung khác nhau trên website.

---

# 5. Thực hiện kiểm thử

Các kịch bản kiểm thử được thực hiện bằng Apache JMeter.

Trong mỗi Thread Group, các Listener sau được sử dụng để thu thập kết quả:

- View Results Tree
- Summary Report
- Graph Results

Các chỉ số được thu thập bao gồm:

- **Response Time**: thời gian phản hồi của server.
- **Throughput**: số lượng request xử lý trong một đơn vị thời gian.
- **Error Rate**: tỷ lệ lỗi khi xử lý request.

Các hình ảnh minh chứng của quá trình kiểm thử được lưu trong thư mục `screenshots`.

---

# 6. Kết quả kiểm thử

| Kịch bản kiểm thử | Thời gian phản hồi trung bình | Throughput        | Tỷ lệ lỗi |
| ----------------- | ----------------------------- | ----------------- | --------- |
| Basic             | ~200 ms                       | ~40 request/giây  | 0%        |
| Heavy             | ~350 ms                       | ~110 request/giây | 0%        |
| Custom            | ~300 ms                       | ~75 request/giây  | 0%        |

---

# 7. Phân tích kết quả

Từ kết quả kiểm thử có thể rút ra một số nhận xét:

- Website phản hồi khá nhanh khi số lượng người dùng thấp.
- Khi số lượng người dùng tăng lên, thời gian phản hồi cũng tăng do hệ thống phải xử lý nhiều request hơn.
- Throughput tăng khi số lượng request tăng lên.
- Trong quá trình kiểm thử không xuất hiện lỗi, cho thấy hệ thống hoạt động ổn định.

Nhìn chung, website có khả năng xử lý tốt với mức tải trung bình.

---

# 8. Kết luận

Qua bài thực hành này, chúng ta đã sử dụng công cụ **Apache JMeter** để thực hiện kiểm thử hiệu năng của một website.

Ba kịch bản kiểm thử đã được thiết kế để mô phỏng các mức tải khác nhau của người dùng. Kết quả cho thấy hệ thống có khả năng xử lý ổn định và không xảy ra lỗi trong quá trình kiểm thử.

Apache JMeter là một công cụ mạnh mẽ và hữu ích trong việc đánh giá hiệu năng của các ứng dụng web.

---

# 9. Cấu trúc thư mục

```
jmeter/
│
├── testplan.jmx
├── sumary.csv
├── screenshots/
│   ├── threadgroup1.png
│   ├── threadgroup2.png
│   ├── threadgroup3.png
│   └── summary_report.png
│
└── README.md
```

---

# 10. Minh chứng

Repository bao gồm các tài liệu và kết quả sau:

- File **JMeter Test Plan (.jmx)**
- File **kết quả kiểm thử (.csv)**
- Ảnh chụp màn hình quá trình kiểm thử
- Báo cáo README.md
