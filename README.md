# SnappPay.Client

A .NET client library for integrating with **SnappPay** payment gateway.

-   GitHub Repository:
    [SnappPay.Client](https://github.com/kavehnorozi/SnappPay.Client)
-   Project Page: [webecco.com/snapppay](https://webecco.com/snapppay)

------------------------------------------------------------------------

## 📦 Installation

You can install the package from **NuGet** (after publishing):

``` bash
dotnet add package SnappPay.Client
```

Or via **Package Manager Console**:

``` powershell
Install-Package SnappPay.Client
```

------------------------------------------------------------------------

## 🚀 Usage

``` csharp
using SnappPay.Client;
using SnappPay.Client.Models;

var service = new SnappPayService(
    baseUrl: "https://api.snappay.ir",
    clientId: "your-client-id",
    clientSecret: "your-client-secret",
    username: "your-username",
    password: "your-password"
);

// Authenticate
string token = await service.AuthenticateAsync();

// Get Payment Token
var paymentTokenResponse = await service.GetPaymentTokenAsync(token, new PaymentTokenRequest
{
    amount = 100000,
    mobile = "09123456789",
    cartList = new List<CartItem> { new CartItem { name = "Product 1", price = 100000 } }
});
```

------------------------------------------------------------------------

## 📖 Features

-   Authentication (OAuth2)
-   Check eligibility
-   Request payment token
-   Update payment
-   Verify / Settle / Revert / Cancel
-   Get transaction status

------------------------------------------------------------------------

## 🔒 Security

This library follows best practices for API consumption.\
Credentials are passed via constructor and **not hardcoded**.

------------------------------------------------------------------------

## 🤝 Contributing

Feel free to fork the project, open issues, or create pull requests.

------------------------------------------------------------------------

## 👨‍💻 Author

**Kaveh Norouzi**\
📱 +98 912 342 0138\
🌐 [webecco.com/snapppay](https://webecco.com/snapppay)

------------------------------------------------------------------------

## 📄 License

This project is licensed under the MIT License - see the
[LICENSE](LICENSE) file for details.

------------------------------------------------------------------------

# SnappPay.Client (نسخه فارسی)

کتابخانه‌ی دات‌نت برای اتصال به درگاه پرداخت **SnappPay**

-   ریپازیتوری گیت‌هاب:
    [SnappPay.Client](https://github.com/kavehnorozi/SnappPay.Client)
-   صفحه معرفی پروژه:
    [webecco.com/snapppay](https://webecco.com/snapppay)

------------------------------------------------------------------------

## 📦 نصب

نصب از طریق **NuGet** (بعد از انتشار):

``` bash
dotnet add package SnappPay.Client
```

یا از طریق **Package Manager Console**:

``` powershell
Install-Package SnappPay.Client
```

------------------------------------------------------------------------

## 🚀 استفاده

``` csharp
using SnappPay.Client;
using SnappPay.Client.Models;

var service = new SnappPayService(
    baseUrl: "https://api.snappay.ir",
    clientId: "client-id-شما",
    clientSecret: "client-secret-شما",
    username: "نام‌کاربری",
    password: "رمزعبور"
);

// دریافت توکن
string token = await service.AuthenticateAsync();

// گرفتن توکن پرداخت
var paymentTokenResponse = await service.GetPaymentTokenAsync(token, new PaymentTokenRequest
{
    amount = 100000,
    mobile = "09123456789",
    cartList = new List<CartItem> { new CartItem { name = "محصول ۱", price = 100000 } }
});
```

------------------------------------------------------------------------

## 📖 امکانات

-   احراز هویت (OAuth2)
-   بررسی امکان‌پذیری پرداخت
-   درخواست توکن پرداخت
-   بروزرسانی پرداخت
-   تایید / تسویه / بازگشت / لغو
-   دریافت وضعیت تراکنش

------------------------------------------------------------------------

## 🔒 امنیت

این لایبرری از اصول استاندارد برای مصرف API پیروی می‌کند.\
اطلاعات حساس از طریق سازنده (constructor) ارسال می‌شوند و در کد
**hardcode نشده‌اند**.

------------------------------------------------------------------------

## 👨‍💻 سازنده

**کاوه نوروزی**\
📱 +989123420138\
🌐 [webecco.com/snapppay](https://webecco.com/snapppay)

------------------------------------------------------------------------

## 📄 مجوز

این پروژه تحت مجوز MIT منتشر شده است. برای اطلاعات بیشتر به فایل
[LICENSE](LICENSE) مراجعه کنید.
