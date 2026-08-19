
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

Bước 5:Xác định Bussiness Requirement:

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


Bước 6: Xác định Bussiness Process

BP01 – Đăng ký và quản lý tài khoản

```mermaid
flowchart TD
    A([Bắt đầu]) --> B{Người dùng là ai?}
    B -->|Khách hàng| C[Khách hàng đăng ký tài khoản]
    B -->|Tài xế| D[Tài xế đăng ký tài khoản]
    C --> E[Nhập thông tin cá nhân]
    D --> F[Nhập thông tin cá nhân và phương tiện]
    E --> G[Hệ thống kiểm tra thông tin]
    F --> G
    G --> H{Thông tin hợp lệ?}
    H -->|Không| I[Thông báo lỗi]
    I --> E
    H -->|Có| J[Tạo tài khoản]
    J --> K[Đăng nhập]
    K --> L[Cập nhật hồ sơ khi cần]
    L --> M([Kết thúc])
```
BP02 – Đặt xe và tìm tài xế

```mermaid
flowchart TD
    A([Khách hàng bắt đầu]) --> B[Đăng nhập]
    B --> C[Nhập điểm đón]
    C --> D[Nhập điểm đến]
    D --> E[Chọn loại xe]
    E --> F[Gửi yêu cầu đặt xe]
    F --> G[Hệ thống tiếp nhận yêu cầu]
    G --> H[Thông báo yêu cầu đã được tiếp nhận]
    H --> I[Xác định tài xế phù hợp]
    I --> J{Có tài xế phù hợp?}

    J -->|Không| K[Thông báo không tìm được tài xế]
    K --> Z([Kết thúc])

    J -->|Có| L[Ưu tiên tài xế phù hợp và gần khách hàng]
    L --> M[Gửi yêu cầu cho tài xế]
    M --> N[Chờ tài xế phản hồi]
    N --> O{Tài xế phản hồi?}

    O -->|Không| P[Hết thời gian phản hồi]
    P --> Q[Chuyển sang tài xế khác]
    Q --> I

    O -->|Có| R{Tài xế chấp nhận?}
    R -->|Không| S[Tài xế từ chối]
    S --> Q

    R -->|Có| T[Xác nhận tài xế nhận chuyến]
    T --> U[Thông báo tài xế cho khách hàng]
    U --> V([Chuyển sang thực hiện chuyến])
```

BP03 – Thực hiện và theo dõi chuyến đi
```mermaid
flowchart TD
    A([Tài xế nhận chuyến]) --> B[Cập nhật trạng thái đang đến]
    B --> C[Theo dõi vị trí tài xế]
    C --> D[Cập nhật thời gian dự kiến đến]
    D --> E[Thông báo cho khách hàng]
    E --> F{Tài xế đã đến điểm đón?}

    F -->|Chưa| C
    F -->|Có| G[Cập nhật trạng thái đã đến]
    G --> H[Thông báo cho khách hàng]
    H --> I[Đón khách]
    I --> J[Cập nhật trạng thái đã đón khách]
    J --> K[Đang di chuyển]
    K --> L[Cập nhật vị trí trong chuyến đi]
    L --> M{Đã đến điểm đến?}

    M -->|Chưa| L
    M -->|Có| N[Hoàn thành chuyến]
    N --> O[Thông báo chuyến đã hoàn thành]
    O --> P([Kết thúc])
```

BP04 – Tính cước và thanh toán
```mermaid
flowchart TD
    A([Chuyến đi hoàn thành]) --> B[Thu thập thông tin chuyến đi]
    B --> C[Xác định loại dịch vụ]
    C --> D[Tính số tiền phải trả]
    D --> E[Thông báo số tiền cho khách hàng]
    E --> F{Phương thức thanh toán?}

    F -->|Tiền mặt| G[Khách hàng thanh toán tiền mặt]
    G --> H[Xác nhận thanh toán]
    H --> I[Lưu giao dịch]

    F -->|Điện tử| J[Gửi yêu cầu đến nhà cung cấp thanh toán]
    J --> K{Thanh toán thành công?}

    K -->|Có| L[Nhận kết quả thanh toán]
    L --> I

    K -->|Không| M[Thông báo thanh toán thất bại]
    M --> N{Cho phép thanh toán lại?}
    N -->|Có| J
    N -->|Không| O[Xử lý theo chính sách doanh nghiệp]
    O --> I

    I --> P[Thông báo kết quả thanh toán]
    P --> Q([Kết thúc])
```
BP05 – Thông báo
```mermaid
flowchart TD
    A([Có sự kiện trong hệ thống]) --> B{Loại sự kiện?}

    B -->|Đặt xe| C[Thông báo yêu cầu đã được tiếp nhận]
    B -->|Tài xế nhận| D[Thông báo tài xế đã nhận chuyến]
    B -->|Tài xế đến| E[Thông báo tài xế đã đến điểm đón]
    B -->|Hoàn thành| F[Thông báo chuyến đã hoàn thành]
    B -->|Thanh toán| G[Thông báo kết quả thanh toán]
    B -->|Chuyến mới| H[Thông báo chuyến mới cho tài xế]
    B -->|Thay đổi chuyến| I[Thông báo thay đổi cho tài xế]

    C --> J[Gửi qua kênh thông báo]
    D --> J
    E --> J
    F --> J
    G --> J
    H --> J
    I --> J

    J --> K{Gửi thành công?}
    K -->|Có| L([Kết thúc])
    K -->|Không| M[Xử lý lỗi gửi thông báo]
    M --> N[Thử lại hoặc chuyển kênh khác]
    N --> L
```
BP06 – Đánh giá tài xế
```mermaid
flowchart TD
    A([Chuyến đi hoàn thành]) --> B[Thông báo khách hàng đánh giá]
    B --> C{Khách hàng đánh giá?}
    C -->|Không| D[Không ghi nhận đánh giá]
    D --> Z([Kết thúc])

    C -->|Có| E[Khách hàng nhập đánh giá]
    E --> F[Hệ thống kiểm tra đánh giá]
    F --> G{Dữ liệu hợp lệ?}
    G -->|Không| H[Thông báo lỗi]
    H --> E
    G -->|Có| I[Lưu đánh giá tài xế]
    I --> J[Cập nhật dữ liệu đánh giá]
    J --> Z([Kết thúc])
```

BP07 – Quản lý vận hành
```mermaid
flowchart TD
    A([Nhân viên vận hành đăng nhập]) --> B[Xác thực tài khoản]
    B --> C{Có quyền truy cập?}

    C -->|Không| D[Từ chối truy cập]
    D --> Z([Kết thúc])

    C -->|Có| E[Truy cập giao diện quản trị]
    E --> F{Cần thực hiện chức năng nào?}

    F -->|Quản lý khách hàng| G[Tra cứu / cập nhật khách hàng]
    F -->|Quản lý tài xế| H[Tra cứu / cập nhật tài xế]
    F -->|Quản lý phương tiện| I[Tra cứu / cập nhật phương tiện]
    F -->|Theo dõi chuyến| J[Xem các chuyến đang diễn ra]
    F -->|Xử lý sự cố| K[Kiểm tra và xử lý chuyến bị lỗi]
    F -->|Tra cứu giao dịch| L[Xem lịch sử giao dịch]

    G --> M[Lưu thay đổi]
    H --> M
    I --> M
    J --> N[Cập nhật thông tin]
    K --> M
    L --> N

    M --> O[Ghi nhận audit log]
    N --> O
    O --> P([Kết thúc])
```
BP08 – Báo cáo hoạt động
```mermaid
flowchart TD
    A([Quản lý yêu cầu báo cáo]) --> B[Chọn loại báo cáo]
    B --> C{Loại báo cáo?}

    C -->|Số lượng chuyến| D[Thu thập dữ liệu chuyến]
    C -->|Doanh thu| E[Thu thập dữ liệu giao dịch]
    C -->|Tỷ lệ hoàn thành| F[Thu thập dữ liệu trạng thái chuyến]
    C -->|Tỷ lệ hủy| G[Thu thập dữ liệu hủy chuyến]
    C -->|Hiệu quả tài xế| H[Thu thập dữ liệu tài xế]

    D --> I[Tổng hợp dữ liệu]
    E --> I
    F --> I
    G --> I
    H --> I

    I --> J[Phân tích dữ liệu]
    J --> K[Hiển thị báo cáo]
    K --> L([Kết thúc])
```
BP09 – Quản lý lỗi và ngoại lệ
```mermaid
flowchart TD
    A([Phát sinh lỗi]) --> B{Loại lỗi?}

    B -->|Không tìm được tài xế| C[Thông báo khách hàng]
    B -->|Tài xế từ chối| D[Tìm tài xế khác]
    B -->|Thanh toán thất bại| E[Thông báo khách hàng]
    B -->|Thông báo thất bại| F[Thử lại / chuyển kênh]
    B -->|Chuyến bị lỗi| G[Thông báo nhân viên vận hành]
    B -->|Mất kết nối| H[Xử lý theo chính sách mất kết nối]

    C --> I[Ghi nhận sự kiện]
    D --> I
    E --> I
    F --> I
    G --> J[Nhân viên vận hành xử lý]
    H --> I

    J --> I
    I --> K[Ghi audit log]
    K --> L([Kết thúc])
```
Bước 7: 


| **ID**    | **Functional Requirement**                                                                                                                                |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FR001** | Hệ thống phải cho phép khách hàng đăng ký tài khoản bằng các thông tin được yêu cầu.                                                                      |
| **FR002** | Hệ thống phải cho phép khách hàng đăng nhập và đăng xuất tài khoản.                                                                                       |
| **FR003** | Hệ thống phải cho phép khách hàng cập nhật thông tin cá nhân.                                                                                             |
| **FR004** | Hệ thống phải cho phép tài xế đăng ký tài khoản hoặc cho phép nhân viên vận hành tạo tài khoản tài xế.                                                    |
| **FR005** | Hệ thống phải cho phép tài xế cập nhật thông tin cá nhân và thông tin phương tiện.                                                                        |
| **FR006** | Hệ thống phải cho phép tài xế cập nhật trạng thái hoạt động, bao gồm sẵn sàng và không sẵn sàng nhận chuyến.                                              |
| **FR007** | Hệ thống phải cho phép khách hàng nhập điểm đón và điểm đến khi đặt xe.                                                                                   |
| **FR008** | Hệ thống phải cho phép khách hàng lựa chọn loại xe/dịch vụ trước khi gửi yêu cầu đặt xe.                                                                  |
| **FR009** | Hệ thống phải cho phép khách hàng gửi yêu cầu đặt xe.                                                                                                     |
| **FR010** | Hệ thống phải ghi nhận và quản lý trạng thái của yêu cầu đặt xe.                                                                                          |
| **FR011** | Hệ thống phải xác định các tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành được cấu hình.                                    |
| **FR012** | Hệ thống phải ưu tiên tài xế phù hợp và gần vị trí đón của khách hàng.                                                                                    |
| **FR013** | Hệ thống phải gửi thông báo yêu cầu chuyến đến tài xế phù hợp.                                                                                            |
| **FR014** | Hệ thống phải cho phép tài xế chấp nhận hoặc từ chối yêu cầu chuyến.                                                                                      |
| **FR015** | Hệ thống phải ghi nhận thời điểm và kết quả phản hồi của tài xế.                                                                                          |
| **FR016** | Hệ thống phải tự động tìm tài xế khác khi tài xế được đề xuất từ chối hoặc không phản hồi trong thời gian quy định.                                       |
| **FR017** | Hệ thống phải thông báo cho khách hàng khi không tìm được tài xế phù hợp.                                                                                 |
| **FR018** | Hệ thống phải xác nhận và cập nhật thông tin tài xế cho khách hàng sau khi tài xế nhận chuyến.                                                            |
| **FR019** | Hệ thống phải cho phép tài xế cập nhật trạng thái đã đến điểm đón.                                                                                        |
| **FR020** | Hệ thống phải cho phép tài xế cập nhật trạng thái đã đón khách.                                                                                           |
| **FR021** | Hệ thống phải cho phép tài xế cập nhật trạng thái đang di chuyển.                                                                                         |
| **FR022** | Hệ thống phải cho phép tài xế cập nhật trạng thái hoàn thành chuyến.                                                                                      |
| **FR023** | Hệ thống phải ghi nhận và cập nhật vị trí của tài xế trong quá trình hoạt động.                                                                           |
| **FR024** | Hệ thống phải cho phép khách hàng theo dõi trạng thái chuyến đi.                                                                                          |
| **FR025** | Hệ thống phải hiển thị thông tin tài xế và thời gian dự kiến tài xế đến cho khách hàng.                                                                   |
| **FR026** | Hệ thống phải lưu trữ lịch sử các chuyến đi của khách hàng.                                                                                               |
| **FR027** | Hệ thống phải xác định số tiền khách hàng phải thanh toán dựa trên loại dịch vụ và thông tin chuyến đi.                                                   |
| **FR028** | Hệ thống phải cho phép khách hàng lựa chọn phương thức thanh toán được hỗ trợ.                                                                            |
| **FR029** | Hệ thống phải gửi yêu cầu thanh toán điện tử đến nhà cung cấp thanh toán bên ngoài.                                                                       |
| **FR030** | Hệ thống phải tiếp nhận và lưu kết quả giao dịch thanh toán từ nhà cung cấp.                                                                              |
| **FR031** | Hệ thống phải thông báo cho khách hàng khi thanh toán điện tử thành công hoặc thất bại.                                                                   |
| **FR032** | Hệ thống phải cho phép xử lý lại giao dịch thanh toán thất bại theo chính sách của doanh nghiệp.                                                          |
| **FR033** | Hệ thống không được lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán.                                                                   |
| **FR034** | Hệ thống phải gửi thông báo khi yêu cầu đặt xe được tiếp nhận.                                                                                            |
| **FR035** | Hệ thống phải gửi thông báo khi tài xế nhận chuyến.                                                                                                       |
| **FR036** | Hệ thống phải gửi thông báo khi tài xế đến điểm đón.                                                                                                      |
| **FR037** | Hệ thống phải gửi thông báo khi chuyến đi hoàn thành.                                                                                                     |
| **FR038** | Hệ thống phải gửi thông báo về kết quả thanh toán.                                                                                                        |
| **FR039** | Hệ thống phải gửi thông báo cho tài xế về chuyến mới và các thay đổi liên quan đến chuyến đang thực hiện.                                                 |
| **FR040** | Hệ thống phải cho phép mở rộng và tích hợp thêm các kênh thông báo mới.                                                                                   |
| **FR041** | Hệ thống phải cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành.                                                                           |
| **FR042** | Hệ thống phải lưu trữ và quản lý kết quả đánh giá của khách hàng.                                                                                         |
| **FR043** | Hệ thống phải cung cấp giao diện quản trị cho nhân viên vận hành.                                                                                         |
| **FR044** | Hệ thống phải cho phép nhân viên vận hành tra cứu và quản lý thông tin khách hàng.                                                                        |
| **FR045** | Hệ thống phải cho phép nhân viên vận hành tra cứu và quản lý thông tin tài xế.                                                                            |
| **FR046** | Hệ thống phải cho phép nhân viên vận hành quản lý thông tin phương tiện.                                                                                  |
| **FR047** | Hệ thống phải cho phép nhân viên vận hành theo dõi các chuyến đang diễn ra.                                                                               |
| **FR048** | Hệ thống phải cho phép nhân viên vận hành kiểm tra trạng thái hoạt động của tài xế.                                                                       |
| **FR049** | Hệ thống phải hỗ trợ nhân viên vận hành xử lý các trường hợp chuyến đi bị lỗi hoặc bất thường.                                                            |
| **FR050** | Hệ thống phải cho phép nhân viên vận hành tra cứu lịch sử giao dịch.                                                                                      |
| **FR051** | Hệ thống phải kiểm soát quyền truy cập của nhân viên đối với các chức năng quản trị.                                                                      |
| **FR052** | Hệ thống phải ghi nhận nhật ký đối với các thao tác quản trị quan trọng.                                                                                  |
| **FR053** | Hệ thống phải cung cấp báo cáo về số lượng chuyến đi.                                                                                                     |
| **FR054** | Hệ thống phải cung cấp báo cáo về doanh thu.                                                                                                              |
| **FR055** | Hệ thống phải cung cấp báo cáo về tỷ lệ chuyến hoàn thành và tỷ lệ hủy.                                                                                   |
| **FR056** | Hệ thống phải cung cấp báo cáo về hiệu quả hoạt động của tài xế.                                                                                          |
| **FR057** | Hệ thống phải cho phép thêm các loại dịch vụ mới mà không phải xây dựng lại toàn bộ hệ thống.                                                             |
| **FR058** | Hệ thống phải cho phép tích hợp thêm phương thức thanh toán hoặc nhà cung cấp thanh toán mới.                                                             |
| **FR059** | Hệ thống phải cho phép các thành phần xử lý thanh toán, thông báo và đặt xe hoạt động độc lập để hạn chế ảnh hưởng dây chuyền khi một thành phần gặp lỗi. |
| **FR060** | Hệ thống phải hỗ trợ triển khai chức năng mới từng phần mà hạn chế ảnh hưởng đến các chức năng đang hoạt động.                                            |

Bước 8
Xác định Bussiness Rules:
| **ID**     | **Business Rule**                                                                                                                        |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **BRL001** | Chỉ khách hàng đã đăng nhập và được xác thực mới được phép tạo yêu cầu đặt xe.                                                           |
| **BRL002** | Chỉ tài xế có tài khoản hợp lệ, đang hoạt động và ở trạng thái sẵn sàng mới được xem xét để nhận chuyến.                                 |
| **BRL003** | Tài xế được lựa chọn phải đáp ứng các tiêu chí phù hợp về vị trí, trạng thái và loại phương tiện/dịch vụ.                                |
| **BRL004** | Hệ thống phải ưu tiên tài xế phù hợp và gần điểm đón của khách hàng theo tiêu chí vận hành đã được doanh nghiệp xác định.                |
| **BRL005** | Khi tài xế từ chối chuyến, hệ thống phải tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu.                           |
| **BRL006** | Khi tài xế không phản hồi trong thời gian quy định, hệ thống phải xem yêu cầu là không được chấp nhận và chuyển sang tìm tài xế khác.    |
| **BRL007** | Một chuyến chỉ được xác nhận khi có một tài xế chấp nhận chuyến thành công.                                                              |
| **BRL008** | Sau khi tài xế nhận chuyến, yêu cầu đó không được tiếp tục gửi đồng thời cho các tài xế khác.                                            |
| **BRL009** | Trạng thái chuyến phải được cập nhật theo trình tự nghiệp vụ phù hợp: đã nhận → tài xế đến → đã đón khách → đang di chuyển → hoàn thành. |
| **BRL010** | Chỉ tài xế được phân công cho chuyến mới được phép cập nhật trạng thái của chuyến đó.                                                    |
| **BRL011** | Thông tin vị trí của tài xế phải được ghi nhận để hỗ trợ tìm tài xế và dự kiến thời gian đến.                                            |
| **BRL012** | Cước chuyến đi phải được xác định dựa trên loại dịch vụ và thông tin chuyến đi theo chính sách tính cước của doanh nghiệp.               |
| **BRL013** | Khách hàng có thể thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử được hệ thống hỗ trợ.                                     |
| **BRL014** | Thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB.                                        |
| **BRL015** | Chỉ giao dịch được nhà cung cấp thanh toán xác nhận thành công mới được ghi nhận là thanh toán điện tử thành công.                       |
| **BRL016** | Khách hàng chỉ được đánh giá tài xế sau khi chuyến đi đã hoàn thành.                                                                     |
| **BRL017** | Nhân viên vận hành chỉ được thực hiện các chức năng quản trị phù hợp với quyền được cấp.                                                 |
| **BRL018** | Các thao tác quản trị quan trọng phải được lưu vết để phục vụ kiểm tra và xử lý sự cố.                                                   |
| **BRL019** | Khách hàng phải được thông báo về các sự kiện quan trọng của chuyến đi và kết quả thanh toán.                                            |
| **BRL020** | Khi một tài xế không nhận chuyến, hệ thống phải tiếp tục quá trình tìm kiếm cho đến khi tìm được tài xế hoặc không còn tài xế phù hợp.   |

Các Exception:
| **ID**    | **Exception**                                    | **Cách xử lý**                                                                                                                     |
| --------- | ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| **EX001** | **Tài xế không phản hồi**                        | Khi hết thời gian phản hồi quy định, hệ thống đánh dấu tài xế không nhận chuyến và tự động tìm tài xế phù hợp tiếp theo.           |
| **EX002** | **Tài xế từ chối chuyến**                        | Hệ thống ghi nhận việc từ chối và tiếp tục tìm tài xế khác mà không yêu cầu khách hàng đặt lại.                                    |
| **EX003** | **Không tìm được tài xế**                        | Hệ thống kết thúc quá trình tìm kiếm và thông báo rõ cho khách hàng rằng hiện không tìm được tài xế phù hợp.                       |
| **EX004** | **Không có tài xế đang sẵn sàng**                | Hệ thống thông báo cho khách hàng và ghi nhận yêu cầu không thể phân công tài xế.                                                  |
| **EX005** | **Thanh toán điện tử thất bại**                  | Hệ thống thông báo kết quả thất bại cho khách hàng và cho phép xử lý/thanh toán lại theo chính sách doanh nghiệp.                  |
| **EX006** | **Nhà cung cấp thanh toán không phản hồi**       | Hệ thống không tự động xác nhận thành công; ghi nhận giao dịch ở trạng thái phù hợp và xử lý lại theo cơ chế của doanh nghiệp.     |
| **EX007** | **Gửi thông báo thất bại**                       | Hệ thống ghi nhận lỗi và thực hiện cơ chế thử lại hoặc sử dụng kênh thông báo khác nếu được hỗ trợ.                                |
| **EX008** | **Mất kết nối mạng của tài xế**                  | Hệ thống ghi nhận trạng thái kết nối không ổn định và xử lý cập nhật vị trí/trạng thái theo chính sách được doanh nghiệp xác định. |
| **EX009** | **Mất kết nối của khách hàng**                   | Hệ thống vẫn duy trì trạng thái yêu cầu/chuyến trên phía server và đồng bộ lại thông tin khi khách hàng kết nối trở lại.           |
| **EX010** | **Tài xế hủy chuyến sau khi đã nhận**            | Hệ thống ghi nhận việc hủy và thực hiện quy trình tìm tài xế thay thế hoặc xử lý theo chính sách hủy chuyến.                       |
| **EX011** | **Khách hàng hủy chuyến**                        | Hệ thống kiểm tra trạng thái chuyến và áp dụng chính sách hủy chuyến tương ứng của doanh nghiệp.                                   |
| **EX012** | **Thông tin đặt xe không hợp lệ**                | Hệ thống thông báo lỗi và yêu cầu khách hàng chỉnh sửa thông tin trước khi gửi yêu cầu.                                            |
| **EX013** | **Tài xế không đáp ứng điều kiện nhận chuyến**   | Hệ thống loại tài xế khỏi danh sách phù hợp và tiếp tục tìm tài xế khác.                                                           |
| **EX014** | **Lỗi hệ thống tại một thành phần**              | Thành phần bị lỗi được xử lý độc lập, hạn chế ảnh hưởng đến các chức năng khác như đặt xe, theo dõi chuyến hoặc quản lý vận hành.  |
| **EX015** | **Người dùng không có quyền thực hiện thao tác** | Hệ thống từ chối thao tác và thông báo người dùng không có quyền truy cập chức năng đó.                                            |

Bước 9:

| **Thực thể**                                      | **Thuộc tính**                                                                                                                                                                                       |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Customer (Khách hàng)**                         | **CustomerID** (PK), FullName, PhoneNumber, Email, Password, Address, AccountStatus, CreatedAt, UpdatedAt                                                                                            |
| **Driver (Tài xế)**                               | **DriverID** (PK), FullName, PhoneNumber, Email, Password, DriverStatus, LicenseNumber, CreatedAt, UpdatedAt                                                                                         |
| **Vehicle (Phương tiện)**                         | **VehicleID** (PK), DriverID (FK), VehicleTypeID (FK), LicensePlate, Brand, Model, Color, VehicleStatus                                                                                              |
| **VehicleType (Loại xe)**                         | **VehicleTypeID** (PK), TypeName, Description, Capacity, BaseFare                                                                                                                                    |
| **Ride (Chuyến đi)**                              | **RideID** (PK), CustomerID (FK), DriverID (FK), VehicleTypeID (FK), PickupLocation, Destination, RequestTime, AcceptedTime, PickupTime, CompletedTime, RideStatus, EstimatedArrivalTime, FareAmount |
| **DriverLocation (Vị trí tài xế)**                | **LocationID** (PK), DriverID (FK), Latitude, Longitude, RecordedAt                                                                                                                                  |
| **RideStatusHistory (Lịch sử trạng thái chuyến)** | **StatusHistoryID** (PK), RideID (FK), Status, UpdatedBy, UpdatedAt                                                                                                                                  |
| **Payment (Thanh toán)**                          | **PaymentID** (PK), RideID (FK), PaymentMethod, Amount, PaymentStatus, TransactionReference, PaymentTime, RetryCount                                                                                 |
| **PaymentProvider (Nhà cung cấp thanh toán)**     | **ProviderID** (PK), ProviderName, ProviderStatus                                                                                                                                                    |
| **Notification (Thông báo)**                      | **NotificationID** (PK), RecipientID, RecipientType, RideID (FK), NotificationType, Message, Channel, NotificationStatus, SentAt                                                                     |
| **NotificationProvider (Nhà cung cấp thông báo)** | **NotificationProviderID** (PK), ProviderName, Channel, ProviderStatus                                                                                                                               |
| **Rating (Đánh giá)**                             | **RatingID** (PK), RideID (FK), CustomerID (FK), DriverID (FK), RatingScore, Comment, CreatedAt                                                                                                      |
| **Cancellation (Hủy chuyến)**                     | **CancellationID** (PK), RideID (FK), CancelledBy, CancellationReason, CancelledAt                                                                                                                   |
| **DriverAssignment (Phân công tài xế)**           | **AssignmentID** (PK), RideID (FK), DriverID (FK), AssignedAt, ResponseTime, ResponseStatus                                                                                                          |
| **Employee (Nhân viên vận hành)**                 | **EmployeeID** (PK), FullName, Email, Password, RoleID (FK), EmployeeStatus, CreatedAt                                                                                                               |
| **Role (Vai trò)**                                | **RoleID** (PK), RoleName, Description                                                                                                                                                               |
| **AuditLog (Nhật ký hệ thống)**                   | **LogID** (PK), EmployeeID (FK), Action, EntityType, EntityID, Timestamp, Description                                                                                                                |

Bước 10: Xác định Non-Bussiness Requirement

| **ID**     | **Non-Business Requirement**     | **Diễn giải**                                                                                                                                   |
| ---------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **NBR001** | **Hiệu năng**                    | Hệ thống phải có khả năng xử lý số lượng lớn yêu cầu đặt xe đồng thời mà không làm giảm đáng kể hiệu năng.                                      |
| **NBR002** | **Khả năng mở rộng**             | Hệ thống phải có khả năng mở rộng khi số lượng khách hàng, tài xế và chuyến đi tăng lên.                                                        |
| **NBR003** | **Khả năng mở rộng độc lập**     | Các thành phần như đặt xe, thanh toán và thông báo phải có khả năng mở rộng độc lập theo nhu cầu tải.                                           |
| **NBR004** | **Tính sẵn sàng**                | Hệ thống phải hoạt động ổn định, đặc biệt trong các thời điểm nhu cầu đặt xe tăng cao.                                                          |
| **NBR005** | **Khả năng chịu lỗi**            | Lỗi tại một thành phần như thanh toán hoặc thông báo không được làm toàn bộ hệ thống đặt xe ngừng hoạt động.                                    |
| **NBR006** | **Khả năng phục hồi**            | Hệ thống phải có khả năng phục hồi và tiếp tục hoạt động sau khi một thành phần hoặc dịch vụ gặp sự cố.                                         |
| **NBR007** | **Bảo mật**                      | Hệ thống phải bảo vệ thông tin cá nhân, thông tin phương tiện, dữ liệu vị trí và dữ liệu giao dịch khỏi truy cập trái phép.                     |
| **NBR008** | **Xác thực**                     | Người dùng phải được xác thực trước khi truy cập các chức năng yêu cầu tài khoản.                                                               |
| **NBR009** | **Phân quyền**                   | Hệ thống phải kiểm soát quyền truy cập dựa trên vai trò, đặc biệt đối với các chức năng quản trị và thao tác nhạy cảm.                          |
| **NBR010** | **Bảo vệ dữ liệu thanh toán**    | Hệ thống không được lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán.                                                         |
| **NBR011** | **Audit / Logging**              | Hệ thống phải lưu vết các thao tác quan trọng để phục vụ kiểm tra, điều tra sự cố và truy vết hoạt động.                                        |
| **NBR012** | **Toàn vẹn dữ liệu**             | Hệ thống phải đảm bảo dữ liệu chuyến đi, thanh toán, tài xế và khách hàng được lưu trữ chính xác và nhất quán.                                  |
| **NBR013** | **Khả năng tích hợp**            | Hệ thống phải có khả năng tích hợp với các nhà cung cấp thanh toán và dịch vụ thông báo bên ngoài.                                              |
| **NBR014** | **Khả năng thay thế thành phần** | Hệ thống phải cho phép thay đổi nhà cung cấp thanh toán, thông báo hoặc một số thành phần kỹ thuật mà không phải xây dựng lại toàn bộ hệ thống. |
| **NBR015** | **Khả năng mở rộng chức năng**   | Kiến trúc hệ thống phải hỗ trợ bổ sung loại dịch vụ, phương thức thanh toán và kênh thông báo mới trong tương lai.                              |
| **NBR016** | **Khả năng bảo trì**             | Hệ thống phải được thiết kế để các chức năng có thể được bảo trì hoặc cập nhật mà hạn chế ảnh hưởng đến các chức năng khác.                     |
| **NBR017** | **Triển khai từng phần**         | Các chức năng mới phải có khả năng được triển khai từng phần mà hạn chế ảnh hưởng đến hệ thống đang hoạt động.                                  |
| **NBR018** | **Khả năng giám sát**            | Hệ thống cần hỗ trợ theo dõi trạng thái hoạt động và phát hiện lỗi của các thành phần quan trọng.                                               |
| **NBR019** | **Khả năng tương thích**         | Hệ thống phải hỗ trợ các môi trường và thiết bị cần thiết để khách hàng, tài xế và nhân viên vận hành sử dụng các chức năng được cung cấp.      |
| **NBR020** | **Khả năng phục vụ tải cao**     | Hệ thống phải duy trì hoạt động khi nhu cầu đặt xe tăng đột biến, đặc biệt trong các thời điểm cao điểm.                                        |


Bước 11:
Vẽ UC

1. Use Case tổng quan
```mermaid
flowchart LR
    Customer([Khách hàng])
    Driver([Tài xế])
    Employee([Nhân viên vận hành])
    Manager([Quản lý / Ban giám đốc])
    Payment([Nhà cung cấp thanh toán])
    Notification([Nhà cung cấp thông báo])

    UC1((Quản lý tài khoản))
    UC2((Đặt xe))
    UC3((Theo dõi chuyến đi))
    UC4((Quản lý chuyến đi))
    UC5((Tìm và phân công tài xế))
    UC6((Tính cước))
    UC7((Thanh toán))
    UC8((Nhận thông báo))
    UC9((Đánh giá tài xế))
    UC10((Quản lý khách hàng))
    UC11((Quản lý tài xế))
    UC12((Quản lý phương tiện))
    UC13((Theo dõi vận hành))
    UC14((Xử lý sự cố))
    UC15((Tra cứu giao dịch))
    UC16((Xem báo cáo))
    UC17((Quản lý phân quyền))
    UC18((Lưu vết thao tác))

    Customer --- UC1
    Customer --- UC2
    Customer --- UC3
    Customer --- UC7
    Customer --- UC8
    Customer --- UC9

    Driver --- UC1
    Driver --- UC4
    Driver --- UC5
    Driver --- UC8

    Employee --- UC10
    Employee --- UC11
    Employee --- UC12
    Employee --- UC13
    Employee --- UC14
    Employee --- UC15
    Employee --- UC17
    Employee --- UC18

    Manager --- UC16

    UC7 --- Payment
    UC8 --- Notification
```

2. Use Case của Khách hàng
```mermaid
flowchart LR
    Customer([Khách hàng])

    UC1((Đăng ký tài khoản))
    UC2((Đăng nhập))
    UC3((Cập nhật thông tin cá nhân))
    UC4((Đặt xe))
    UC5((Theo dõi chuyến đi))
    UC6((Xem lịch sử chuyến đi))
    UC7((Xem cước chuyến đi))
    UC8((Thanh toán))
    UC9((Đánh giá tài xế))
    UC10((Nhận thông báo))

    Customer --- UC1
    Customer --- UC2
    Customer --- UC3
    Customer --- UC4
    Customer --- UC5
    Customer --- UC6
    Customer --- UC7
    Customer --- UC8
    Customer --- UC9
    Customer --- UC10
```

Đặc tả use case:
UC001 – Đăng ký tài khoản khách hàng

| **Thuộc tính**     | **Đặc tả**                                                                                                                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Use Case ID**    | UC001                                                                                                                                                                                                                          |
| **Tên**            | Đăng ký tài khoản khách hàng                                                                                                                                                                                                   |
| **Actor**          | Khách hàng                                                                                                                                                                                                                     |
| **Mục tiêu**       | Cho phép khách hàng tạo tài khoản để sử dụng các chức năng của hệ thống CAB.                                                                                                                                                   |
| **Tiền điều kiện** | Khách hàng chưa có tài khoản hợp lệ.                                                                                                                                                                                           |
| **Hậu điều kiện**  | Tài khoản khách hàng được tạo thành công và có thể đăng nhập.                                                                                                                                                                  |
| **Luồng chính**    | 1. Khách hàng chọn đăng ký.<br>2. Hệ thống hiển thị biểu mẫu đăng ký.<br>3. Khách hàng nhập thông tin cá nhân.<br>4. Hệ thống kiểm tra tính hợp lệ.<br>5. Hệ thống tạo tài khoản.<br>6. Hệ thống thông báo đăng ký thành công. |
| **Ngoại lệ**       | Nếu thông tin không hợp lệ → hệ thống thông báo lỗi và yêu cầu nhập lại.<br>Nếu email/số điện thoại đã tồn tại → hệ thống thông báo tài khoản đã tồn tại.                                                                      |

