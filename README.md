# Hệ thống quản lý Ngân hàng máu cấp Tỉnh

**Dự án:** Hệ thống Quản lý Ngân hàng Máu cấp Tỉnh - Cụ thể tại Thành phố Hà Nội (Provincial Blood Bank Management System - PBBMS)

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
* **Nâng cao trải nghiệm của người hiến máu**, thông qua việc theo dõi lịch sử hiến máu.

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
4. Sau khi chiến dịch kết thúc, quyền truy cập của tài khoản sẽ chuyển sang trạng thái tạm khóa.


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
