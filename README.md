Hướng dẫn sử dụng dự án Blazor

1. Tạo và chạy dự án Blazor:

dotnet new blazorserver -o DemoASP_NET
cd DemoASP_NET
dotnet run

dotnet new blazorserver: Tạo dự án Blazor Server.

-o DemoASP_NET: Đặt tên thư mục là DemoASP_NET.

dotnet run: Chạy ứng dụng.

2. Xem trực tiếp thay đổi khi code:

dotnet watch run

Lệnh này sẽ tự động reload khi bạn chỉnh sửa mã nguồn.

3. Liệt kê các mẫu dự án có sẵn:

dotnet new list

4. Tạo một dự án MVC:

dotnet new mvc -o MyMvcApp
cd MyMvcApp
dotnet run

5. Hướng dẫn sử dụng trong VS Code:

Cài đặt môi trường:

Cài đặt .NET SDK: Tải từ dotnet.microsoft.com.

Cài đặt VS Code: Tải từ code.visualstudio.com.

Cài đặt extension "C#":

Mở VS Code → Extensions (Ctrl + Shift + X).

Tìm "C#" → Cài đặt.

Mở dự án trong VS Code:

code .

Chạy và debug trong VS Code:

Mở Run & Debug (Ctrl + Shift + D).

Chọn .NET Core Launch (web) nếu là Blazor hoặc MVC.

Nhấn Start Debugging (F5).

