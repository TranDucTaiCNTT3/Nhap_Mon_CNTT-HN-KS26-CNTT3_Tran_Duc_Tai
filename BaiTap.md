# 🌱 Hướng dẫn cài đặt cảm biến độ ẩm

## 1. Tổng quan 

Cảm biến độ ẩm giúp theo dõi độ ẩm không khí trong nhà lưới , đảm bảo môi trường tối ưu cho Lan phát triển 

**THIẾT BỊ CẦN CHUẨN BỊ**

- Cảm biến độ ẩm (DHT22 / AM2302)
- Raspberry Pi / Jeston / SoC
- Dây nối Dupont
- Tua vít , băng keo , ốc vít 
- Thẻ nhớ đã cài hệ thống 

## 2. Các bước cài đặt 

### 1. Cập nhật hệ thống

Mở Terminal và cập nhật danh sách gói.

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Cài đặt thư viện cho cảm biến DHT22

Cài đặt thư viện đọc dữ liệu từ cảm biến.

```bash
sudo apt install -y git python3-pip
sudo pip3 install Adafruit_DHT
```

### 3. Kích hoạt giao tiếp 1-Wire (nếu dùng DHT22)

Bật giao tiếp 1-Wire trên hệ thống.

```bash
sudo raspi-config
```

Chọn `Interface Options` → `1-Wire` → `Enable` nếu thiết bị và cảm biến của bạn yêu cầu.

### 4. Kiểm tra module đã được nhận

Sau khi cấu hình, kiểm tra thiết bị.

```bash
ls /sys/bus/w1/devices/
```

Kết quả có thể có dạng `28-xxxxxxxx` với cảm biến tương thích 1-Wire.

### 5. Chạy thử chương trình đọc cảm biến

Tải mã mẫu và chuyển đến thư mục ví dụ.

```bash
git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT/examples
```

Chạy chương trình mẫu:

```bash
python3 AdafruitDHT.py 22 4
```

Trong đó, `22` là loại cảm biến DHT22 và `4` là số chân GPIO ví dụ được sử dụng.

### 6. Tự động chạy khi khởi động (tùy chọn)

Mở crontab:

```bash
crontab -e
```

Thêm dòng sau để chạy chương trình mỗi 5 phút:

```bash
*/5 * * * * python3 /home/pi/read_dht22.py
```

Thay đường dẫn bằng vị trí thực tế của chương trình trên thiết bị.
## 3. Bảng so sánh cảm biến

| Tiêu chí | Cảm biến cũ | Cảm biến mới |
|---|---|---|
| Nguyên lý | Điện trở | Điện dung |
| Độ bền | Dễ bị ăn mòn hơn | Chống ăn mòn tốt hơn |
| Chi phí | Thấp | Cao hơn |
| Bảo trì | Thường xuyên hơn | Ít thường xuyên hơn |

## 4. Checklist kiểm tra thiết bị

- [x] Kiểm tra nguồn điện.
- [x] Kết nối cảm biến với bộ điều khiển.
- [x] Vị trí đặt máy đã ổn chưa .
- [ ] Đọc thử dữ liệu độ ẩm.
- [ ] Kiểm tra máy bơm.
- [ ] Xác nhận hệ thống hoạt động bình thường.

