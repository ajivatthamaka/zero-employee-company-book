# Chương 8: Ai Làm Gì

> "Giám đốc điều hành tốt nhất là người đủ sáng suốt để chọn những người tốt để làm những gì họ muốn và đủ kiềm chế bản thân không can thiệp vào khi họ làm."
> — Theodore Roosevelt

Mọi công ty đều bắt đầu với cùng một câu hỏi: ai làm gì?

Các AI agent không thay đổi câu hỏi này. Chúng làm sắc nét nó. Nhân viên người có thể ứng biến, đặt câu hỏi, lấy tín hiệu trong hành lang. Agent thì không thể. Chúng cần các vai trò được đặt tên, ranh giới cứng và các mối quan hệ được trình bày rõ ràng. Không có cấu trúc đó, bạn có sự hỗn loạn tốn kém, không phải một công ty.

Nếu bạn muốn một doanh nghiệp chạy trong khi bạn ngủ, hãy suy nghĩ như một CEO. Công việc đầu tiên của CEO là quyết định ai làm gì.

## Vai Trò, Không Phải Công Cụ

Hầu hết mọi người mua AI theo cách họ mua thiết bị: "Tôi cần một công cụ để viết bài blog." "Tôi cần một công cụ để phân tích dữ liệu." "Tôi cần một công cụ để trả lời email khách hàng." Họ mua chức năng.

Một CEO thuê vai trò. "Tôi cần một người viết nội dung." "Tôi cần một chuyên gia phân tích dữ liệu." "Tôi cần một đại diện hỗ trợ." Sự khác biệt không phải là ngữ nghĩa. Công cụ nằm trong ngăn kéo. Vai trò nằm trong một tổ chức, với trách nhiệm, thẩm quyền và ai đó để chịu trách nhiệm.

Trong Paperclip, mỗi agent lấp đầy một vai trò: chức danh, nhiệm vụ, vị trí trong hệ thống phân cấp, mối quan hệ với các agent khác. Bạn không cài đặt phần mềm. Bạn tuyển dụng cho một vị trí.

Kiểm tra nó theo cách này: nếu bạn thuê người cho công việc, bài tuyển dụng sẽ nói gì? Viết bài đó. Bạn bây giờ có một định nghĩa vai trò.

## Bốn Sơ Đồ Tổ Chức

Bốn cấu trúc cho công ty không có nhân viên. Đây là những giả thuyết. Hãy điều chỉnh chúng.

### Nhà Xuất Bản Nội Dung

Điểm khởi đầu phổ biến nhất, vì nội dung là nơi AI agent làm tốt nhất ngày nay.

```
Bạn (Nhà sáng lập/CEO)
├── Editorial Director Agent
│   ├── Writer Agent #1 (bài dài)
│   ├── Writer Agent #2 (ngắn/mạng xã hội)
│   └── SEO Agent
├── Publishing Agent (lên lịch, đăng bài)
└── Analytics Agent (theo dõi lưu lượng, tương tác)
```

**Cách hoạt động:** Bạn đặt chiến lược biên tập: chủ đề, giọng điệu, đối tượng, mục tiêu. Editorial Director biến điều đó thành các bài tập. Các Writer thực hiện. SEO Agent tối ưu hóa trước khi xuất bản. Publishing Agent lên lịch và phân phối. Analytics báo cáo hiệu suất.

**Bạn xử lý:** Chiến lược, giọng điệu, nội dung được đánh dấu, quan hệ khách hàng.

### Thương Mại Điện Tử

```
Bạn (Nhà sáng lập/CEO)
├── Product Research Agent
├── Copywriting Agent (danh sách, mô tả)
├── Customer Support Agent
├── Inventory/Pricing Agent
└── Marketing Agent (email, mạng xã hội)
```

**Cách hoạt động:** Product Research theo dõi xu hướng và đối thủ. Copywriting tạo ra và làm mới danh sách. Customer Support xử lý các yêu cầu, leo thang những yêu cầu khó cho bạn. Inventory theo dõi hàng tồn kho và đề xuất thay đổi giá. Marketing chạy email và các chiến dịch mạng xã hội.

**Bạn xử lý:** Lựa chọn sản phẩm, thỏa thuận nhà cung cấp, thương hiệu, khiếu nại leo thang.

### Hỗ Trợ SaaS

```
Bạn (Nhà sáng lập/Nhà phát triển)
├── QA Agent (kiểm tra, phát hiện lỗi)
├── Documentation Agent
├── Customer Support Agent (vé)
├── Marketing Agent (blog, mạng xã hội, email)
└── Analytics Agent (dữ liệu sử dụng, tín hiệu rời bỏ)
```

**Cách hoạt động:** Bạn xây dựng sản phẩm. QA kiểm tra nó. Documentation giữ các trang trợ giúp cập nhật. Customer Support trả lời vé và FAQ. Marketing viết và quảng bá. Analytics theo dõi hành vi người dùng và đánh dấu rủi ro rời bỏ.

**Bạn xử lý:** Mã, kiến trúc, tài khoản chính, chiến lược.

### Agency

```
Bạn (Nhà sáng lập/Giám đốc Tài khoản)
├── Project Manager Agent
│   ├── Specialist Agent #1 (khác nhau theo dịch vụ)
│   ├── Specialist Agent #2
│   └── Specialist Agent #3
├── Client Communication Agent (cập nhật trạng thái, báo cáo)
└── Business Development Agent (tiếp cận, đề xuất)
```

**Cách hoạt động:** Bạn lấy khách hàng và xác định phạm vi công việc. Project Manager chia thành các nhiệm vụ và giao cho các chuyên gia. Các chuyên gia thực thi. Client Communication gửi cập nhật và biên soạn báo cáo. Business Development tìm kiếm khách hàng mới.

**Bạn xử lý:** Mối quan hệ, xác định phạm vi, xem xét chất lượng, định hướng.

Đây là các mẫu, không phải quy định. Công ty của bạn sẽ có hình dạng riêng. Nguyên tắc vẫn giữ: đặt tên vai trò, giao nhiệm vụ, vẽ đường giới hạn.

## Những Gì Có Trong Định Nghĩa Vai Trò

Kết quả của agent phụ thuộc vào định nghĩa vai trò của nó. Bỏ qua ở đây và bạn trả giá sau.

**Chức danh.** Vai trò này được gọi là gì?

**Nhiệm vụ.** Agent này làm gì? Hãy cụ thể. "Xử lý nội dung" là mơ hồ. "Viết các bài blog 1.000–1.500 từ về các chủ đề được giao, tuân theo hướng dẫn phong cách công ty, được tối ưu hóa cho các từ khóa mục tiêu, được giao nộp bằng định dạng markdown." Điều đó, agent có thể thực hiện.

**Thẩm quyền.** Agent này có thể tự quyết định gì? Điều gì cần phê duyệt? Một người viết có thể tự do chọn các tiêu đề phụ nhưng cần chữ ký phê duyệt về chủ đề. Một agent hỗ trợ có thể xử lý hoàn tiền dưới $50 nhưng leo thang bất cứ điều gì trên đó.

**Ranh giới.** Agent này *không* được làm gì? Nêu rõ. "Không liên hệ trực tiếp với khách hàng." "Không thực hiện mua hàng."

**Tiêu chuẩn.** Công việc tốt trông như thế nào? Hãy cho ví dụ. "Bài viết phải chính xác, sử dụng giọng nói chủ động, bao gồm ít nhất ba tiêu đề phụ, và kết thúc bằng lời kêu gọi hành động."

**Báo cáo.** Agent này trả lời cho ai? Ai trả lời cho nó? Ai nó làm việc bên cạnh?

Mọi sự mơ hồ bạn giải quyết ở đây là một vấn đề quản lý bạn không bao giờ phải đối mặt.

## Cách Công Việc Chảy

Trong một sơ đồ tổ chức Paperclip, hệ thống phân cấp quản lý sự chuyển động của công việc.

**Xuống.** Mục tiêu công ty vào từ trên cùng. Một agent cấp cao chia thành các nhiệm vụ nhỏ hơn và ủy quyền. Điều này tiếp tục cho đến khi mỗi nhiệm vụ đủ cụ thể để một agent hoàn thành.

**Lên.** Kết quả leo lên. Mỗi cấp xem xét, tổng hợp hoặc hành động theo những gì nổi lên từ dưới lên.

**Ngang.** Các agent ở cùng cấp chuyển công việc cho nhau. Người viết trao bản thảo cho SEO Agent. SEO Agent trao bản sao được tối ưu hóa cho Publishing Agent. Bạn xác định các bàn giao này trong cấu trúc tổ chức.

**Phẳng hay nhiều lớp?** Phẳng có nghĩa là bạn chỉ đạo agent không có lớp trung gian. Nó hoạt động cho ba đến năm agent đang làm các công việc riêng biệt. Đơn giản, và bạn giữ tầm nhìn trực tiếp về mọi thứ. Nhiều lớp có nghĩa là bạn chỉ đạo các nhà quản lý người chỉ đạo công nhân. Nó phù hợp với sáu agent trở lên, các nhiệm vụ chồng chéo hoặc khối lượng công việc bạn không thể xem xét một mình. Các nhà quản lý lọc: họ kiểm tra kết quả công nhân để bạn chỉ thấy công việc hoàn thành hoặc các vấn đề được đánh dấu.

Bắt đầu phẳng. Thêm các lớp khi bạn dành nhiều thời gian xem xét kết quả hơn là suy nghĩ về định hướng.

## Dạy Kỹ Năng Mới Khi Chạy

Paperclip cho phép bạn tiêm các kỹ năng mới vào agent mà không cần xây dựng lại chúng. Trao cho người viết của bạn một hướng dẫn phong cách mới. Cung cấp cho SEO Agent các phương pháp từ khóa mới. Tóm tắt cho agent hỗ trợ về một đợt ra mắt sản phẩm. Agent hấp thụ tài liệu mới và giữ lại tài liệu cũ.

Hai hệ quả theo sau. Thứ nhất, agent cải thiện đều đặn. Khi bạn học những gì hoạt động, bạn cung cấp cho họ hướng dẫn sắc bén hơn. Thứ hai, bạn có thể xoay chuyển nhanh chóng. Đối thủ mới? Tải nghiên cứu cạnh tranh vào chuyên gia phân tích của bạn. Góc nội dung mới? Cập nhật Editorial Director. Sự thay đổi theo mùa? Tinh chỉnh lại agent của bạn mà không cần vẽ lại toàn bộ sơ đồ.

## Một Nhà Sáng Lập, Mười Vai Trò

Trong một công ty không có nhân viên, công việc của bạn thay đổi. Bạn không làm công việc. Bạn không giám sát nó theo nghĩa cũ. Bạn đang thiết kế tổ chức và đưa ra các quyết định mà agent không thể.

**Bạn làm:**
- Đặt chiến lược và mục tiêu
- Thiết kế và điều chỉnh sơ đồ tổ chức
- Xem xét kết quả được đánh dấu, không phải tất cả kết quả, chỉ những gì đòi hỏi phán đoán của bạn
- Đưa ra quyết định quan trọng về tiền, mối quan hệ và đạo đức
- Tiêm kỹ năng và điều chỉnh vai trò
- Theo dõi ngân sách và số liệu toàn công ty

**Bạn không làm:**
- Viết bản thảo đầu tiên
- Xử lý các nhiệm vụ thường xuyên
- Phối hợp agent hàng ngày (hệ thống phân cấp làm điều đó)
- Kiểm tra mọi sản phẩm giao nộp (nhật ký kiểm tra làm; bạn xem xét theo lịch của mình)

Đây là phương trình nhà sáng lập một người, đội ngũ mười người trong thực tế. Bạn làm việc ở cấp độ CEO trong khi agent xử lý việc thực thi. Mỗi giờ bạn dành cho chiến lược và cấu trúc nhân lên qua mỗi agent bên dưới bạn.

## Ba Agent Đầu Tiên

Bắt đầu với ba agent. Không hơn.

Chọn ba công việc sẽ tạo ra sự khác biệt lớn nhất ngay bây giờ. Xác định vai trò của họ một cách cẩn thận, giao công việc, học cách họ hành xử. Chạy chúng trong một hoặc hai tuần trước khi thêm cái thứ tư.

Sự cám dỗ là thiết kế một công ty mười lăm agent vào ngày đầu tiên. Hãy cưỡng lại nó. Mỗi agent là một vai trò cần xác định, một mối quan hệ cần quản lý, một ngân sách cần đặt. Xây dựng từ những gì bạn biết, không phải từ những gì bạn đoán.
