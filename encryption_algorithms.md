# Các thuật toán mã hóa và chế độ

## AES (Advanced Encryption Standard)
- Thuật toán mã hóa đối xứng hiện đại.
- Phổ biến với độ dài khóa **128-bit** hoặc **256-bit**.

![](./Encryption_Algorithms/aes.png)

---

## AES-128-CBC / AES-256-CBC
- **CBC (Cipher Block Chaining) Mode**: Mã hóa khối nối tiếp, mỗi khối được mã hóa dựa trên khối trước.
- Sử dụng khóa **128-bit** hoặc **256-bit**.

![](./Encryption_Algorithms/aes_cbc.png)

---

## CBC Mode
- Chế độ mã hóa khối, cần IV (Vector khởi tạo) để tăng tính bảo mật.

![](./Encryption_Algorithms/cbc_mode.png)

---

## Random hóa IV trong AES-CBC
- Vector khởi tạo (IV) được tạo ngẫu nhiên.
- Đảm bảo tính duy nhất của dữ liệu mã hóa trong CBC.

![](./Encryption_Algorithms/aes_cbc_iv.png)

---

## 3DES
- Thuật toán mã hóa đối xứng cũ hơn AES.
- Kém an toàn hơn và tốc độ chậm hơn.

![](./Encryption_Algorithms/3des.png)

---

## RC4
- Thuật toán mã hóa dòng (stream cipher) cũ.
- Hiện không an toàn và không được khuyến nghị sử dụng.

![](./Encryption_Algorithms/rc4.png)

---

## AES-GCM (Galois/Counter Mode)
- Chế độ mã hóa hiện đại.
- Kết hợp mã hóa và xác thực (**AEAD - Authenticated Encryption with Associated Data**).
- Ví dụ: `AES_256_GCM`.

![](./Encryption_Algorithms/aes_gcm.png)

---

## AEAD Cipher (Authenticated Encryption with Associated Data)
- Loại mã hóa kết hợp **mã hóa** và **xác thực**.
- Ví dụ: **AES-GCM**, **CHACHA20-POLY1305**.

![](./Encryption_Algorithms/aead_cipher.png)

---

## CHACHA20 / CHACHA20-POLY1305
- Thuật toán mã hóa dòng hiện đại.
- Thay thế **RC4**.
- Thường kết hợp với **Poly1305** để xác thực dữ liệu.

![](./Encryption_Algorithms/chacha_20.png)

