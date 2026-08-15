#LeTienDat_241230697
# QUẢN LÝ SINH VIÊN

## 1. Giới thiệu

**Quản lý sinh viên** là chương trình Console được xây dựng bằng **C#**, sử dụng danh sách `List<SinhVien>` để lưu trữ và quản lý thông tin sinh viên.

Chương trình cung cấp các chức năng cơ bản của một hệ thống quản lý sinh viên như:

* Nhập thông tin sinh viên.
* Hiển thị danh sách sinh viên.
* Tìm kiếm sinh viên theo mã.
* Tìm kiếm sinh viên gần đúng theo tên.
* Cập nhật thông tin sinh viên.
* Xóa sinh viên theo mã.
* Sắp xếp sinh viên theo họ tên.
* Sắp xếp sinh viên theo điểm trung bình.
* Hiển thị sinh viên có điểm trung bình từ 8 trở lên.
* Tìm sinh viên có điểm trung bình cao nhất.
* Tính điểm trung bình của toàn bộ sinh viên.
* Thống kê sinh viên theo ngành học.
* Thống kê sinh viên theo trạng thái.
* Thoát chương trình.

---

## 2. Mục tiêu của dự án

Dự án được thực hiện nhằm:

* Làm quen với ngôn ngữ lập trình **C#**.
* Thực hành xây dựng chương trình Console.
* Làm quen với **class** và **object** trong C#.
* Thực hành sử dụng **List<T>** để lưu trữ dữ liệu.
* Thực hành các thao tác thêm, sửa, xóa và tìm kiếm dữ liệu.
* Thực hành sắp xếp và thống kê dữ liệu.
* Rèn luyện tư duy lập trình thông qua việc xây dựng chương trình quản lý thực tế.

---

## 3. Công nghệ sử dụng

| Công nghệ           | Mô tả                                    |
| ------------------- | ---------------------------------------- |
| C#                  | Ngôn ngữ lập trình chính                 |
| .NET                | Nền tảng chạy chương trình               |
| Console Application | Giao diện chương trình                   |
| `List<SinhVien>`    | Cấu trúc dữ liệu lưu danh sách sinh viên |
| `DateTime`          | Lưu trữ ngày sinh                        |

---

## 4. Cấu trúc dự án

```text
LtdLesson01/
│
├── Program.cs
├── Menu.cs
├── SinhVien.cs
└── README.md
```

### `SinhVien.cs`

Đây là lớp mô tả đối tượng sinh viên.

Các thuộc tính của lớp `SinhVien` gồm:

| Thuộc tính  | Kiểu dữ liệu | Ý nghĩa              |
| ----------- | ------------ | -------------------- |
| `maSV`      | `string`     | Mã sinh viên         |
| `hoTen`     | `string`     | Họ và tên            |
| `ngaySinh`  | `DateTime`   | Ngày sinh            |
| `gioiTinh`  | `bool`       | Giới tính            |
| `eMail`     | `string`     | Địa chỉ email        |
| `sDT`       | `string`     | Số điện thoại        |
| `nganhHoc`  | `string`     | Ngành học            |
| `dTB`       | `float`      | Điểm trung bình      |
| `trangThai` | `bool`       | Trạng thái sinh viên |

Các thuộc tính này được khai báo trong lớp `SinhVien` và sử dụng property với `get`/`set`.

### `Menu.cs`

Đây là file chứa hàm `Main()` và menu điều khiển chương trình.

Chương trình tạo một danh sách:

```csharp
List<SinhVien> students = new List<SinhVien>();
```

Sau đó sử dụng vòng lặp `do...while` kết hợp với `switch` để xử lý lựa chọn của người dùng.

### `Program.cs`

File này chứa các hàm xử lý nghiệp vụ của chương trình, được gọi từ menu.

---

## 5. Các chức năng chính

### 5.1. Nhập thông tin sinh viên

Cho phép người dùng nhập và thêm một sinh viên mới vào danh sách.

Chức năng được gọi thông qua:

```text
1. Nhập thông tin sinh viên
```

---

### 5.2. Hiển thị thông tin sinh viên

Hiển thị thông tin của các sinh viên hiện có trong danh sách.

```text
2. Hiển thị thông tin sinh viên
```

---

### 5.3. Tìm sinh viên theo mã

Cho phép tìm kiếm chính xác một sinh viên dựa trên mã sinh viên.

```text
3. Tìm sinh viên theo mã
```

---

### 5.4. Tìm gần đúng theo tên

Cho phép tìm kiếm sinh viên dựa trên tên được nhập vào.

Chức năng hỗ trợ tìm kiếm gần đúng thay vì yêu cầu nhập chính xác toàn bộ họ tên.

```text
4. Tìm gần đúng theo tên
```

---

### 5.5. Cập nhật thông tin sinh viên

Cho phép tìm sinh viên và cập nhật lại thông tin của sinh viên đó.

```text
5. Cập nhật thông tin sinh viên
```

---

### 5.6. Xóa sinh viên

Cho phép xóa sinh viên dựa trên mã sinh viên.

```text
6. Xóa sinh viên theo mã
```

---

### 5.7. Sắp xếp theo họ tên

Sắp xếp danh sách sinh viên theo họ tên.

```text
7. Sắp xếp theo họ tên
```

---

### 5.8. Sắp xếp theo điểm trung bình

Sắp xếp danh sách sinh viên dựa trên điểm trung bình.

```text
8. Sắp xếp theo điểm trung bình
```

---

### 5.9. Hiển thị sinh viên có điểm từ 8 trở lên

Lọc danh sách và hiển thị những sinh viên có điểm trung bình **từ 8 trở lên**.

```text
9. Hiển thị sinh viên có điểm từ 8 trở lên
```

---

### 5.10. Tìm sinh viên có điểm cao nhất

Tìm và hiển thị sinh viên có điểm trung bình cao nhất trong danh sách.

```text
10. Hiển thị sinh viên có điểm cao nhất
```

---

### 5.11. Tính điểm trung bình toàn bộ sinh viên

Tính điểm trung bình dựa trên điểm trung bình của các sinh viên trong danh sách.

```text
11. Điểm trung bình toàn bộ sinh viên
```

---

### 5.12. Thống kê sinh viên theo ngành

Thống kê số lượng sinh viên dựa trên ngành học.

```text
12. Thống kê sinh viên theo ngành
```

---

### 5.13. Thống kê sinh viên theo trạng thái

Thống kê sinh viên dựa trên trạng thái được lưu trong thuộc tính `trangThai`.

```text
13. Thống kê sinh viên theo trạng thái
```

---

### 5.14. Thoát chương trình

Kết thúc chương trình.

```text
14. Thoát
```

Menu hiện tại của chương trình được tổ chức từ lựa chọn 1 đến 14 như trên.

---

## 6. Menu chương trình

Khi chạy chương trình, người dùng sẽ thấy menu:

```text
==== MENU ====
1. Nhập thông tin sinh viên
2. Hiển thị thông tin sinh viên
3. Tìm sinh viên theo mã
4. Tìm gần đúng theo tên
5. Cập nhật thông tin sinh viên
6. Xóa sinh viên theo mã
7. Sắp xếp theo họ tên
8. Sắp xếp theo điểm trung bình
9. Hiển thị sinh viên có điểm từ 8 trở lên.
10. Hiển thị sinh viên có điểm cao nhất.
11. Điểm trung bình toàn bộ sinh viên.
12. Thống kê sinh viên theo ngành.
13. Thống kê sinh viên theo trạng thái.
14. Thoát
```

## Người dùng nhập số tương ứng với chức năng muốn thực hiện. Chương trình tiếp tục chạy cho đến khi người dùng chọn `14`.

## 7. Dữ liệu mẫu

Chương trình hiện có dữ liệu sinh viên mẫu được khởi tạo ban đầu.

Ví dụ:

```text
Mã sinh viên: SV001
Họ tên: Nguyen Van A
Ngày sinh: 01/01/2000
Giới tính: true
Email: nguyenvana@example.com
Số điện thoại: 0123456789
Ngành học: CNTT
Điểm trung bình: 8.5
Trạng thái: true
```

và:

```text
Mã sinh viên: SV002
Họ tên: Tran Thi B
Ngày sinh: 02/02/2001
Giới tính: false
Email: Chungtrinhj@gmaii.com
Số điện thoại: 0987654321
Ngành học: Kinh te
Điểm trung bình: 7.2
Trạng thái: true
```

Các dữ liệu mẫu này được khởi tạo trực tiếp trong danh sách `students` trong chương trình.

---

## 8. Cách chạy chương trình

### Bước 1: Mở project

Mở project `LtdLesson01` bằng môi trường phát triển hỗ trợ C#/.NET.

### Bước 2: Kiểm tra các file

Đảm bảo project có các file:

```text
Program.cs
Menu.cs
SinhVien.cs
```

### Bước 3: Build project

Thực hiện Build để kiểm tra chương trình có lỗi biên dịch hay không.

### Bước 4: Chạy chương trình

Chạy project bằng nút **Run/Start** hoặc phím tắt tương ứng với môi trường phát triển đang sử dụng.

### Bước 5: Sử dụng menu

Nhập số từ `1` đến `14` để lựa chọn chức năng.

Ví dụ:

```text
Nhập lựa chọn của bạn: 2
```

Chương trình sẽ thực hiện chức năng hiển thị thông tin sinh viên.

---

## 9. Luồng hoạt động của chương trình

```text
Bắt đầu
   │
   ▼
Khởi tạo danh sách sinh viên
   │
   ▼
Hiển thị MENU
   │
   ▼
Nhập lựa chọn
   │
   ▼
Xử lý lựa chọn bằng switch
   │
   ├── 1 → Thêm sinh viên
   ├── 2 → Hiển thị sinh viên
   ├── 3 → Tìm theo mã
   ├── 4 → Tìm gần đúng theo tên
   ├── 5 → Cập nhật sinh viên
   ├── 6 → Xóa sinh viên
   ├── 7 → Sắp xếp theo họ tên
   ├── 8 → Sắp xếp theo điểm
   ├── 9 → Lọc sinh viên có điểm >= 8
   ├── 10 → Tìm điểm cao nhất
   ├── 11 → Tính điểm trung bình
   ├── 12 → Thống kê theo ngành
   ├── 13 → Thống kê theo trạng thái
   └── 14 → Thoát
   │
   ▼
Quay lại MENU
   │
   └── Nếu lựa chọn != 14
           │
           └──────► Tiếp tục
```

---

## 10. Kiến thức C# được áp dụng

Trong dự án có sử dụng các kiến thức cơ bản của C# như:

* Namespace.
* Class.
* Property.
* Object.
* `List<T>`.
* `DateTime`.
* Kiểu dữ liệu `string`, `bool`, `float`.
* Vòng lặp `do...while`.
* Cấu trúc điều kiện `switch...case`.
* Hàm/phương thức.
* Tham số truyền vào phương thức.
* Khởi tạo object bằng object initializer.

Ví dụ khởi tạo đối tượng:

```csharp
new SinhVien
{
    maSV = "SV001",
    hoTen = "Nguyen Van A",
    ngaySinh = new DateTime(2000, 1, 1),
    gioiTinh = true,
    eMail = "nguyenvana@example.com",
    sDT = "0123456789",
    nganhHoc = "CNTT",
    dTB = 8.5f,
    trangThai = true
};
```

---

## 11. Cấu trúc dữ liệu

Danh sách sinh viên được lưu bằng:

```csharp
List<SinhVien> students
```

Trong đó:

* `List` là danh sách có thể thay đổi kích thước.
* `SinhVien` là kiểu dữ liệu của từng phần tử.
* `students` là biến chứa danh sách sinh viên.

Cách tổ chức này cho phép chương trình dễ dàng thêm, xóa, tìm kiếm và sắp xếp các đối tượng sinh viên.

---

## 12. Xử lý lựa chọn người dùng

Chương trình sử dụng `switch` để kiểm tra lựa chọn được nhập từ bàn phím.

Ví dụ:

```csharp
switch (choice)
{
    case "1":
        ThemSinhVien(students);
        break;

    case "2":
        HienThi(students);
        break;

    case "3":
        TimTheoMa(students);
        break;

    // ...

    case "14":
        Console.WriteLine("Thoát chương trình.");
        break;

    default:
        Console.WriteLine("Lựa chọn không hợp lệ. Vui lòng chọn lại.");
        break;
}
```

Nếu người dùng nhập lựa chọn không nằm trong menu, chương trình thông báo lựa chọn không hợp lệ và cho phép chọn lại.

---

## 13. Ưu điểm

* Giao diện Console đơn giản, dễ sử dụng.
* Menu rõ ràng.
* Có nhiều chức năng quản lý sinh viên.
* Sử dụng `List<SinhVien>` phù hợp với bài toán.
* Có chức năng tìm kiếm, sắp xếp và thống kê.
* Chương trình được chia thành lớp `SinhVien` và các phương thức xử lý, giúp dễ quản lý code.

---

## 14. Hạn chế

Phiên bản hiện tại là chương trình Console và dữ liệu được lưu trong bộ nhớ khi chương trình chạy.

Khi chương trình kết thúc, dữ liệu được nhập trong quá trình chạy không được lưu vào cơ sở dữ liệu hoặc file bên ngoài.

Ngoài ra, một số thông tin trong chương trình hiện đang sử dụng kiểu `bool` cho giới tính và trạng thái nên cách hiển thị phụ thuộc vào phần xử lý trong các phương thức.

---

## 15. Hướng phát triển

Trong tương lai có thể mở rộng dự án bằng cách:

* Lưu dữ liệu sinh viên vào file `.txt`, `.json` hoặc cơ sở dữ liệu.
* Thêm chức năng nhập/xuất danh sách sinh viên.
* Kiểm tra dữ liệu đầu vào.
* Kiểm tra mã sinh viên bị trùng.
* Cải thiện cách hiển thị giới tính và trạng thái.
* Thêm chức năng phân loại sinh viên theo học lực.
* Thêm chức năng lọc sinh viên theo ngành.
* Thêm nhiều tiêu chí tìm kiếm.
* Xây dựng giao diện Windows Forms hoặc WPF.
* Kết nối cơ sở dữ liệu SQL Server.

---

## 16. Tác giả

**Dự án:** Quản lý sinh viên
**Ngôn ngữ:** C#
**Loại ứng dụng:** Console Application
**Namespace:** `LtdLesson01`

---

## 17. Kết luận

Dự án là một chương trình quản lý sinh viên cơ bản được xây dựng bằng C#. Thông qua dự án, người học có thể thực hành các kiến thức quan trọng về lập trình C# như class, object, property, danh sách `List<T>`, vòng lặp, `switch`, tìm kiếm, sắp xếp và thống kê dữ liệu.

Đây là nền tảng để tiếp tục phát triển các chương trình quản lý có quy mô lớn hơn và áp dụng thêm cơ sở dữ liệu hoặc giao diện đồ họa trong các bài tập, dự án tiếp theo.
