![image](https://github.com/user-attachments/assets/ca95a7bf-e1c7-46c4-8e62-283d6dca241c)

<h1>About me </h1>
<ul>
    <a href = '' ><li>Bùi Thị Hồng Tươi </li></a>
    <a href = '' ><li>Mã số sinh viên: 23015124</li></a>
    <a href = '' ><li>Thiết kế web nâng cao-1-3-24.TH3</li></a>
</ul>
<p>I'm from PHENIKAA UNIVERSITY</p>

# Tên dự án : Shop bán sách

# Mô tả dự án:
    -Là một trang web bán sách trực tuyến được xây dựng bằng Laravel.
    -Người dùng có thể đăng ký, đăng nhập, xem danh sách sách, tìm kiếm, thêm vào giỏ hàng và   đặt hàng.
    -Quản trị viên (Admin) có thể quản lý sách, danh mục, người dùng và đơn hàng.
    -Hệthống sử dụng các models chính như: User, Book, Cart, Order, Review, Category.
    -Hướng tới thiết kế MVC rõ ràng, dễ mở rộng trong tương lai.
    
# Chức năng chính:
 ✔️ Đăng ký, xác thực email, đăng nhập, đặt lại mặt khẩu
 ✔️ Quản lý danh mục sách (Thêm/Sửa/Xóa) 
 ✔️ Tìm kiếm và lọc sách theo tiêu đề, tác giả 
 ✔️ Hệ thống giỏ hàng và thanh toán trực tuyến 
 ✔️ Quản lý tài khoản người dùng và đơn hàng 
 ✔️ Giao diện thân thiện, responsive với Bootstrap
 ✔️ Quản lý khách hàng, hóa đơn

# Ngôn ngữ sử dụng:
 HTML, CSS, JavaScript, PHP, Bootstrap, MySQL,.....
 
# Cấu trúc thư mục:
admin: Chứa các tệp PHP liên quan đến phần quản trị trang web.
css: Chứa các tệp CSS để định dạng giao diện trang web.
images: Chứa các hình ảnh được sử dụng trong trang web.
js: Chứa các tệp JavaScript để thêm tính năng tương tác.
uploaded_img: Chứa các hình ảnh sản phẩm được tải lên.
Các tệp PHP

# Cơ sở dữ liệu:

![Screenshot 2025-06-25 150746](https://github.com/user-attachments/assets/369a4323-5f1c-40da-8732-81d71fe58a12) 
 
## Sơ đồ chức năng (Use case diagram):
![deepseek_mermaid_20250625_4990d2](https://github.com/user-attachments/assets/659d0057-974b-4137-9182-bec7d90bb13d)

## Activity Diagram (Ví dụ: Đặt hàng - Place Order):
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

## Link Readme (.io)



## Link Repo

https://github.com/hongtuoi0208/shop-ban-sach

## Module:

-**Composer**

{
    "$schema": "https://getcomposer.org/schema.json",
    "name": "laravel/laravel",
    "type": "project",
    "description": "The skeleton application for the Laravel framework.",
    "keywords": ["laravel", "framework"],
    "license": "MIT",
    "require": {
        "php": "^8.2",
        "laravel/framework": "^12.0",
        "laravel/tinker": "^2.10.1"
    },
    "require-dev": {
        "fakerphp/faker": "^1.23",
        "laravel/pail": "^1.2.2",
        "laravel/pint": "^1.13",
        "laravel/sail": "^1.41",
        "mockery/mockery": "^1.6",
        "nunomaduro/collision": "^8.6",
        "phpunit/phpunit": "^11.5.3"
    },
    "autoload": {
        "psr-4": {
            "App\\": "app/",
            "Database\\Factories\\": "database/factories/",
            "Database\\Seeders\\": "database/seeders/"
        }
    },
    "autoload-dev": {
        "psr-4": {
            "Tests\\": "tests/"
        }
    },
    "scripts": {
        "post-autoload-dump": [
            "Illuminate\\Foundation\\ComposerScripts::postAutoloadDump",
            "@php artisan package:discover --ansi"
        ],
        "post-update-cmd": [
            "@php artisan vendor:publish --tag=laravel-assets --ansi --force"
        ],
        "post-root-package-install": [
            "@php -r \"file_exists('.env') || copy('.env.example', '.env');\""
        ],
        "post-create-project-cmd": [
            "@php artisan key:generate --ansi",
            "@php -r \"file_exists('database/database.sqlite') || touch('database/database.sqlite');\"",
            "@php artisan migrate --graceful --ansi"
        ],
        "dev": [
            "Composer\\Config::disableProcessTimeout",
            "npx concurrently -c \"#93c5fd,#c4b5fd,#fb7185,#fdba74\" \"php artisan serve\" \"php artisan queue:listen --tries=1\" \"php artisan pail --timeout=0\" \"npm run dev\" --names=server,queue,logs,vite"
        ]
    },
    "extra": {
        "branch-alias": {
            "dev-master": "12.x-dev"
        },
        "laravel": {
            "dont-discover": []
        }
    },
    "config": {
        "optimize-autoloader": true,
        "preferred-install": "dist",
        "sort-packages": true,
        "allow-plugins": {
            "pestphp/pest-plugin": true,
            "php-http/discovery": true
        }
    },
    "minimum-stability": "dev",
    "prefer-stable": true
}


-**Database**:

<?php

namespace Database\Factories;

use Illuminate\Database\Eloquent\Factories\Factory;
use Illuminate\Support\Facades\Hash;
use Illuminate\Support\Str;

/**
 * @extends \Illuminate\Database\Eloquent\Factories\Factory<\App\Models\User>
 */
class UserFactory extends Factory
{
    /**
     * The current password being used by the factory.
     */
    protected static ?string $password;

    /**
     * Define the model's default state.
     *
     * @return array<string, mixed>
     */
    public function definition(): array
    {
        return [
            'name' => fake()->name(),
            'email' => fake()->unique()->safeEmail(),
            'email_verified_at' => now(),
            'password' => static::$password ??= Hash::make('password'),
            'remember_token' => Str::random(10),
        ];
    }

    /**
     * Indicate that the model's email address should be unverified.
     */
    public function unverified(): static
    {
        return $this->state(fn (array $attributes) => [
            'email_verified_at' => null,
        ]);
    }
}







































