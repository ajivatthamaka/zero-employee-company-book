# Chương 5: Paperclip

> "Đầu tiên chúng ta định hình công cụ của mình, sau đó công cụ của chúng ta định hình chúng ta."
> — John Culkin

Hàng nghìn công cụ AI tồn tại. Hàng trăm framework agent. Hàng chục nền tảng quy trình làm việc. Paperclip không phải là bất kỳ trong số chúng.

Paperclip cho phép bạn thuê các AI agent, gán cho họ chức danh công việc, đặt họ trong một sơ đồ tổ chức, giao nhiệm vụ với các luồng hội thoại, đặt ngân sách hàng tháng với giới hạn chi tiêu cứng, yêu cầu phê duyệt của con người cho các quyết định lớn, và ghi lại mọi hành động trong hồ sơ kiểm tra vĩnh viễn.

Nó không giúp bạn sử dụng AI. Nó giúp bạn *vận hành* AI. Như một công ty. Vì đó là những gì bạn đang xây dựng.

Nếu dự đoán của Sam Altman về các công ty tỷ đô một người sẽ tồn tại, và toán học từ các chương trước nói điều đó sẽ xảy ra, chúng sẽ chạy trên thứ gì đó như Paperclip. Không phải chatbot. Không phải quy trình làm việc. Một hệ điều hành cho một công ty AI.

## Không Phải Chatbot, Không Phải Framework, Không Phải Quy Trình Làm Việc

Trước những gì nó làm, những gì nó không làm. Điều này quan trọng vì hầu hết mọi người sẽ xếp Paperclip vào một hộp với các công cụ họ đã biết. Mọi hộp đều sai.

**Nó không phải là chatbot.** Bạn không nói chuyện với nó. Không có giao diện cuộc trò chuyện nơi bạn đặt câu hỏi và nhận câu trả lời. Nó điều phối; nó không trò chuyện.

**Nó không phải là agent framework.** Các framework như LangChain, CrewAI, hoặc AutoGen giúp bạn *xây dựng* agent. Paperclip không xây dựng agent. Nó quản lý chúng, bất kể chúng được xây dựng như thế nào. Nó hoạt động với Claude Code, Cursor, các custom HTTP agent, bash script, hoặc bất cứ thứ gì khác có thể nhận hướng dẫn và trả về kết quả.

**Nó không phải là công cụ xây dựng quy trình làm việc.** Các công cụ như Zapier, Make, hoặc n8n chuỗi các bước được xác định trước: "khi điều này xảy ra, làm điều đó." Paperclip không chuỗi các bước. Nó mô hình hóa các tổ chức, với hệ thống phân cấp, ủy quyền, và các quyết định chảy lên và xuống một cấu trúc. Sự khác biệt giữa công thức nấu ăn và một nhà hàng.

**Nó không phải là trình quản lý prompt.** Nó không lưu trữ hoặc tinh chỉnh prompt. Nó quản lý *agent*, các thực thể bền vững với vai trò, ngân sách, quyền hạn và lịch sử.

Ngừng so sánh nó với thứ gì đó khác và Paperclip trở nên rõ ràng: cơ sở hạ tầng tổ chức để vận hành các AI agent như nhân viên. Không hơn, không kém.

## Tổ Chức Agent Như Một Công Ty

Paperclip dựa trên một nhận thức: nếu bạn muốn AI agent thực hiện công việc của một công ty, hãy tổ chức chúng như một công ty.

**Sơ đồ tổ chức.** Mỗi agent giữ một vị trí xác định. Vai trò, đường báo cáo, cấp độ. Một người viết nội dung báo cáo cho giám đốc biên tập, người báo cáo cho trưởng tiếp thị. Điều này quyết định cách nhiệm vụ được ủy quyền, cách quyết định leo thang, và ai có thẩm quyền về gì.

**Phân cấp mục tiêu.** Mục tiêu công ty chảy xuống qua hệ thống phân cấp. Nếu mục tiêu là "xuất bản 20 bài viết tháng này," trưởng tiếp thị chia thành các bài tập biên tập, giám đốc biên tập chuyển chúng cho người viết, và tiến độ cuộn lại. Sự đồng thuận từ sứ mệnh đến thực thi.

**Nhiều công ty.** Bạn có thể chạy nhiều công ty từ một phiên bản Paperclip, mỗi công ty với dữ liệu riêng biệt. Một công ty nội dung, một hoạt động thương mại điện tử, và một công ty tư vấn, mỗi công ty với agent, ngân sách và quản trị riêng.

Điều này có vẻ hiển nhiên. Nhưng hầu hết các công cụ AI khác không nghĩ theo cách này. Hầu hết được xây dựng xung quanh các nhiệm vụ, prompt, hoặc quy trình làm việc, không phải các tổ chức. Cược của Paperclip là cấu trúc tổ chức *là* sản phẩm. Nó biến một tập hợp AI agent thành một doanh nghiệp hoạt động.

## Heartbeat, Ngân Sách và Công Tắc Khẩn Cấp

### Công Việc Có Lịch Mà Không Cần Bạn

Các agent trong Paperclip hoạt động theo các lịch gọi là heartbeat, các khoảng thời gian tự động đánh thức chúng. Người viết nội dung của bạn kiểm tra lịch biên tập hàng ngày. Agent SEO của bạn tinh chỉnh nội dung đã xuất bản hàng tuần. Agent nghiên cứu của bạn tạo ra các phân tích cạnh tranh hàng tháng.

Đây là điều làm cho thực tế "kiểm tra dashboard trong khi uống cà phê" có thể. Công việc xảy ra theo lịch, không phải theo lệnh.

### Mọi Nhiệm Vụ, Mọi Bước, Đều Được Ghi Lại

Mọi phần công việc đều là một nhiệm vụ với một luồng hội thoại đầy đủ đính kèm. Khi một agent làm việc trên một nhiệm vụ, chuỗi lý luận, hành động và quyết định của nó được ghi lại. Nếu một agent ủy quyền cho agent khác, luồng tiếp tục. Nếu bạn can thiệp, bạn thấy những gì đã xảy ra, theo thứ tự nào, và tại sao.

Trong một công ty truyền thống, bạn thường không thể biết nhân viên đã đạt đến một kết quả như thế nào. Trong Paperclip, mọi bước được ghi lại theo mặc định.

### Giới Hạn Cứng Về Chi Tiêu

Điều này phân biệt Paperclip với mọi thứ khác. Mỗi agent có ngân sách hàng tháng, một giới hạn cứng về các cuộc gọi API và tính toán. Ở 80%, có cảnh báo. Ở 100%, agent dừng lại. Không có ngoại lệ, không có vượt chi.

Bạn theo dõi chi phí trên các agent, nhiệm vụ, dự án và toàn bộ công ty. Bạn biết mỗi đô la đi đâu. Hãy thử có được sự minh bạch đó với nhân viên người.

### Cổng Cho Phán Đoán Của Con Người

Không phải mọi thứ đều nên chạy tự động. Paperclip xử lý điều này thông qua các cổng phê duyệt, các điểm kiểm tra nơi một số hành động nhất định yêu cầu chữ ký của bạn trước khi tiến hành.

Phê duyệt mọi email hướng tới khách hàng? Đặt cổng. Xem xét nội dung trước khi xuất bản? Cổng nó. Kiểm soát khi nào agent mới được thuê hoặc chiến lược thay đổi? Phê duyệt cấp hội đồng quản trị.

Đây là quản trị, không phải quan liêu. Bạn quyết định những gì bị kiểm soát và những gì chạy tự do. Hệ thống thực thi nó.

### Hồ Sơ Kiểm Tra Vĩnh Viễn

Mọi quyết định, mọi cuộc gọi công cụ, mọi nhiệm vụ đã hoàn thành. Được ghi lại và bất biến. Bạn không thể chỉnh sửa nhật ký. Các agent không thể chỉnh sửa nhật ký. Những gì đã xảy ra vẫn còn trên hồ sơ.

Điều này cho bạn điều mà hầu hết các công ty với nhân viên người thiếu: trách nhiệm hoàn hảo. Kết quả xấu? Theo dõi những gì đã sai, ở bước nào, với đầu vào nào. Kết quả tốt? Xem những gì đã hoạt động và tái tạo nó.

### Ghi Đè Hoàn Toàn, Bất Cứ Lúc Nào

Đôi khi bạn cần rút phích cắm. Paperclip cho phép bạn chấm dứt bất kỳ agent nào, ghi đè bất kỳ nhiệm vụ nào, can thiệp tại bất kỳ thời điểm nào. Agent của bạn làm việc một mình, nhưng bạn giữ công tắc khẩn cấp.

Điều này quan trọng trong đầu bạn cũng như trong thực tế. Biết rằng bạn có toàn quyền kiểm soát giúp dễ dàng hơn để để agent hoạt động. Bạn không đang giao chìa khóa. Bạn đang ủy quyền với sự giám sát.

## Mang Bất Kỳ Runtime Nào Bạn Muốn

Một trong những quyết định mạnh mẽ nhất của Paperclip: nó không quan tâm agent của bạn được xây dựng như thế nào. Nó quản lý lớp tổ chức (vai trò, nhiệm vụ, ngân sách, quản trị) và để trí thông minh cho bất kỳ runtime nào bạn thích.

- Claude Code cho phát triển
- Custom HTTP agent cho các chức năng chuyên biệt
- Bash script cho tự động hóa thường xuyên
- Kết hợp và phối hợp trên toàn bộ sơ đồ tổ chức

Khi các mô hình và runtime cải thiện, và chúng sẽ, công ty Paperclip của bạn cải thiện cùng với chúng. Bạn không bị khóa vào một nhà cung cấp. Bạn đang xây dựng một cấu trúc tổ chức có thể kết nối với trí thông minh tốt nhất có sẵn bất kỳ lúc nào.

Bối cảnh AI sẽ trông khác trong hai năm. Vai trò, hệ thống phân cấp, ngân sách, quản trị: đây là các khái niệm quản lý, không phải cược công nghệ. Chúng sẽ không thay đổi.

## Miễn Phí, Mã Nguồn Mở, Một Lệnh

Paperclip được cấp phép MIT và mã nguồn mở. Bạn có thể đọc mọi dòng mã. Không có tài khoản, không có đăng ký, không có phí sử dụng. Nó chạy trên máy của bạn với cơ sở dữ liệu Postgres nhúng.

Cài đặt:

```
npx paperclipai onboard --yes
```

Từ không có gì đến chạy cơ sở hạ tầng công ty AI trong vài phút. Chúng ta sẽ làm cùng nhau trong Chương 7.

Miễn phí và mã nguồn mở quan trọng hơn chi phí. Không bị khóa vào nhà cung cấp, không có thay đổi giá bất ngờ, không có sự phụ thuộc vào một công ty có thể thay đổi hướng đi hoặc sụp đổ. Cơ sở hạ tầng của bạn thuộc về bạn.

## Cliphub: Mẫu Công Ty Như Sản Phẩm

Paperclip đã công bố Cliphub, một marketplace cho các mẫu công ty được xây dựng sẵn, hiện đang được phát triển. Thay vì thiết kế công ty AI của bạn từ đầu, bạn tải xuống một mẫu (công ty nội dung, hoạt động thương mại điện tử, công ty tư vấn) với agent, vai trò, ngân sách và quy trình làm việc đã được cấu hình.

Duyệt nó theo cách bạn duyệt App Store, nhưng thay vì tải xuống ứng dụng, bạn tải xuống cấu trúc công ty. "Công ty nội dung với 5 agent, cài đặt và tùy chỉnh." "Đội vận hành thương mại điện tử, cắm vào sản phẩm của bạn và bắt đầu." "Bộ phận hỗ trợ khách hàng, xử lý vé trong 24 giờ."

Cliphub chưa hoạt động. Nhưng tầm nhìn quan trọng: bắt đầu một công ty AI dễ như cài đặt một mẫu. Nếu bạn muốn là một trong những người *tạo ra* những mẫu đó, và bán chúng, cửa sổ đang mở ngay bây giờ.

## Những Khoảnh Khắc Nền Tảng

Mỗi sự chuyển dịch kinh tế lớn đều có nền tảng của nó. Cách mạng công nghiệp có nhà máy. Kỷ nguyên máy tính có văn phòng. Internet có trình duyệt. Di động có app store.

Kỷ nguyên AI có gì?

Không nhất thiết là Paperclip theo tên, mặc dù nó là ứng cử viên mạnh nhất ngày nay, mà là khái niệm mà nó đại diện: một cách có cấu trúc để tổ chức, quản lý và quản trị các AI agent như một công ty. Ai đó sẽ xây dựng cơ sở hạ tầng tiêu chuẩn cho các doanh nghiệp AI-native. Các nhà sáng lập đang xây dựng trên cơ sở hạ tầng đó bây giờ nắm giữ tương đương với việc đã xây dựng trên internet năm 1996 hoặc App Store năm 2008.
