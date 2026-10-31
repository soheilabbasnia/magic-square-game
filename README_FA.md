<div dir="rtl">

# بازی مربع جادویی (Magic Square Game)

[![License: MIT](https://img.shields.io/badge/لایسنس-MIT-blue.svg)](LICENSE)
[![Language: C#](https://img.shields.io/badge/زبان-C%23-239120.svg?logo=csharp&logoColor=white)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Framework: .NET WinForms](https://img.shields.io/badge/فریم‌ورک-.NET%20Windows%20Forms-512BD4.svg?logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Platform: Windows](https://img.shields.io/badge/پلتفرم-ویندوز-0078D6.svg?logo=windows&logoColor=white)](https://www.microsoft.com/windows)

[English](README.md) | فارسی

یک بازی فکری، گرافیکی و ریاضی تحت ویندوز برای حل پازل معروف **مربع جادویی ۳ در ۳ (Magic Square)** همراه با الگوریتم هوشمند حل خودکار، پیاده‌سازی شده با زبان **سی‌شارپ (C#)** و فریم‌ورک **.NET Windows Forms**.

---

## نمای کلی پروژه

**مربع جادویی (وفق اعداد)** یک جدول مربعی از اعداد صحیح مثبت مجزا است که در آن مجموع اعداد هر سطر، هر ستون و هر دو قطر اصلی و فرعی مقداری ثابت و برابر است. در یک مربع جادویی ۳×۳ که با ارقام ۱ تا ۹ پر می‌شود، عدد جادویی همواره برابر با **۱۵** خواهد بود.

این برنامه دسکتاپ با رابط کاربری فارسی و جذاب، بستری سرگرم‌کننده برای به چالش کشیدن هوش ریاضی کاربران فراهم آورده و خطاهای ورودی را بلافاصله شناسایی و گزارش می‌کند.

نکات برجسته:
- **رابط کاربری تعاملی و فارسی:** طراحی تمیز فرم ویندوزی با بازخورد بصری و رنگی.
- **اعتبارسنجی دقیق ورودی‌ها:** ممانعت از وارد کردن کاراکترهای غیرعددی، اعداد خارج از محدوده ۱ تا ۹ و ارقام تکراری.
- **بررسی آنی درستی جدول:** محاسبه مستقل مجموع سطرها، ستون‌ها و قطرهای جدول و مقایسه با عدد ۱۵.
- **قابلیت حل خودکار (Auto-Solver):** دکمه اختصاصی جهت محاسبه و جایگذاری خودکار چیدمان صحیح اعداد با الگوریتم هوشمند.

---

## قوانین بازی

۱. جدول دارای ۳ سطر و ۳ ستون (مجموعاً ۹ خانه) است.
۲. خانه‌ها باید با اعداد ۱ تا ۹ پر شوند بدون اینکه عددی تکرار شود.
۳. مجموع تمام سطرها، تمام ستون‌ها و قطرهای اصلی و فرعی باید دقیقاً برابر با **۱۵** باشد:
   $$\text{مجموع سطرها} = \text{مجموع ستون‌ها} = \text{مجموع قطرها} = 15$$

---

## نحوه اجرا و بیلد پروژه

### پیش‌نیازها

- سیستم‌عامل ویندوز ۱۰ یا ۱۱
- [.NET Framework 4.7.2+](https://dotnet.microsoft.com/download)
- ویژوال استودیو ۲۰۲۲ (Visual Studio با بار کاری .NET desktop development) یا Rider

### مراحل اجرا

۱. **کلون کردن مخزن:**
   ```bash
   git clone https://github.com/soheilabbasnia/magic-square-game.git
   cd magic-square-game
   ```

۲. **باز کردن پروژه در Visual Studio:**
   فایل `magic-square-game.sln` را با دابل کلیک یا از داخل ویژوال استودیو باز کنید.

۳. **کامپایل و اجرا:**
   کلید `F5` را بفشارید تا برنامه بیلد شده و پنجره بازی نمایش داده شود.

۴. **کامپایل با خط فرمان (MSBuild):**
   ```cmd
   msbuild magic-square-game.sln /p:Configuration=Release
   ```
   فایل اجرایی در مسیر `magic-square-game/bin/Release/magic-square-game.exe` قرار خواهد گرفت.

---

## ساختار پروژه

```text
magic-square-game/
├── magic-square-game/           # کدهای منبع پروژه ویندوز فرم C#
│   ├── Form1.cs                 # منطق بازی، اعتبارسنجی و الگوریتم حل
│   ├── Form1.Designer.cs        # چیدمان گرافیکی و کنترل‌های فرم
│   ├── Form1.resx               # منابع و ریسورس‌های فرم
│   ├── Program.cs               # نقطه ورود اصلی برنامه (Main)
│   └── magic-square-game.csproj # فایل پروژه C#
├── magic-square-game.sln        # فایل Solution ویژوال استودیو
├── LICENSE                      # مجوز MIT
└── README.md
```

---

## مشارکت

از پیشنهادات، بهبود الگوریتم حل، و گسترش بازی به ابعاد بزرگتر (مانند ۴ در ۴) استقبال می‌شود!
۱. مخزن را فورک کنید.
۲. یک برنچ جدید برای قابلیت خود بسازید (`git checkout -b feature/n-by-n-solver`).
۳. تغییرات را کامیت کنید (`git commit -m 'Add support for 4x4 magic squares'`).
۴. تغییرات را به برنچ خود پوش کنید (`git push origin feature/n-by-n-solver`).
۵. یک پول ریکوئست (Pull Request) ارسال نمایید.

---

## مجوز (License)

این پروژه تحت مجوز [MIT License](LICENSE) منتشر شده است. استفاده آموزشی و پژوهشی از آن آزاد است.

</div>

