# Chương 7: Mở Terminal

> "Cách để bắt đầu là ngừng nói chuyện và bắt đầu làm."
> — Walt Disney

Đóng các tab khác của bạn. Mở terminal của bạn. Trong 30 phút bạn sẽ có công ty AI đầu tiên của mình đang chạy.

Không phải bản demo. Không phải thí nghiệm tư duy. Đang chạy, với agent, nhiệm vụ và dashboard bạn có thể xem theo thời gian thực.

## Những Gì Bạn Cần

Hai điều:

**Node.js (phiên bản 18 hoặc cao hơn).** Kiểm tra bằng cách gõ:

```
node --version
```

Nếu bạn thấy 18, 20, hoặc cao hơn, hãy tiếp tục. Nếu không, hãy cài đặt phiên bản LTS mới nhất từ nodejs.org. Hai phút.

**Một terminal.** Trên macOS: Terminal hoặc iTerm2. Trên Windows: PowerShell hoặc Windows Terminal. Trên Linux: bất cứ thứ gì bạn đã sử dụng. Nếu bạn có thể gõ một lệnh và nhấn Enter, bạn có mọi kỹ năng mà chương này yêu cầu.

Không Docker. Không tài khoản đám mây. Không API key. Không thẻ tín dụng.

## Bước 1: Cài Đặt Paperclip

```
npx paperclipai onboard --yes
```

Một lệnh. Nó tải xuống Paperclip, thiết lập cơ sở dữ liệu Postgres nhúng, tạo cấu trúc thư mục và khởi chạy nền tảng. Cờ `--yes` chấp nhận các mặc định, hoàn toàn đúng cho lần chạy đầu tiên.

Thiết lập mất một đến ba phút tùy thuộc vào kết nối của bạn. Khi hoàn tất, bạn thấy một URL cục bộ, thường là `http://localhost:3000`.

Mở nó. Đó là dashboard Paperclip của bạn, hệ điều hành cho công ty AI của bạn.

## Bước 2: Đặt Tên Công Ty Của Bạn

Dashboard nhắc bạn tạo một công ty. Ba trường quan trọng:

**Tên.** Chọn điều gì đó thực sự. "Acme Content" hoạt động, nhưng "Adams Media Group" hoạt động tốt hơn. Bạn sẽ coi trọng nó hơn khi nó mang tên mà bạn sẽ đặt trên danh thiếp.

**Mô tả.** Một hoặc hai câu. "Sản xuất nội dung blog được tối ưu hóa SEO cho ngành tài chính cá nhân" tốt hơn "kiểm tra đồ AI." Tính cụ thể định hình cách bạn thiết kế agent và giao công việc.

**Mục tiêu.** Công ty này tồn tại để làm gì? "Xuất bản 4 bài blog chất lượng cao mỗi tuần" hoặc "Xử lý và trả lời các yêu cầu của khách hàng trong vòng 2 giờ." Mục tiêu phân cấp xuống cho agent của bạn. Làm cho chúng cụ thể và có thể đo lường được.

Nhấp tạo. Công ty của bạn bây giờ có dashboard, bảng nhiệm vụ, bộ theo dõi ngân sách và sơ đồ tổ chức trống. Đến lúc thuê người.

## Bước 3: Thuê Một Agent

Điều hướng đến Agents và tạo một agent mới.

**Tên và vai trò.** Đặt cho nó một tên và chức danh. "Alex, Người Viết Nội Dung" hoặc "Morgan, Chuyên Gia Phân Tích Nghiên Cứu." Tên là trang trí. Mô tả vai trò quan trọng. Viết nó như một bài tuyển dụng: "Viết các bài blog 1.000-1.500 từ về chủ đề tài chính cá nhân. Tuân theo các thực hành SEO tốt nhất. Tạo ra văn xuôi rõ ràng, hấp dẫn cho đối tượng người lớn phổ thông."

**Runtime.** Điều này cho Paperclip biết loại agent cần xây dựng:
- Người dùng Claude: chọn runtime Claude Code
- API ưa thích: cấu hình một custom HTTP agent
- Tùy chọn đơn giản nhất: một bash script agent cho các nhiệm vụ tự động cơ bản

Bạn có thể thay đổi runtime sau. Chọn một cái và tiếp tục.

**Ngân sách.** Đặt giới hạn hàng tháng. $50 là đủ để thử nghiệm mà không lo lắng.

**Heartbeat.** Tần suất agent nên kiểm tra công việc? Người viết nội dung: hàng ngày. Dịch vụ khách hàng: hàng giờ. Trình tạo báo cáo hàng tuần: hàng tuần. Phù hợp nhịp độ với công việc.

Nhấp tạo. Nhân viên đầu tiên của bạn được thuê. Không có phỏng vấn. Không có thư mời. Không có hai tuần thông báo từ công việc trước.

## Bước 4: Giao Công Việc

Đến bảng nhiệm vụ. Tạo một nhiệm vụ. Giao nó cho agent của bạn.

Giữ cái đầu tiên đơn giản và cụ thể:

- **Công ty nội dung:** "Viết một bài blog 1.200 từ về 5 chiến lược lập ngân sách hàng đầu cho freelancer. Bao gồm phần giới thiệu, năm chiến lược được xác định rõ ràng với giải thích, và kết luận. Tối ưu hóa cho từ khóa 'mẹo lập ngân sách cho freelancer.'"

- **Công ty nghiên cứu:** "Biên soạn một phân tích cạnh tranh về 5 công cụ quản lý dự án hàng đầu cho các nhóm nhỏ. Đối với mỗi công cụ, bao gồm giá cả, tính năng chính, ưu điểm, nhược điểm và người dùng mục tiêu. Trình bày theo định dạng có cấu trúc."

- **Thương mại điện tử:** "Viết mô tả sản phẩm cho 10 mặt hàng sau [liệt kê các mặt hàng]. Mỗi mô tả phải là 100-150 từ, nêu bật các lợi ích chính và bao gồm lời kêu gọi hành động rõ ràng."

Chú ý tính cụ thể. Các AI agent, như nhân viên người, làm việc tốt hơn với các bản tóm tắt rõ ràng. "Viết điều gì đó về lập ngân sách" tạo ra nội dung lộn xộn. Bản tóm tắt ở trên tạo ra thứ gì đó bạn có thể xuất bản.

Gửi nhiệm vụ. Nếu heartbeat đến hạn, agent sẽ lấy nó. Nếu không, kích hoạt một lần chạy thủ công.

Xem luồng nhiệm vụ khi agent làm việc. Mọi bước trong chuỗi lý luận được ghi vào luồng hội thoại, sự minh bạch từ Chương 5, trong hành động.

## Bước 5: Đọc Luồng, Không Chỉ Kết Quả

Khi agent của bạn hoàn thành, hãy cưỡng lại sự thôi thúc bỏ qua thẳng đến sản phẩm giao nộp. Nghiên cứu luồng nhiệm vụ. Đó là nơi bạn học được.

**Trong luồng, tìm kiếm:**
- Cách agent hiểu bản tóm tắt của bạn
- Những bước nó đã thực hiện
- Những quyết định bạn không mong đợi
- Bao nhiêu ngân sách nhiệm vụ tiêu thụ

**Trong kết quả, hỏi:**
- Bạn có xuất bản điều này, gửi cho khách hàng hoặc hành động theo nó không?
- Nó còn thiếu ở đâu? "Không tốt" không cho bạn biết gì. Hãy cụ thể.
- Bạn sẽ thay đổi gì trong bản tóm tắt lần sau?

Nhiệm vụ đầu tiên này hiệu chỉnh kỳ vọng của bạn nhiều như nó tạo ra công việc. Bạn đang học những gì agent của bạn có thể làm, cách nó lý luận, và hướng dẫn nào mang lại kết quả tốt nhất. Mọi nhiệm vụ theo sau sẽ sắc bén hơn vì nó.

## Năm Phút Với Dashboard

Công ty, agent, nhiệm vụ hoàn thành. Bây giờ hãy khám phá.

**Tổng quan công ty.** Tên, mô tả, mục tiêu, các chỉ số cấp cao: số lượng agent, nhiệm vụ đang hoạt động, nhiệm vụ đã hoàn thành, tổng chi tiêu.

**Sơ đồ tổ chức.** Chỉ có một agent bây giờ. Hệ thống phân cấp, vai trò và đường báo cáo xuất hiện ở đây khi bạn phát triển.

**Bảng nhiệm vụ.** Tất cả các nhiệm vụ: đang chờ, đang tiến hành, đã hoàn thành, bị chặn. Mỗi nhiệm vụ có luồng hội thoại, agent được giao và trạng thái. Đây là trung tâm chỉ huy của bạn.

**Theo dõi ngân sách.** Chi tiêu theo agent, tổng hàng tháng, phần trăm sử dụng. Màu xanh lá cây có nghĩa là lành mạnh, màu vàng có nghĩa là đang tiếp cận giới hạn, màu đỏ có nghĩa là đã dừng lại.

**Nhật ký kiểm tra.** Hồ sơ bất biến của mọi thứ đã xảy ra. Mọi hành động agent, mọi quyết định, mọi cuộc gọi công cụ. Khi bạn cần biết tại sao điều gì đó xảy ra, hãy tìm ở đây.

## Những Khó Khăn Thường Gặp

**"Không tìm thấy lệnh" trên npx.** Node.js chưa được cài đặt hoặc không có trong PATH của bạn. Cài đặt lại từ nodejs.org và chọn hộp để thêm nó vào PATH hệ thống của bạn.

**Cổng đang được sử dụng.** Thứ gì đó khác chiếm cổng 3000. Dừng dịch vụ kia hoặc cấu hình một cổng khác.

**Agent bỏ qua nhiệm vụ mới.** Kiểm tra lịch heartbeat. Nếu bạn đặt nó là hàng ngày và vừa tạo nhiệm vụ, agent sẽ không chạy cho đến ngày mai. Kích hoạt một lần chạy thủ công.

**Kết quả yếu.** Hầu như luôn là vấn đề tóm tắt, không phải vấn đề agent. Làm cho mô tả cụ thể hơn. Bao gồm ví dụ về kết quả tốt. Đặt các ràng buộc rõ ràng về độ dài, định dạng và giọng điệu.

**Ngân sách cạn kiệt nhanh.** Kiểm tra tầng mô hình. Các mô hình Opus-class tốn nhiều hơn nhiều mỗi token so với Haiku-class. Đối với hầu hết các nhiệm vụ, Sonnet-class cho sự cân bằng tốt nhất giữa chất lượng và chi phí.

## Những Gì Đã Xảy Ra Trong 30 Phút

Bạn đã cài đặt một hệ điều hành công ty AI. Tạo ra một công ty với tên, mô tả và mục tiêu. Thuê một nhân viên AI với vai trò, ngân sách và lịch trình. Giao công việc, theo dõi thực thi và xem xét kết quả. Bạn có dashboard hiển thị hoạt động, tài chính và hồ sơ kiểm tra.

Hầu hết mọi người nghĩ điều này còn nhiều năm nữa. Bạn vừa làm nó trong khi uống cà phê.

Tối nay, agent này có thể tạo ra công việc theo lịch hàng ngày. Đến cuối tuần, ba hoặc bốn agent bao phủ các chức năng khác nhau. Đến cuối tháng, một công ty hoạt động đầy đủ tạo ra sản lượng thực sự.

Nhưng các agent rải rác chạy các nhiệm vụ không phải là một công ty. Chúng là một sandbox. Xây dựng điều gì đó thực sự có nghĩa là suy nghĩ như một CEO: xác định vai trò, thiết kế hệ thống phân cấp, tạo ra các luồng ủy quyền, xây dựng một tổ chức chạy mà không cần bạn.

Đó là chương tiếp theo.
