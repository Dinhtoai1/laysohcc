# 🏢 Hệ Thống Quản Lý Hàng Đợi

## 🚀 Cách khởi động

### Khởi động nhanh:
1. Nhấp đúp vào file `start.bat`
2. Hệ thống sẽ tự động cài đặt và khởi động

### Khởi động thủ công:
```bash
npm install
node server.js
```

## 🌐 Truy cập hệ thống

### Từ máy chủ (máy chạy server):
- http://localhost:3000

### Từ các máy khác trong cùng mạng:
- http://[IP-CỦA-MÁY-CHỦ]:3000
- Ví dụ: http://192.168.1.100:3000

## 📱 Các trang chính

| Trang | Đường dẫn | Mô tả |
|-------|-----------|-------|
| Trang chủ | `/` | Chọn dịch vụ và lấy số |
| Nhân viên | `/staff` | Gọi số, gọi lại |
| Quản trị | `/admin` | Quản lý hệ thống |
| Màn hình chính | `/all-counters-display` | Hiển thị tất cả quầy + âm thanh |
| Màn hình số | `/number-display` | Hiển thị số hiện tại |

## 🔧 Cấu hình mạng

### Đối với mạng LAN:
1. Đảm bảo tất cả máy trong cùng mạng WiFi/LAN
2. Tắt Windows Firewall hoặc cho phép port 3000
3. Kiểm tra IP máy chủ: `ipconfig` (Windows) hoặc `ip addr` (Linux)

### Để mở port 3000 trên Windows:
```cmd
netsh advfirewall firewall add rule name="Node.js App" dir=in action=allow protocol=TCP localport=3000
```

## 🌍 Triển khai lên Internet

### Cách 1: Sử dụng ngrok (miễn phí, tạm thời)
```bash
# Cài đặt ngrok
npm install -g ngrok

# Chạy server
node server.js

# Mở terminal khác và chạy:
ngrok http 3000
```

### Cách 2: VPS/Cloud hosting
- **Heroku**: Miễn phí (với giới hạn)
- **Vercel**: Miễn phí cho static sites
- **DigitalOcean**: $5/tháng
- **AWS EC2**: Free tier 1 năm

### Cách 3: Tự host với Dynamic DNS
- Sử dụng No-IP hoặc DuckDNS
- Cấu hình router port forwarding
- Thiết lập DDNS

## 🔒 Bảo mật

### Cho mạng LAN:
- Chỉ cho phép truy cập từ các IP đáng tin cậy
- Sử dụng mật khẩu mạnh cho admin

### Cho Internet:
- Sử dụng HTTPS
- Thiết lập authentication
- Cấu hình firewall
- Backup dữ liệu thường xuyên

## 🛠️ Yêu cầu hệ thống

- Node.js 14+ 
- RAM: 512MB+
- Ổ cứng: 100MB+
- Windows/Linux/macOS

## 📞 Hỗ trợ

Nếu gặp vấn đề:
1. Kiểm tra Node.js đã cài đặt: `node --version`
2. Kiểm tra port 3000 có bị chiếm: `netstat -an | findstr 3000`
3. Kiểm tra firewall và antivirus
4. Restart máy và thử lại
# laysohcc
