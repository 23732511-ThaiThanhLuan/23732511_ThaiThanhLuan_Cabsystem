
Bước 1:

1. Ngữ cảnh nghiệp vụ

Công ty ABC là doanh nghiệp cung cấp dịch vụ đặt xe trực tuyến. Khách hàng có thể đặt xe thông qua tổng đài hoặc ứng dụng, trong khi tài xế thực hiện chuyến và nhân viên vận hành quản lý hoạt động. Tuy nhiên, quy trình hiện tại còn phụ thuộc nhiều vào thao tác thủ công và các thông tin chưa được quản lý tập trung.

Doanh nghiệp muốn xây dựng một nền tảng CAB mới để quản lý xuyên suốt quy trình từ đặt xe → tìm tài xế → thực hiện chuyến → tính cước → thanh toán → đánh giá, đồng thời có khả năng phục vụ số lượng lớn người dùng và mở rộng trong tương lai.

2. Bussiness Problem
Công ty ABC đang gặp khó khăn trong việc quản lý và mở rộng hoạt động đặt xe do quy trình phân công tài xế còn thủ công, thông tin chuyến đi và thanh toán chưa được quản lý tập trung, khả năng theo dõi của khách hàng còn hạn chế và hệ thống hiện tại khó đáp ứng khi quy mô tăng. Điều này làm giảm hiệu quả vận hành, ảnh hưởng đến trải nghiệm khách hàng và hạn chế khả năng phát triển các dịch vụ mới.

Bước 2:

| **Stakeholder**                    | **Vai trò / Mối quan tâm**                                                                                                                                             |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Khách hàng**                     | Đăng ký, đặt xe, theo dõi chuyến đi, thanh toán và đánh giá tài xế; quan tâm đến tốc độ, tính chính xác, minh bạch và trải nghiệm sử dụng.                             |
| **Tài xế**                         | Nhận và thực hiện chuyến, cập nhật trạng thái, thông tin phương tiện và vị trí; quan tâm đến việc nhận chuyến phù hợp, thông tin chính xác và thuận tiện khi làm việc. |
| **Nhân viên vận hành**             | Quản lý khách hàng, tài xế, phương tiện và chuyến đi; theo dõi chuyến đang diễn ra và xử lý các trường hợp lỗi; quan tâm đến khả năng kiểm soát và xử lý nhanh.        |
| **Quản lý / Ban giám đốc**         | Theo dõi hiệu quả hoạt động, doanh thu, số lượng chuyến, tỷ lệ hoàn thành/hủy; quan tâm đến hiệu quả kinh doanh, khả năng mở rộng và phát triển hệ thống.              |
| **Bộ phận tài chính / kế toán**    | Theo dõi doanh thu, giao dịch và đối soát thanh toán; quan tâm đến tính chính xác, đầy đủ và an toàn của dữ liệu giao dịch.                                            |
| **Nhà cung cấp thanh toán**        | Xử lý các giao dịch thanh toán điện tử; quan tâm đến tính chính xác, bảo mật và khả năng tích hợp ổn định với hệ thống CAB.                                            |
| **Nhà cung cấp dịch vụ thông báo** | Cung cấp các kênh gửi thông báo cho khách hàng và tài xế; quan tâm đến khả năng gửi thông báo chính xác, ổn định và có thể mở rộng thêm kênh.                          |
| **Business Analyst**               | Thu thập, phân tích và làm rõ nhu cầu của các bên liên quan; quan tâm đến việc xác định đúng phạm vi, yêu cầu, quy tắc nghiệp vụ và các vấn đề còn chưa rõ.            |
| **Đội phát triển / IT**            | Phân tích, xây dựng và triển khai hệ thống; quan tâm đến yêu cầu rõ ràng, khả năng mở rộng, tích hợp và bảo trì hệ thống.                                              |


Ma trận stakeholder:

                         MỨC ĐỘ QUAN TÂM
                  THẤP                     CAO
              ┌─────────────────────┬─────────────────────┐
        CAO   │                     │  MANAGE CLOSELY     │
              │  KEEP SATISFIED     │                     │
QUYỀN         │ • Nhà cung cấp      │ • Ban giám đốc      │
LỰC           │   thanh toán        │ • Nhân viên vận hành│
              │ • Nhà cung cấp      │                     │
              │   thông báo         │                     │
              ├─────────────────────┼─────────────────────┤
        THẤP  │                     │  KEEP INFORMED      │
              │  MONITOR            │                     │
              │ • Tài chính/kế toán │ • Khách hàng        │
              │ • Đội IT/Phát triển │ • Tài xế            │
              │                     │ • Business Analyst  │
              └─────────────────────┴─────────────────────┘

Bước 3:
Bussiness Goal của khách hàng:

Business Goals

BG001: Hỗ trợ đặt xe trực tuyến
Mục đích: Cho phép khách hàng tạo yêu cầu đặt xe một cách nhanh chóng, thuận tiện và quản lý toàn bộ quá trình đặt xe trên một nền tảng tập trung.

BG002: Tự động hóa việc tìm và phân công tài xế
Mục đích: Tự động xác định và lựa chọn tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành, đồng thời tiếp tục tìm tài xế khác nếu tài xế được đề xuất từ chối hoặc không phản hồi.

BG003: Hỗ trợ theo dõi chuyến đi
Mục đích: Cho phép khách hàng và nhân viên vận hành theo dõi trạng thái chuyến đi, thông tin tài xế và thời gian dự kiến tài xế đến.

BG004: Hỗ trợ quản lý và thực hiện chuyến đi
Mục đích: Cho phép tài xế nhận chuyến, cập nhật các trạng thái trong quá trình thực hiện và ghi nhận thông tin vị trí để hỗ trợ vận hành.

BG005: Hỗ trợ tính cước và thanh toán
Mục đích: Tính toán số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi, đồng thời hỗ trợ thanh toán tiền mặt và thanh toán điện tử thông qua nhà cung cấp bên ngoài.

BG006: Quản lý thông báo tập trung
Mục đích: Đảm bảo khách hàng và tài xế nhận được thông báo kịp thời về các sự kiện quan trọng của chuyến đi, đồng thời cho phép mở rộng thêm các kênh thông báo trong tương lai.

BG007: Hỗ trợ quản lý vận hành
Mục đích: Cung cấp cho nhân viên vận hành khả năng quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý các trường hợp bất thường.

BG008: Hỗ trợ báo cáo và quản lý hiệu quả kinh doanh
Mục đích: Cung cấp dữ liệu về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế để hỗ trợ quản lý và ra quyết định.

BG009: Đảm bảo an toàn và bảo mật thông tin
Mục đích: Bảo vệ thông tin cá nhân, dữ liệu vị trí, dữ liệu giao dịch và kiểm soát quyền truy cập đối với các chức năng nhạy cảm.

BG010: Đảm bảo khả năng mở rộng và phát triển hệ thống
Mục đích: Xây dựng nền tảng có thể phục vụ số lượng lớn khách hàng và tài xế, cho phép mở rộng độc lập các thành phần và bổ sung dịch vụ, phương thức thanh toán hoặc nhà cung cấp mới trong tương lai.

BG011: Đảm bảo tính ổn định và liên tục của hệ thống
Mục đích: Hạn chế việc lỗi ở một chức năng như thanh toán hoặc thông báo ảnh hưởng đến toàn bộ hệ thống đặt xe, đồng thời cho phép triển khai các chức năng mới từng phần mà ít ảnh hưởng đến hệ thống đang hoạt động.
