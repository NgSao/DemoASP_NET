# Hướng dẫn sử dụng dự án Blazor

## 1. Tạo và chạy dự án Blazor:
```sh
dotnet new blazorserver -o DemoASP_NET
cd DemoASP_NET
dotnet run
```
- `dotnet new blazorserver`: Tạo dự án Blazor Server.
- `-o DemoASP_NET`: Đặt tên thư mục là DemoASP_NET.
- `dotnet run`: Chạy ứng dụng.

## 2. Xem trực tiếp thay đổi khi code:
```sh
dotnet watch run
```
Lệnh này sẽ tự động reload khi bạn chỉnh sửa mã nguồn.

## 3. Liệt kê các mẫu dự án có sẵn:
```sh
dotnet new list
```

## 4. Tạo một dự án MVC:
```sh
dotnet new mvc -o MyMvcApp
cd MyMvcApp
dotnet run
```

## 5. Hướng dẫn sử dụng trong VS Code:
### Cài đặt môi trường:
- **Cài đặt .NET SDK**: Tải từ [dotnet.microsoft.com](https://dotnet.microsoft.com).
- **Cài đặt VS Code**: Tải từ [code.visualstudio.com](https://code.visualstudio.com).
- **Cài đặt extension "C#"**:
  - Mở VS Code → Extensions (Ctrl + Shift + X).
  - Tìm "C#" → Cài đặt.

### Mở dự án trong VS Code:
```sh
code .
```

### Chạy và debug trong VS Code:
1. Mở **Run & Debug** (Ctrl + Shift + D).
2. Chọn **.NET Core Launch (web)** nếu là Blazor hoặc MVC.
3. Nhấn **Start Debugging (F5)**.

