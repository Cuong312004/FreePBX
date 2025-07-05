
# 📞 FreePBX Asterisk IP PBX System

> Đồ án môn học **Công nghệ truyền thông đa phương tiện** – NT536.P21  
> Trường Đại học Công nghệ Thông tin – ĐHQG TP.HCM  
> Nhóm 17: Lưu Quốc Cường, Nguyễn Phạm Tiến Đạt, Lê Minh Hoàng, Bùi Minh Quân  

## 🎯 Mục tiêu dự án

Xây dựng một hệ thống **Tổng đài IP (IP PBX)** sử dụng phần mềm mã nguồn mở **FreePBX** và **Asterisk**. Hệ thống đáp ứng các chức năng của một tổng đài hiện đại như:

- Liên lạc nội bộ (extension-to-extension)
- Gọi ra ngoài công ty
- Nhận cuộc gọi từ số public
- Hệ thống IVR trả lời tự động
- Ghi âm và hộp thư thoại
- Hàng đợi, nhóm gọi (ring all, ring hunt)
- Blacklist, nhạc chờ, follow-me...

## 🛠️ Công cụ và môi trường

- **FreePBX**: Giao diện đồ họa để cấu hình tổng đài
- **Asterisk**: Engine xử lý cuộc gọi
- **Softphone**: Zoiper, 3CX, MicroSIP để thực hiện cuộc gọi
- **Môi trường ảo hóa**: VMware để mô phỏng hạ tầng tổng đài

## 🧱 Kiến trúc hệ thống

![Asterisk Architecture](https://github.com/Cuong312004/FreePBX/blob/main/Asterisk_Architecture.png)

## 🔧 Các chức năng nổi bật

| Chức năng | Mô tả |
|----------|--------|
| 📞 Gọi nội bộ | Gọi giữa các máy nhánh (extensions) |
| 📤 Gọi ra ngoài | Gọi qua số `0951000017` với prefix `9` |
| 📥 Gọi từ ngoài | Gọi đến số công ty `0952014317`, IVR tự động phát |
| 🔊 IVR | Người gọi có thể bấm phím để đến đúng phòng ban |
| 🏢 Hội nghị | Extension `4174` dùng để họp nội bộ với mật khẩu |
| 📦 Ring Group | Gọi đến phòng kỹ thuật (ring hunt) / bán hàng (ring all) |
| 📬 Voicemail | Lưu và phát lại lời nhắn cho Giám đốc |
| 📛 Blacklist | Tự động từ chối cuộc gọi từ số bị chặn |
| 🎶 Music on Hold | Phát nhạc chờ khi máy bận hoặc đang giữ |
| 📅 Time Condition | Chặn cuộc gọi sau giờ hành chính |
| 🔁 Follow Me | Chuyển tiếp cuộc gọi qua nhiều thiết bị |

## 📂 Cấu hình quan trọng

- `iax_custom.conf` và `pjsip_custom.conf`: Định nghĩa máy nhánh
- `extensions_custom.conf`: Dialplan cấu hình các luồng cuộc gọi
- `queues_custom.conf`: Hàng đợi cuộc gọi
- `blacklist.conf`: Danh sách số bị chặn
- `voicemail_custom.conf`: Cấu hình hộp thư thoại
- `musiconhold_custom.conf`: Nhạc chờ khi giữ máy

## 📈 Kết quả triển khai

- ✅ Hệ thống gọi hoạt động ổn định, đúng chức năng
- ✅ Phản hồi âm thanh rõ ràng, logic IVR dễ hiểu
- ✅ Triển khai và kiểm thử trên nhiều softphone khác nhau
- ✅ Áp dụng được lý thuyết VoIP và IP PBX vào thực tế

## 🚀 Hướng phát triển

- Tăng cường bảo mật SIP bằng TLS/SRTP
- Triển khai hệ thống trên cloud (AWS, Azure)
- Tích hợp xử lý âm thanh và chatbot bằng NLP
- Giao diện web thống kê lịch sử và phân tích cuộc gọi

## 📚 Tài liệu tham khảo

- Tài liệu bài giảng môn học – Trường ĐH CNTT
- [Zoiper Softphone](https://www.zoiper.com)
- [3CX Softphone](https://www.3cx.com/voip/softphone/)
- Asterisk & FreePBX Documentation

---

> 🎓 Đồ án thực hiện tháng 05 năm 2025 – Trường ĐH Công Nghệ Thông Tin – ĐHQG HCM
> Báo cáo chi tiết tại FreePBX_report.pdf
