# Hệ thống quản lý Ngân hàng máu Thành phố Hà Nội

> Thông tin nhóm:
> Nguyễn Hoàng Biên - B23DCKH007
> Hoàng Văn Chính - B23DCKH011
> Nguyễn Đăng Cường - B23DCKH015
> Hán Hữu Đăng - B23DCKH019

### PHẦN 1: MÔ TẢ HỆ THỐNG

#### 1. Mô tả chung về hệ thống và lý do lựa chọn

**Mô tả chung:**

Hệ thống quản lý Ngân hàng máu Thành phố Hà Nội là một nền tảng phần mềm quản trị tập trung, được thiết kế để số hóa toàn diện quy trình cung ứng máu nhân đạo trên địa bàn Thành phố Hà Nội. Hệ thống này đóng vai trò là cầu nối liên kết năm nhóm đối tượng chính bao gồm: Người hiến máu, Cán bộ y tế tiếp nhận, Kỹ thuật viên xét nghiệm, Bệnh viện tuyến dưới và Ban Quản trị. Phạm vi của hệ thống bao phủ toàn bộ vòng đời của một đơn vị máu, bắt đầu từ thao tác đăng ký hiến máu trực tuyến của người dân, ghi nhận kết quả khám lâm sàng, tiếp nhận máu, quản lý kết quả xét nghiệm năm bệnh truyền nhiễm bắt buộc cho mọi đơn vị: HIV, HBV, HCV, giang mai + ABO/Rh(D) + sàng lọc kháng thể bất thường; sốt rét theo điều kiện nguy cơ., lưu trữ kho lạnh, cho đến khâu phân phối theo yêu cầu cấp cứu của các cơ sở y tế.

**Lý do lựa chọn đề tài:**
Dự án PBBMS được nghiên cứu, thiết kế và đề xuất phát triển dựa trên những lỗ hổng trong kiến trúc thông tin y tế hiện tại, cũng như các vấn đề thực tiễn cấp bách trong công tác quản lý cung ứng máu tại Việt Nam, đặc biệt là trong giai đoạn bản lề của công cuộc chuyển đổi số y tế quốc gia (2024 - 2026). Các luận điểm chiến lược làm cơ sở cho dự án bao gồm:

* **Khắc phục quy trình thủ công:** Hiện tại, nhiều điểm hiến máu lưu động quy trình còn tồn tại biểu mẫu và mức độ số hóa không đồng nhất theo cơ sở/điểm hiến, vẫn còn có nơi sử dụng giấy tờ in sẵn để người dân điền tờ khai y tế. Điều này gây tốn kém thời gian, dễ thất lạc hồ sơ và tạo áp lực lớn cho khâu nhập liệu vào máy tính sau khi chiến dịch kết thúc. [link](https://vienhuyethoc.vn/huong-dan-nhan-ket-qua-hien-mau/)

* **Tối ưu hóa công tác điều phối:** Tình trạng thiếu máu/căng thẳng tồn kho thường được ghi nhận vào các giai đoạn cao điểm (cuối năm, trước–sau Tết) và theo mùa (mùa hè), thể hiện qua các thông báo/kêu gọi tiếp nhận máu và kế hoạch dự trữ của cơ quan/đơn vị chuyên trách. Do đó, một hệ thống điều phối dữ liệu và kế hoạch (đề xuất) có cơ sở thực tiễn để cải thiện khả năng nắm bắt nhu cầu–tồn kho–chiến dịch huy động [link](https://moh.gov.vn/home?_101_struts_action=%2Fasset_publisher%2Fview_content&_101_type=content&_101_urlTitle=du-tru-80-000-on-vi-mau-cho-cuoi-nam-va-tet-nguyen-an&p_p_id=101&p_p_lifecycle=0&p_p_mode=view&p_p_state=maximized)
* **Giảm thiểu lãng phí chế phẩm máu:** Các chế phẩm máu có hạn sử dụng rất ngắn (tiểu cầu chỉ lưu trữ tối đa 5 ngày). Việc áp dụng thuật toán quản lý xuất kho FEFO (First Expired, First Out - Hết hạn trước, Xuất trước) Phần mềm có thể hỗ trợ ưu tiên xuất kho các đơn vị gần hết hạn (nguyên tắc ‘gần hết hạn xuất trước’) và cảnh báo sớm, từ đó giảm nguy cơ hủy do quá hạn và giảm mất cân đối phân bổ; hiệu quả thực tế phụ thuộc quy trình vận hành, năng lực vận chuyển chuỗi lạnh, và cơ chế phối hợp liên cơ sở. [link](https://vienhuyethoc.vn/han-su-dung-cua-mau/)
* **Nâng cao trải nghiệm và sự gắn kết của người hiến máu:**Tỷ lệ hiến máu của Việt Nam đã đạt khoảng 1,74%, nhưng thách thức lớn hơn là giữ chân người hiến máu nhắc lại. Một nguyên nhân quan trọng là sau khi hiến máu, người dân gần như không biết máu của mình có đạt chuẩn hay đã được sử dụng như thế nào do thiếu một kênh thông tin liên tục. PBBMS hướng tới giải quyết vấn đề này bằng hệ thống thông báo cá nhân hóa, từ cập nhật kết quả xét nghiệm an toàn đến thông tin đơn vị máu đã được sử dụng cứu chữa bệnh nhân. Nhờ đó, hệ thống tăng tính minh bạch, củng cố niềm tin và tạo động lực cảm xúc để người dân tiếp tục hiến máu trong tương lai.

#### 2. Khảo sát các hệ thống tương tự

Để xây dựng hệ thống PBBMS đáp ứng đúng tiêu chuẩn y tế tại Việt Nam, nhóm đã tiến hành khảo sát hai mô hình hệ thống phần mềm có liên quan đang được vận hành thực tế.

**Hệ thống 1: Ứng dụng di động "Hiến máu" của Viện Huyết học - Truyền máu Trung ương (NIHBT)**

* **Mô tả:** Đây là Ứng dụng “Hiến máu” được NIHBT phối hợp Viettel phát triển, cho phép người hiến: tra cứu thông tin hiến máu, địa điểm hiến máu, nhu cầu máu của bệnh viện; đăng ký/đặt lịch hiến; theo dõi lịch sử hiến máu; xem hành trình đơn vị máu hiến và kết quả hiến máu (sau khoảng thời gian cập nhật). Ứng dụng có lưu ý về điều kiện đối sánh thông tin cá nhân (số giấy tờ/điện thoại) và phạm vi dữ liệu hiện chỉ cập nhật từ NIHBT và một số cơ sở dùng chung phần mềm quản lý hiến máu. [link](https://vienhuyethoc.vn/hm/)
* **Ưu điểm:** * Cung cấp giao diện trực quan cho người dùng cuối (End-User).
* Cho phép người dân đăng ký lịch hiến máu, tra cứu địa điểm tổ chức hiến máu gần nhất.
* Tích hợp tính năng xem lại lịch sử hiến máu, nhận chứng nhận hiến máu điện tử và tra cứu kết quả xét nghiệm máu cá nhân một cách bảo mật.


* **Nhược điểm (Khoảng trống để PBBMS giải quyết):** Ứng dụng này chủ yếu tập trung vào tương tác với người hiến máu (Front-end). Các nghiệp vụ lõi như quản lý kho lạnh phức tạp, thuật toán ghép nối đơn hàng giữa Viện Huyết học và các bệnh viện tuyến dưới (Back-end điều phối) thuộc về hệ thống quản trị nội bộ riêng biệt, chưa tạo thành một cổng thông tin duy nhất cho cả người dân và các bệnh viện đa khoa cấp huyện cùng truy cập thao tác.

**Hệ thống 2: Phân hệ Quản lý Ngân hàng máu trong các Hệ thống Thông tin Bệnh viện (Hospital Information System - HIS)**

* **Mô tả:** Các phần mềm quản lý bệnh viện tổng thể như VNPT HIS, Viettel HIS được triển khai tại nhiều bệnh viện tuyến tỉnh và tuyến huyện; trong một số trường hợp, các hệ thống này có tích hợp chức năng hoặc module liên quan đến quản lý kho máu.[link](https://vnpt.vn/doanh-nghiep/giai-phap-cntt/dich-vu-phan-mem-quan-ly-benh-vien-vnpt-his/)
* **Ưu điểm:** * giúp bệnh viện theo dõi tồn kho, gắn thông tin người bệnh và chỉ định truyền máu, và chuẩn hóa báo cáo nội bộ. [link](https://solutions.viettel.vn/vi/y-te-so/phan-mem-quan-ly-benh-vien-viettel-his.html)
* Gắn kết trực tiếp dữ liệu nhóm máu của bệnh nhân đang điều trị với chỉ định truyền máu của bác sĩ.


* **Nhược điểm (Khoảng trống để PBBMS giải quyết):** Các hệ thống HIS này mang tính cục bộ (Siloed Data). Khi Bệnh viện X hết máu nhóm O, họ phải gọi điện thoại thủ công lên Viện Huyết học tuyến trên để xin cấp phát, thay vì một phương thức liên lạc chung.

**Lý do lựa chọn đề tài:**
Dự án PBBMS được nghiên cứu, thiết kế và đề xuất phát triển dựa trên những lỗ hổng trong kiến trúc thông tin y tế hiện tại, cũng như các vấn đề thực tiễn cấp bách trong công tác quản lý cung ứng máu tại Việt Nam, đặc biệt là trong giai đoạn bản lề của công cuộc chuyển đổi số y tế quốc gia (2024 - 2026). Các luận điểm chiến lược làm cơ sở cho dự án bao gồm:

* **Khắc phục quy trình thủ công:** Hiện tại, nhiều điểm hiến máu lưu động quy trình còn tồn tại biểu mẫu và mức độ số hóa không đồng nhất theo cơ sở/điểm hiến, vẫn còn có nơi sử dụng giấy tờ in sẵn để người dân điền tờ khai y tế. Điều này gây tốn kém thời gian, dễ thất lạc hồ sơ và tạo áp lực lớn cho khâu nhập liệu vào máy tính sau khi chiến dịch kết thúc. [link](https://vienhuyethoc.vn/huong-dan-nhan-ket-qua-hien-mau/)

* **Tối ưu hóa công tác điều phối:** Tình trạng thiếu máu/căng thẳng tồn kho thường được ghi nhận vào các giai đoạn cao điểm (cuối năm, trước–sau Tết) và theo mùa (mùa hè), thể hiện qua các thông báo/kêu gọi tiếp nhận máu và kế hoạch dự trữ của cơ quan/đơn vị chuyên trách. Do đó, một hệ thống điều phối dữ liệu và kế hoạch (đề xuất) có cơ sở thực tiễn để cải thiện khả năng nắm bắt nhu cầu–tồn kho–chiến dịch huy động [link](https://moh.gov.vn/home?_101_struts_action=%2Fasset_publisher%2Fview_content&_101_type=content&_101_urlTitle=du-tru-80-000-on-vi-mau-cho-cuoi-nam-va-tet-nguyen-an&p_p_id=101&p_p_lifecycle=0&p_p_mode=view&p_p_state=maximized)
* **Giảm thiểu lãng phí chế phẩm máu:** Các chế phẩm máu có hạn sử dụng rất ngắn (tiểu cầu chỉ lưu trữ tối đa 5 ngày). Việc áp dụng thuật toán quản lý xuất kho FEFO (First Expired, First Out - Hết hạn trước, Xuất trước) Phần mềm có thể hỗ trợ ưu tiên xuất kho các đơn vị gần hết hạn (nguyên tắc ‘gần hết hạn xuất trước’) và cảnh báo sớm, từ đó giảm nguy cơ hủy do quá hạn và giảm mất cân đối phân bổ; hiệu quả thực tế phụ thuộc quy trình vận hành, năng lực vận chuyển chuỗi lạnh, và cơ chế phối hợp liên cơ sở. [link](https://vienhuyethoc.vn/han-su-dung-cua-mau/)
* **Nâng cao trải nghiệm và sự gắn kết của người hiến máu:** Tỷ lệ hiến máu của Việt Nam đã đạt khoảng 1,74%, nhưng thách thức lớn hơn là giữ chân người hiến máu nhắc lại. Một nguyên nhân quan trọng là sau khi hiến máu, người dân gần như không biết máu của mình có đạt chuẩn hay đã được sử dụng như thế nào do thiếu một kênh thông tin liên tục. PBBMS hướng tới giải quyết vấn đề này bằng hệ thống thông báo cá nhân hóa, từ cập nhật kết quả xét nghiệm an toàn đến thông tin đơn vị máu đã được sử dụng cứu chữa bệnh nhân. Nhờ đó, hệ thống tăng tính minh bạch, củng cố niềm tin và tạo động lực cảm xúc để người dân tiếp tục hiến máu trong tương lai.

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

**4. Nhân viên quản lý kho (Inventory Manager)**

Nhóm người dùng này bao gồm các nhân viên làm việc tại **kho lưu trữ máu của Trung tâm Huyết học**. Họ chịu trách nhiệm quản lý các túi máu đã hoàn thành xét nghiệm và được đưa vào hệ thống kho lạnh bảo quản.

Nhiệm vụ của nhân viên quản lý kho trong hệ thống bao gồm:

* Quét mã vạch trên túi máu để xác định thông tin và trạng thái của túi máu trong hệ thống.
* Quản lý túi máu: Cập nhật **vị trí lưu trữ của túi máu** trong kho, ví dụ như tủ lạnh, ngăn chứa hoặc kệ bảo quản, xác nhận xóa bỏ túi máu quá hạn.
* Theo dõi **số lượng máu tồn kho theo từng nhóm máu và từng loại chế phẩm máu**.
* Xác nhận thao tác **nhập kho và xuất kho túi máu** khi có yêu cầu cấp phát từ bệnh viện.
* Kiểm tra hạn sử dụng của các túi máu và phối hợp với hệ thống để đảm bảo nguyên tắc **FEFO (First Expired, First Out)**, ưu tiên xuất các túi máu có hạn sử dụng gần nhất.

Tài khoản của nhân viên quản lý kho **không được phép tự đăng ký trên hệ thống**. Quy trình cấp tài khoản được thực hiện như sau:

1. Trung tâm Huyết học – Truyền máu lập danh sách nhân viên phụ trách quản lý kho máu.
2. Danh sách được gửi cho quản trị viên hệ thống để tạo tài khoản.
3. Quản trị viên gán quyền **Inventory Manager** cho các tài khoản này.
4. Các tài khoản chỉ được phép truy cập vào **phân hệ quản lý kho máu và xuất nhập kho**, không có quyền truy cập vào dữ liệu cá nhân của người hiến máu.

**5. Nhân viên bệnh viện tuyến dưới (Hospital Staff)**

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


**6. Ban Quản trị hệ thống (System Administrator)**

Nhóm này bao gồm cán bộ thuộc:

* **Sở Y tế Thành phố Hà Nội**
* **Trung tâm Huyết học – Truyền máu Hà Nội**
* **Hội Chữ thập đỏ** tham gia quản lý các chiến dịch hiến máu.

Ban quản trị có quyền cao nhất trong hệ thống và chịu trách nhiệm:

* Tạo và quản lý tài khoản người dùng cho các nhóm nhân viên y tế và bệnh viện.
* Tạo mới, chỉnh sửa hoặc hủy các **chiến dịch hiến máu**.
* Theo dõi số liệu thống kê về lượng máu thu thập, tồn kho và phân phối.
* Xuất báo cáo phục vụ công tác quản lý của Sở Y tế.


### Người dùng có những chức năng gì và hoạt động ra sao?

* **Đối với Người hiến máu:** Người dùng truy cập cổng thông tin web, đăng ký tài khoản và nhập thông tin cá nhân hoặc đăng nhập nếu đã có tài khoản. Người dùng có thể xem các chiến dịch đang được mở trên địa bàn Hà Nội bất cứ lúc nào. Nếu hệ thống kiểm tra lịch sử hiến máu lớn hơn 12 tuần [(Thông tin)](https://www.vinmec.com/vie/bai-viet/thoi-gian-toi-thieu-giua-cac-lan-hien-mau-la-bao-lau-de-dam-bao-suc-khoe-vi), người dùng được phép chọn địa điểm chiến dịch và khung giờ (Time-slot) để đặt lịch hẹn.

* **Đối với Cán bộ y tế:** Sử dụng thiết bị di động quét mã QR lịch hẹn của người dân. Cán bộ tiến hành đo đạc và nhập các chỉ số như huyết áp, nhịp tim và lấy máu xét nghiệm nhanh và gửi đến cho kỹ thuật viên xét nghiệm (có hợp lệ hay không). Nếu chỉ số hợp lệ, cán bộ nhấn nút "Đồng ý lấy máu", hệ thống sẽ gửi lệnh máy in xuất ra một tem mã vạch để dán lên túi máu.

* **Đối với Kỹ thuật viên xét nghiệm:** Kỹ thuật viên đăng nhập vào hệ thống và sử dụng máy quét mã vạch trên ống máu xét nghiệm nhanh để truy xuất thông tin. Trước tiên, kỹ thuật viên thực hiện xét nghiệm nhanh tại chỗ đối với ống máu xét nghiệm nhanh và nhập kết quả xét nghiệm nhanh vào hệ thống. Nếu kết quả xét nghiệm nhanh không đạt yêu cầu, kết quả sẽ được kỹ thuật viên cập nhật kết quả lên hệ thống, lúc này sẽ không lấy máu hiến của bệnh nhân. Nếu kết quả đạt yêu cầu, **Cán bộ y tế** sẽ có thể ấn vào nút đồng ý lấy máu để lấy máu của người hiến. Sau khi lấy máu và túi máu được chuyển về, kỹ thuật viên tiếp tục lấy 3–4 ống máu nhỏ từ túi máu để thực hiện các xét nghiệm chuyên sâu nhằm sàng lọc các bệnh truyền nhiễm bắt buộc. Sau khi hoàn tất các xét nghiệm, kỹ thuật viên tiếp tục cập nhật kết quả xét nghiệm (âm tính hoặc dương tính) vào hệ thống. Nếu kết quả xét nghiệm chuyên sâu đạt yêu cầu (âm tính), túi máu được chuyển sang trạng thái sẵn sàng lưu trữ trong kho.

* **Đối với Nhân viên quản lý kho:** Nhân viên quản lý kho đăng nhập vào phân hệ quản lý kho máu để thực hiện các thao tác quản lý túi máu trong kho. Nhân viên có thể sử dụng máy quét mã vạch để xem vị trí lưu trữ và thông tin chi tiết của từng túi máu trong hệ thống. Ngoài ra, nhân viên quản lý kho chịu trách nhiệm quản lý trạng thái các túi máu, theo dõi hạn sử dụng và cập nhật vị trí lưu trữ của túi máu trong kho lạnh. Hệ thống cũng cung cấp chức năng xem các báo cáo thống kê tồn kho theo từng nhóm máu và loại chế phẩm để hỗ trợ công tác quản lý. Khi có yêu cầu cấp phát máu, nhân viên quản lý kho có thể tạo và duyệt các yêu cầu cấp máu trực tiếp từ nhân viên nội bộ hoặc duyệt các yêu cầu cấp máu gửi từ bệnh viện tuyến dưới, đảm bảo việc xuất kho được thực hiện đúng quy trình và cập nhật trạng thái túi máu trong hệ thống.

* **Đối với Bệnh viện tuyến dưới:** Nhân viên bệnh viện đăng nhập, điền biểu mẫu điện tử xin cấp máu chỉ định rõ mức độ ưu tiên. Hệ thống tại Trung tâm Huyết học sẽ tiếp nhận, chạy thuật toán FEFO để tìm kiếm các túi máu phù hợp nhất, trừ đi số lượng tồn kho và thông báo trạng thái "Đang vận chuyển" về lại màn hình của bệnh viện.


### Những thông tin/đối tượng thực thể mà hệ thống cần xử lý

1. **Tài khoản người dùng (User):** Lưu trữ thông tin cá nhân, nhóm máu, lịch sử hiến máu, mật khẩu mã hóa.
2. **Hồ sơ sức khỏe (Health Record):** Lưu trữ các chỉ số sức khỏe của mỗi lần hiến máu.
3. **Chiến dịch (Campaign):** Lưu trữ thông tin địa điểm, thời gian, sức chứa tối đa.
4. **Túi máu (Blood Bag):** Đối tượng quan trọng nhất, lưu trữ mã vạch, ngày lấy máu, ngày hết hạn, trạng thái hiện tại (An toàn, Nhiễm bệnh, Hết hạn, Đã xuất kho).
5. **Yêu cầu cấp phát (Blood Request):** Lưu trữ thông tin bệnh viện yêu cầu, số lượng đơn vị máu cần, thời gian yêu cầu và trạng thái đáp ứng.


### Quan hệ giữa các đối tượng (Thực thể)

* Một Người hiến máu có thể tham gia nhiều Chiến dịch khác nhau, chỉ cần đủ điều kiện về thời gian.
* Một Chiến dịch có thể tiếp nhận hàng ngàn Người hiến máu đăng ký.
* Một Người hiến máu đóng góp tạo ra một Túi máu trong mỗi lần hiến hợp lệ.
* Một Túi máu chỉ có duy nhất một bộ Hồ sơ sức khỏe và Kết quả xét nghiệm đi kèm.
* Một Túi máu sau khi đạt tiêu chuẩn xét nghiệm sẽ được *Nhân viên quản lý kho* tiếp nhận và lưu trữ trong kho lạnh.
* Một Yêu cầu cấp phát từ bệnh viện có thể bao gồm nhiều Túi máu khác nhau, nhưng một Túi máu chỉ được cấp phát cho một Yêu cầu cấp phát duy nhất.

### 3. Mô hình nghiệp vụ bằng UML

**Xác định các Actor (Tác nhân) của hệ thống:**

1. **Người hiến máu (Blood Donor):** Tác nhân độc lập bên ngoài hệ thống.
2. **Người dùng nội bộ (Internal User):** Tác nhân tổng quát (Super-actor) đại diện cho tất cả nhân sự có tài khoản cấp phát nội bộ. Tác nhân này chứa 05 tác nhân con (Sub-actors) kế thừa chức năng đăng nhập, bao gồm:
* Cán bộ y tế
* Kỹ thuật viên xét nghiệm
* Kỹ thuật viên kho
* Nhân viên bệnh viện tuyến dưới
* Ban quản trị

**Các Use Case chi tiết với từng Actor:**

**Actor: Người hiến máu**
* **UC01: Đăng ký tài khoản:** Bắt buộc bao gồm luồng `<<Include>>` **Nhập thông tin cá nhân** để định danh.
* **UC02: Đăng nhập:** Truy cập vào hệ thống dành cho người dùng cuối.
* **UC03: Quản lý hồ sơ cá nhân:** Cập nhật các thông tin cá nhân
* **UC04: Tra cứu chiến dịch:** Khi thực hiện chức năng này, hệ thống bắt buộc chạy luồng `<<Include>>` **Kiểm tra điều kiện hiến máu** (thời gian giữa các lần hiến). Nếu thỏa mãn điều kiện, ca sử dụng này có thể mở rộng `<<Extend>>` sang chức năng **Đặt lịch hiến máu**.
* **UC05: Xem lịch sử hiến máu và tải chứng nhận điện tử:** Truy xuất kết quả của các lần tham gia trước.


**Actor: Người dùng nội bộ (Và các tác nhân kế thừa)**
* **UC06: Đăng nhập:** Toàn bộ 5 tác nhân con đều kế thừa tính năng xác thực tài khoản qua cổng nội bộ này.


**Actor: Cán bộ y tế**
* **UC07: Quét QR lịch hẹn và nhập các chỉ số cơ bản của người hiến máu (đủ / không đủ điều kiện):** Trong trường hợp người hiến được đánh giá là "Đủ điều kiện", chức năng này sẽ kích hoạt luồng `<<Extend>>` **Sinh mã vạch cho ống máu xét nghiệm nhanh**.
* **UC08: Ấn nút đồng ý lấy máu:** Hành động này bắt buộc hệ thống thực thi luồng `<<Include>>` **Tự động in mã vạch cho túi máu**.


* **Actor: Kỹ thuật viên xét nghiệm**
* **UC09: Nhập kết quả xét nghiệm nhanh (đủ / không đủ điều kiện):** Nếu kết quả là đạt (đủ điều kiện), hệ thống sẽ kích hoạt luồng `<<Extend>>` **Sinh mã vạch cho túi máu và các ống máu xét nghiệm chuyên sâu** để chuẩn bị cho khâu chọc tĩnh mạch.
* **UC10: Nhập kết quả xét nghiệm chuyên sâu (đủ / không đủ điều kiện):** Sau khi hoàn tất nhập kết quả của 5 bệnh truyền nhiễm, nếu túi máu an toàn (đủ điều kiện), hệ thống sẽ tự động kích hoạt luồng `<<Extend>>` **Tự động sắp xếp vị trí và ghi nhận ngày hết hạn của túi máu** mà không cần con người tính toán thủ công.


* **Actor: Kỹ thuật viên kho**
* **UC11: Quét mã vạch để xem vị trí đặt túi máu, thông tin của túi máu:** Truy xuất hồ sơ vật lý trong kho lạnh.
* **UC12: Quản lý túi máu:** Thực hiện các nghiệp vụ kiểm kê, xử lý túi máu lỗi hoặc quá hạn.
* **UC13: Xem báo cáo thống kê tồn kho:** Theo dõi số lượng theo nhóm máu và chế phẩm.
* **UC14: Tạo và duyệt yêu cầu cấp máu trực tiếp của nhân viên nội bộ:** Xử lý các chỉ định truyền máu ngay tại đơn vị sở tại.
* **UC15: Duyệt yêu cầu cấp máu của bệnh viện tuyến dưới:** Chấp thuận và tiến hành xuất kho cho các đơn hàng từ xa.


* **Actor: Nhân viên bệnh viện tuyến dưới**
* **UC16: Tạo đơn yêu cầu cấp máu (khẩn cấp / bình thường):** Khi hoàn tất biểu mẫu, hệ thống bắt buộc thực thi luồng `<<Include>>` **Gửi yêu cầu đến Kỹ thuật viên kho** để thông báo lập tức.
* **UC17: Theo dõi tiến độ của đơn yêu cầu cấp máu:** Xem trạng thái đơn hàng (đang duyệt, đang xuất kho).


* **Actor: Ban quản trị**
* **UC18: Quản lý tài khoản:** Cấp phát, phân quyền, khóa tài khoản cho toàn bộ hệ sinh thái "Người dùng nội bộ".
* **UC19: Quản lý các chiến dịch hiến máu:** Tổ chức, sắp xếp lịch trình và địa điểm tiếp nhận.
* **UC20: Trích xuất báo cáo thống kê lượt người hiến và tỷ lệ hủy máu quá hạn:** Phục vụ công tác quản lý vĩ mô của Sở Y tế.


### 4. Bảng yêu cầu người dùng (User Requirements)

| ID | Mô tả chi tiết yêu cầu người dùng | Độ ưu tiên |
| --- | --- | --- |
| UR-01 | Hệ thống phải cung cấp chức năng "Đăng ký tài khoản" cho Người hiến máu, yêu cầu bắt buộc phải hoàn thành biểu mẫu "Nhập thông tin cá nhân" mới được phép lưu vào cơ sở dữ liệu. | Cao |
| UR-02 | Khi Người hiến máu chọn "Tra cứu chiến dịch", hệ thống phải tự động chạy quy trình ngầm "Kiểm tra điều kiện hiến máu" (Ví dụ: khoảng cách thời gian từ lần hiến trước). Nếu thỏa mãn, giao diện mới hiển thị thêm tính năng "Đặt lịch hiến máu". | Cao |
| UR-03 | Hệ thống phải thiết kế một cổng "Đăng nhập" chung (Single Sign-On module) cho tác nhân "Người dùng nội bộ", tự động phân quyền giao diện tùy thuộc vào vai trò (Cán bộ y tế, Xét nghiệm, Kho, Bệnh viện, Ban quản trị). | Cao |
| UR-04 | Sau khi Cán bộ y tế quét mã QR và nhập chỉ số sinh tồn đạt chuẩn (Đủ điều kiện), hệ thống phải tự động sinh ra một mã vạch chuyên biệt dành riêng cho "Ống máu xét nghiệm nhanh" để sử dụng tại chỗ. | Cao |
| UR-05 | Khi Kỹ thuật viên xét nghiệm nhập kết quả xét nghiệm nhanh là "Đủ điều kiện", hệ thống phải lập tức sinh ra bộ mã vạch đồng bộ cho cả "Túi máu chính" và "Các ống máu xét nghiệm chuyên sâu". | Cao |
| UR-06 | Khi Cán bộ y tế thao tác "Ấn nút đồng ý lấy máu" trên giao diện, hệ thống phải gửi lệnh kết nối thiết bị ngoại vi để tự động in tem mã vạch vật lý cho túi máu. | Cao |
| UR-07 | Khi Kỹ thuật viên xét nghiệm hoàn tất "Nhập kết quả xét nghiệm chuyên sâu" với kết quả an toàn, phần mềm phải chạy thuật toán để: (1) Tự động sắp xếp vị trí khuyên dùng trong tủ lạnh và (2) Tự động cộng số ngày để ghi nhận chính xác hạn sử dụng của túi máu đó. | Cao |
| UR-08 | Hệ thống cung cấp cho Kỹ thuật viên kho công cụ quét mã vạch trên túi máu vật lý để truy xuất chính xác vị trí đang đặt túi máu và toàn bộ thông tin lịch sử của túi máu đó. | Trung bình |
| UR-09 | Hệ thống cung cấp giao diện cho Kỹ thuật viên kho duyệt hai loại yêu cầu cấp máu: (1) Yêu cầu trực tiếp từ nội bộ trung tâm và (2) Yêu cầu từ các bệnh viện tuyến dưới gửi về. | Cao |
| UR-10 | Khi Nhân viên bệnh viện tuyến dưới nhấn hoàn tất "Tạo đơn yêu cầu cấp máu", hệ thống bắt buộc phải đẩy một thông báo (Notification) ngay lập tức đến màn hình làm việc của Kỹ thuật viên kho trực ca. | Cao |
| UR-11 | Ban quản trị có thẩm quyền cao nhất để vận hành chức năng "Trích xuất báo cáo", lọc số liệu thống kê về lượt người tham gia hiến máu và tỷ lệ túi máu bị hủy bỏ do quá hạn sử dụng. | Trung bình |

---

