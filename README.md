# tamrin-20-2 فرهاد بانویی 
<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <title>طراحی پایگاه داده استاندارد برای یک فروشگاه</title>
</head>
<body>
    <h1>طراحی پایگاه داده استاندارد برای یک فروشگاه</h1>

    <p>یک پایگاه داده به خوبی طراحی شده برای هر فروشگاهی ضروری است و امکان مدیریت کارآمد محصولات، مشتریان، سفارشات و سایر اطلاعات حیاتی را فراهم می کند. در اینجا خلاصه ای از اصول طراحی استاندارد و جداول اصلی موجود است:</p>

    <h2>اصول طراحی</h2>

    <ul>
        <li>**مدل رابطه نهاد (ERM):** این رویکرد موجودیت های اصلی (به عنوان مثال، محصولات، مشتریان، سفارشات) در سیستم و نحوه ارتباط آنها با یکدیگر را شناسایی می کند.</li>
        <li>**عادی سازی:** این فرآیند افزونگی داده ها را به حداقل می رساند و یکپارچگی داده ها را تضمین می کند.</li>
        <li>**انواع داده ها:** انتخاب انواع داده های مناسب برای هر ستون (مثلاً متن برای نام محصول، عدد صحیح برای کمیت) دقت داده و کارایی ذخیره سازی را بهبود می بخشد.</li>
    </ul>

    <h2>جداول اصلی</h2>

    <h3>محصولات</h3>

    <p>این جدول اطلاعاتی را در مورد اقلامی که می فروشید ذخیره می کند، معمولاً شامل:</p>

    <ul>
        <li>شناسه محصول (کلید اصلی)</li>
        <li>نام</li>
        <li>شرح</li>
        <li>قیمت</li>
        <li>مقدار موجودی</li>
        <li>دسته (کلید خارجی ارجاع به جدول دسته‌ها، در صورت وجود)</li>
        <li>سایر جزئیات مرتبط مانند برند، اندازه، رنگ و غیره</li>
    </ul>

    <h3>مشتریان</h3>

    <p>این جدول اطلاعات مشتری را نشان می دهد:</p>

    <ul>
        <li>شناسه مشتری (کلید اصلی)</li>
        <li>نام</li>
        <li>اطلاعات تماس (ایمیل، شماره تلفن)</li>
        <li>آدرس حمل و نقل (می تواند یک جدول جداگانه برای چندین آدرس باشد)</li>
        <li>اطلاعات برنامه وفاداری (اختیاری)</li>
    </ul>

    <h3>سفارشات</h3>

    <p>این جدول خریدهای مشتری را دنبال می کند:</p>

    <ul>
        <li>شناسه سفارش (کلید اصلی)</li>
        <li>شناسه مشتری (کلید خارجی مرجع جدول مشتریان)</li>
        <li>تاریخ سفارش</li>
        <li>وضعیت سفارش (به عنوان مثال، در انتظار، ارسال، لغو شده)</li>
        <li>مبلغ کل</li>
    </ul>

    <h3>موارد سفارش</h3>

    <p>این جدول سفارشات را با محصولات خاص پیوند می دهد:</p>

    <ul>
        <li>شناسه سفارش (جدول سفارشات مرجع کلید خارجی)</li>
        <li>شناسه محصول (جدول محصولات مرجع کلید خارجی)</li>
        <li>مقدار خریداری شده</li>
        <li>قیمت واحد</li>
        <li>جمع فرعی</li>
    </ul>

    <h2>جداول اضافی (اختیاری)</h2>

    <ul>
        <li>دسته بندی ها: اگر تنوع محصول زیادی دارید، یک جدول جداگانه برای دسته بندی محصولات می تواند سازماندهی را بهبود بخشد.</li>
        <li>کارکنان: برای مدیریت کارکنان، جدولی با جزئیات و نقش های کارمند.</li>
        <li>تامین کنندگان: اگر اطلاعات تامین کننده را ردیابی می کنید، جدولی برای ذخیره جزئیات تامین کننده.</li>
        <li>تراکنش ها: برای ثبت جزئیات پرداخت فردی یک سفارش.</li>
    </ul>

    <h2>مزایای طراحی استاندارد</h2>

    <ul>
        <li>**کارایی:** بازیابی و دستکاری داده ها را از طریق جداول و روابط کاملاً تعریف شده ساده می کند.</li>
        <li>**مقیاس پذیری:** ساختار را می توان به راحتی برای سازگاری با رشد آینده و عملکردهای جدید منطبق کرد.</li>
        <li>**یکپارچگی
