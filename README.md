![image](https://github.com/user-attachments/assets/ca95a7bf-e1c7-46c4-8e62-283d6dca241c)

<h1>About me </h1>
<ul>
    <a href = '' ><li>Bùi Thị Hồng Tươi </li></a>
    <a href = '' ><li>Mã số sinh viên: 23015124</li></a>
    <a href = '' ><li>Thiết kế web nâng cao-1-3-24.TH3</li></a>
</ul>
<p>I'm from PHENIKAA UNIVERSITY</p>

# Tên dự án : Shop bán sách

# Mô tả dự án
    -Là một trang web bán sách trực tuyến được xây dựng bằng Laravel.
    -Người dùng có thể đăng ký, đăng nhập, xem danh sách sách, tìm kiếm, thêm vào giỏ hàng và   đặt hàng.
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

# Sơ đồ liên quan

![use-cases](https://github.com/user-attachments/assets/7f115c60-f294-479f-b130-1301c48d37f4)

# Sơ đồ class diagram

![class-diagram](https://github.com/user-attachments/assets/2ad9fc27-e928-4fbf-ad64-e7a2e54d8a04)

# Sơ đồ UML

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
## Class Diagram 
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
## Sơ đồ thuật toán

![deepseek_mermaid_20250625_694871](https://github.com/user-attachments/assets/89409eb6-dcd6-45f7-b76b-89b5c3566dbb)
 
## Sơ đồ chức năng (Use case diagram)
![deepseek_mermaid_20250625_4990d2](https://github.com/user-attachments/assets/659d0057-974b-4137-9182-bec7d90bb13d)
































![image](https://github.com/user-attachments/assets/a6fb7a36-40ee-48cc-b5f3-f127d72741a4)

<ul>
    <a href = '' ><li>Đinh Nhật Tân </li></a>
    <a href = '' ><li>Mã số sinh viên: 23013018</li></a>
    <a href = '' ><li>Thiết kế web nâng cao-1-3-24.TH4</li></a>
</ul>

# Tên dự án : Shop đồ chơi

# Giới thiệu về dự án:
 Website bán đồ chơi online giúp người dùng có thể xem, tìm kiếm, đặt mua các sản phẩm như mô hình, búp bê, lego,.....Người quản lý  có thể thêm/sửa/xóa sản phẩm, quản lý đơn hàng và danh mục đồ chơi. Laravel được sử dụng để tổ chức cấu trúc MVC rõ ràng, tích hợp các chức năng như xác thực người dùng, giỏ hàng, và thanh toán.

# Sơ đồ lớp (Class Diagram)

![deepseek_mermaid_20250625_34294a](https://github.com/user-attachments/assets/46473358-3fcf-4f44-832a-53fa912cdcf2)

# Activity Diagram

![deepseek_mermaid_20250625_34294a](https://github.com/user-attachments/assets/18fa2c2f-c944-4199-9b2e-d637838d487e)

# Sơ đồ thuật toán
![deepseek_mermaid_20250625_694871](https://github.com/user-attachments/assets/3f2edb23-a91d-4122-b1c3-a740e768fa23)

# Sơ đồ chức năng (Use case Diagram)














