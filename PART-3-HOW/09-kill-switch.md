# Chương 9: Công Tắc Khẩn Cấp

> "Tin tưởng, nhưng hãy xác minh."
> — Ronald Reagan

Câu hỏi đầu tiên mọi người hỏi về các công ty AI: "Điều gì sẽ xảy ra nếu có sự cố?"

Câu hỏi tốt. Nếu bạn giao hoạt động cho các AI agent, ngay cả với sự giám sát, hệ thống cần các kiểm soát cứng. Không phải hướng dẫn. Không phải chính sách. Các giới hạn cơ học ngăn chặn kết quả xấu bất kể agent nào làm gì.

Đây là nơi công ty không có nhân viên ngừng là sự mới lạ và trở thành một doanh nghiệp. Đồ chơi có tính năng. Công ty có quản trị.

## Ba Lớp Kiểm Soát Ngân Sách

Chúng ta đã đề cập đến kinh tế học trong Chương 6. Bây giờ là các kiểm soát.

Paperclip thực thi chi tiêu qua ba cấp độ:

### Giới Hạn Hàng Tháng Cho Mỗi Agent

Mỗi agent có giới hạn chi tiêu hàng tháng: số tiền tối đa nó có thể chi cho các cuộc gọi API, tính toán và sử dụng công cụ. Bạn đặt giới hạn này khi tạo và điều chỉnh bất kỳ lúc nào.

Đây không phải là gợi ý. Hệ thống thực thi nó.

Phù hợp ngân sách với vai trò. Một người viết nội dung tạo ra các bài hàng ngày có thể cần $150-$200/tháng. Một analytics agent chạy báo cáo hàng tuần, $30-$50. Một research agent thực hiện các nghiên cứu sâu, $200-$400.

Khi có nghi ngờ, đặt thấp hơn. Tăng ngân sách mất vài giây. Hoàn tác công việc từ một agent chi tiêu quá mức thì không.

### Cảnh Báo Nhẹ Ở 80%

Khi một agent đạt 80% ngân sách của nó, Paperclip thông báo cho bạn. Điều này cho bạn thời gian để quyết định:

- **Tăng ngân sách** nếu agent đang làm công việc có giá trị
- **Giảm khối lượng công việc** bằng cách hoãn các nhiệm vụ không quan trọng
- **Điều tra** liệu agent có đang chi tiêu tốt hay đang đốt tiền vào sự phức tạp không cần thiết
- **Không làm gì** và để nó chạy đến giới hạn cứng

Cảnh báo 80% là đèn kiểm tra động cơ của bạn. Nó không có nghĩa là có gì đó sai. Nó có nghĩa là hãy chú ý.

### Dừng Hoàn Toàn Ở 100%

Khi một agent cạn kiệt ngân sách, nó dừng lại. Không có nhiệm vụ mới, không có công việc đang chờ, không có cuộc gọi API, cho đến khi chu kỳ hàng tháng reset hoặc bạn tăng phân bổ.

Điều này loại bỏ các chi phí vượt mức. Bất kể có bao nhiêu nhiệm vụ đang xếp hàng, bất kể công việc khẩn cấp đến mức nào, agent không thể vượt quá ngân sách của nó. Hệ thống thực thi điều này về mặt cơ học, không phải thông qua sự tin tưởng.

Bất kỳ ai đã nhận được một hóa đơn AWS bất ngờ sẽ đánh giá cao thiết kế này.

### Theo Dõi Chi Phí Theo Nhiệm Vụ, Dự Án, Agent và Tháng

Ngoài ngân sách cho mỗi agent, Paperclip theo dõi chi phí theo nhiệm vụ, dự án, agent, công ty và kỳ thời gian, tuần qua tuần và tháng qua tháng.

Tính chi tiết này cho phép bạn cải thiện. Có thể research agent của bạn chi $100 cho mỗi phân tích cạnh tranh khi một cách tiếp cận đơn giản hơn sẽ tốn $20 và tạo ra 90% giá trị. Có thể một agent hiệu quả hơn nhiều về chi phí so với một agent khác làm công việc tương tự. Có thể các nhiệm vụ ngày Thứ Ba tốn nhiều hơn các nhiệm vụ ngày Thứ Sáu vì cách bạn viết tóm tắt.

Bạn không thể cải thiện những gì bạn không thể đo lường.

## Các Cổng Phê Duyệt

Không phải mọi thứ đều nên chạy tự động. Một số quyết định quá quan trọng, quá tinh tế hoặc quá rủi ro để ủy quyền hoàn toàn. Các cổng phê duyệt cho phép bạn giữ quyền kiểm soát của con người ở nơi quan trọng.

Cổng phê duyệt là điểm kiểm tra nơi agent dừng lại và chờ phê duyệt của bạn trước khi tiếp tục. Bạn quyết định những gì bị kiểm soát.

### Kiểm Soát Những Điều Này

**Liên lạc bên ngoài.** Email, bài đăng mạng xã hội, phản hồi khách hàng. Cho đến khi bạn tin tưởng agent trong cuộc trò chuyện, hãy kiểm soát mọi thứ hướng ra ngoài.

**Xuất bản.** Bài blog, danh sách sản phẩm, bản sao tiếp thị. Xem xét trước khi nó được công khai.

**Quyết định tài chính.** Thay đổi giá, khuyến nghị mua hàng, hoàn tiền trên ngưỡng.

**Thay đổi cơ cấu.** Thuê agent mới, thay đổi sơ đồ tổ chức, sửa đổi quy tắc quản trị. Luôn yêu cầu chữ ký của bạn.

**Thực thi chiến lược.** Khi một agent cấp cao phát triển kế hoạch, hãy xem xét nó trước khi các agent cấp dưới thực hiện.

### Để Những Điều Này Chạy

**Xử lý nội bộ.** Nghiên cứu, phân tích, soạn thảo, tổ chức dữ liệu. Công việc ở trong hệ thống của bạn và không chạm vào bất cứ điều gì bên ngoài.

**Hoạt động thường xuyên.** Các nhiệm vụ tuân theo các mẫu đã được thiết lập với kết quả có thể dự đoán. Khi bạn đã xác minh một agent xử lý tốt một nhiệm vụ định kỳ, hãy để nó chạy.

**Nhiệm vụ ít rủi ro.** Công việc mà kết quả xấu nhất là "Tôi cần làm lại," không phải "Tôi đã làm hỏng mối quan hệ khách hàng."

### Nới Lỏng Theo Thời Gian

Bắt đầu bằng cách kiểm soát tích cực. Xem xét mọi thứ. Học những gì agent của bạn tạo ra. Xây dựng niềm tin từng bước.

Khi niềm tin tăng lên, nới lỏng các cổng. Để nội dung thường xuyên xuất bản mà không cần xem xét. Để dịch vụ khách hàng xử lý các yêu cầu tiêu chuẩn một mình. Giữ các cổng về những gì có rủi ro thực sự.

Mục tiêu là cân bằng. Quá nhiều cổng và bạn làm tắc nghẽn công ty của chính mình. Quá ít và bạn tin tưởng AI với các quyết định nó không nên đưa ra một mình.

## Hồ Sơ Kiểm Tra

Mọi hành động trong Paperclip đều được ghi lại. Mọi cuộc gọi công cụ, mọi điểm quyết định, mọi kết quả, mọi giao nhiệm vụ, mọi ủy quyền, trong một hồ sơ bất biến.

Điều này cho bạn điều mà hầu hết các công ty với nhân viên người không bao giờ đạt được: trách nhiệm hoàn chỉnh.

**Chuỗi quyết định.** Khi một agent tạo ra kết quả, hãy theo dõi ngược lại qua mọi bước. Nó đã truy cập thông tin gì? Nó đã áp dụng lý luận gì? Nó đã xem xét các lựa chọn thay thế nào?

**Mẫu hiệu suất.** Theo thời gian, nhật ký tiết lộ agent nào hiệu quả nhất, agent nào tạo ra công việc tốt nhất và agent nào cần điều chỉnh.

**Điều tra lỗi.** Khi có sự cố, và nó sẽ xảy ra, bạn có thể xác định chính xác điều gì đã xảy ra, ở đâu và tại sao. Không đoán mò.

**Bằng chứng tuân thủ.** Nếu bạn hoạt động trong một ngành được quản lý, nhật ký kiểm tra cung cấp hồ sơ tài liệu mà các cơ quan quản lý yêu cầu.

### Cách Sử Dụng Chúng

Đừng đọc mọi mục. Điều đó đánh bại mục đích của tự động hóa.

**Đánh giá hàng tuần.** Dành 30 phút quét nhật ký để tìm các mẫu: hành vi bất ngờ, ngoại lệ hiệu quả, lỗi chưa được phát hiện.

**Giám sát dựa trên ngoại lệ.** Đặt cảnh báo cho các sự kiện cụ thể: cảnh báo ngân sách, kích hoạt cổng phê duyệt, thất bại nhiệm vụ. Chỉ xem xét những điều này trừ khi bạn có lý do để tìm hiểu sâu hơn.

**Nghiên cứu sâu hàng tháng.** Chọn một agent hoặc một quy trình làm việc và theo dõi hồ sơ kiểm tra hoàn chỉnh của nó. Điều này giữ bạn kết nối với cách công ty của bạn hoạt động và thường tiết lộ các cải tiến.

## Dừng, Ghi Đè, Chấm Dứt

Bạn luôn có công tắc khẩn cấp.

Bất kỳ lúc nào, bạn có thể:

- **Dừng agent:** Ngừng nó nhận nhiệm vụ mới trong khi bạn điều tra hoặc điều chỉnh cấu hình của nó
- **Ghi đè nhiệm vụ:** Sửa đổi, chuyển hướng hoặc hủy công việc đang tiến hành
- **Chấm dứt agent:** Xóa nó khỏi sơ đồ tổ chức vĩnh viễn

Đây không phải là biện pháp khẩn cấp. Chúng là các công cụ quản lý bình thường. Bạn sẽ dừng dự án của một nhân viên người nếu ưu tiên thay đổi. Bạn sẽ chuyển hướng công việc nếu cách tiếp cận sai. Bạn sẽ để ai đó ra đi nếu vai trò không hoạt động.

Sự khác biệt: với AI agent, những hành động này là tức thì và rõ ràng. Không có cuộc trò chuyện khó xử, không có trợ cấp thôi việc, không có thời gian thông báo. Quyết định, thực thi, tiếp tục.

## Phân Lập Dữ Liệu Giữa Các Công Ty

Nếu bạn chạy nhiều công ty trên một phiên bản Paperclip (một trong những mẫu mở rộng mạnh mẽ nhất, được thảo luận trong Chương 10), mỗi công ty hoạt động trong sự phân lập dữ liệu hoàn chỉnh.

- Agent trong Công ty A không thể truy cập dữ liệu của Công ty B
- Ngân sách được theo dõi độc lập theo từng công ty
- Nhật ký kiểm tra được tách biệt
- Sơ đồ tổ chức là riêng biệt

Đây không phải là tính năng tiện lợi. Đây là một sự cần thiết pháp lý và đạo đức khi các công ty của bạn xử lý các khách hàng, ngành hoặc mức độ nhạy cảm khác nhau. Sự phân lập là về mặt kiến trúc, không dựa trên quyền. Nó giữ ngay cả khi agent hành xử không mong đợi.

## Ba Mẫu Quản Trị

### Tuần 1-4: Khóa Chặt

- Kiểm soát tất cả liên lạc bên ngoài
- Kiểm soát tất cả xuất bản
- Xem xét tất cả kết quả agent bằng tay
- Đặt ngân sách thận trọng (50% những gì bạn mong đợi cần)
- Đánh giá nhật ký kiểm tra hàng ngày

### Tháng 2-6: Tin Tưởng Có Chọn Lọc

- Kiểm soát liên lạc bên ngoài và xuất bản cho các chủ đề hoặc khách hàng mới
- Để các quy trình đã được thiết lập chạy không có cổng
- Chỉ xem xét các mục được đánh dấu
- Đặt ngân sách từ dữ liệu sử dụng thực tế
- Đánh giá nhật ký kiểm tra hàng tuần

### Tháng 6+: Chỉ Ngoại Lệ

- Chỉ kiểm soát các quyết định quan trọng (chiến lược, khách hàng mới, thay đổi cơ cấu)
- Các hoạt động thường xuyên chạy tự động
- Chỉ đánh giá dựa trên ngoại lệ
- Ngân sách được tinh chỉnh thông qua phân tích dữ liệu
- Nghiên cứu sâu kiểm tra hàng tháng

Chuyển từ bị khóa chặt sang chỉ ngoại lệ dựa trên bằng chứng, không phải sự nhiệt tình. Tiến lên khi dữ liệu của bạn cho thấy agent tạo ra công việc chất lượng trong phạm vi ranh giới của họ, không phải trước đó.

## Những Gì Điều Này Làm Có Thể

Quản trị không làm chậm bạn. Nó tăng tốc bạn.

Không có nó, bạn nghi ngờ mọi hành động tự động. Bạn kiểm tra một cách ám ảnh. Bạn không thể ngủ mà không tự hỏi agent của bạn đang làm gì.

Với quản trị, bạn biết các ranh giới giữ, ngân sách không thể bị vượt quá, mọi hành động được ghi lại, và các cổng phê duyệt sẽ bắt những gì cần chú ý của bạn. Sự chắc chắn đó giải phóng bạn để tập trung vào chiến lược, tăng trưởng và các quyết định chỉ bạn mới có thể đưa ra.
