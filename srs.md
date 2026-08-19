
Bước 1: Xác định ngữ cảnh nghiệp vụ và Bussiness Problem

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

| **Business Goal**                                          | **Mục đích**                                                                                                                                                                                                 |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **BG001: Hỗ trợ đặt xe trực tuyến**                        | Cho phép khách hàng tạo yêu cầu đặt xe nhanh chóng, thuận tiện và quản lý toàn bộ quá trình đặt xe trên một nền tảng tập trung.                                                                              |
| **BG002: Tự động hóa việc tìm và phân công tài xế**        | Tự động xác định và lựa chọn tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành; tiếp tục tìm tài xế khác nếu tài xế được đề xuất từ chối hoặc không phản hồi.                     |
| **BG003: Hỗ trợ theo dõi chuyến đi**                       | Cho phép khách hàng và nhân viên vận hành theo dõi trạng thái chuyến đi, thông tin tài xế và thời gian dự kiến tài xế đến.                                                                                   |
| **BG004: Hỗ trợ quản lý và thực hiện chuyến đi**           | Cho phép tài xế nhận chuyến, cập nhật các trạng thái trong quá trình thực hiện và ghi nhận thông tin vị trí để hỗ trợ vận hành.                                                                              |
| **BG005: Hỗ trợ tính cước và thanh toán**                  | Tính toán số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi; hỗ trợ thanh toán tiền mặt và thanh toán điện tử thông qua nhà cung cấp bên ngoài.                                       |
| **BG006: Quản lý thông báo tập trung**                     | Đảm bảo khách hàng và tài xế nhận được thông báo kịp thời về các sự kiện quan trọng của chuyến đi, đồng thời cho phép mở rộng thêm các kênh thông báo trong tương lai.                                       |
| **BG007: Hỗ trợ quản lý vận hành**                         | Cung cấp cho nhân viên vận hành khả năng quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý các trường hợp bất thường.                                                                              |
| **BG008: Hỗ trợ báo cáo và quản lý hiệu quả kinh doanh**   | Cung cấp dữ liệu về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế để hỗ trợ quản lý và ra quyết định.                                                             |
| **BG009: Đảm bảo an toàn và bảo mật thông tin**            | Bảo vệ thông tin cá nhân, dữ liệu vị trí, dữ liệu giao dịch và kiểm soát quyền truy cập đối với các chức năng nhạy cảm.                                                                                      |
| **BG010: Đảm bảo khả năng mở rộng và phát triển hệ thống** | Xây dựng nền tảng có thể phục vụ số lượng lớn khách hàng và tài xế, cho phép mở rộng độc lập các thành phần và bổ sung dịch vụ, phương thức thanh toán hoặc nhà cung cấp mới trong tương lai.                |
| **BG011: Đảm bảo tính ổn định và liên tục của hệ thống**   | Hạn chế việc lỗi ở một chức năng như thanh toán hoặc thông báo ảnh hưởng đến toàn bộ hệ thống đặt xe, đồng thời cho phép triển khai các chức năng mới từng phần mà ít ảnh hưởng đến hệ thống đang hoạt động. |


Bước 4: 
Xác định phạm vi

1. In Scope – Trong phạm vi

| **Nhóm**                | **Phạm vi hệ thống CAB**                                                                                                                      |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Quản lý tài khoản**   | Đăng ký, đăng nhập, cập nhật thông tin khách hàng và tài xế; xác thực người dùng.                                                             |
| **Đặt xe**              | Nhập điểm đón, điểm đến, lựa chọn loại xe, tạo và tiếp nhận yêu cầu đặt xe.                                                                   |
| **Tìm tài xế**          | Xác định tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và tiêu chí vận hành; tự động tìm tài xế khác khi tài xế từ chối/không phản hồi. |
| **Quản lý tài xế**      | Quản lý hồ sơ, phương tiện, trạng thái hoạt động và khả năng nhận chuyến của tài xế.                                                          |
| **Quản lý chuyến đi**   | Nhận chuyến, cập nhật trạng thái: đã đến điểm đón → đã đón khách → đang di chuyển → hoàn thành; lưu thông tin chuyến đi.                      |
| **Theo dõi vị trí**     | Ghi nhận vị trí tài xế để hỗ trợ tìm tài xế gần khách và dự kiến thời gian đến.                                                               |
| **Theo dõi chuyến**     | Khách hàng theo dõi trạng thái yêu cầu/chuyến đi, tài xế và thời gian dự kiến đến.                                                            |
| **Tính cước**           | Xác định số tiền phải trả dựa trên loại dịch vụ và thông tin chuyến đi.                                                                       |
| **Thanh toán**          | Hỗ trợ tiền mặt và thanh toán điện tử; tích hợp nhà cung cấp thanh toán bên ngoài; xử lý giao dịch thất bại.                                  |
| **Thông báo**           | Thông báo cho khách hàng/tài xế về yêu cầu đặt xe, nhận chuyến, tài xế đến, hoàn thành chuyến và kết quả thanh toán.                          |
| **Đánh giá**            | Cho phép khách hàng đánh giá tài xế sau khi hoàn thành chuyến.                                                                                |
| **Quản trị vận hành**   | Nhân viên quản lý khách hàng, tài xế, phương tiện, chuyến đi, trạng thái tài xế và các trường hợp lỗi.                                        |
| **Phân quyền**          | Kiểm soát quyền truy cập các chức năng quản trị và thao tác nhạy cảm.                                                                         |
| **Lịch sử & giao dịch** | Tra cứu lịch sử chuyến đi và lịch sử giao dịch.                                                                                               |
| **Báo cáo**             | Báo cáo số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động tài xế.                                                 |
| **Bảo mật & Audit**     | Bảo vệ dữ liệu cá nhân, vị trí, giao dịch và lưu vết các thao tác quan trọng.                                                                 |
| **Khả năng mở rộng**    | Thiết kế nền tảng cho phép mở rộng số lượng người dùng và bổ sung dịch vụ, phương thức thanh toán, kênh thông báo mới.                        |

2. Out of Scope / Chưa xác định – Ngoài hoặc chưa thuộc phạm vi hiện tại

   
| **Nội dung**                                        | **Trạng thái**                                                                            |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Chi tiết công thức tính cước**                    | Chưa xác định, cần BA làm rõ với khách hàng.                                              |
| **Tiêu chí và thuật toán ưu tiên tài xế**           | Chưa chốt, cần xác nhận với doanh nghiệp.                                                 |
| **Thời gian tài xế phải phản hồi**                  | Chưa xác định.                                                                            |
| **Chính sách hủy chuyến**                           | Chưa xác định.                                                                            |
| **Cách xử lý khi mất kết nối mạng**                 | Chưa xác định.                                                                            |
| **Thời gian lưu trữ dữ liệu**                       | Chưa xác định.                                                                            |
| **Thông tin nhạy cảm của thẻ/tài khoản thanh toán** | **Không lưu trực tiếp trên CAB**; do nhà cung cấp thanh toán bên ngoài xử lý.             |
| **Hệ thống của nhà cung cấp thanh toán**            | CAB chỉ tích hợp và nhận kết quả giao dịch, không xây dựng hệ thống thanh toán bên ngoài. |
| **Hệ thống cung cấp dịch vụ thông báo bên ngoài**   | CAB tích hợp với nhà cung cấp nhưng không xây dựng hạ tầng của nhà cung cấp.              |

Xác định Bussiness Requirement:
| **Business Requirement**                    | **Diễn giải**                                                                                                                                                                                     |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BR01: Đặt xe trực tuyến**                 | Hệ thống phải hỗ trợ khách hàng tạo yêu cầu đặt xe bằng cách nhập điểm đón, điểm đến và lựa chọn loại xe phù hợp.                                                                                 |
| **BR02: Tìm và phân công tài xế**           | Hệ thống phải tự động tìm và phân công tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành.                                                                              |
| **BR03: Theo dõi chuyến đi**                | Hệ thống phải cho phép khách hàng theo dõi trạng thái yêu cầu và chuyến đi, thông tin tài xế và thời gian dự kiến tài xế đến.                                                                     |
| **BR04: Quản lý chuyến đi**                 | Hệ thống phải hỗ trợ tài xế nhận hoặc từ chối chuyến và cập nhật các trạng thái trong quá trình thực hiện chuyến.                                                                                 |
| **BR05: Quản lý vị trí tài xế**             | Hệ thống phải ghi nhận thông tin vị trí của tài xế để hỗ trợ tìm tài xế gần khách hàng và dự kiến thời gian đến.                                                                                  |
| **BR06: Tính cước chuyến đi**               | Hệ thống phải xác định số tiền khách hàng cần thanh toán dựa trên loại dịch vụ và thông tin chuyến đi.                                                                                            |
| **BR07: Thanh toán**                        | Hệ thống phải hỗ trợ thanh toán bằng tiền mặt và phương thức điện tử thông qua nhà cung cấp thanh toán bên ngoài, đồng thời xử lý trường hợp giao dịch thất bại.                                  |
| **BR08: Quản lý thông báo**                 | Hệ thống phải gửi thông báo cho khách hàng và tài xế về các sự kiện quan trọng như tạo yêu cầu, nhận chuyến, tài xế đến, hoàn thành chuyến và kết quả thanh toán.                                 |
| **BR09: Đánh giá tài xế**                   | Hệ thống phải cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành.                                                                                                                   |
| **BR10: Quản lý tài khoản và hồ sơ**        | Hệ thống phải hỗ trợ quản lý thông tin tài khoản, hồ sơ khách hàng, tài xế và thông tin phương tiện.                                                                                              |
| **BR11: Quản lý vận hành**                  | Hệ thống phải cung cấp giao diện để nhân viên vận hành quản lý khách hàng, tài xế, phương tiện, chuyến đi và hỗ trợ xử lý các trường hợp bất thường.                                              |
| **BR12: Phân quyền quản trị**               | Hệ thống phải kiểm soát quyền truy cập để đảm bảo nhân viên chỉ được thực hiện các chức năng phù hợp với quyền hạn.                                                                               |
| **BR13: Quản lý lịch sử và giao dịch**      | Hệ thống phải lưu trữ và cho phép tra cứu lịch sử chuyến đi, thông tin thanh toán và giao dịch phục vụ vận hành và kiểm tra.                                                                      |
| **BR14: Báo cáo hoạt động**                 | Hệ thống phải cung cấp báo cáo về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế.                                                                       |
| **BR15: Bảo mật và lưu vết**                | Hệ thống phải bảo vệ thông tin cá nhân, dữ liệu vị trí và dữ liệu giao dịch, đồng thời lưu vết các thao tác quan trọng để phục vụ kiểm tra.                                                       |
| **BR16: Khả năng mở rộng**                  | Hệ thống phải có khả năng phục vụ số lượng lớn khách hàng và tài xế, đồng thời cho phép bổ sung dịch vụ, phương thức thanh toán và kênh thông báo mới mà hạn chế ảnh hưởng đến hệ thống hiện tại. |
| **BR17: Đảm bảo tính liên tục của dịch vụ** | Hệ thống phải hạn chế việc lỗi tại một thành phần như thanh toán hoặc thông báo làm ảnh hưởng đến toàn bộ chức năng đặt xe.                                                                       |



