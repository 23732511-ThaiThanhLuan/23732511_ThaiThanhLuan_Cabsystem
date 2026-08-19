
Bước 1:

1. Ngữ cảnh nghiệp vụ

Công ty ABC là doanh nghiệp cung cấp dịch vụ đặt xe trực tuyến. Khách hàng có thể đặt xe thông qua tổng đài hoặc ứng dụng, trong khi tài xế thực hiện chuyến và nhân viên vận hành quản lý hoạt động. Tuy nhiên, quy trình hiện tại còn phụ thuộc nhiều vào thao tác thủ công và các thông tin chưa được quản lý tập trung.

Doanh nghiệp muốn xây dựng một nền tảng CAB mới để quản lý xuyên suốt quy trình từ đặt xe → tìm tài xế → thực hiện chuyến → tính cước → thanh toán → đánh giá, đồng thời có khả năng phục vụ số lượng lớn người dùng và mở rộng trong tương lai.

2. Bussiness Problem
Công ty ABC đang gặp khó khăn trong việc quản lý và mở rộng hoạt động đặt xe do quy trình phân công tài xế còn thủ công, thông tin chuyến đi và thanh toán chưa được quản lý tập trung, khả năng theo dõi của khách hàng còn hạn chế và hệ thống hiện tại khó đáp ứng khi quy mô tăng. Điều này làm giảm hiệu quả vận hành, ảnh hưởng đến trải nghiệm khách hàng và hạn chế khả năng phát triển các dịch vụ mới.

Bước 2:

| STT | Stakeholder                         | Vai trò                                       | Mối quan tâm / nhu cầu chính                                                       |
| --: | ----------------------------------- | --------------------------------------------- | ---------------------------------------------------------------------------------- |
|   1 | **Khách hàng**                      | Người sử dụng dịch vụ đặt xe                  | Đăng ký, đặt xe, theo dõi chuyến, thanh toán, xem lịch sử và đánh giá tài xế       |
|   2 | **Tài xế**                          | Người trực tiếp thực hiện chuyến xe           | Nhận chuyến, chấp nhận/từ chối, cập nhật trạng thái, quản lý phương tiện và vị trí |
|   3 | **Nhân viên vận hành**              | Quản lý và giám sát hoạt động đặt xe          | Theo dõi chuyến, tài xế, khách hàng; xử lý chuyến lỗi; hỗ trợ vận hành             |
|   4 | **Quản lý vận hành**                | Giám sát hiệu quả hoạt động                   | Theo dõi số chuyến, tỷ lệ hoàn thành/hủy, hiệu quả tài xế và các vấn đề vận hành   |
|   5 | **Ban giám đốc / Lãnh đạo ABC**     | Định hướng và ra quyết định kinh doanh        | Doanh thu, hiệu quả hoạt động, khả năng mở rộng và phát triển dịch vụ              |
|   6 | **Nhân viên quản trị hệ thống**     | Quản lý tài khoản, quyền và cấu hình hệ thống | Phân quyền, quản lý người dùng, bảo mật và cấu hình                                |
|   7 | **Nhà cung cấp dịch vụ thanh toán** | Xử lý giao dịch thanh toán điện tử            | Tiếp nhận yêu cầu thanh toán, trả kết quả giao dịch thành công/thất bại            |
|   8 | **Nhà cung cấp dịch vụ thông báo**  | Gửi thông báo đến khách hàng/tài xế           | Gửi thông báo đặt xe, nhận chuyến, trạng thái chuyến, thanh toán...                |
|   9 | **Bộ phận tài chính/kế toán**       | Theo dõi và đối soát giao dịch                | Doanh thu, thanh toán, lịch sử giao dịch và đối soát                               |
|  10 | **Business Analyst (BA)**           | Phân tích nghiệp vụ và làm rõ yêu cầu         | Xác định phạm vi, yêu cầu, quy trình, business rules và vấn đề cần xác nhận        |
|  11 | **Đội phát triển hệ thống**         | Xây dựng và triển khai CAB                    | Hiểu và hiện thực hóa yêu cầu nghiệp vụ thành hệ thống                             |
|  12 | **Bộ phận IT / vận hành hệ thống**  | Đảm bảo hệ thống hoạt động ổn định            | Hiệu năng, khả năng mở rộng, giám sát, bảo mật và xử lý sự cố                      |

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
