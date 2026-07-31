# Project: Phishing Attack Investigation

## Introduction

Tấn công phishing (lừa đảo trực tuyến) là một trong những mối đe dọa an ninh mạng phổ biến, trong đó kẻ tấn công giả mạo một tổ chức hoặc cá nhân đáng tin cậy nhằm đánh lừa người dùng cung cấp thông tin nhạy cảm. Dự án này nhằm trang bị các kỹ năng cần thiết để nhận diện, điều tra và ứng phó hiệu quả với các cuộc tấn công phishing.

## Lab Set-up và các Tools cần sử dụng 

Để tiến hành điều tra một cuộc tấn công phishing, bạn cần xây dựng một môi trường mô phỏng bao gồm các công cụ phục vụ cho việc phân tích email. Dưới đây là cấu hình môi trường chi tiết:

### 1. Email Server 

**Mô tả**: Thiết lập một máy chủ email cục bộ (local email server) hoặc sử dụng dịch vụ mô phỏng email để gửi và nhận thư điện tử. Điều này cho phép bạn phân tích các email phishing một cách an toàn mà không làm lộ hoặc đặt tài khoản email thật của mình trước các rủi ro tiềm ẩn.

**Tools**:

- **MailCatcher**: Đây là một máy chủ SMTP đơn giản dùng để tiếp nhận và lưu trữ các email gửi đến, cho phép người dùng xem, kiểm tra và phân tích nội dung email ở giai đoạn sau.

### 2. Các mẫu email lừa đảo (Phishing Email)

**Mô tả**: Thu thập một bộ mẫu email lừa đảo để phân tích. Các mẫu này có thể được lấy từ các kho lưu trữ công cộng, diễn đàn an ninh mạng hoặc được tạo ra cho mục đích giáo dục.

### 3. Công cụ phân tích email
- **Thunderbird** : Trình quản lý email mã nguồn mở do Mozilla phát triển, hỗ trợ nhiều tài khoản email và có các tính năng quản lý email mạnh mẽ.
- **Email Header Analysis Tools**: Các công cụ trực tuyến như MXToolbox hoặc EmailHeaders.net có thể phân tích và đánh giá tiêu đề email.

## Thiết lập môi trường thực nghiệm

### 1. Cài đặt thunderbird

- Tải xuống và cài đặt Thunderbird từ [trang web chính thức](https://www.thunderbird.net/).
- Thiết lập tài khoản email bằng cách sử dụng máy chủ email thực hoặc máy chủ email ảo.

### 2. Thiết lập máy chủ email

- Cài đặt Mailcatcher:
  ```sh
  gem install mailcatcher
  mailcatcher

Truy cập MailCatcher tại http://127.0.0.1:1080/ để xem các email đã được thu thập.

### 3. Thu thập các mẫu email lừa đảo

Tải xuống các mẫu tấn công lừa đảo từ PhishTank hoặc OpenPhish. Nhập các mẫu này vào Thunderbird để phân tích.

### 4. phân tích và điều tra email phishing

- Xác định và ghi lại các dấu hiệu lừa đảo trực tuyến phổ biến
- Phân tích tiêu đề email (Địa chỉ IP của người gửi, thông tin máy chủ đã được xác định,  sự sai lệch nào trong thông tin của người gửi)
- Điều tra các liên kết đáng ngờ (các liên kết URL, tệp đính kèm)
- Thực hiện ứng phó khi có sự cố xảy ra

