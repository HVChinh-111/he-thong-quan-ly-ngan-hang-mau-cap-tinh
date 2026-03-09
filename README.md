# Hệ thống quản lý Ngân hàng máu cấp Tỉnh

**Dự án:** Hệ thống Quản lý Ngân hàng Máu cấp Tỉnh - Cụ thể tại Thành phố Hà Nội (Provincial Blood Bank Management System - PBBMS)

### Biên
---

### PHẦN 1: MÔ TẢ HỆ THỐNG

#### 1. Mô tả chung về hệ thống và lý do lựa chọn

**Mô tả chung:**
Hệ thống Quản lý Ngân hàng Máu cấp Tỉnh (PBBMS) là một nền tảng phần mềm quản trị tập trung, được thiết kế để số hóa toàn diện quy trình cung ứng máu nhân đạo trên địa bàn Thành phố Hà Nội. Hệ thống này đóng vai trò là cầu nối liên kết năm nhóm đối tượng chính bao gồm: Người hiến máu, Cán bộ y tế tiếp nhận, Kỹ thuật viên xét nghiệm, Bệnh viện tuyến dưới và Ban Quản trị. Phạm vi của hệ thống bao phủ toàn bộ vòng đời của một đơn vị máu, bắt đầu từ thao tác đăng ký hiến máu trực tuyến của người dân, ghi nhận kết quả khám lâm sàng, tiếp nhận máu, quản lý kết quả xét nghiệm năm bệnh truyền nhiễm bắt buộc (HIV, Viêm gan B, Viêm gan C, Giang mai và Sốt rét), lưu trữ kho lạnh, cho đến khâu phân phối theo yêu cầu cấp cứu của các cơ sở y tế.

**Lý do lựa chọn đề tài:**
Dự án được lựa chọn phát triển dựa trên những vấn đề thực tiễn trong công tác quản lý máu tại Việt Nam hiện nay, cụ thể bao gồm các lý do sau:

* **Khắc phục quy trình thủ công:** Hiện tại, nhiều điểm hiến máu lưu động vẫn sử dụng giấy tờ in sẵn để người dân điền tờ khai y tế. Điều này gây tốn kém thời gian, dễ thất lạc hồ sơ và tạo áp lực lớn cho khâu nhập liệu vào máy tính sau khi chiến dịch kết thúc. *(khảo sát lại, hiện nay có đúng là còn thế không)*
* **Tối ưu hóa công tác điều phối:** Tình trạng khan hiếm máu thường xuyên diễn ra vào các dịp cao điểm như Lễ Tết hoặc dịp hè. Một hệ thống tập trung giúp Sở Y tế và Trung tâm Huyết học nắm bắt chính xác số lượng tồn kho của từng nhóm máu (A, B, AB, O) theo thời gian thực, từ đó phát động các chiến dịch kêu gọi mục tiêu và hiệu quả.
* **Giảm thiểu lãng phí chế phẩm máu:** Các chế phẩm máu có hạn sử dụng rất ngắn (tiểu cầu chỉ lưu trữ tối đa 5 ngày). Việc áp dụng thuật toán quản lý xuất kho FEFO (First Expired, First Out - Hết hạn trước, Xuất trước) bằng phần mềm sẽ loại bỏ sai sót của con người, đảm bảo không có túi máu nào bị tiêu hủy do quá hạn sử dụng trong khi bệnh viện khác lại đang thiếu hụt.
* **Nâng cao trải nghiệm và sự gắn kết của người hiến máu:** Việc thiếu một kênh thông tin liên tục khiến người hiến máu hiếm khi biết được máu của họ đã được sử dụng như thế nào. Tính năng thông báo hành trình túi máu sẽ thúc đẩy động lực hiến máu nhắc lại của người dân.

#### 2. Khảo sát các hệ thống tương tự

Để xây dựng hệ thống PBBMS đáp ứng đúng tiêu chuẩn y tế tại Việt Nam, nhóm đã tiến hành khảo sát hai mô hình hệ thống phần mềm có liên quan đang được vận hành thực tế.

**Hệ thống 1: Ứng dụng di động "Hiến máu" của Viện Huyết học - Truyền máu Trung ương (NIHBT)**

* **Mô tả:** Đây là ứng dụng chính thức và phổ biến nhất tại Việt Nam dành cho người hiến máu nhân đạo, được liên kết trực tiếp với cơ sở dữ liệu quốc gia về dân cư.
* **Ưu điểm:** * Cung cấp giao diện trực quan cho người dùng cuối (End-User).
* Cho phép người dân đăng ký lịch hiến máu, tra cứu địa điểm tổ chức hiến máu gần nhất.
* Tích hợp tính năng xem lại lịch sử hiến máu, nhận chứng nhận hiến máu điện tử và tra cứu kết quả xét nghiệm máu cá nhân một cách bảo mật.


* **Nhược điểm (Khoảng trống để PBBMS giải quyết):** Ứng dụng này chủ yếu tập trung vào tương tác với người hiến máu (Front-end). Các nghiệp vụ lõi như quản lý kho lạnh phức tạp, thuật toán ghép nối đơn hàng giữa Viện Huyết học và các bệnh viện tuyến dưới (Back-end điều phối) thuộc về hệ thống quản trị nội bộ riêng biệt, chưa tạo thành một cổng thông tin duy nhất cho cả người dân và các bệnh viện đa khoa cấp huyện cùng truy cập thao tác.

**Hệ thống 2: Phân hệ Quản lý Ngân hàng máu trong các Hệ thống Thông tin Bệnh viện (Hospital Information System - HIS)**

* **Mô tả:** Các phần mềm quản lý bệnh viện tổng thể (ví dụ như VNPT HIS, Viettel HIS) đang được triển khai tại các bệnh viện tuyến tỉnh và tuyến huyện đều có một module nhỏ mang tên "Quản lý Kho máu".
* **Ưu điểm:** * Quản lý tốt số lượng máu nội bộ đang có sẵn trong tủ lạnh của khoa Hồi sức cấp cứu tại bệnh viện đó.
* Gắn kết trực tiếp dữ liệu nhóm máu của bệnh nhân đang điều trị với chỉ định truyền máu của bác sĩ.


* **Nhược điểm (Khoảng trống để PBBMS giải quyết):** Các hệ thống HIS này mang tính cục bộ (Siloed Data). Khi Bệnh viện X hết máu nhóm O, họ phải gọi điện thoại thủ công lên Viện Huyết học tuyến trên để xin cấp phát, thay vì hệ thống HIS tự động đẩy một yêu cầu điện tử (e-Request) lên một nền tảng quản lý kho máu chung của toàn tỉnh để xử lý tự động. PBBMS được sinh ra để lấp đầy khoảng trống giao tiếp giữa kho máu trung tâm và các hệ thống HIS của từng bệnh viện.

---

### Đăng
---

### PHẦN 2: THU THẬP YÊU CẦU

#### 1. Bảng thuật ngữ chuyên ngành và hệ thống

| Thuật ngữ (Tiếng Anh, có note cả loại từ bằng "()") | Thuật ngữ (Tiếng Việt) | Ý nghĩa |
| --- | --- | --- |
| **Nhóm thuật ngữ về Người dùng & Tác nhân** |  |  |
| Blood Donor (Noun) | Người hiến máu | Cá nhân tự nguyện cung cấp máu, đáp ứng đủ các tiêu chuẩn về sức khỏe, độ tuổi và cân nặng theo quy định y tế. |
| Medical Staff (Noun) | Cán bộ y tế (Tuyến đầu) | Bác sĩ hoặc y tá làm nhiệm vụ tiếp đón, đo chỉ số sinh tồn và khám sàng lọc cho người hiến tại các điểm thu nhận máu. |
| Phlebotomist (Noun) | Nhân viên lấy máu | Nhân viên y tế chuyên trách thực hiện thao tác dùng kim thu thập máu từ tĩnh mạch người hiến vào túi máu. |
| Lab Technician (Noun) | Kỹ thuật viên xét nghiệm | Người phụ trách phân tích mẫu máu để xác định nhóm máu và sàng lọc các bệnh truyền nhiễm (HIV, Viêm gan B, Viêm gan C, Giang mai). |
| Inventory Manager (Noun) | Nhân viên quản lý kho | Người chịu trách nhiệm nhập túi máu vào các tủ bảo quản lạnh, theo dõi hạn sử dụng và xử lý xuất kho. |
| Hospital Staff (Noun) | Nhân viên bệnh viện | Đại diện từ các bệnh viện tuyến dưới có nhu cầu xin cấp phát máu để điều trị cho bệnh nhân. |
| System Admin (Noun) | Quản trị viên hệ thống | Người quản lý tài khoản, phân quyền sử dụng và cấu hình các danh mục hệ thống. |
| **Nhóm thuật ngữ về Chuyên môn Y tế & Xét nghiệm** |  |  |
| Clinical Screening (Noun) | Khám sàng lọc | Bước đánh giá sức khỏe ban đầu, bao gồm đo huyết áp, nhịp tim, cân nặng và phỏng vấn tiền sử bệnh lý để quyết định người dân có đủ điều kiện hiến hay không. |
| Whole Blood (Noun) | Máu toàn phần | Máu được lấy trực tiếp từ cơ thể người hiến, chưa qua quá trình ly tâm hay tách chiết các thành phần. |
| Red Blood Cells (Noun) | Khối hồng cầu | Thành phần của máu có chức năng vận chuyển oxy, thường được tách ra từ máu toàn phần và có thời gian bảo quản khoảng 35 đến 42 ngày. |
| Plasma (Noun) | Huyết tương | Phần dịch trong suốt, màu vàng nhạt của máu, có thể được bảo quản đông lạnh lên đến 1 năm. |
| Rh Factor (Noun) | Kháng nguyên Rh | Một loại protein trên bề mặt hồng cầu. Trạng thái Rh dương tính (+) hoặc âm tính (-) quyết định tính tương thích khi truyền máu. |
| Infectious Disease (Noun) | Bệnh truyền nhiễm | Các bệnh lây qua đường máu bắt buộc phải xét nghiệm sàng lọc trước khi nhập kho (Ví dụ: HIV, Viêm gan B, Viêm gan C). |
| **Nhóm thuật ngữ về Quy trình & Quản lý Hệ thống** |  |  |
| Blood Donation Campaign (Noun) | Chiến dịch hiến máu | Một sự kiện có thời gian và địa điểm cụ thể (Ví dụ: Lễ hội Xuân Hồng tại Đại học Bách Khoa) nhằm thu hút người dân đến hiến máu. |
| Blood Bag (Noun) | Túi máu | Đơn vị lưu trữ vật lý của máu. Trên hệ thống, túi máu là một thực thể được quản lý độc lập. |
| Barcode ID (Noun) | Mã vạch định danh | Chuỗi ký tự duy nhất (Ví dụ: BAG-2026-001) được in ra và dán lên túi máu ngay sau khi lấy máu để ẩn danh thông tin người hiến và theo dõi vòng đời túi máu. |
| Expiration Date (Noun) | Hạn sử dụng | Ngày cuối cùng mà một túi máu hoặc chế phẩm máu có thể được sử dụng an toàn cho bệnh nhân. |
| Time-slot (Noun) | Lịch hẹn | Khung thời gian cụ thể mà người hiến máu đăng ký trước trên hệ thống để tránh tình trạng chờ đợi quá tải tại điểm hiến máu. |
| Blood Request Form (Noun) | Phiếu yêu cầu cấp máu | Đơn từ điện tử do bệnh viện tạo ra, ghi rõ loại máu, nhóm máu, số lượng và mức độ khẩn cấp cần cung cấp. |
| First Expired First Out (Noun Phrase) | Hết hạn trước, Xuất trước | Thuật toán ưu tiên xuất kho: Túi máu nào có ngày hết hạn gần nhất sẽ được hệ thống đề xuất xuất kho trước để tránh lãng phí. |

#### 2. Mô hình nghiệp vụ bằng ngôn ngữ tự nhiên

**Mục tiêu và phạm vi hệ thống:**

* **Mục tiêu:** Xây dựng một nền tảng số hóa khép kín, tự động hóa luồng thông tin từ khâu tiếp nhận máu ngoài cộng đồng đến khâu lưu trữ trong kho lạnh và phân phối đến giường bệnh. Mục tiêu cốt lõi là đảm bảo an toàn truyền máu, chống lãng phí chế phẩm và đáp ứng nhanh chóng các ca cấp cứu khẩn cấp.
* **Phạm vi:** Hệ thống được triển khai áp dụng cho toàn bộ các điểm hiến máu lưu động, Trung tâm Huyết học - Truyền máu cấp tỉnh và toàn mạng lưới các bệnh viện công lập, tư nhân trên địa bàn Thành phố Hà Nội.

**Ai có thể sử dụng phần mềm?**
Hệ thống cấp quyền truy cập cho năm nhóm đối tượng: Người hiến máu, Cán bộ y tế tiếp nhận *(những bệnh viện nào?, quy trình cấp tài khoản như thế nào? nếu cấp tài khoản thì cấp cho những người nào, quy trình cấp tài khoản như thế nào? còn nếu tự đăng ký tài khoản thì xác thực để cấp quyền như thế nào?)*, Kỹ thuật viên xét nghiệm, Nhân viên hành chính của Bệnh viện tuyến dưới và Ban Quản trị hệ thống (Sở Y tế hoặc Hội Chữ thập đỏ).

---

### Chính
---

**Người dùng có những chức năng gì và hoạt động ra sao?**

* **Đối với Người hiến máu:** Người dùng truy cập cổng thông tin web, tải lên ảnh Căn cước công dân để hệ thống nhận diện. Sau đó, họ trả lời bộ câu hỏi khai báo y tế điện tử. Nếu hệ thống kiểm tra lịch sử hiến máu lớn hơn 84 ngày, người dùng được phép chọn địa điểm chiến dịch và khung giờ (Time-slot) để đặt lịch hẹn.
* **Đối với Cán bộ y tế:** Sử dụng thiết bị di động hoặc máy tính bảng quét mã QR lịch hẹn của người dân. Cán bộ tiến hành đo đạc và nhập các chỉ số như huyết áp, nhịp tim và kết quả xét nghiệm máu (có hợp lệ hay không) vào hệ thống. Nếu chỉ số hợp lệ, cán bộ nhấn nút "Đồng ý lấy máu", hệ thống sẽ gửi lệnh máy in xuất ra một tem mã vạch để dán lên túi máu.
* **Đối với Kỹ thuật viên xét nghiệm:** Đăng nhập vào phân hệ quản lý kho. Kỹ thuật viên dùng máy quét mã vạch trên túi máu, cập nhật kết quả xét nghiệm âm tính hoặc dương tính. Nếu âm tính, kỹ thuật viên gán vị trí lưu trữ (Ví dụ: Tủ lạnh số 02, Ngăn số 04) để đưa vào kho. *(sai)*
* **Đối với Bệnh viện tuyến dưới:** Nhân viên bệnh viện đăng nhập, điền biểu mẫu điện tử xin cấp máu chỉ định rõ mức độ ưu tiên. Hệ thống tại Trung tâm Huyết học sẽ tiếp nhận, chạy thuật toán FEFO để tìm kiếm các túi máu phù hợp nhất, trừ đi số lượng tồn kho và thông báo trạng thái "Đang vận chuyển" về lại màn hình của bệnh viện.

**Những thông tin/đối tượng thực thể mà hệ thống cần xử lý:**

1. **Tài khoản người dùng (User):** Lưu trữ thông tin cá nhân, định danh, nhóm máu, mật khẩu mã hóa.
2. **Hồ sơ sức khỏe (Health Record):** Lưu trữ các chỉ số sinh tồn của mỗi lần hiến máu.
3. **Chiến dịch (Campaign):** Lưu trữ thông tin địa điểm, thời gian, sức chứa tối đa.
4. **Túi máu (Blood Bag):** Đối tượng quan trọng nhất, lưu trữ mã vạch, ngày lấy máu, ngày hết hạn, trạng thái hiện tại (An toàn, Nhiễm bệnh, Hết hạn, Đã xuất kho).
5. **Yêu cầu cấp phát (Blood Request):** Lưu trữ thông tin bệnh viện yêu cầu, số lượng đơn vị máu cần, thời gian yêu cầu và trạng thái đáp ứng.

**Quan hệ giữa các đối tượng (Thực thể):**

* Một Người hiến máu có thể tham gia nhiều Chiến dịch khác nhau qua các năm.
* Một Chiến dịch có thể tiếp nhận hàng ngàn Người hiến máu đăng ký.
* Một Người hiến máu đóng góp tạo ra một Túi máu trong mỗi lần hiến hợp lệ.
* Một Túi máu chỉ có duy nhất một bộ Hồ sơ sức khỏe và Kết quả xét nghiệm đi kèm.
* Một Yêu cầu cấp phát từ bệnh viện có thể bao gồm nhiều Túi máu khác nhau, nhưng một Túi máu chỉ được cấp phát cho một Yêu cầu cấp phát duy nhất.

---

### Cường
---

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
* UC11: Cập nhật kết quả xét nghiệm 5 bệnh truyền nhiễm cho túi máu.
* UC12: Cập nhật vị trí lưu trữ túi máu vào kho lạnh.
* UC13: Xem biểu đồ thống kê tồn kho theo nhóm máu thời gian thực.
* UC14: Xác nhận phiếu xuất kho máu.


* **Actor: Bệnh viện tuyến dưới**
* UC15: Tạo lập đơn yêu cầu cấp phát máu khẩn cấp hoặc bình thường.
* UC16: Theo dõi trạng thái tiến độ của đơn yêu cầu cấp máu.


* **Actor: Ban Quản trị**
* UC17: Tạo mới, chỉnh sửa, hủy bỏ các chiến dịch hiến máu.
* UC18: Quản lý tài khoản của cán bộ y tế, kỹ thuật viên và bệnh viện.
* UC19: Trích xuất báo cáo thống kê lượt người hiến và tỷ lệ hủy máu.



#### 4. Bảng yêu cầu người dùng (User Requirements)

Bảng dưới đây liệt kê các yêu cầu chức năng hệ thống cần phải có, được phân định theo mức độ ưu tiên để phục vụ cho việc lập kế hoạch phát triển (Sprint Planning).

| ID Yêu cầu | Mô tả chi tiết yêu cầu người dùng | Độ ưu tiên |
| --- | --- | --- |
| UR-01 | Hệ thống phải cho phép người dân tạo tài khoản bằng số Căn cước công dân và xác thực qua mã OTP gửi về điện thoại di động. | Cao |
| UR-02 | Hệ thống phải tự động kiểm tra cơ sở dữ liệu và chặn hành động đăng ký hiến máu nếu khoảng cách thời gian từ lần hiến gần nhất nhỏ hơn 84 ngày. | Cao |
| UR-03 | Hệ thống phải cho phép người dùng lựa chọn khung giờ (Time-slot) để hiến máu, mỗi khung giờ giới hạn sức chứa để tránh quá tải tại điểm hiến máu. | Trung bình |
| UR-04 | Hệ thống phải có chức năng sinh mã vạch ngẫu nhiên và không trùng lặp cho mỗi túi máu ngay tại thời điểm cán bộ y tế nhấn xác nhận lấy máu. | Cao |
| UR-05 | Hệ thống phải ngắt kết nối hiển thị tên người hiến máu khỏi giao diện của phòng xét nghiệm, kỹ thuật viên chỉ thao tác kiểm tra bệnh dựa trên mã vạch túi máu. | Cao |
| UR-06 | Hệ thống phải tự động đánh dấu túi máu là "Hủy bỏ do nhiễm bệnh" và khóa tính năng xuất kho nếu kỹ thuật viên cập nhật bất kỳ 1 trong 5 xét nghiệm có kết quả dương tính. | Cao |
| UR-07 | Hệ thống phải chạy một tác vụ ngầm vào lúc 00:00 mỗi ngày để kiểm tra hạn sử dụng và tự động đổi trạng thái thành "Đã hết hạn" đối với các túi máu quá hạn. | Cao |
| UR-08 | Hệ thống phải hiển thị bản đồ số hóa số lượng máu tồn kho, chia màu cảnh báo (Xanh, Vàng, Đỏ) khi một nhóm máu cụ thể tụt xuống dưới mức dự trữ an toàn. | Trung bình |
| UR-09 | Hệ thống phải cung cấp giao diện để Bệnh viện tuyến dưới điền yêu cầu xin cấp phát máu, bắt buộc chọn nhóm máu và số lượng đơn vị. | Cao |
| UR-10 | Hệ thống phải tự động đề xuất danh sách túi máu xuất kho theo đúng thuật toán FEFO (Ưu tiên các túi máu chuẩn bị hết hạn được xuất đi trước) cho kỹ thuật viên kho. | Cao |
| UR-11 | Hệ thống phải có cơ chế Khóa bi quan (Pessimistic Locking) để tránh tình trạng hai bệnh viện cùng được hệ thống cấp phát chung một túi máu nhóm O cuối cùng. | Cao |
| UR-12 | Hệ thống phải gửi thông báo qua Email hoặc SMS tự động cho người hiến máu ngay khi túi máu của họ được xuất kho để truyền cho bệnh nhân. | Thấp |
| UR-13 | Hệ thống phải cho phép Ban Quản trị xuất các báo cáo dạng file Excel về số lượng người hiến theo chiến dịch và tỷ lệ các nhóm máu thu thập được. | Trung bình |

---


