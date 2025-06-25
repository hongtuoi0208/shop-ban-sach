![MyProject Banner](https://github.com/ca-xao-xa-ot/BookStore/blob/main/public/assets/images/myproject.jpeg?raw=true)
<h1>About me </h1>
<ul>
    <a href = '' ><li>Bùi Thị Hồng Tươi </li></a>
    <a href = '' ><li>Mã số sinh viên: 23015124</li></a>
    <a href = '' ><li>Thiết kế web nâng cao-1-3-24.TH3</li></a>
</ul>
<p>I'm from PHENIKAA UNIVERSITY</p>

# Shop-Ban-Sach-Laravel

# Sinh viên thực hiện
- **Họ và tên :** Bùi Thị Hồng Tươi
- **Mã số sinh viên :** 23015124
- **Lớp:** Thiết kế web nâng cao-1-3-24(TH3)

# Tên dự án : Shop bán sách

# Mô tả dự án
    -Là một trang web bán sách trực tuyến được xây dựng bằng Laravel.
    -Người dùng có thể đăng ký, đăng nhập, xem danh sách sách, tìm kiếm, thêm vào giỏ hàng và        đặt hàng.
    -Quản trị viên (Admin) có thể quản lý sách, danh mục, người dùng và đơn hàng.
    -Hệthống sử dụng các models chính như: User, Book, Cart, Order, Review, Category.
    -Hướng tới thiết kế MVC rõ ràng, dễ mở rộng trong tương lai.
    
# CHỨC NĂNG chính:
 ✔️ Đăng ký, xác thực email, đăng nhập, đặt lại mặt khẩu
 ✔️ Quản lý danh mục sách (Thêm/Sửa/Xóa) 
 ✔️ Tìm kiếm và lọc sách theo tiêu đề, tác giả 
 ✔️ Hệ thống giỏ hàng và thanh toán trực tuyến 
 ✔️ Quản lý tài khoản người dùng và đơn hàng 
 ✔️ Giao diện thân thiện, responsive với Bootstrap
 ✔️ Quản lý khách hàng, hóa đơn

# Ngôn ngữ sử dụng:
 HTML, CSS, JavaScript, PHP, Bootstrap, MySQL,.....
 
# Cấu trúc thư mục
admin: Chứa các tệp PHP liên quan đến phần quản trị trang web.
css: Chứa các tệp CSS để định dạng giao diện trang web.
images: Chứa các hình ảnh được sử dụng trong trang web.
js: Chứa các tệp JavaScript để thêm tính năng tương tác.
uploaded_img: Chứa các hình ảnh sản phẩm được tải lên.
Các tệp PHP

# Cơ sở dữ liệu

![184755435-bb97a62a-4cdd-408d-9a5a-526430f50c64](https://github.com/user-attachments/assets/fff39a10-bc56-4c9e-9d34-a77704503633)

# Dữ liệu mẫu

| Bảng             | Số lượng record mẫu |
| ---------------- | ------------------- |
| user             | 5                   |
| product          | 100                 |
| product_review   | 150                 |
| category         | 15                  |
| product_category | 100                 |
| cart             | 2                   |
| cart_item        | 5                   |
| orders           | 25                  |
| order_item       | 60                  |
| wishlist_item    | 30                  |

# Sơ đồ liên quan

![use-cases](https://github.com/user-attachments/assets/7f115c60-f294-479f-b130-1301c48d37f4)

# Sơ đồ class diagram

![class-diagram](https://github.com/user-attachments/assets/2ad9fc27-e928-4fbf-ad64-e7a2e54d8a04)

# Sơ đồ lớp UML

![Screenshot 2025-06-25 150746](https://github.com/user-attachments/assets/369a4323-5f1c-40da-8732-81d71fe58a12)

# Database Diagram
![68747470733a2f2f692e696d6775722e636f6d2f35326f513479782e6a7067](https://github.com/user-attachments/assets/0c82b505-389a-4d01-b2b7-ced86e824a65)

## Activity Diagram (Ví dụ: Đặt hàng - Place Order)
```mermaid
flowchart TD
    A[User] -->|Chon sach| B[Them vao gio hang]
    B --> C[Chuyen toi Gio hang]
    C --> D[Nhan Dat hang]
    D --> E[Nhap thong tin giao hang]
    E --> F[Xac nhan đon hang]
    F --> G[Luu đon hang vao CSDL]
    G --> H[Hien thi thong bao thanh cong]

```
## Activity Diagram (Ví dụ: Xoá sách - Admin)
```mermaid
flowchart TD
A[Admin] --> B[Click nút 'Xóa' sách]
B --> C[Hiện hộp thoại xác nhận]
C -->|Đồng ý| D[Xóa sách khỏi CSDL]
D --> E[Reload danh sách sách]
C -->|Hủy| F[Không làm gì cả]



```
## Class Diagram (Phiên bản rút gọn)
```mermaid
classDiagram
    class User {
        +user_id: int
        +name: string
        +email: string
        +password: string
        +register()
        +login()
    }

    class Book {
        +book_id: int
        +title: string
        +author: string
        +price: float
        +stock: int
        +description: string
        +category_id: int
    }

    class Cart {
        +cart_id: int
        +user_id: int
        +addItem(book_id: int, quantity: int)
        +removeItem(book_id: int)
    }

    class Order {
        +order_id: int
        +user_id: int
        +total_amount: float
        +status: string
        +createOrder()
    }

    class Category {
        +category_id: int
        +name: string
    }

    class Review {
        +review_id: int
        +user_id: int
        +book_id: int
        +rating: int
        +comment: string
    }

    User "1" --> "*" Order
    User "1" --> "1" Cart
    User "1" --> "*" Review
    Book "1" --> "*" Review
    Book "*" --> "1" Category
    Order "*" --> "*" Book : contains
```


































# Họ và tên: Đinh Nhật Tân
# Mã số sinh viên : 23013018
# Lớp: Thiết kế web nâng cao-1-3-24-TH4

# Tên dự án : Shop đồ chơi

# Giới thiệu về dự án:
 Website bán đồ chơi online giúp người dùng có thể xem, tìm kiếm, đặt mua các sản phẩm như mô hình, búp bê, lego,.....Người quản lý  có thể thêm/sửa/xóa sản phẩm, quản lý đơn hàng và danh mục đồ chơi. Laravel được sử dụng để tổ chức cấu trúc MVC rõ ràng, tích hợp các chức năng như xác thực người dùng, giỏ hàng, và thanh toán.






























