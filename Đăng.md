
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

### 2. Mô hình nghiệp vụ bằng ngôn ngữ tự nhiên

#### Mục tiêu và phạm vi hệ thống

**Mục tiêu**

Mục tiêu của hệ thống PBBMS là xây dựng một nền tảng số hóa thống nhất nhằm quản lý toàn bộ quy trình hiến máu và phân phối máu trên địa bàn Thành phố Hà Nội. Hệ thống cho phép tự động hóa luồng thông tin từ khâu người dân đăng ký hiến máu, khám sàng lọc sức khỏe, thu nhận máu, xét nghiệm an toàn truyền máu, lưu trữ kho lạnh cho đến khi các đơn vị máu được cấp phát cho bệnh viện để phục vụ điều trị.

Việc triển khai hệ thống nhằm đạt được các mục tiêu chính sau:

* Đảm bảo **an toàn truyền máu** thông qua việc kiểm soát chặt chẽ dữ liệu xét nghiệm và lịch sử túi máu.
* **Tối ưu hóa quản lý tồn kho máu**, giúp cơ quan quản lý nắm được số lượng máu theo từng nhóm máu và chế phẩm theo thời gian thực.
* **Giảm thiểu lãng phí chế phẩm máu**, đặc biệt đối với các thành phần có hạn sử dụng ngắn như tiểu cầu.
* **Rút ngắn thời gian đáp ứng các ca cấp cứu**, giúp bệnh viện tuyến dưới có thể gửi yêu cầu cấp máu trực tuyến thay vì phải liên hệ thủ công.
* **Nâng cao trải nghiệm của người hiến máu**, thông qua việc theo dõi lịch sử hiến máu và nhận thông báo về việc sử dụng túi máu.

**Phạm vi**

Hệ thống được thiết kế để triển khai trên toàn bộ hệ thống cung ứng máu của Thành phố Hà Nội, bao gồm:

* **Các điểm hiến máu lưu động** được tổ chức tại trường đại học, cơ quan nhà nước, doanh nghiệp và các sự kiện cộng đồng.
* **Trung tâm Huyết học – Truyền máu cấp tỉnh**, đóng vai trò là đơn vị quản lý kho máu trung tâm, thực hiện xét nghiệm và phân phối máu.
* **Các bệnh viện công lập và tư nhân trên địa bàn thành phố**, bao gồm bệnh viện tuyến trung ương, tuyến thành phố, tuyến quận/huyện và bệnh viện chuyên khoa có nhu cầu tiếp nhận máu để điều trị cho bệnh nhân.

Hệ thống tập trung quản lý dữ liệu của toàn bộ các đơn vị trên một nền tảng thống nhất, cho phép chia sẻ thông tin tồn kho và yêu cầu cấp máu theo thời gian thực.

#### Ai có thể sử dụng phần mềm

Hệ thống PBBMS được thiết kế cho **năm nhóm người dùng chính**, mỗi nhóm có quyền truy cập và chức năng riêng.

**1. Người hiến máu (Blood Donor)**

Đây là người dân tự nguyện tham gia hiến máu nhân đạo. Người hiến máu có thể:

* Tạo tài khoản trên hệ thống bằng **số Căn cước công dân và số điện thoại cá nhân**.
* Xác thực tài khoản thông qua **mã OTP gửi về điện thoại**.
* Khai báo thông tin cá nhân và điền **tờ khai sức khỏe điện tử** trước khi tham gia hiến máu.
* Tra cứu danh sách các **chiến dịch hiến máu đang diễn ra**, lựa chọn địa điểm và khung giờ phù hợp.
* Xem **lịch sử hiến máu**, kết quả xét nghiệm và chứng nhận hiến máu điện tử.

Người hiến máu **được phép tự đăng ký tài khoản**, nhưng hệ thống sẽ kiểm tra tính hợp lệ của thông tin định danh và điều kiện hiến máu trước khi cho phép đặt lịch.


**2. Cán bộ y tế tiếp nhận (Medical Staff)**

Nhóm người dùng này bao gồm:

* Bác sĩ hoặc y tá thuộc **Trung tâm Huyết học – Truyền máu Hà Nội**.
* Nhân viên y tế được **phân công tham gia các chiến dịch hiến máu lưu động** tại các cơ sở như trường đại học, cơ quan nhà nước hoặc doanh nghiệp.

Cán bộ y tế tiếp nhận có nhiệm vụ:

* Quét mã QR lịch hẹn của người hiến máu khi họ đến điểm hiến.
* Thực hiện khám sàng lọc lâm sàng, bao gồm đo huyết áp, nhịp tim, cân nặng và kiểm tra tiền sử bệnh.
* Nhập các chỉ số sức khỏe vào hệ thống và quyết định người hiến có đủ điều kiện hiến máu hay không.
* Xác nhận thao tác lấy máu và kích hoạt hệ thống **tạo mã vạch định danh cho túi máu**.

Nhóm người dùng này **không được phép tự đăng ký tài khoản**.

Quy trình cấp tài khoản được thực hiện như sau:

1. Trung tâm Huyết học hoặc Sở Y tế lập danh sách nhân sự tham gia chiến dịch hiến máu.
2. Quản trị viên hệ thống tạo tài khoản cho từng cán bộ dựa trên **mã số nhân viên và chứng chỉ hành nghề y tế**.
3. Tài khoản được cấp quyền truy cập vào hệ thống trong **khoảng thời gian diễn ra chiến dịch hiến máu**.
4. Sau khi chiến dịch kết thúc, quyền truy cập của tài khoản có thể bị thu hồi hoặc chuyển sang trạng thái tạm khóa.


**3. Kỹ thuật viên xét nghiệm (Lab Technician)**

Nhóm này bao gồm các kỹ thuật viên làm việc tại **phòng xét nghiệm của Trung tâm Huyết học – Truyền máu cấp tỉnh**.

Nhiệm vụ của họ trong hệ thống bao gồm:

* Quét mã vạch trên túi máu để truy xuất hồ sơ xét nghiệm.
* Thực hiện các xét nghiệm sàng lọc bệnh truyền nhiễm bắt buộc, bao gồm HIV, Viêm gan B, Viêm gan C, Giang mai và Sốt rét.
* Nhập kết quả xét nghiệm vào hệ thống.
* Phân loại túi máu thành các trạng thái như **đạt chuẩn, nhiễm bệnh hoặc không đạt tiêu chuẩn**.
* Gán vị trí lưu trữ túi máu trong kho lạnh.

Tương tự cán bộ y tế tiếp nhận, **tài khoản của kỹ thuật viên xét nghiệm được tạo bởi quản trị viên hệ thống**, không cho phép tự đăng ký.


**4. Nhân viên bệnh viện tuyến dưới (Hospital Staff)**

Nhóm này bao gồm:

* Nhân viên hành chính hoặc nhân viên của **khoa huyết học, khoa hồi sức cấp cứu hoặc khoa truyền máu** tại các bệnh viện trên địa bàn Hà Nội.
* Các bệnh viện có thể là **bệnh viện tuyến trung ương, tuyến thành phố hoặc tuyến quận/huyện**.

Nhân viên bệnh viện có thể sử dụng hệ thống để:

* Tạo **phiếu yêu cầu cấp phát máu điện tử** khi bệnh viện cần truyền máu cho bệnh nhân.
* Chỉ định **nhóm máu, loại chế phẩm và số lượng đơn vị máu cần cấp phát**.
* Theo dõi trạng thái xử lý yêu cầu từ Trung tâm Huyết học.

Tài khoản của nhóm người dùng này được tạo theo quy trình:

1. Bệnh viện gửi danh sách nhân viên phụ trách truyền máu cho Sở Y tế.
2. Quản trị viên hệ thống tạo tài khoản và gán quyền truy cập cho từng nhân viên.
3. Mỗi tài khoản được liên kết với **mã định danh của bệnh viện tương ứng**.


**5. Ban Quản trị hệ thống (System Administrator)**

Nhóm này bao gồm cán bộ thuộc:

* **Sở Y tế Thành phố Hà Nội**
* **Trung tâm Huyết học – Truyền máu Hà Nội**
* **Hội Chữ thập đỏ** tham gia quản lý các chiến dịch hiến máu.

Ban quản trị có quyền cao nhất trong hệ thống và chịu trách nhiệm:

* Tạo và quản lý tài khoản người dùng cho các nhóm nhân viên y tế và bệnh viện.
* Tạo mới, chỉnh sửa hoặc hủy các **chiến dịch hiến máu**.
* Theo dõi số liệu thống kê về lượng máu thu thập, tồn kho và phân phối.
* Xuất báo cáo phục vụ công tác quản lý của Sở Y tế.


