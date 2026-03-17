# Chương 6: Tính Toán

> "Hãy cẩn thận với những chi phí nhỏ; một vết rò nhỏ sẽ đắm một con tàu lớn."
> — Benjamin Franklin

Nhân viên trung bình tại Mỹ có giá 85.000 đô la mỗi năm về lương. Nhưng lương chỉ là điểm khởi đầu. Thêm bảo hiểm y tế (7.000–15.000 đô la), thuế bảng lương (7,65%), đóng góp hưu trí, nghỉ phép có lương, thiết bị, giấy phép phần mềm, không gian văn phòng, chi phí quản lý, HR, đào tạo, và chi phí mà không ai lập ngân sách cho (doanh chuyển, ở mức 50–200% lương hàng năm mỗi lần ra đi) và chi phí thực sự rơi vào khoảng 120.000 đến 170.000 đô la mỗi người mỗi năm.

Một AI agent trên Paperclip có giá 50 đến 500 đô la mỗi tháng.

Khoảng cách đó không phải là một cải tiến nhỏ. Đó là một sự thay đổi cơ cấu. Nếu bạn đang quyết định giữa việc thuê nhân viên đầu tiên và xây dựng sơ đồ tổ chức AI đầu tiên, chương này là nơi bạn đưa ra quyết định.

## Một Nhân Viên Thực Sự Tốn Bao Nhiêu

Hầu hết các nhà sáng lập nghĩ về lương. Con số thực chạy gấp 1,4 đến 2 lần đó.

**Thù lao trực tiếp.** Lương, thưởng, hoa hồng, con số trong tin tuyển dụng.

**Phúc lợi.** Bảo hiểm y tế trung bình 7.911 đô la cho bảo hiểm cá nhân và 22.463 đô la cho bảo hiểm gia đình mỗi năm (dữ liệu Kaiser Family Foundation 2024). Thêm nha khoa, thị lực, bảo hiểm nhân thọ và khuyết tật.

**Thuế bảng lương.** An sinh xã hội (6,2%), Medicare (1,45%), thất nghiệp liên bang và tiểu bang. Bạn trả những khoản này trên lương. Chúng không được khấu trừ từ lương.

**Hưu trí.** Một khoản đóng góp 401(k) cạnh tranh có giá 3–6% lương.

**Nghỉ phép có lương.** Công nhân trung bình tại Mỹ nhận được 10 ngày nghỉ phép, 8 ngày ốm, và 7–10 ngày nghỉ lễ có lương, khoảng 5–6 tuần lương cho không có sản lượng. Với mức lương 85.000 đô la, đó là khoảng 8.000 đô la không sản xuất có lương.

**Thiết bị và phần mềm.** Laptop, màn hình, điện thoại, bàn làm việc, giấy phép. Ngân sách 3.000–5.000 đô la mỗi nhân viên mỗi năm.

**Không gian văn phòng.** Chi phí trung bình mỗi nhân viên: 12.000–18.000 đô la mỗi năm ở một thành phố Mỹ cấp trung. Nhiều hơn nhiều ở San Francisco, New York, hoặc Los Angeles.

**Chi phí quản lý.** Mỗi nhân viên cần được quản lý. Tỷ lệ tiêu chuẩn là một quản lý cho 5–8 báo cáo trực tiếp. Thời gian và lương của quản lý đó được phân bổ trên toàn đội.

**HR và hành chính.** Bảng lương, tuân thủ, tuyển dụng, đào tạo nhân viên mới, đánh giá hiệu suất, giải quyết xung đột, thôi việc. Hoặc bạn làm điều đó (và thời gian của bạn có chi phí) hoặc bạn thuê HR, nghĩa là nhiều nhân viên hơn.

**Đào tạo.** Nhân viên mới mất 3–6 tháng để đạt năng suất đầy đủ. Trong quá trình làm quen, bạn trả toàn bộ giá cho sản lượng một phần.

**Doanh chuyển.** Tỷ lệ doanh chuyển tự nguyện trung bình tại Mỹ khoảng 25% hàng năm. Khi ai đó ra đi, bạn mất kiến thức thể chế, dành nhiều tháng tuyển dụng và khởi động lại chu kỳ đào tạo. Chi phí ước tính: 50–200% lương hàng năm của vai trò.

Cộng lại. Một nhân viên 85.000 đô la thực sự tốn 120.000–170.000 đô la. Một đội ngũ năm người chạy 600.000–850.000 đô la mỗi năm trước khi bất kỳ ai giao hàng.

## Một Agent Tốn Bao Nhiêu

Chi phí AI agent đến từ ba nguồn.

**Cuộc gọi API.** Đây là chi phí chính. Mỗi khi agent sử dụng mô hình, để viết, phân tích, quyết định hoặc liên lạc, nó thực hiện một cuộc gọi API được tính theo số lượng token (đại khái, số lượng từ). Giá hiện tại cho các mô hình có khả năng:
- Công việc nhanh, đủ tốt (Claude Haiku-class): $0,25–$1,25 trên mỗi triệu token
- Công việc chất lượng cao (Claude Sonnet-class): $3–$15 trên mỗi triệu token
- Lý luận phức tạp cao cấp (Claude Opus-class): $15–$75 trên mỗi triệu token

Một triệu token là khoảng 750.000 từ, tương đương mười cuốn tiểu thuyết. Một nhiệm vụ kinh doanh điển hình (viết bài, phân tích dữ liệu, tóm tắt nghiên cứu) sử dụng 2.000–10.000 token. Đó là phần nhỏ của một cent đến vài cent mỗi nhiệm vụ ở các tầng thấp hơn.

**Tính toán và lưu trữ.** Paperclip chạy cục bộ với cơ sở dữ liệu Postgres nhúng. Trên máy của bạn, chi phí tăng thêm là không. Bạn sử dụng phần cứng bạn đã sở hữu. Để có sẵn sàng 24/7 trên máy chủ đám mây, ngân sách 20–100 đô la mỗi tháng.

**Công cụ bên thứ ba.** Nếu agent của bạn cần các API trả tiền (dịch vụ email, nhà cung cấp dữ liệu, nền tảng tiếp thị) những chi phí đó tồn tại. Nhưng bạn cũng sẽ trả chúng với nhân viên người.

**Chi phí hàng tháng thực tế theo khối lượng công việc:**
- Agent nhẹ (một vài nhiệm vụ mỗi ngày): $20–$50/tháng
- Agent vừa phải (công việc hàng ngày ổn định): $50–$200/tháng
- Agent nặng (công việc liên tục, phức tạp): $200–$500/tháng

## $427.000 vs. $6.600

Một so sánh cụ thể. Hãy xem một hoạt động tiếp thị nội dung nhỏ, loại mà hàng nghìn nhà sáng lập đang điều hành ngay bây giờ.

**Đội Ngũ Truyền Thống (5 nhân viên):**
| Vai trò | Lương | Chi phí đầy đủ |
|------|--------|-------------|
| Người viết nội dung #1 | $55.000 | $77.000 |
| Người viết nội dung #2 | $55.000 | $77.000 |
| Biên tập viên | $65.000 | $91.000 |
| Chuyên gia SEO | $60.000 | $84.000 |
| Quản lý dự án | $70.000 | $98.000 |
| **Tổng cộng** | **$305.000** | **$427.000/năm** |

**Công Ty AI Paperclip:**
| Vai trò Agent | Tầng Mô Hình | Chi phí hàng tháng |
|-----------|-----------|-------------|
| Writing Agent #1 | Sonnet-class | $150 |
| Writing Agent #2 | Sonnet-class | $150 |
| Editing Agent | Sonnet-class | $100 |
| SEO Agent | Haiku-class | $50 |
| Project Coordination Agent | Haiku-class | $50 |
| Hosting (VPS) | — | $50 |
| **Tổng cộng** | | **$550/tháng = $6.600/năm** |

$427.000 so với $6.600. **Giảm chi phí 98,5%.**

So sánh này không hoàn toàn tương đương. Đội ngũ người mang lại phán đoán, mối quan hệ và bản năng sáng tạo mà AI agent hiện tại không thể tái tạo. Đội ngũ AI yêu cầu sự giám sát của bạn, và thời gian của bạn có giá trị. Một số nhiệm vụ sẽ luôn cần người viết.

Nhưng đối với phần lớn tiếp thị nội dung (bài blog, bài SEO, mạng xã hội, bản tin email) đội ngũ AI tạo ra sản lượng tương đương với một phần nhỏ chi phí. Khoảng cách chất lượng thu hẹp mỗi quý.

Câu hỏi không phải là liệu AI có sánh ngang với con người trong mọi thứ không. Câu hỏi là liệu AI có xử lý đủ nhiệm vụ đủ tốt để biện minh cho sự chuyển đổi không. Đối với ngày càng nhiều chức năng kinh doanh, câu trả lời là có.

## 8.760 Giờ Mỗi Năm

Một chiều kích chi phí không bao giờ xuất hiện trong các so sánh lương: thời gian.

Một nhân viên người làm việc khoảng 2.000 giờ mỗi năm. Trừ đi các cuộc họp, email, bữa trưa và chuyển đổi ngữ cảnh. Các nghiên cứu năng suất cho thấy hầu hết công nhân tri thức tạo ra 3–4 giờ sản lượng thực sự mỗi ngày, và bạn nhận được 750–1.000 giờ năng suất mỗi năm.

Một Paperclip agent với lập lịch heartbeat làm việc 24 giờ mỗi ngày, 365 ngày mỗi năm: 8.760 giờ. Ở mức sử dụng 80% thận trọng (tính đến hàng đợi nhiệm vụ, thời gian xử lý và thời gian nhàn rỗi), đó là khoảng 7.000 giờ năng suất.

Một AI agent tạo ra gấp 7–9 lần giờ năng suất so với một nhân viên người. Bạn có thể chạy nhiều agent cùng một lúc.

Đây không phải là về việc AI "tốt hơn" con người. Đó là sự bất đối xứng về thời gian có sẵn. Khi nhân viên của đối thủ cạnh tranh của bạn về nhà lúc 5 giờ chiều, công ty AI của bạn tiếp tục chạy. Cuối tuần, ngày lễ, ngày bệnh. Agent của bạn không dừng lại.

Theo năm tháng, điều đó kết hợp thành một khoảng cách vận hành rất lớn.

## Chi Phí Cận Biên Bằng Phẳng

Các công ty truyền thống phải đối mặt với một sự thật khó: mở rộng quy mô đòi hỏi nhiều người hơn, nghĩa là nhiều chi phí hơn, quản lý nhiều hơn, phức tạp hơn, và thường kém hiệu quả hơn. Từ 5 nhân viên lên 50 không tốn gấp 10 lần. Nó tốn gấp 12–15 lần. Bạn cần quản lý cấp trung, HR, văn phòng lớn hơn và chi phí giao tiếp tăng theo cấp số nhân với quy mô đội ngũ.

Các công ty AI mở rộng theo hướng ngược lại. Thêm một agent vào sơ đồ tổ chức Paperclip của bạn tốn 50–500 đô la mỗi tháng, tương tự dù bạn có 3 agent hay 30. Không có chi phí quản lý. Không có phúc lợi. Không có thời gian làm quen. Không có mở rộng văn phòng. Chi phí cận biên của tăng trưởng gần như bằng phẳng.

Đây là lý do tại sao các startup AI-native yêu cầu ít vốn hơn 22% so với các startup truyền thống, theo dữ liệu ngành gần đây. Không chỉ rẻ hơn để bắt đầu, mà rẻ hơn đáng kể để phát triển.

Và đây là toán học đằng sau công ty tỷ đô một người của Altman. Một người không thực hiện công việc của một nghìn. Một người điều phối các AI agent có chi phí mở rộng tuyến tính trong khi sản lượng mở rộng theo cấp số nhân. Những tỷ suất lợi nhuận đó đẩy định giá lên tầng mây.

## Kiểm Soát Ngân Sách Trong Paperclip

Rẻ và có kiểm soát không phải là một. Nỗi sợ phổ biến nhất về AI agent không phải là chúng sẽ thất bại. Đó là chúng sẽ làm việc quá nhiều và tạo ra hóa đơn API khổng lồ.

Paperclip giải quyết điều này trực tiếp.

**Ngân sách hàng tháng cho mỗi agent.** Mỗi agent có giới hạn chi tiêu cứng. Không phải hướng dẫn, mà là giới hạn.

**Cảnh báo nhẹ ở 80%.** Khi một agent đạt 80% ngân sách của nó, bạn được thông báo. Thời gian để quyết định: tăng ngân sách, giảm khối lượng công việc, hoặc để nó đạt giới hạn và dừng lại.

**Dừng tự động ở 100%.** Khi một agent cạn kiệt ngân sách, nó dừng lại. Không có ngoại lệ. Không có bất ngờ. Không có chi phí vượt mức. Nó dừng lại cho đến khi chu kỳ hàng tháng reset hoặc bạn tăng phân bổ.

**Theo dõi chi phí chi tiết.** Chi tiêu theo agent, theo nhiệm vụ, theo dự án, trên toàn bộ công ty. Bạn có thể phát hiện vấn đề nhanh chóng. Có thể các agent viết của bạn hiệu quả về chi phí nhưng agent nghiên cứu của bạn đốt ngân sách vào độ sâu không cần thiết.

Điều này cho bạn khả năng hiển thị tài chính tốt hơn so với hầu hết các công ty có được về lực lượng lao động người của họ. Hỏi bất kỳ quản lý nào nhân viên cụ thể tốn bao nhiêu để tạo ra một sản phẩm cụ thể, và bạn sẽ nhận được cái nhìn trống rỗng. Paperclip cho bạn biết chính xác, đến từng xu.

## Nơi Con Người Vẫn Chiến Thắng

AI không thay thế con người trong mọi chức năng. Chưa đến lúc đó, và có thể không bao giờ trong một số lĩnh vực.

**Các mối quan hệ quan trọng.** Chốt một thỏa thuận 500.000 đô la, quản lý một mối quan hệ đối tác chính, xử lý một cuộc khủng hoảng khách hàng. Những điều này đòi hỏi trí tuệ cảm xúc, sự đồng cảm và phán đoán dưới áp lực mà AI không cung cấp một cách đáng tin cậy.

**Công việc sáng tạo ban đầu.** AI tạo ra nội dung mạnh mẽ trong các mẫu đã được thiết lập. Nó gặp khó khăn với tầm nhìn thực sự gốc, loại định nghĩa một thương hiệu, tung ra một khoảnh khắc văn hóa, hoặc tạo ra điều gì đó thị trường chưa từng thấy.

**Phán đoán chiến lược.** AI có thể phân tích dữ liệu và trình bày các lựa chọn. Nó không thể cảm nhận thị trường, đọc giữa các dòng của một bước đi của đối thủ, hay đưa ra những quyết định trực giác mà các nhà sáng lập kinh nghiệm đưa ra từ nhiều năm nhận dạng mẫu.

**Điều hướng đạo đức.** Khi quyết định đúng đắn mơ hồ, khi các giá trị mâu thuẫn, các bên liên quan không đồng ý, hoặc câu trả lời pháp lý và câu trả lời đạo đức phân kỳ, bạn muốn con người đưa ra quyết định đó.

Cách tiếp cận thông minh nhất cho nhiều nhà sáng lập: AI agent xử lý 80–90% công việc có hệ thống, có thể lặp lại và có thể mở rộng. Bạn dành năng lượng của mình vào 10–20% nơi con người không thể thay thế.

Ngay cả trong một công ty "không có nhân viên," một nhân viên quan trọng rất nhiều: bạn. Kinh tế học của không không phải là về việc loại bỏ phán đoán của con người. Chúng là về việc làm cho nó có giá trị hơn bằng cách giải phóng nó khỏi mọi thứ không yêu cầu nó.

## Ước Tính Chi Phí Của Bạn

Trước Phần III, nơi bạn xây dựng công ty của mình, một framework nhanh:

1. Liệt kê các vai trò bạn sẽ thuê cho một đội ngũ truyền thống
2. Ước tính chi phí đầy đủ (lương x 1,4 tối thiểu)
3. Xác định vai trò nào AI agent có thể xử lý (hầu hết các vai trò vận hành, phân tích và nội dung đều đủ tiêu chuẩn)
4. Ước tính chi phí agent: nhẹ ($30/tháng), vừa phải ($150/tháng), nặng ($350/tháng)
5. Thêm lưu trữ ($50/tháng) và chi phí API bên thứ ba
6. So sánh tổng số

Đối với hầu hết các hoạt động kinh doanh nhỏ, tiết kiệm đạt 90–98%. Ngay cả các ước tính thận trọng cho thấy giảm 80%+.

Kinh tế học rõ ràng. Công cụ miễn phí. Hãy xây dựng.
