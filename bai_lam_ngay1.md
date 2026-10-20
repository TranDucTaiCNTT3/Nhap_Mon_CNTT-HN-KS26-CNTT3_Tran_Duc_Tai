# BÀI LÀM – ÔN TẬP NGÀY 1

- **Họ tên:** Trần Đức Tài
- **Lớp:** HNKS26CNTT3
- **Link repository:*https://github.com/TranDucTaiCNTT3/Nhap_Mon_CNTT-HN-KS26-CNTT3_Tran_Duc_Tai* 
- **Hệ điều hành (Windows/macOS):** Windows 

## Phần A. Tổ chức thư mục bằng GUI

> Phần A được chấm qua kết quả B1 (tên thư mục gốc) và kết quả liệt kê toàn bộ dự án B8 ở Phần B, không cần ghi thêm ở đây.

## Phần B. Thao tác bằng CLI

### Các lệnh đã chạy (B1–B7)

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
pwd
ls 
mv .\lich_hoc.txt .\docs\
mv .\logo_trung_tam.PNG .\media\ ; mv .\anh_lop_hoc.JPG .\media\
cp .\media\logo_trung_tam.PNG .\archive\
rm .\temp_201.tmp
rm .\temp_202.tmp
cd logs
ls 
cd ..
cd docs
Copy-Item ..\media\anh_lop_hoc.JPG ..\archive\
cd .. 
Get-ChildItem -Recurse -Force
```

### Kết quả B1 (pwd)

```text
Path
----
C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh

Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh
```

### Kết quả liệt kê toàn bộ dự án – B8 (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/20/2026  10:28 PM                archive
d-----        10/20/2026  10:21 PM                data
d-----        10/20/2026  10:25 PM                docs
d-----        10/20/2026  10:21 PM                logs
d-----        10/20/2026  10:26 PM                media
------        10/19/2026  10:04 AM             83 .env
-a----        10/19/2026  10:04 AM            902 bai_lam_ngay1.md


    Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh\archive


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026  10:04 AM          13559 anh_lop_hoc.JPG
-a----        10/19/2026  10:04 AM           5184 logo_trung_tam.PNG


    Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026  10:04 AM           5070 hoc_vien_khoa_3.xlsx


    Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026  10:04 AM             67 lich_hoc.txt


    Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026  10:04 AM           1072 access.log


    Directory: C:\LamBaiTap\starter-kit\Trung Tam Tieng Anh\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026  10:04 AM          13559 anh_lop_hoc.JPG
-a----        10/19/2026  10:04 AM           5184 logo_trung_tam.PNG
```

## Tự chấm (điền sau khi có đáp án)

- **Điểm tự chấm:** ..../100
- **Lỗi mình đã mắc và cách sửa:**
