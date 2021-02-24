## Kong + Konga + Webserver nginx + Sample service

Đầu tiên, khởi động `Kong` + `Konga`
- Chaỵ lệnh `docker-compose up -d`
- Sau khi hoàn thành, kiểm tra bằng cách gửi request đến Kong admin: `curl -i http://localhost:8001`
- Tiếp tục, truy cập `http://localhost:1337` để dùng Kong bằng trình duyệt Konga
- Đăng nhập vào Konga bằng tài khoản dành cho Admin (`username`: `admin`, `password`: `adminadminadmin`)
- Tạo một `connection` đến `Kong admin` thông qua url `http://${ip_kong_admin}:8001`

![](https://i.imgur.com/SzTt0FH.png)

Khởi động, một `sample service` để kiểm thử `Kong Gateway`
- Đầu tiên, đi đến thư mục `web-server` bằng lệnh: `cd web-server`
- Và chạy lệnh: `docker-compose up -d` để khởi tạo một web server như thực tế (dùng `nginx` làm `reverse proxy`) và một service sample
