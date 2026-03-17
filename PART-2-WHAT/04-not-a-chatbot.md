# Chương 4: Không Phải Chatbot

> "Vấn đề thực sự không phải là liệu máy móc có suy nghĩ không mà là liệu con người có suy nghĩ không."
> — B.F. Skinner

ChatGPT không phải là nhân viên. Nó là một thực tập sinh thông minh quên tất cả mọi thứ mỗi khi bạn đóng tab.

Bạn giao cho nó một nhiệm vụ, nó cố gắng hết sức, rồi biến mất. Mở một cuộc trò chuyện mới và nó không biết bạn là ai, bạn đã hỏi gì trước đây, hay doanh nghiệp của bạn làm gì. Nó không thể tự mình sử dụng công cụ. Nó không thể lên lịch công việc tiếp theo. Nó không thể kiểm tra kết quả của mình so với các tiêu chuẩn của bạn. Nó làm những gì bạn hỏi, ngay bây giờ, và không làm gì khác.

Điều đó hữu ích. Nhưng nó không phải là một lực lượng lao động.

Để xây dựng công ty không có nhân viên, bạn cần các AI agent. Và nếu bạn sẽ điều phối chúng như một CEO, bạn cần hiểu chúng là gì, chúng hoạt động như thế nào, và chúng khác với chatbot mà bạn đã sử dụng để viết lại email như thế nào.

Chương này là nền tảng cho Phần III, nơi chúng ta xây dựng công ty của bạn. Nắm vững nó, và mọi thứ còn lại sẽ rõ ràng.

## Ba Tầng: Chatbot, Copilot, Agent

Thế giới AI có một vấn đề về thuật ngữ. Mọi thứ đều được gọi là "AI," từ một gợi ý tự động hoàn thành đơn giản đến một hệ thống có thể nghiên cứu, viết, xuất bản và phân tích kết quả. Đây không phải là những thứ giống nhau.

**Chatbot** có tính phản ứng. Bạn đặt câu hỏi. Chúng trả lời. Sự tương tác bắt đầu và kết thúc với đầu vào của bạn. ChatGPT, Claude, Gemini: trong các giao diện chat mặc định của chúng, đây là chatbot. Mạnh mẽ, nhưng chúng chờ đợi bạn. Không có đầu vào, không có đầu ra.

**Copilot** làm việc cùng bạn trong thời gian thực. GitHub Copilot gợi ý mã khi bạn gõ. Trợ lý viết cung cấp hoàn thành câu. Công cụ email thông minh soạn thảo câu trả lời. Copilot dự đoán nhu cầu của bạn, nhưng chúng vẫn hoạt động trong *phiên làm việc* của bạn. Bạn lái. Chúng gợi ý.

**Agent** tự hành động. Bạn cung cấp cho chúng một mục tiêu, và chúng tìm cách đạt được nó. Chúng chia các nhiệm vụ phức tạp thành các nhiệm vụ con. Chúng sử dụng công cụ: duyệt web, chạy mã, đọc tệp, gọi API. Chúng quyết định làm gì tiếp theo dựa trên những gì đã xảy ra ở bước trước. Chúng có thể làm việc mà không cần bạn có mặt.

Hãy nghĩ về GPS (chatbot, trả lời khi được hỏi), giáo viên lái xe (copilot, hướng dẫn bạn trong thời gian thực), và tài xế riêng (agent, bạn đặt tên điểm đến, họ lo phần còn lại).

Nếu bạn đang xây dựng công ty không có nhân viên, bạn cần tài xế riêng. Nhiều người trong số họ. Với các chuyên môn khác nhau. Và một cách để phối hợp họ.

## Bốn Dấu Hiệu Của Một Agent

Bốn khả năng phân biệt một AI agent với chatbot hoặc copilot. Tất cả bốn đều có mặt: agent. Còn thiếu bất kỳ điều nào: thứ gì đó kém hơn.

### 1. Tính Tự Chủ

Một agent hành động mà không cần hướng dẫn từng bước. Bạn xác định mục tiêu, "viết phân tích thị trường về ngành protein thực vật," và agent quyết định cách thực hiện nó. Nghiên cứu gì, tham khảo nguồn nào, cách cấu trúc phân tích, kết luận gì.

Đây không phải là làm theo kịch bản. Đó là phán đoán về quy trình. Chatbot làm những gì bạn hỏi. Agent quyết định những gì cần làm.

### 2. Sử Dụng Công Cụ

Một agent vươn xa hơn việc tạo văn bản. Nó duyệt các trang web, đọc và ghi tệp, thực thi mã, gọi API, tìm kiếm cơ sở dữ liệu, gửi email và làm việc với phần mềm khác. Điều này biến đổi AI từ một máy tư duy thành một máy thực hiện.

Hỏi ChatGPT "kiểm tra giá Bitcoin hiện tại," và nó tạo ra văn bản *trông như* một giá nhưng có thể sai. Nó dự đoán câu trả lời chính xác trông như thế nào từ dữ liệu đào tạo. Một AI agent gọi một API giá, truy xuất số thực tế, và báo cáo nó. Sự khác biệt giữa thực hiện và giả vờ.

### 3. Bộ Nhớ và Tính Bền Vững

Một agent nhớ. Không chỉ trong một cuộc trò chuyện, mà qua các phiên. Nó biết những gì nó đã làm hôm qua. Nó nhớ sở thích của bạn, bối cảnh kinh doanh của bạn, phản hồi của bạn về công việc trước đây của nó. Trạng thái liên tục này cho phép nó cải thiện theo thời gian và hoạt động nhất quán trong công ty của bạn.

Chatbot cung cấp cho bạn một khởi đầu mới mỗi cuộc trò chuyện. Agent cho bạn sự liên tục. Sự khác biệt giữa một nhân viên tạm thời đến mà không biết gì và một nhân viên sau sáu tháng làm việc.

### 4. Hành Vi Hướng Mục Tiêu

Một agent làm việc hướng tới mục tiêu, không chỉ là các prompt. Cung cấp cho nó mục tiêu như "tăng lưu lượng truy cập blog của chúng tôi 20% trong quý này," và nó phát triển kế hoạch, thực thi các nhiệm vụ, đo lường tiến độ và điều chỉnh hướng đi dựa trên kết quả.

Đây là khả năng tiên tiến nhất, và không phải tất cả các triển khai đều xử lý nó như nhau. Nhưng đó là hướng mà mọi thứ đang di chuyển, và đó là điều làm cho công ty không có nhân viên có thể. Bạn ngừng quản lý các nhiệm vụ. Bạn đặt mục tiêu và xem xét kết quả.

## Các Runtime Agent

Nếu agent là nhân viên, runtime là cách họ đến làm việc. Paperclip không phụ thuộc runtime. Nó điều phối agent bất kể chúng được xây dựng như thế nào. Nhưng các loại chính đáng biết:

**Claude Code** — Agent lập trình của Anthropic. Nó đọc tệp, viết mã, chạy lệnh terminal và làm việc với môi trường phát triển của bạn một mình. Một trong những agent có khả năng nhất cho công việc kỹ thuật.

**Cursor và các IDE agent tương tự** — Các AI agent được nhúng trong trình soạn thảo mã hiểu toàn bộ codebase, thực hiện các thay đổi trên nhiều tệp, và thực thi các nhiệm vụ phát triển.

**Custom HTTP agent** — Các agent bạn xây dựng hoặc tìm thấy đã được xây dựng sẵn giao tiếp qua các giao thức web tiêu chuẩn. Chúng có thể phục vụ bất kỳ chức năng kinh doanh nào: viết nội dung, phân tích dữ liệu, liên lạc khách hàng, nghiên cứu.

**Bash script agent** — Hình thức đơn giản nhất: các tự động hóa theo kịch bản mà Paperclip có thể lên lịch và quản lý. Không thông minh theo nghĩa AI, nhưng đáng tin cậy cho các nhiệm vụ thường xuyên.

Hiểu biết chính: Paperclip không quan tâm loại agent nào thực hiện công việc. Nó quan tâm đến cấu trúc. Ai báo cáo cho ai, mỗi agent xử lý gì, ngân sách của họ là gì, liệu họ có đáp ứng mục tiêu không. Một CEO thực sự không cần biết chi tiết kỹ thuật về cách mỗi nhân viên làm việc. CEO cần biết vai trò được lấp đầy và công việc đang hoàn thành.

## Agent Trong Tay, Công Ty Phía Trước

Hiểu về agent phân biệt các nhà sáng lập xây dựng công ty tỷ đô với những người chỉ sử dụng ChatGPT hiệu quả hơn. Bạn không thể điều phối những gì bạn không hiểu.

Các sự thật bây giờ đã ở trong tay. Agent là các hệ thống tự chủ, sử dụng công cụ, bền vững, hướng mục tiêu. Mọi thứ khác trong AI là thứ gì đó kém hơn.

Góc độ thực tế, cách triển khai chúng, đến trong hai chương tiếp theo, nơi Paperclip biến các agent này thành một công ty có cấu trúc. Bạn cần nền tảng này trước.

## Một Freelancer vs. Một Công Ty

Một agent làm việc một mình giống như một freelancer. Nó có thể làm công việc tốt, nhưng bạn quản lý nó trực tiếp. Bạn giao nhiệm vụ, xem xét kết quả, xử lý việc phối hợp với mọi thứ khác.

Hai hoặc ba agent làm việc một mình là ba freelancer. Bây giờ bạn dành tất cả thời gian quản lý bàn giao. Ai làm gì? Theo thứ tự nào? Ai kiểm tra công việc của ai? Bạn đã tạo ra một vấn đề phối hợp ăn mòn thời gian bạn đã tiết kiệm.

Một tổ chức agent, với các vai trò được xác định, đường báo cáo, quy trình ủy quyền, ngân sách và quản trị, là một công ty. Sự phối hợp được xây dựng vào cấu trúc. Các nhiệm vụ chảy từ mục tiêu đến vai trò đến thực thi mà không cần bạn quản lý mọi bàn giao. Bạn xem xét. Bạn chỉ đạo. Bạn quyết định. Hệ thống chạy.

Đó là sự khác biệt giữa việc sử dụng AI agent và xây dựng một công ty AI. Nền tảng làm cho cấu trúc đó có thể, biến các agent freelancer thành một công ty có tổ chức, là những gì tiếp theo.
