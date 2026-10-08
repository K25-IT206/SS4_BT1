# Rà soát User Story và sắp xếp Product Backlog — FoodNow

## Bước 1. Tìm lỗi theo INVEST

| Mã | Kết quả và lý do |
|---|---|
| US1 | **Đạt:** Vai trò rõ, một việc, có lợi ích, thử được bằng cách chọn loại món rồi xem kết quả. |
| US2 | **T (Testable — kiểm thử được):** “Đẹp”, “dễ dùng” và “hài lòng” chưa có tiêu chí quan sát hoặc đo lường thống nhất, nên nhóm và Tester khó xác định khi nào hoàn thành. |
| US3 | **N (Negotiable — có thể thương lượng) và V (Valuable — có giá trị):** Product Backlog vẫn có thể chứa việc kỹ thuật, nhưng câu này áp đặt React như giải pháp và chưa nêu kết quả kỹ thuật cụ thể mang lại giá trị gì. Có thể viết thành một technical story nếu nêu rõ vấn đề và lợi ích cần đạt, chẳng hạn giảm thời gian tải hoặc giảm công sức bảo trì. |
| US4 | **S (Small — đủ nhỏ):** Gộp nhiều năng lực độc lập: xem báo cáo theo các mốc thời gian, lọc theo khu vực/nhà hàng, xuất Excel và tự gửi email; khó ước lượng, ưu tiên và hoàn tất trong một Sprint như một story. “Theo dõi kinh doanh” cũng chưa đủ cụ thể để làm tiêu chí nghiệm thu. |

## Bước 2. Sửa lỗi

### a) Viết lại US2 với tiêu chí “dễ dùng” đo được

**US2:** Là một khách hàng, tôi muốn hoàn tất đặt một món đã chọn trong tối đa 3 bước trên giao diện đặt món, để đặt món nhanh và thuận tiện.

**Tiêu chí đo lường:** Trong kiểm thử khả dụng với ít nhất 5 khách hàng đại diện, ít nhất 4 người hoàn tất luồng đặt món trong tối đa 3 bước mà không cần trợ giúp. Nhóm cần thống nhất trước điểm bắt đầu/kết thúc của luồng và cách ghi nhận bước để kết quả kiểm thử nhất quán.

### b) Tách US4 và đặt trong cây Epic → Feature → User Story

**Epic: Báo cáo và theo dõi hiệu quả kinh doanh**

└── **Feature: Báo cáo doanh thu**

&nbsp;&nbsp;&nbsp;&nbsp;├── **US4.1 — Xem báo cáo:** Là một admin, tôi muốn xem doanh thu theo ngày, tuần hoặc tháng và lọc theo khu vực hoặc nhà hàng, để theo dõi tình hình kinh doanh theo phạm vi mình quan tâm.

&nbsp;&nbsp;&nbsp;&nbsp;└── **US4.2 — Xuất và gửi báo cáo:** Là một admin, tôi muốn xuất báo cáo doanh thu đã chọn thành tệp Excel và gửi báo cáo đó qua email cho ban giám đốc, để chia sẻ số liệu kinh doanh thuận tiện.

US4.2 là một bản tách ban đầu; trong Refinement, nhóm nên xác nhận việc xuất Excel và gửi email có thể ước lượng, hoàn tất cùng nhau hay cần tách tiếp thành hai story riêng.

## Bước 3. Xếp lại Product Backlog

### a) Thứ tự ưu tiên đề xuất

Thứ tự dưới đây giả định mục tiêu gần nhất là cải thiện hành trình đặt món cho khách hàng, đồng thời cung cấp báo cáo quản trị sau đó. Product Owner có thể điều chỉnh theo dữ liệu và mục tiêu kinh doanh thực tế.

| Thứ tự | Story | Lý do |
|---:|---|---|
| 1 | **US1 — Lọc nhà hàng theo loại món** | Giúp khách hàng tìm được lựa chọn phù hợp, trực tiếp hỗ trợ khám phá món ăn trong luồng đặt món. |
| 2 | **US2 — Hoàn tất đặt món trong tối đa 3 bước** | Tập trung giảm trở ngại trong trải nghiệm đặt món; tiêu chí kiểm thử giúp xác định tác động sau khi triển khai. |
| 3 | **US4.1 — Xem báo cáo doanh thu theo thời gian và bộ lọc** | Cung cấp khả năng quan sát hoạt động kinh doanh cốt lõi cho admin; là nền tảng hợp lý trước khi chia sẻ báo cáo. |
| 4 | **US4.2 — Xuất và gửi báo cáo** | Bổ sung khả năng phân phối số liệu; nên thực hiện sau khi định dạng và nội dung báo cáo đã được xác nhận. |

### b) Mức chi tiết theo DEEP và công việc trong Refinement

DEEP là **Detailed appropriately** (chi tiết ở mức phù hợp), **Emergent** (backlog tiếp tục phát triển), **Estimated** (được ước lượng) và **Prioritized** (được sắp ưu tiên). Story đứng đầu cần đủ rõ để nhóm hiểu giá trị, thảo luận cách làm, xác định tiêu chí nghiệm thu và ước lượng; không cần đặc tả mọi chi tiết triển khai từ đầu. Backlog vẫn có thể thay đổi khi có thông tin mới.

Trước khi đưa story vào Sprint, nhóm cần cùng Product Owner rà soát và làm rõ phạm vi/tiêu chí nghiệm thu, kiểm tra phụ thuộc và khả năng hoàn tất trong Sprint, chia nhỏ nếu cần, ước lượng theo cách nhóm thống nhất, rồi xác nhận thứ tự ưu tiên và năng lực Sprint. Product Owner quyết định giá trị và thứ tự ưu tiên; Developers chịu trách nhiệm về ước lượng và kế hoạch thực hiện.
