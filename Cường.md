#### 3. Mô hình nghiệp vụ bằng UML

**Xác định các Actor của hệ thống:**

1. Người hiến máu (Donor)
2. Cán bộ y tế (Medical Staff)
3. Kỹ thuật viên xét nghiệm & Kho (Lab Technician)
4. Bệnh viện tuyến dưới (Hospital)
5. Ban Quản trị (Admin)

**Các Use Case chi tiết cho từng Actor:**

* **Actor: Người hiến máu**
* UC01: Đăng ký tài khoản hệ thống.
* UC02: Đăng nhập / Đăng xuất.
* UC03: Quản lý hồ sơ cá nhân.
* UC04: Điền tờ khai y tế điện tử.
* UC05: Tra cứu chiến dịch và đặt lịch hẹn hiến máu.
* UC06: Xem lịch sử hiến máu và tải chứng nhận điện tử.


* **Actor: Cán bộ y tế**
* UC07: Quét mã QR kiểm tra thông tin lịch hẹn.
* UC08: Ghi nhận chỉ số sinh tồn lâm sàng.
* UC09: Từ chối hoặc Phê duyệt người dân đủ điều kiện lấy máu.
* UC10: Khởi tạo mã định danh (Barcode) cho túi máu vật lý.


* **Actor: Kỹ thuật viên xét nghiệm & Kho**
* UC11: Ghi nhận kết quả điều chế phẩm máu (xét nghiệm) (Chương 4 mục 2 https://luatvietnam.vn/y-te/thong-tu-26-2013-tt-byt-bo-y-te-82981-d1.html).
* UC12: Cập nhật kết quả xét nghiệm 5 bệnh truyền nhiễm cho túi máu.
* UC13: Cập nhật vị trí lưu trữ túi máu vào kho lạnh.
* UC14: Xem biểu đồ thống kê tồn kho theo thời gian thực.
* UC15: Xác nhận phiếu xuất kho máu.
* UC16: Lập phiếu và xác nhận tiêu hủy túi máu không đạt tiêu chuẩn (Chương 4 mục 1 điều 18 khoản 5 https://luatvietnam.vn/y-te/thong-tu-26-2013-tt-byt-bo-y-te-82981-d1.html).


* **Actor: Bệnh viện tuyến dưới**
* UC17: Tạo lập đơn yêu cầu cấp phát máu khẩn cấp hoặc bình thường.
* UC18: Theo dõi trạng thái tiến độ của đơn yêu cầu cấp máu.
* UC19: Xác nhận nhập kho nội bộ tại bệnh viện sau khi nhận máu từ ngân hàng máu (Chương 5 điều 40 https://luatvietnam.vn/y-te/thong-tu-26-2013-tt-byt-bo-y-te-82981-d1.html).


* **Actor: Ban Quản trị**
* UC20: Tạo mới, chỉnh sửa, hủy bỏ các chiến dịch hiến máu.
* UC21: Quản lý tài khoản của cán bộ y tế, kỹ thuật viên và bệnh viện.
* UC22: Trích xuất báo cáo thống kê lượt người hiến và tỷ lệ hủy máu.



### 4. Bảng yêu cầu người dùng (User Requirements)

| ID | Mô tả yêu cầu hệ thống | Độ ưu tiên | Mapping (Use Case) |
| :--- | :--- | :--- | :-- |
| **I** | **Luồng nghiệp vụ Người hiến máu** | | |
| UR-01 | Hệ thống phải cho phép người dùng định danh (đăng ký xác thực OTP, đăng nhập) và quản lý cập nhật hồ sơ cá nhân. | Cao | UC01, UC02, UC03 |
| UR-02 | Hệ thống phải cung cấp quy trình đặt lịch khép kín: điền tờ khai y tế, tra cứu chiến dịch, chọn lịch hẹn và chặn tự động nếu chưa đủ khoảng cách ngày quy định. | Cao | UC04, UC05 |
| UR-03 | Hệ thống phải lưu trữ lịch sử hiến máu trọn đời và cho phép người dùng tải xuống chứng nhận điện tử. | Trung bình | UC06 |
| **II** | **Luồng nghiệp vụ Cán bộ y tế** | | |
| UR-04 | Hệ thống phải hỗ trợ quét mã QR để tra cứu nhanh lịch hẹn, ghi nhận các chỉ số sinh tồn lâm sàng và đưa ra quyết định phê duyệt/từ chối lấy máu. | Cao | UC07, UC08, UC09 |
| UR-05 | Hệ thống phải tự động phát sinh mã định danh (Barcode) duy nhất cho từng túi máu ngay khi cán bộ xác nhận lấy máu thành công. | Cao | UC10 |
| **III** | **Luồng nghiệp vụ Kỹ thuật viên xét nghiệm & Kho** | | |
| UR-06 | Hệ thống phải cho phép ghi nhận kết quả điều chế và xét nghiệm 5 bệnh truyền nhiễm dưới cơ chế ẩn danh thông tin người hiến (chỉ hiển thị mã túi máu). | Cao | UC11, UC12 |
| UR-07 | Hệ thống phải tự động đánh dấu "Hủy bỏ" và khóa tính năng xuất kho nếu túi máu có kết quả xét nghiệm dương tính hoặc quá hạn sử dụng. | Cao | UC12 |
| UR-08 | Hệ thống phải cung cấp công cụ quản lý vị trí lưu trữ vật lý trong kho lạnh và trực quan hóa tồn kho theo nhóm máu theo thời gian thực. | Cao | UC13, UC14 |
| UR-09 | Hệ thống phải hỗ trợ luồng xuất kho tự động đề xuất theo thuật toán FEFO (Hết hạn trước - Xuất trước) và lập phiếu tiêu hủy cho túi máu không đạt. | Cao | UC15, UC16 |
| **IV** | **Luồng nghiệp vụ Bệnh viện tuyến dưới** | | |
| UR-10 | Hệ thống phải cho phép bệnh viện tạo đơn xin cấp phát máu, theo dõi tiến độ xử lý đơn và xác nhận nhập kho nội bộ sau khi nhận được máu. | Cao | UC17, UC18, UC19 |
| **V** | **Luồng nghiệp vụ Ban Quản trị** | | |
| UR-11 | Hệ thống phải cung cấp giao diện quản lý toàn diện để tổ chức các chiến dịch hiến máu và phân quyền tài khoản cho nhân sự y tế, bệnh viện. | Cao | UC20, UC21 |
| UR-12 | Hệ thống phải hỗ trợ trích xuất báo cáo, thống kê dữ liệu chuyên sâu (lượt người hiến, tỷ lệ hủy/nhóm máu) để phục vụ công tác quản lý. | Trung bình | UC22 |
| **VI** | **Ràng buộc Hệ thống** | | |
| UR-13 | Hệ thống phải đảm bảo cơ chế xử lý đồng thời để ngăn chặn việc một túi máu bị cấp phát trùng lặp cho nhiều bệnh viện tại cùng một thời điểm. | Cao | |