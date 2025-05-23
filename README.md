# Shaparak Identity Encryption - Golang

 **رمزنگاری اطلاعات هویتی دارنده کارت ((تطبیق کارت با کد ملی))**  
بر اساس پروتکل شاپرک، پیاده‌سازی شده با زبان برنامه‌نویسی Go (Golang)

---

##  درباره پروژه

این پروژه یک ابزار ساده‌ی رمزنگاری برای داده‌های هویتی (کد ملی و ...) است که مطابق با الگوریتم **AES-128 CBC با Padding نوع PKCS7** پیاده‌سازی شده است.

> شاپرک به شما یک مقدار `Key` و یک مقدار `IV` به صورت **Base64** ارسال می‌کند.  
> شما باید این مقادیر را ابتدا با استفاده از الگوریتم Base64 **decode** کرده،  
> و سپس برای رمزنگاری رشته اطلاعاتی از آن استفاده کنید.

خروجی به صورت Base64 ارائه می‌شود و می‌تواند در پیاده سازی درگاه پرداخت خود استفاده شود.


نکته: این پروژه برای انکریپت کد ملی افراد حقیقی جهت پرداخت بر روی درگاه های پرداخت با صنف خاص تعبیه شده است

---

##  ورودی‌ها

برنامه از کاربر ۳ ورودی به صورت CLI دریافت می‌کند:

1. **IV** (به صورت Base64، طول ۱۶ بایت)
2. **Key** (به صورت Base64، طول ۱۶ بایت)
3. **کد ملی** (عدد ۱۰ رقمی)

---

##  روش اجرا

### 1. دریافت پروژه

```bash
git clone https://github.com/mahdifj/shaparak-identity-encryption-golang.git
cd shaparak-identity-encryption-golang
