
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


Ma trận stakeholder
| Stakeholder                        | Mức độ ảnh hưởng | Mức độ quan tâm | Nhóm                  | Chiến lược quản lý                                                                      |
| ---------------------------------- | ---------------- | --------------- | --------------------- | --------------------------------------------------------------------------------------- |
| **Ban giám đốc / Lãnh đạo ABC**    | Cao              | Cao             | 🟥 **Manage Closely** | Thường xuyên trao đổi, xác nhận mục tiêu, phạm vi, ưu tiên và các quyết định quan trọng |
| **Quản lý vận hành**               | Cao              | Cao             | 🟥 **Manage Closely** | Làm việc thường xuyên để xác định quy trình, business rules và các vấn đề vận hành      |
| **Nhân viên vận hành**             | Trung bình       | Cao             | 🟧 **Keep Informed**  | Thu thập yêu cầu, quan sát quy trình thực tế, lấy phản hồi và cập nhật thay đổi         |
| **Khách hàng**                     | Trung bình       | Cao             | 🟧 **Keep Informed**  | Khảo sát/phỏng vấn nhu cầu, kiểm thử trải nghiệm và thu thập phản hồi                   |
| **Tài xế**                         | Trung bình       | Cao             | 🟧 **Keep Informed**  | Tìm hiểu quy trình nhận chuyến, cập nhật trạng thái, vị trí và các khó khăn thực tế     |
| **Quản trị hệ thống**              | Cao              | Trung bình      | 🟨 **Keep Satisfied** | Tham vấn về phân quyền, bảo mật, cấu hình và vận hành hệ thống                          |
| **Bộ phận tài chính/kế toán**      | Trung bình       | Trung bình      | 🟨 **Keep Satisfied** | Xác định yêu cầu về thanh toán, doanh thu, giao dịch và đối soát                        |
| **Nhà cung cấp thanh toán**        | Cao              | Trung bình      | 🟨 **Keep Satisfied** | Phối hợp về API, trạng thái giao dịch, lỗi thanh toán và bảo mật                        |
| **Nhà cung cấp thông báo**         | Trung bình       | Trung bình      | 🟩 **Monitor**        | Phối hợp khi tích hợp và khi có thay đổi về kênh thông báo                              |
| **Đội phát triển hệ thống**        | Cao              | Cao             | 🟥 **Manage Closely** | Trao đổi yêu cầu, tính khả thi, ưu tiên và các thay đổi trong quá trình phát triển      |
| **Bộ phận IT / vận hành hệ thống** | Cao              | Cao             | 🟥 **Manage Closely** | Thống nhất yêu cầu về hiệu năng, khả năng mở rộng, bảo mật và giám sát                  |
