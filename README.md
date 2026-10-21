# DE3-WordPress: Website quảng bá sản phẩm Vịt Quay Đạt Tiến

- Sinh viên: Nông Tiến Đạt
- MSSV: DTC245200172
- Đề: Đề 3, WordPress + MySQL + phpMyAdmin

## Kiến trúc
Client → Nginx (HTTPS, reverse proxy) → WordPress → MySQL.
Prometheus, Grafana và các exporter giám sát. Loki và Promtail thu thập log.
Mạng `backend` là internal, chứa MySQL.

## Cách chạy
1. git clone repo, rồi `cd DE3-WordPress`
2. `cp .env.example .env` và điền mật khẩu mạnh
3. Tạo chứng chỉ tự ký (mục 3.2 trong hướng dẫn)
4. `docker compose up -d`

## Địa chỉ truy cập
- Website: https://192.168.77.136
- phpMyAdmin: `ssh -L 8081:127.0.0.1:8081 dat@192.168.77.136`, rồi mở http://127.0.0.1:8081
- Grafana: `ssh -L 3000:127.0.0.1:3000 dat@192.168.77.136`, rồi mở http://127.0.0.1:300
