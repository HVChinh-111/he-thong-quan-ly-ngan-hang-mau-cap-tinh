
### PHẦN 1: MÔ TẢ HỆ THỐNG

#### 1. Mô tả chung về hệ thống và lý do lựa chọn

**Mô tả chung:**

Hệ thống Quản lý Ngân hàng Máu cấp Tỉnh (PBBMS) là một nền tảng phần mềm quản trị tập trung, được thiết kế để số hóa toàn diện quy trình cung ứng máu nhân đạo trên địa bàn Thành phố Hà Nội. Hệ thống này đóng vai trò là cầu nối liên kết năm nhóm đối tượng chính bao gồm: Người hiến máu, Cán bộ y tế tiếp nhận, Kỹ thuật viên xét nghiệm, Bệnh viện tuyến dưới và Ban Quản trị. Phạm vi của hệ thống bao phủ toàn bộ vòng đời của một đơn vị máu, bắt đầu từ thao tác đăng ký hiến máu trực tuyến của người dân, ghi nhận kết quả khám lâm sàng, tiếp nhận máu, quản lý kết quả xét nghiệm năm bệnh truyền nhiễm bắt buộc cho mọi đơn vị: HIV, HBV, HCV, giang mai + ABO/Rh(D) + sàng lọc kháng thể bất thường; sốt rét theo điều kiện nguy cơ., lưu trữ kho lạnh, cho đến khâu phân phối theo yêu cầu cấp cứu của các cơ sở y tế.

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


* **Nhược điểm (Khoảng trống để PBBMS giải quyết):** Các hệ thống HIS này mang tính cục bộ (Siloed Data). Khi Bệnh viện X hết máu nhóm O, họ phải gọi điện thoại thủ công lên Viện Huyết học tuyến trên để xin cấp phát, thay vì hệ thống HIS tự động đẩy một yêu cầu điện tử (e-Request) lên một nền tảng quản lý kho máu chung của toàn tỉnh để xử lý tự động. Nếu các HIS hiện có chưa hỗ trợ liên thông yêu cầu cấp phát và tồn kho theo mạng lưới, PBBMS (đề xuất) hướng tới lấp khoảng trống liên thông và điều phối giữa ‘kho máu trung tâm’ và các cơ sở sử dụng máu
---