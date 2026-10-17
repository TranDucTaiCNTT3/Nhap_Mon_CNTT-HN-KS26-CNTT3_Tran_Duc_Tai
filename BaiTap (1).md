# 🚀 Smart-Farm – Hệ thống trang trại thông minh

## 1. Mô tả dự án

Smart-Farm là hệ thống IoT giúp người nông dân giám sát môi trường và tự động tưới cây tại trang trại Lan.

**Mục tiêu:** Tiết kiệm nước, giảm công sức và hỗ trợ chăm sóc cây hiệu quả.

## 2. Hướng dẫn cài đặt

1.  Kết nối cảm biến nhiệt độ và độ ẩm đất với bộ điều khiển.
    
2.  Kết nối bộ điều khiển với mạng.
    
3.  Cấu hình ngưỡng nhiệt độ và độ ẩm phù hợp.
    
4.  Kiểm tra máy bơm trước khi vận hành.
    
## 3. Tính năng

-   Thu thập dữ liệu cảm biến.
    
-   Theo dõi nhiệt độ và độ ẩm đất.
    
-   Tự động điều khiển máy bơm theo điều kiện cài đặt.
    
-   Gửi cảnh báo khi cảm biến gặp lỗi.
    

## 4. Bảng thông số hệ thống


## 4. Bảng thông số hệ thống

| Thông số | Giá trị minh họa | Ý nghĩa |
|---|---|---|
| Nhiệt độ | 28,6°C | Theo dõi nhiệt độ môi trường |
| Độ ẩm không khí | 78% | Đánh giá độ ẩm không khí |
| Độ ẩm đất | 65% | Theo dõi độ ẩm đất |
| Ánh sáng | 1200 lux | Theo dõi cường độ ánh sáng |
| Kết nối | Wi-Fi/Internet | Truyền dữ liệu lên hệ thống |
| Thiết bị | Máy bơm, quạt, đèn | Điều khiển tự động |


## 5. Sơ đồ hệ thống


![Ảnh Sơ Đồ Hệ Thống](![](blob:https://chatgpt.com/49bd3a09-5b60-48da-bfa5-8774958c1f84))

Cảm biến → Bộ điều khiển IoT → Máy bơm  
　　　　　　　　　↓  
　　　　　　Ứng dụng giám sát

## 6. Chu kỳ Fetch–Decode–Execute

 **Fetch:** CPU lấy lệnh cần thực hiện từ bộ nhớ.
 
 **Decode:** CPU giải mã lệnh để xác định thao tác cần thực hiện.

 **Execute:** CPU thực hiện lệnh. Trong hệ thống, bộ điều khiển xử lý điều kiện tưới và điều khiển máy bơm theo chương trình.

## 7. Mô hình kim tự tháp DIKW

```
             /    \
            /      \ 
           / Wisdom \       Quyết định tưới phù hợp
          /----------\
         / Knowledge  \     Hiểu cây có thể thiếu nước
        /--------------\
       /  Information   \   Nhiệt độ cao, đất khô
      /------------------\
     /       Data         \ Nhiệt độ 36°C, độ ẩm 25%
    /______________________\
```

-   **Data (Dữ liệu):** Nhiệt độ 36°C, độ ẩm đất 25%.
    
-   **Information (Thông tin):** Nhiệt độ cao và đất đang khô.
    
-   **Knowledge (Tri thức):** Điều kiện này có thể làm cây thiếu nước.
    
-   **Wisdom (Trí tuệ):** Quyết định tưới khi phù hợp, tránh tưới quá nhiều.
    

## 8. Lưu ý an toàn

-   Kiểm tra cảm biến và máy bơm định kỳ.
    
-   Nếu RAM gần đầy do nhật ký, kiểm tra tiến trình và dung lượng log.
    
-   Thiết lập xoay vòng log hoặc lưu trữ log cũ để hạn chế chiếm bộ nhớ.
    
-   Sao lưu log cần thiết trước khi xóa; chỉ xóa log cũ đã xác nhận không còn cần thiết.
    
-   Không xóa toàn bộ dữ liệu hệ thống hoặc tắt dịch vụ quan trọng để giải phóng RAM.
