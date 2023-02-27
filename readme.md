# **Chủ đề: Tạo Web đọc truyện chữ**
## I. Giới thiệu
### 1. Mục tiêu đề tài
- Crawl dữ liệu truyện từ một web truyện khác và tạo web đọc truyện từ dữ liệu đã được crawl
- Web cần đáp ứng các chức năng:
    + Thu thập dữ liệu truyện, lưu trữ vào Database
    + Liên kết Database với web truyện
    + Tạo chức năng search một truyện bất kì theo tên
### 2. Trang truyện crawl: <https://allnovel.net/>
### 3. Database
    Novel(#NID, Theme, Poster)
    Chapter(#CID, Content, Page)
    Novel_Chapter(#NID,#CID)
### 4. Công nghệ sử dụng
- Python: Ngôn ngữ dùng để crawl dữ liệu
- ExpressJS: Framework Nodejs, công cụ back-end chính của Project
- Handlebar, CSS, SCSS: công cụ front-end của Project
- Sqlite3: Hệ quản trị cơ sở dữ liệu, lưu trữ dữ liệu thu thập được
## II. Cấu trúc Thư mục
    C:/Users/PC/PROJECT-1
    ├───novel_content
    ├───Novel_Crawl_2
    │   ├───__pycache__
    │   ├───scrapper
    │       └───__pycache__
    └───Project-web
    │   ├───models
    │   ├───node_modules
    │   ├───src
    │   │   ├───app
    │   │   │   └───controllers
    │   │   ├───public
    │   │   │   └───css
    │   │   ├───resources
    │   │   │   ├───scss     
    │   │   │   └───views
    │   │   │   │   ├───layouts
    │   │   │   │   └───partials
    │   │   ├───routes
    │   │   └───utils
## III. Chi tiết từng thư mục
### 1. Novel_Crawl_2
- Thực hiện Crawl dữ liệu truyện và đưa vào database trong thư mục models
- Sử dụng thư viện Beautiful Soup để lấy dữ liệu ra từ file HTML
### 2. Project-web
#### a. Package models
- Thao tác và tạo Database theo yêu cầu với các câu lệnh SQL
#### b. Package src
- Là phần code chính để tạo trang web, liên kết với CSDL để trả đúng yêu cầu đặt ra
- Sử dụng mô hình MVC để thiết kế giao diện cho người dùng

    | Thư mục | Chức năng | 
    |:--------|:------:|
    | app  | Chứa các file controller  |  
    | public  |  Chứa các file static và được public  |  
    | resources | Chứa các file tạo ra giao diện trang web | 
    | routes | Chứa các đường dẫn của trang web | 
    | utils | Chứa các hàm xử lý, liên kết với dữ liệu trong database| 
#### c. Package novel_content
- Lưu trữ thông tin từng truyện được crawl
## IV. Tổng kết
### 1. Quá trình thực hiện
- Tiến độ thực hiện dự án:
    - Tuần 1 - 3: Thực hiện Crawl dữ liệu và đưa vào database
    - Tuần 3 - 10: Học HTML, CSS, JavaScript, NodeJS
    - Tuần 10 - 11: Thực hiện tạo Project, cấu trúc thư mục theo mô hình MVC
    - Tuần 12 - Hiện tại: Thực hiện làm tất cả các chức năng cho trang web
### 2. Kết quả đạt được
- Đã thực hiện được những nội dung đề ra
- Phát triển thêm chức năng Search Truyện theo tên
### 3. Chức năng phát triển thêm
Do thời gian có hạn nên em còn một vài chức năng chưa có thời gian làm như
- Học ReactJS để phần front-end được khoa học hơn
- Cải thiện thêm về phần front-end
- Thêm chức năng đánh dấu truyện đã truy cập và truy cập nhiều
- Dữ liệu được crawl mở rộng hơn, hiện tại mỗi truyện mới có 5 chương đầu 
