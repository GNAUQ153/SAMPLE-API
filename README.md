# SampleAPI - Minimal Web API with MongoDB

## Tổng quan
- Dự án này sử dụng framework ASP.NET để tạo một API đơn giản thực hiện các thao tác CRUD trên cơ sở dữ liệu MongoDB về cửa hàng sách (`BookStore`).
- Dự án này bao gồm các chức năng cơ bản, như thêm/ xóa/ sửa, truy xuất các thông tin về sách (`Book`).

## Cấu trúc dự án

### **Controllers**
- Chứa lớp `BooksController` để định nghĩa các API endpoints.
- Các phương thức chính:
  - `GET /api/books`: Lấy danh sách tất cả các sách.
  - `GET /api/books/{id}`: Lấy thông tin chi tiết của một sách theo ID.
  - `POST /api/books`: Thêm mới một sách vào cơ sở dữ liệu.
  - `PUT /api/books/{id}`: Cập nhật thông tin sách theo ID.
  - `DELETE /api/books/{id}`: Xóa một sách khỏi cơ sở dữ liệu.

### **Models**
- Gồm hai lớp chính:
  - **`Book`**:
    - Đại diện cho thông tin sách trong cơ sở dữ liệu.
    - Các thuộc tính:
      - `Id`: Định danh duy nhất của sách (do MongoDB tự động tạo).
      - `Name`: Tên sách.
      - `Price`: Giá sách.
      - `Category`: Thể loại sách.
      - `Author`: Tác giả.
  - **`BookStoreDatabaseSettings`**:
    - Chứa thông tin cấu hình kết nối MongoDB:
      - `ConnectionString`: Chuỗi kết nối MongoDB.
      - `DatabaseName`: Tên cơ sở dữ liệu.
      - `BooksCollectionName`: Tên bộ sưu tập trong cơ sở dữ liệu.

### **Services**
- Gồm lớp `BooksService` thực hiện các tác vụ tương tác với MongoDB.
- Các chức năng chính:
  - Truy xuất toàn bộ danh sách sách hoặc một sách cụ thể.
  - Thêm mới, cập nhật và xóa sách.
  - Sử dụng thư viện `MongoDB.Driver` để thao tác với cơ sở dữ liệu.

## Kết quả đạt được
- Tích hợp thành công MongoDB với ASP.NET Core.
- Phát triển một Web API tối giản với các thao tác CRUD.
- Có kinh nghiệm làm việc với dependency injection và Swagger.
