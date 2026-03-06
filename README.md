# Dự án Kiểm thử Tự động cho Website AirBnB

## Giới thiệu tổng quan
Dự án này tập trung vào việc áp dụng kiểm thử tự động cho nền tảng đặt phòng trực tuyến AirBnB. Mục tiêu chính là đảm bảo chất lượng, tính ổn định và tính chính xác của các chức năng cốt lõi trên hệ thống web. Quá trình kiểm thử bao gồm việc lập kế hoạch chi tiết, thiết kế kịch bản chuyên sâu và tiến hành tự động hóa các thao tác người dùng bằng khung làm việc Playwright kết hợp với Java.

## Thông tin dự án
- Tên dự án: Kiểm thử tự động cho website AirBnB
- Thời gian bắt đầu: 10/11/2025
- Thời gian kết thúc: 24/12/2025
- Đối tượng đánh giá: Nền tảng web AirBnB
- Loại hình thực hiện: Kiểm thử chức năng, Kiểm thử tự động (UI Automation Testing)

## Công cụ và Công nghệ sử dụng
Dự án được xây dựng dựa trên các công cụ và thư viện kỹ thuật chuyên dụng trong lĩnh vực kiểm thử phần mềm, cụ thể bao gồm:
- Ngôn ngữ lập trình: Java 23
- Khung kiểm thử tự động: Playwright (phiên bản 1.45.1)
- Khung quản lý và tổ chức kịch bản: TestNG (phiên bản 7.8.0)
- Trình quản lý dự án và đóng gói: Apache Maven
- Báo cáo kết quả kiểm thử: ExtentReports (phiên bản 5.1.1)
- Trình ghi log hệ thống: SLF4J

## Cấu trúc lưu trữ
Mã nguồn dự án được tổ chức chặt chẽ theo cấu trúc chuẩn của Maven, giúp quá trình bảo trì và mở rộng sau này trở nên dễ dàng hơn:
- /src/main: Chứa mã nguồn thiết lập cấu hình cơ sở, quản lý trình duyệt và các định nghĩa phần tử giao diện theo mô hình Page Object Model (POM).
- /src/test: Lưu trữ danh sách các kịch bản kiểm thử tự động đã được chuyển thể qua ngôn ngữ lập trình cùng với TestNG.
- /documentation: Không gian lưu trữ dữ liệu phân tích, bao gồm Kế hoạch kiểm thử (Test Plan), Các testcase chi tiết và Báo cáo tổng kết chạy test. Có đầy đủ định dạng văn bản (Word, Excel), file thuyết trình (PowerPoint) và PDF.
- /reports: Chứa các tệp HTML báo cáo kết quả trích xuất tự động qua ExtentReports sau mỗi lần thực thi bộ kiểm thử.
- testng.xml: Tệp cài đặt trung tâm của TestNG giúp linh hoạt lựa chọn nhóm chức năng và chạy hàng loạt Test Cases.
- pom.xml: Tệp quản lý các thư viện và thiết lập quan trọng của Maven đối với dự án.

## Hướng dẫn cài đặt và sử dụng

### 1. Yêu cầu hệ thống ban đầu
- Máy tính hệ điều hành Windows/macOS/Linux đã cài đặt sẵn Java Development Kit (JDK 23).
- Cài đặt Apache Maven và cấu hình đầy đủ biến môi trường.
- Một môi trường soạn thảo mã nguồn tích hợp (IDE như IntelliJ IDEA hoặc Eclipse).

### 2. Cài đặt dự án
Bước 1: Tải toàn bộ mã nguồn dự án về máy tính cấu hình cục bộ.
Bước 2: Sử dụng IDE để mở thư mục dự án.
Bước 3: Mở cửa sổ dòng lệnh (terminal) tại thư mục gốc của dự án (có chứa file pom.xml) và tiến hành tải các thư viện bằng câu lệnh:
mvn clean install -DskipTests

### 3. Thực thi kịch bản
Để khởi chạy hệ thống phân tích và chạy test động qua trình duyệt, bạn có thể áp dụng một trong hai phương pháp dưới đây:

Phương pháp 1: Chạy trực tiếp qua giao diện dòng lệnh bằng công cụ Maven
mvn test

Phương pháp 2: Mở file testng.xml bên trong giao diện làm việc của IDE, nhấp chuột phải và lựa chọn lệnh "Run...".

### 4. Đánh giá báo cáo
Sau khi quá trình kiểm tra chức năng hoàn thành, bộ máy báo cáo sẽ tổng hợp kết quả từng bước chạy thành các biểu đồ trực quan và văn bản (Pass/Fail/Skip).
Truy cập vào thư mục /reports trong máy, sau đó mở tệp báo cáo định dạng HTML hiển thị gần nhất trên trình duyệt web để rà soát chất lượng chức năng.

## Tài liệu đính kèm
Đối với các cá nhân tham gia vào dự án, bạn có thể tra cứu toàn bộ hồ sơ thiết kế kiểm thử trong thư mục /documentation của kho lưu trữ này. Bao gồm:
- Kế hoạch thiết kế và phạm vi kiểm thử
- Bảng rà soát kịch bản thiết kế phần mềm
- Tệp báo cáo đầu ra chi tiết theo các giai đoạn
- Bảng trình bày thuyết minh về toàn bộ phương pháp thực hiện dự án
