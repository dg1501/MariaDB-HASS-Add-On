## PHÁT TRIỂN ỨNG DỤNG VỚI MÃ NGUỒN MỞ (MARIADB + HASS + ADD ON)
### HỌ TÊN: NGUYỄN ĐỨC DƯƠNG
### LỚP: K58KTP
### MSSV: K225480106093

---

### PHẦN 1: CHUẨN BỊ

1. Mở Ubuntu (Máy ảo)

- Mở terminal -> Kiểm tra 

`docker --version`
`docker compose version`

<img width="912" height="684" alt="{5500BDCA-ED36-4507-A320-3D822ABD5689}" src="https://github.com/user-attachments/assets/82f393b2-c8b0-42fd-bf12-4b4d9e04fbfb" /></p>

👉 **Docker (phiên bản 29.1.3): Là nền tảng dùng để đóng gói ứng dụng cùng với tất cả các thư viện và cấu hình cần thiết vào một đơn vị duy nhất gọi là Container, giúp ứng dụng chạy ổn định và đồng nhất trên bất kỳ môi trường máy chủ nào.**

👉 **Docker Compose: Là công cụ giúp bạn quản lý và vận hành nhiều Container cùng một lúc thông qua một tệp cấu hình duy nhất (thường là docker-compose.yml), thay vì phải khởi chạy từng Container bằng các dòng lệnh riêng biệt một cách thủ công.**

---

### PHẦN 2: CÀI HOME ASSISTANT + MARIADB

1. Tạo thư mục project

`mkdir hass-project`

`cd hass-project`

<img width="894" height="666" alt="{2344A989-3F83-45A1-B6E4-D9CC57311891}" src="https://github.com/user-attachments/assets/e5a3217f-ea1f-4e50-a1ef-da3097213e4f" /></p>

2. Tạo file docker-compose.yml

`nano docker-compose.yml`

<img width="1102" height="831" alt="{4F23400B-ED26-4CB8-9547-E3382E0AF1AB}" src="https://github.com/user-attachments/assets/8647a1f5-9d62-475e-a9d6-17c2e2cbaad7" /></p>

3. Chạy hệ thống

`docker compose up -d`

<img width="893" height="672" alt="{43A81BAD-13A2-49A4-AA98-9BAB2F8BADA7}" src="https://github.com/user-attachments/assets/6211e128-193d-4f92-87dc-c95030c2385c" /></p>

4. Kiểm tra

`docker ps`

<img width="894" height="672" alt="{89461C23-807A-4496-96FC-0AF0837553F7}" src="https://github.com/user-attachments/assets/52c24196-7130-4210-aadc-b364543eaf73" /></p>

👉 Phải có:

*hass*

*hass-mariadb*

*hass-nodered*

5. Truy cập Local

👉 Mở Hass `http://IP:8123`

<img width="1920" height="1029" alt="{38F4FC02-C9A3-47DD-B47F-7F91A31154EE}" src="https://github.com/user-attachments/assets/aa98e4d7-404c-4a7b-904e-9a31980706a6" /></p>

👉 Mở Nodered `http://IP:1881`

<img width="1919" height="1022" alt="{943AE448-D52E-4832-9FA2-22D1CC49B56A}" src="https://github.com/user-attachments/assets/675393be-3e07-4c07-b407-0791382553f1" /></p>

---

### PHẦN 3: KẾT NỐI MARIADB

1. Mở file `nano config/configuration.yaml`

<img width="892" height="668" alt="{AA0A94D1-E696-42D7-B578-41691FB9588A}" src="https://github.com/user-attachments/assets/0e2b9944-6314-4e7e-8b81-bc513e99b448" /></p>

2. Restart

`docker restart hass`

<img width="901" height="682" alt="{FE35F921-CC43-4FA3-91DB-2A8B9E15515D}" src="https://github.com/user-attachments/assets/79793c1b-768a-434c-8e17-c99ecc9e572b" /></p>







