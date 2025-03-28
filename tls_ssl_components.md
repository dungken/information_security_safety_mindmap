# Thành phần cơ bản trong giao thức TLS/SSL

## Cipher Suite
- Bộ thuật toán mã hóa được sử dụng trong TLS/SSL.
- Bao gồm các thuật toán mã hóa, hash, và trao đổi khóa.
- Ví dụ: `TLS_RSA_WITH_AES_128_CBC_SHA`.

![](./TLS_SSL_Components/cipher_suite.png)

---

## Random Client / Random Server
- Các giá trị ngẫu nhiên do client và server tạo ra.
- Đảm bảo tính duy nhất trong quá trình trao đổi khóa.

![](./TLS_SSL_Components/random_client_server.png)

---

## Master Key / Pre Master Key
- **Pre Master Key**: Được tạo trong quá trình bắt tay TLS.
- **Master Key**: Sinh ra từ Pre Master Key, dùng để tạo các khóa phiên.

![](./TLS_SSL_Components/master_key&pre_master_key.png)

---

## Key Material (Khóa phiên)
- Tập hợp các khóa được tạo từ Master Key.
- Bao gồm **Session Key** và **MAC Key**.

![](./TLS_SSL_Components/key_material.png)

---

## Session Key
- Khóa tạm thời dùng để mã hóa dữ liệu trong một phiên giao tiếp.

![](./TLS_SSL_Components/session_key.png)

---

## MAC Key
- Khóa dùng để tạo **MAC**.
- Đảm bảo tính toàn vẹn dữ liệu.

![](./TLS_SSL_Components/mac_key.png)

---

## Session ID
- Định danh phiên TLS.
- Giúp tái sử dụng kết nối TLS mà không cần bắt tay lại.

![](./TLS_SSL_Components/session_id.png)

---

## ChangeCipherSpec
- Tin nhắn trong TLS.
- Báo hiệu rằng các bên đã sẵn sàng sử dụng bộ mã hóa đã thỏa thuận.

![](./TLS_SSL_Components/change_cipher_spec.png)