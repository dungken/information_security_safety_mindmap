# Tổng Quan về Mã Hóa và Bảo Mật SSL/TLS

Đây là tài liệu tổng quan về các khái niệm cơ bản liên quan đến mã hóa và bảo mật SSL/TLS, bao gồm các thuật toán, giao thức và các cơ chế bảo mật trong việc trao đổi thông tin an toàn qua mạng.

## 0. SSL/TLS
Tổng quan về SSL/TLS và các phiên bản của nó.

[Chi tiết về SSL/TLS](./ssl_tls.md)


## 1. Khái Niệm Cơ Bản về Mã Hóa và Bảo Mật

Mã hóa là quá trình biến đổi dữ liệu thành một dạng không thể đọc được nhằm bảo vệ thông tin trong quá trình truyền tải. Bảo mật trong giao tiếp mạng giúp đảm bảo rằng dữ liệu không bị rò rỉ hoặc sửa đổi bởi các bên không mong muốn.

- **Khóa công khai / Khóa riêng tư**: Dùng trong mã hóa bất đối xứng, nơi khóa công khai mã hóa và khóa riêng tư giải mã.
- **RSA**: Thuật toán mã hóa bất đối xứng phổ biến.
- **Diffie-Hellman**: Phương pháp trao đổi khóa tạo ra một khóa chung mà không cần chia sẻ trực tiếp qua mạng.
- **Thuật toán mã hóa yếu**: Các thuật toán với độ dài khóa ngắn dễ bị tấn công.
- **Thuật toán hash**: Hàm băm như SHA-1, SHA-256 dùng để kiểm tra tính toàn vẹn.
- **MAC**: Mã xác thực thông điệp để đảm bảo tính toàn vẹn của dữ liệu.
- **Chứng chỉ số**: Giấy chứng nhận xác thực danh tính các thực thể sử dụng khóa công khai.

[Chi tiết về Khái Niệm Cơ Bản về Mã Hóa và Bảo Mật](./security_fundamentals.md)


## 2. Thành Phần Cơ Bản trong Giao Thức TLS/SSL

Giao thức TLS/SSL giúp bảo vệ dữ liệu trong quá trình truyền tải qua mạng bằng cách sử dụng các thuật toán mã hóa và xác thực.

- **Cipher Suite**: Bộ thuật toán mã hóa và trao đổi khóa được sử dụng trong TLS.
- **Master Key / Pre Master Key**: Khóa chính dùng để sinh ra các khóa phiên trong quá trình bắt tay.
- **Session Key**: Khóa tạm thời dùng trong phiên giao tiếp để mã hóa dữ liệu.
- **ChangeCipherSpec**: Tin nhắn báo hiệu sự thay đổi trong bộ mã hóa.

[Chi tiết về Thành Phần Cơ Bản trong Giao Thức TLS/SSL](./tls_ssl_components.md)

## 3. Các Thuật Toán Mã Hóa và Chế Độ

Các thuật toán mã hóa và chế độ mã hóa trong TLS đóng vai trò quan trọng trong việc bảo vệ dữ liệu trong quá trình trao đổi.

- **AES**: Thuật toán mã hóa đối xứng hiện đại với độ dài khóa 128-bit hoặc 256-bit.
- **AES-CBC**: Chế độ mã hóa khối nối tiếp.
- **3DES**: Thuật toán mã hóa đối xứng cũ, kém an toàn hơn AES.
- **RC4**: Thuật toán mã hóa dòng cũ, không còn an toàn.
- **AES-GCM**: Chế độ mã hóa kết hợp mã hóa và xác thực.
- **CHACHA20**: Thuật toán mã hóa dòng hiện đại thay thế RC4.

[Chi tiết về Các Thuật Toán Mã Hóa và Chế Độ](./encryption_algorithms.md)

## 4. Quá Trình Trao Đổi Khóa và Bảo Mật Nâng Cao

Quá trình trao đổi khóa trong TLS là cốt lõi để đảm bảo sự bảo mật của các phiên giao tiếp qua mạng.

- **ECDHE Key Exchange**: Phiên bản hiện đại của Diffie-Hellman, sử dụng đường cong elip.
- **Forward Secrecy**: Đảm bảo các phiên giao tiếp trước đó vẫn an toàn ngay cả khi khóa dài hạn bị lộ.
- **PRF**: Hàm tạo số ngẫu nhiên giả để sinh khóa từ Master Key.

[Chi tiết về Quá Trình Trao Đổi Khóa và Bảo Mật Nâng Cao](./key_exchange_security.md)

## 5. Các Cuộc Tấn Công và Lỗ Hổng

Các cuộc tấn công và lỗ hổng trong giao thức SSL/TLS có thể phá vỡ bảo mật của dữ liệu trao đổi.

- **MITM (Man-in-the-Middle)**: Kẻ tấn công chặn và sửa đổi thông tin giữa client và server.
- **Replay Attack**: Tấn công gửi lại dữ liệu hợp lệ đã bị chặn.
- **BEAST, POODLE Attack**: Khai thác lỗ hổng trong CBC Mode của SSL/TLS.
- **Padding Oracle Attack**: Khai thác cách hệ thống xử lý padding trong mã hóa khối.

[Chi tiết về  Các Cuộc Tấn Công và Lỗ Hổng](./security_threads_vulnerabilities.md)

## 6. Các Khái Niệm TLS Hiện Đại và Tối Ưu Hóa

TLS hiện đại cung cấp các tính năng bảo mật mạnh mẽ để bảo vệ dữ liệu trong quá trình trao đổi.

- **TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384**: Cipher suite hiện đại với các thuật toán mạnh mẽ.
- **Fragmentation**: Chia nhỏ dữ liệu thành các gói trong quá trình truyền tải.
- **Round-trip**: Thời gian giao tiếp giữa client và server trong quá trình bắt tay.
- **0-RTT / 1-RTT**: Các chế độ bắt tay TLS cho phép truyền tải nhanh hơn, nhưng ít an toàn hơn.

[Chi tiết về  Các Khái Niệm TLS Hiện Đại và Tối Ưu Hóa](./modern_tls_optimization.md)
