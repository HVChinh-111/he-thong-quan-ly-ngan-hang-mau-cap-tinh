 
**Dự án:** Hệ thống Quản lý Ngân hàng Máu cấp Tỉnh — Cụ thể tại Thành phố Hà Nội (Provincial Blood Bank Management System — PBBMS)

### PHẦN 1: MÔ TẢ HỆ THỐNG

#### Mô tả chung về hệ thống và lý do lựa chọn

**Mô tả chung (đề xuất của dự án / giả định thiết kế):**  
Hệ thống Quản lý Ngân hàng Máu cấp Tỉnh (PBBMS) được mô tả như một nền tảng phần mềm quản trị tập trung nhằm số hóa và điều phối các hoạt động liên quan đến **thu thập, xét nghiệm sàng lọc, điều chế, lưu trữ, và phân phối máu/chế phẩm máu** trên phạm vi một mạng lưới (trong đề tài này là địa bàn Thành phố Hà Nội). Mô hình “điều phối tập trung” và “mạng lưới cung ứng máu tích hợp” phù hợp với khuyến nghị của WHO về việc các hoạt động thu gom–xét nghiệm–xử lý–lưu trữ–phân phối cần được điều phối thống nhất bằng chính sách và tiêu chuẩn nhằm đảm bảo chất lượng, an toàn và khả năng cung ứng. [1](https://www.who.int/news-room/fact-sheets/detail/blood-safety-and-availability)

Trong thiết kế đề xuất, hệ thống đóng vai trò cầu nối liên kết các nhóm người dùng chính như: người hiến máu, nhân viên tiếp nhận, kỹ thuật viên xét nghiệm/chế biến, cơ sở sử dụng máu (bệnh viện), và quản trị hệ thống. Phạm vi nghiệp vụ dự kiến bao phủ “vòng đời” một đơn vị máu từ đăng ký hiến máu, tiếp nhận và sàng lọc trước hiến, lấy máu, xét nghiệm sàng lọc, bảo quản theo chuỗi lạnh, và phân phối cho điều trị/cấp cứu. Các bước nghiệp vụ này tương thích với mô tả chuỗi hoạt động trong hệ thống truyền máu của WHO và quy định/định hướng tổ chức hoạt động truyền máu trong văn bản hướng dẫn của Việt Nam.[2](https://www.who.int/news-room/fact-sheets/detail/blood-safety-and-availability)

**Điểm chỉnh sửa quan trọng (fact-check về xét nghiệm “bắt buộc”):**  
Tài liệu gốc nêu “xét nghiệm năm bệnh truyền nhiễm bắt buộc (HIV, Viêm gan B, Viêm gan C, Giang mai và Sốt rét)”. Theo Circular 26/2013/TT-BYT, **các xét nghiệm bắt buộc áp dụng cho tất cả đơn vị máu và thành phần máu hiến** bao gồm:  
- Xét nghiệm nhóm máu: ABO, Rh(D), và sàng lọc kháng thể bất thường.  
- Xét nghiệm sàng lọc tác nhân lây truyền qua đường truyền máu: HIV, viêm gan B, viêm gan C, và giang mai. [3](https://thuvienphapluat.vn/van-ban/EN/The-thao-Y-te/Circular-No-26-2013-TT-BYT-guidance-on-the-blood-transfusion/271388/tieng-anh.aspx)

**Sốt rét (malaria) không phải xét nghiệm “bắt buộc cho mọi đơn vị”** trong Circular 26/2013/TT-BYT, nhưng **được yêu cầu trong các tình huống nguy cơ cụ thể** (người hiến sống/làm việc ở vùng sốt rét theo công bố của Bộ Y tế; hoặc mới đi/về từ vùng dịch theo mốc thời gian quy định; hoặc có tiền sử mắc sốt rét theo mốc thời gian quy định). [3](https://thuvienphapluat.vn/van-ban/EN/The-thao-Y-te/Circular-No-26-2013-TT-BYT-guidance-on-the-blood-transfusion/271388/tieng-anh.aspx)

Trong khuôn khổ thiết kế PBBMS, phần “quản lý kết quả xét nghiệm” nên được mô tả chính xác là: quản lý **các xét nghiệm bắt buộc theo Circular 26/2013/TT-BYT** và hỗ trợ quản lý **các xét nghiệm bổ sung theo chỉ định/điều kiện nguy cơ** (ví dụ: sốt rét theo tiêu chí nguy cơ; CMV trong một số trường hợp đặc biệt). [3](https://thuvienphapluat.vn/van-ban/EN/The-thao-Y-te/Circular-No-26-2013-TT-BYT-guidance-on-the-blood-transfusion/271388/tieng-anh.aspx)

Nguồn xác thực: WHO (donation testing; tổ chức mạng lưới máu), Circular 26/2013/TT-BYT.[4](https://www.who.int/teams/health-product-policy-and-standards/standards-and-specifications/blood-and-products-of-human-origin/quality-and-safety/donation-testing)

**Lý do lựa chọn đề tài:**  
Dự án được lựa chọn phát triển dựa trên những vấn đề thực tiễn trong công tác quản lý và điều phối máu, đặc biệt nhấn mạnh các bài toán: biến động nguồn cung theo mùa/cao điểm, hạn sử dụng ngắn của chế phẩm (đặc biệt là tiểu cầu), và nhu cầu tăng cường số hóa/quản trị dữ liệu để phối hợp liên cơ sở. [5](https://moh.gov.vn/home?_101_struts_action=%2Fasset_publisher%2Fview_content&_101_type=content&_101_urlTitle=du-tru-80-000-on-vi-mau-cho-cuoi-nam-va-tet-nguyen-an&p_p_id=101&p_p_lifecycle=0&p_p_mode=view&p_p_state=maximized)

* **Khắc phục quy trình thủ công:** Hiện tại, tài liệu gốc nhận định “nhiều điểm hiến máu lưu động vẫn sử dụng giấy tờ in sẵn…”. Khẳng định này **chưa đủ bằng chứng công khai để kết luận cho Hà Nội** (cần khảo sát thực địa theo từng điểm hiến/đơn vị tổ chức). Tuy nhiên, có bằng chứng rằng quy trình hiến máu vẫn có các “phiếu/biểu mẫu” trong thực hành (ví dụ: NIHBT nhắc tới “phiếu đăng ký hiến máu” khi người hiến cung cấp email; và một số bệnh viện có hệ thống biểu mẫu quy trình). Vì vậy, nên diễn đạt thận trọng: “quy trình còn tồn tại biểu mẫu và mức độ số hóa không đồng nhất theo cơ sở/điểm hiến; cần khảo sát thực địa tại Hà Nội.”  
  **Đánh dấu:** Chưa xác thực được bằng nguồn chính thống (theo phạm vi “nhiều điểm hiến máu lưu động tại Hà Nội”). [6](https://vienhuyethoc.vn/huong-dan-nhan-ket-qua-hien-mau/)

* **Tối ưu hóa công tác điều phối:** Tình trạng thiếu máu/căng thẳng tồn kho thường được ghi nhận vào các giai đoạn cao điểm (cuối năm, trước–sau Tết) và theo mùa (mùa hè), thể hiện qua các thông báo/kêu gọi tiếp nhận máu và kế hoạch dự trữ của cơ quan/đơn vị chuyên trách. Do đó, một hệ thống điều phối dữ liệu và kế hoạch (đề xuất) có cơ sở thực tiễn để cải thiện khả năng nắm bắt nhu cầu–tồn kho–chiến dịch huy động. [7](https://moh.gov.vn/home?_101_struts_action=%2Fasset_publisher%2Fview_content&_101_type=content&_101_urlTitle=du-tru-80-000-on-vi-mau-cho-cuoi-nam-va-tet-nguyen-an&p_p_id=101&p_p_lifecycle=0&p_p_mode=view&p_p_state=maximized) 

* **Giảm thiểu lãng phí chế phẩm máu:** Chế phẩm máu có hạn sử dụng hữu hạn; riêng tiểu cầu trong thực hành phổ biến tại Việt Nam được nêu “tối đa 5 ngày” (khi bảo quản theo điều kiện phù hợp). Vì vậy, bài toán giảm hủy do quá hạn là xác đáng. Tuy nhiên, câu “đảm bảo không có túi máu nào bị tiêu hủy do quá hạn… trong khi bệnh viện khác lại đang thiếu hụt” là **khẳng định quá mạnh** (không thể cam kết tuyệt đối chỉ bằng phần mềm).  
  **Chỉnh sửa đúng theo bằng chứng:** “Phần mềm có thể hỗ trợ ưu tiên xuất kho các đơn vị gần hết hạn (nguyên tắc ‘gần hết hạn xuất trước’) và cảnh báo sớm, từ đó giảm nguy cơ hủy do quá hạn và giảm mất cân đối phân bổ; hiệu quả thực tế phụ thuộc quy trình vận hành, năng lực vận chuyển chuỗi lạnh, và cơ chế phối hợp liên cơ sở.” [8](https://vienhuyethoc.vn/han-su-dung-cua-mau/)

* **Nâng cao trải nghiệm và sự gắn kết của người hiến máu:** Luận điểm “thiếu kênh thông tin liên tục” mang tính quan sát và cần khảo sát định lượng nếu muốn kết luận ở mức độ phổ quát. Tuy nhiên, có bằng chứng rằng NIHBT phát triển ứng dụng nhằm “chăm sóc, tạo trải nghiệm… vận động hiến máu nhắc lại” và cung cấp chức năng theo dõi “hành trình đơn vị máu hiến” và kết quả hiến máu. Do đó, nên chỉnh thành: “Tính năng theo dõi lịch sử hiến máu/kết quả và hành trình đơn vị máu có thể góp phần tăng trải nghiệm và hỗ trợ vận động hiến máu nhắc lại.” [9](https://vienhuyethoc.vn/hm/)

#### Khảo sát các hệ thống tương tự

Để xây dựng hệ thống PBBMS đáp ứng đúng tiêu chuẩn, cần đối chiếu với các mô hình đang vận hành thực tế và các định hướng số hóa/liên thông quản lý người hiến máu và đơn vị máu. [10](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html) 

**Hệ thống 1: Ứng dụng di động “Hiến máu” của Viện Huyết học - Truyền máu Trung ương (NIHBT)**

* **Mô tả (đã xác thực và chỉnh sửa):** Ứng dụng “Hiến máu” được NIHBT phối hợp Viettel phát triển, cho phép người hiến: tra cứu thông tin hiến máu, địa điểm hiến máu, nhu cầu máu của bệnh viện; đăng ký/đặt lịch hiến; theo dõi lịch sử hiến máu; xem hành trình đơn vị máu hiến và kết quả hiến máu (sau khoảng thời gian cập nhật). Ứng dụng có lưu ý về điều kiện đối sánh thông tin cá nhân (số giấy tờ/điện thoại) và phạm vi dữ liệu hiện chỉ cập nhật từ NIHBT và một số cơ sở dùng chung phần mềm quản lý hiến máu. [11](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html)

  **Điểm chỉnh sửa quan trọng:** Câu “được liên kết trực tiếp với cơ sở dữ liệu quốc gia về dân cư” trong tài liệu gốc **không tìm được bằng chứng chính thống trong tài liệu công khai của NIHBT** (các hướng dẫn công khai chỉ nêu yêu cầu trùng khớp thông tin định danh giữa hồ sơ hiến máu và hồ sơ khai báo trên app).  
  **Đánh dấu:** Chưa xác thực được bằng nguồn chính thống. [12](https://vienhuyethoc.vn/hm/)

* **Ưu điểm (đã xác thực và chỉnh sửa):**
  * Cung cấp giao diện cho người hiến máu/End-user: tra cứu thông tin, địa điểm, nhu cầu máu, tin tức. [13](https://vienhuyethoc.vn/hm/)
  * Cho phép đăng ký/đặt lịch hiến máu và theo dõi lịch sử hiến máu.  [13](https://vienhuyethoc.vn/hm/)
  * Cho phép xem kết quả hiến máu và “hành trình đơn vị máu” theo cơ chế xác thực (PIN/mật khẩu), với thời gian cập nhật thường sau hiến khoảng 7–15 ngày (không tính cuối tuần/ngày lễ theo hướng dẫn).  [11](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html)

  **Điểm chỉnh sửa quan trọng:** Tài liệu gốc nêu “nhận chứng nhận hiến máu điện tử”. Các tài liệu công khai của NIHBT và MOH thể hiện **giấy chứng nhận hiến máu** (giấy) và giá trị bồi hoàn máu; NIHBT cũng hướng dẫn người hiến kiểm tra/giữ giấy chứng nhận trong một số trường hợp. Vì vậy, trong phạm vi fact-check, không nên khẳng định đã có “chứng nhận điện tử” trong app. [14](https://moh.gov.vn/chuong-trinh-muc-tieu-quoc-gia/-/asset_publisher/7ng11fEWgASC/content/thong-tin-quyen-loi-va-che-o-oi-voi-nguoi-hien-mau-tinh-nguyen?inheritRedirect=false)

* **Nhược điểm (Khoảng trống để PBBMS giải quyết) — đã chỉnh sửa theo bằng chứng:** Ứng dụng “Hiến máu” hiện thiên về tương tác với người hiến và chỉ bao phủ dữ liệu của NIHBT và một số cơ sở dùng chung phần mềm; vì vậy, để đạt mục tiêu “điều phối cấp tỉnh/thành phố” theo nghĩa liên thông đa cơ sở, vẫn cần cơ chế liên thông dữ liệu rộng hơn giữa địa phương–trung tâm máu–bệnh viện tiếp nhận/sử dụng máu. Nhận định này phù hợp với định hướng của lãnh đạo MOH về nhu cầu “kết nối thông tin, xây dựng cơ sở dữ liệu người hiến máu thống nhất, liên thông giữa các địa phương, giữa các trung tâm máu, bệnh viện có tiếp nhận máu,” cũng như khuyến nghị của WHO về mạng lưới cung ứng máu tích hợp/điều phối thống nhất. [15](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html) 

Nguồn xác thực: NIHBT (hướng dẫn app, FAQ, hướng dẫn nhận kết quả), MOH/TTXVN định hướng liên thông dữ liệu, WHO policy/fact sheet. [16](https://vienhuyethoc.vn/hm/) 

**Hệ thống 2: Phân hệ quản lý ngân hàng máu trong các Hệ thống Thông tin Bệnh viện (Hospital Information System — HIS)**

* **Mô tả (đã xác thực một phần và chỉnh sửa):** Nhiều cơ sở y tế triển khai các nền tảng HIS để quản lý hoạt động khám chữa bệnh. Tài liệu gốc nêu ví dụ VNPT HIS và Viettel HIS; các mô tả sản phẩm công khai của nhà cung cấp xác nhận đây là các hệ thống HIS tổng thể. [17](https://vnpt.vn/doanh-nghiep/giai-phap-cntt/dich-vu-phan-mem-quan-ly-benh-vien-vnpt-his/)

  Riêng với Viettel HIS, trang mô tả công khai có đề cập đến báo cáo của phân hệ LIS bao gồm nội dung “quản lý kho máu” (ở mức mô tả tính năng). Do đó, có thể giữ nhận định rằng **một số nền tảng HIS có hỗ trợ nghiệp vụ liên quan quản lý kho máu**, nhưng mức độ triển khai cụ thể (quy trình cấp phát, liên thông với trung tâm máu, chuẩn dữ liệu…) cần được đánh giá theo từng bệnh viện/hợp đồng triển khai. [18](https://solutions.viettel.vn/vi/y-te-so/phan-mem-quan-ly-benh-vien-viettel-his.html)

* **Ưu điểm (chỉnh thành giả định thiết kế/nhận định cần khảo sát):** Việc tích hợp nghiệp vụ kho máu vào HIS/LIS có thể giúp bệnh viện theo dõi tồn kho, gắn thông tin người bệnh và chỉ định truyền máu, và chuẩn hóa báo cáo nội bộ. Tuy nhiên, mô tả chi tiết “tủ lạnh của khoa Hồi sức cấp cứu” hay các chức năng cụ thể khác **chưa có tài liệu chính thống công khai đủ để xác thực như một thực trạng phổ biến**, do đó nên coi là giả định khảo sát/đầu bài nghiệp vụ cần làm rõ khi khảo sát thực địa.  
  **Đánh dấu:** Chưa xác thực được bằng nguồn chính thống (ở mức mô tả phổ quát cho “các bệnh viện tuyến tỉnh/tuyến huyện”).  [19](https://solutions.viettel.vn/vi/y-te-so/phan-mem-quan-ly-benh-vien-viettel-his.html)
* **Nhược điểm (Khoảng trống để PBBMS giải quyết) — đã chỉnh sửa theo bằng chứng:** Nhận định “dữ liệu mang tính cục bộ/siloed” và việc phải “gọi điện thoại thủ công” là mô tả quy trình vận hành cụ thể, cần khảo sát thực địa để kết luận. Tuy nhiên, nhu cầu **tăng kết nối giữa các cơ sở truyền máu và đồng bộ dữ liệu phục vụ điều phối** đã được nêu rõ trong các phát biểu/chỉ đạo và hội nghị chuyên môn cấp quốc gia (MOH/TTXVN; VietnamPlus trích ý kiến Cục Quản lý Khám, chữa bệnh). Vì vậy, nên diễn đạt đúng mức: “Nếu các HIS hiện có chưa hỗ trợ liên thông yêu cầu cấp phát và tồn kho theo mạng lưới, PBBMS (đề xuất) hướng tới lấp khoảng trống liên thông và điều phối giữa ‘kho máu trung tâm’ và các cơ sở sử dụng máu.” [10](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html) 

Nguồn xác thực: mô tả sản phẩm HIS (VNPT/Viettel) và định hướng chính sách/chuyên môn về liên thông dữ liệu quản lý người hiến máu và dịch vụ máu. [20](https://vnpt.vn/doanh-nghiep/giai-phap-cntt/dich-vu-phan-mem-quan-ly-benh-vien-vnpt-his/)

### Tổng kết mức độ tin cậy

**Những nội dung đã xác thực tốt:**  
Các phần liên quan đến tối thiểu xét nghiệm sàng lọc bắt buộc (HIV, HBV, HCV, giang mai), xét nghiệm nhóm máu ABO/RhD và nguyên tắc điều phối/tổ chức mạng lưới cung ứng máu; các thông tin về hạn dùng tiểu cầu “tối đa 5 ngày” theo mô tả thực hành của NIHBT; và việc tồn tại nhu cầu điều phối máu theo mùa/cao điểm đều có nguồn chính thống hỗ trợ. [21](https://thuvienphapluat.vn/van-ban/EN/The-thao-Y-te/Circular-No-26-2013-TT-BYT-guidance-on-the-blood-transfusion/271388/tieng-anh.aspx)

**Những nội dung đã chỉnh sửa:**  
(1) “5 bệnh truyền nhiễm bắt buộc” được chỉnh thành “4 tác nhân bắt buộc + sốt rét theo điều kiện nguy cơ”; (2) các câu khẳng định mang tính cam kết tuyệt đối về không hủy túi máu được giảm mức (chỉ khẳng định “giảm nguy cơ/giảm lãng phí”); (3) mô tả app “Hiến máu” được chỉnh để bỏ/đánh dấu các điểm chưa đủ chứng cứ (liên kết CSDLQG dân cư; chứng nhận điện tử). [22](https://thuvienphapluat.vn/van-ban/EN/The-thao-Y-te/Circular-No-26-2013-TT-BYT-guidance-on-the-blood-transfusion/271388/tieng-anh.aspx)

**Những nội dung chưa tìm được nguồn chính thống đủ mạnh:**  
Tỷ lệ/độ phổ biến của việc dùng “giấy tờ in sẵn” tại các điểm hiến máu lưu động ở Hà Nội; và mô tả “gọi điện thoại thủ công” như một quy trình chuẩn/đại trà khi bệnh viện cần xin cấp phát máu (cần khảo sát thực địa). [23](https://vienhuyethoc.vn/huong-dan-nhan-ket-qua-hien-mau/)

**Khuyến nghị khảo sát thực địa:**  
Ưu tiên khảo sát tại các điểm hiến máu lưu động và các bệnh viện tuyến huyện/tuyến tỉnh trong phạm vi Hà Nội để xác định: mức độ số hóa biểu mẫu; luồng dữ liệu từ hiến máu → xét nghiệm → kho lạnh → phân phối; và mức độ liên thông hiện có giữa bệnh viện–trung tâm máu–Sở Y tế. [24](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html)

## Fact-Check Summary Table

| Phần nội dung | Trạng thái xác thực (Đúng / Đúng một phần / Cần sửa / Chưa xác thực được) | Ghi chú chỉnh sửa | Nguồn |
|---|---|---|---|
| PBBMS là nền tảng điều phối tập trung cho chuỗi cung ứng máu | Đúng một phần | Đây là **mô tả đề xuất**; bổ sung căn cứ rằng WHO khuyến nghị điều phối theo mạng lưới tích hợp/chuẩn hóa. |[1](https://www.who.int/news-room/fact-sheets/detail/blood-safety-and-availability)  |
| Phạm vi bao phủ vòng đời đơn vị máu (thu thập–xét nghiệm–lưu trữ–phân phối) | Đúng một phần | Giữ như chuỗi nghiệp vụ khung; gắn nguồn WHO/MOH về các hoạt động trong hệ thống máu. | [2](https://www.who.int/news-room/fact-sheets/detail/blood-safety-and-availability) |
| “5 bệnh truyền nhiễm bắt buộc: HIV, HBV, HCV, giang mai, sốt rét” | Cần sửa | Sửa thành: **bắt buộc cho mọi đơn vị**: HIV, HBV, HCV, giang mai + ABO/Rh(D) + sàng lọc kháng thể bất thường; **sốt rét theo điều kiện nguy cơ**. |[25](https://thuvienphapluat.vn/van-ban/EN/The-thao-Y-te/Circular-No-26-2013-TT-BYT-guidance-on-the-blood-transfusion/271388/tieng-anh.aspx)|
| Thiếu máu cao điểm dịp lễ/Tết và mùa hè | Đúng | Có bằng chứng từ NIHBT/MOH về kế hoạch dự trữ và lời kêu gọi hiến máu trong các giai đoạn cao điểm. |[7](https://moh.gov.vn/home?_101_struts_action=%2Fasset_publisher%2Fview_content&_101_type=content&_101_urlTitle=du-tru-80-000-on-vi-mau-cho-cuoi-nam-va-tet-nguyen-an&p_p_id=101&p_p_lifecycle=0&p_p_mode=view&p_p_state=maximized)   |
| Tiểu cầu “tối đa 5 ngày” | Đúng | Giữ nguyên; gắn nguồn NIHBT và MOH (bài MOH cũng nhắc tiểu cầu tối đa 5 ngày). |[8](https://vienhuyethoc.vn/han-su-dung-cua-mau/)|
| “FEFO đảm bảo không có túi máu nào bị tiêu hủy do quá hạn…” | Cần sửa | Hạ mức khẳng định: phần mềm **giảm nguy cơ** quá hạn/hủy, không cam kết tuyệt đối; hiệu quả phụ thuộc vận hành. |[26](https://vienhuyethoc.vn/han-su-dung-cua-mau/) |
| “Nhiều điểm hiến máu lưu động vẫn dùng giấy tờ in sẵn” (Hà Nội) | Chưa xác thực được | Chỉ có bằng chứng gián tiếp về tồn tại “phiếu/biểu mẫu”; cần khảo sát theo địa bàn Hà Nội. | [6](https://vienhuyethoc.vn/huong-dan-nhan-ket-qua-hien-mau/)
 |
| App “Hiến máu” do NIHBT phát triển, giúp đăng ký/đặt lịch, xem lịch sử, xem kết quả và hành trình đơn vị máu | Đúng | Nêu đúng tính năng theo hướng dẫn chính thức; có mốc cập nhật 7–15 ngày. | [9](https://vienhuyethoc.vn/hm/) |
| App “Hiến máu” liên kết trực tiếp CSDL quốc gia về dân cư | Chưa xác thực được | Không thấy được khẳng định này trong hướng dẫn công khai của NIHBT; chỉ có yêu cầu trùng khớp thông tin định danh. | [9](https://vienhuyethoc.vn/hm/)|
| App có “chứng nhận hiến máu điện tử” | Chưa xác thực được | Nguồn chính thống nêu giấy chứng nhận (giấy) và giá trị bồi hoàn máu; không đủ căn cứ xác nhận e-certificate trong app. | [14](https://moh.gov.vn/chuong-trinh-muc-tieu-quoc-gia/-/asset_publisher/7ng11fEWgASC/content/thong-tin-quyen-loi-va-che-o-oi-voi-nguoi-hien-mau-tinh-nguyen?inheritRedirect=false) |
| HIS có module “quản lý kho máu” (đại trà cho mọi nền tảng) | Đúng một phần | Viettel HIS mô tả có “quản lý kho máu” trong báo cáo LIS; phạm vi triển khai thực tế vẫn cần khảo sát theo bệnh viện. |[18](https://solutions.viettel.vn/vi/y-te-so/phan-mem-quan-ly-benh-vien-viettel-his.html) |
| “Bệnh viện X hết nhóm O phải gọi điện thủ công…” | Chưa xác thực được | Có định hướng cấp quốc gia về liên thông dữ liệu/điều phối; nhưng mô tả quy trình gọi điện là chi tiết vận hành, cần khảo sát thực địa. | [10](https://chinhsachcuocsong.vnanet.vn/ung-dung-chuyen-doi-so-y-te-vao-quan-ly-nguoi-hien-mau-va-cac-don-vi-mau/33577.html)  |
