**Người dùng có những chức năng gì và hoạt động ra sao?**

* **Đối với Người hiến máu:** Người dùng truy cập cổng thông tin web, đăng ký tài khoản và nhập thông tin cá nhân hoặc đăng nhập nếu đã có tài khoản. Sau đó, họ trả lời bộ câu hỏi khai báo y tế điện tử. Nếu hệ thống kiểm tra lịch sử hiến máu lớn hơn 12 tuần [(Thông tin)](https://www.vinmec.com/vie/bai-viet/thoi-gian-toi-thieu-giua-cac-lan-hien-mau-la-bao-lau-de-dam-bao-suc-khoe-vi), người dùng được phép chọn địa điểm chiến dịch và khung giờ (Time-slot) để đặt lịch hẹn.
* **Đối với Cán bộ y tế:** Sử dụng thiết bị di động hoặc máy tính bảng quét mã QR lịch hẹn của người dân. Cán bộ tiến hành đo đạc và nhập các chỉ số như huyết áp, nhịp tim và lấy máu xét nghiệm (có hợp lệ hay không). Nếu chỉ số hợp lệ, cán bộ nhấn nút "Đồng ý lấy máu", hệ thống sẽ gửi lệnh máy in xuất ra một tem mã vạch để dán lên túi máu.
* **Đối với Kỹ thuật viên xét nghiệm:** Đăng nhập vào phân hệ quản lý kho. Kỹ thuật viên dùng máy quét mã vạch trên túi máu, lấy 3-4 ống máu nhỏ để làm xét nghiệm chuyên sâu và cập nhật kết quả xét nghiệm âm tính hoặc dương tính. Nếu âm tính, kỹ thuật viên gán vị trí lưu trữ (Ví dụ: Tủ lạnh số 02, Ngăn số 04) để đưa vào kho.
* **Đối với Bệnh viện tuyến dưới:** Nhân viên bệnh viện đăng nhập, điền biểu mẫu điện tử xin cấp máu chỉ định rõ mức độ ưu tiên. Hệ thống tại Trung tâm Huyết học sẽ tiếp nhận, chạy thuật toán FEFO để tìm kiếm các túi máu phù hợp nhất, trừ đi số lượng tồn kho và thông báo trạng thái "Đang vận chuyển" về lại màn hình của bệnh viện.

**Những thông tin/đối tượng thực thể mà hệ thống cần xử lý:**

1. **Tài khoản người dùng (User):** Lưu trữ thông tin cá nhân, nhóm máu, lịch sử hiến máu, mật khẩu mã hóa.
2. **Hồ sơ sức khỏe (Health Record):** Lưu trữ các chỉ số sức khỏe của mỗi lần hiến máu.
3. **Chiến dịch (Campaign):** Lưu trữ thông tin địa điểm, thời gian, sức chứa tối đa.
4. **Túi máu (Blood Bag):** Đối tượng quan trọng nhất, lưu trữ mã vạch, ngày lấy máu, ngày hết hạn, trạng thái hiện tại (An toàn, Nhiễm bệnh, Hết hạn, Đã xuất kho).
5. **Yêu cầu cấp phát (Blood Request):** Lưu trữ thông tin bệnh viện yêu cầu, số lượng đơn vị máu cần, thời gian yêu cầu và trạng thái đáp ứng.

**Quan hệ giữa các đối tượng (Thực thể):**

* Một Người hiến máu có thể tham gia nhiều Chiến dịch khác nhau, chỉ cần đủ điều kiện về thời gian.
* Một Chiến dịch có thể tiếp nhận hàng ngàn Người hiến máu đăng ký.
* Một Người hiến máu đóng góp tạo ra một Túi máu trong mỗi lần hiến hợp lệ.
* Một Túi máu chỉ có duy nhất một bộ Hồ sơ sức khỏe và Kết quả xét nghiệm đi kèm.
* Một Yêu cầu cấp phát từ bệnh viện có thể bao gồm nhiều Túi máu khác nhau, nhưng một Túi máu chỉ được cấp phát cho một Yêu cầu cấp phát duy nhất.
