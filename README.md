# Hướng dẫn sử dụng dự án trong VSCode


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


# Hướng dẫn sử dụng dự án trong VSCode
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



------
dotnet add package Microsoft.EntityFrameworkCore --version 8.0.13
dotnet add package Microsoft.EntityFrameworkCore.Design --version 8.0.13
dotnet add package Microsoft.EntityFrameworkCore.Relational --version 8.0.13

Program.cs
-----

using Demo_ASPNet.Data;
using Microsoft.EntityFrameworkCore;

var builder = WebApplication.CreateBuilder(args);


// Đăng ký DbContext kết nối MySQL
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseMySql(
        builder.Configuration.GetConnectionString("MySqlConnection"),
        ServerVersion.AutoDetect(builder.Configuration.GetConnectionString("MySqlConnection"))
    ));

builder.Services.AddControllersWithViews();
var app = builder.Build();
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Home/Error");
    // The default HSTS value is 30 days. You may want to change this for production scenarios, see https://aka.ms/aspnetcore-hsts.
    app.UseHsts();
}

app.UseHttpsRedirection();
app.UseStaticFiles();
app.UseRouting();
app.UseAuthorization();
app.MapControllers();


// Route cho ProductController
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Product}/{action=Index}/{id?}");

// Route mặc định cho các controller khác
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");

app.Run();



-----
appsting.json
  "ConnectionStrings": {
    "MySqlConnection": "server=localhost;database=MyAspNetDb;user=root;password=root"
  },

