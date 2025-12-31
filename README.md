<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>سرای سنتی قصر</title>

<style>
body{
    margin:0;
    font-family:Tahoma, sans-serif;
    background:linear-gradient(135deg,#f6efe4,#e7d8c3);
    color:#3b2a1a;
}

/* عنوان بدون کادر */
.title{
    text-align:center;
    padding:22px 10px 10px;
    font-size:20px;
    font-weight:bold;
    color:#7a4e2d;
}

/* کارت‌های دسته‌بندی */
.categories{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:14px;
    padding:16px;
}
.card{
    background:linear-gradient(145deg,#fff6e8,#e3cfa1);
    border-radius:16px;
    padding:28px 10px;
    text-align:center;
    font-size:14px;
    box-shadow:0 6px 16px rgba(90,60,30,.25);
    cursor:pointer;
    transition:.25s;
}
.card:hover{
    transform:scale(1.04);
    background:linear-gradient(145deg,#f3e0b8,#d2ad68);
}

/* صفحات منو */
.menu{
    display:none;
    padding:18px;
    animation:fade .3s ease-in;
}
@keyframes fade{
    from{opacity:0;transform:translateY(10px)}
    to{opacity:1;transform:none}
}

/* عنوان دسته */
h2{
    font-size:16px;
    margin:10px 0 12px;
    padding-bottom:6px;
    border-bottom:2px dashed #b9965a;
    color:#6b4423;
}

/* آیتم‌ها */
ul{list-style:none;padding:0;margin:0}
li{
    display:flex;
    justify-content:space-between;
    padding:7px 0;
    font-size:13px;
    border-bottom:1px dotted #d6c2a1;
}
li:last-child{border:none}

/* دکمه بازگشت */
.back{
    display:inline-block;
    margin-bottom:14px;
    background:linear-gradient(145deg,#c6a15a,#8a5c2c);
    color:#fff;
    padding:7px 16px;
    border-radius:20px;
    font-size:12px;
    cursor:pointer;
    box-shadow:0 4px 10px rgba(0,0,0,.25);
}
</style>
</head>

<body>

<div class="title">سرای سنتی قصر</div>

<div class="categories" id="cats">
    <div class="card" onclick="openMenu('ice')">🍨 بستنی و آیس پک</div>
    <div class="card" onclick="openMenu('cake')">🍰 کیک‌ها</div>
    <div class="card" onclick="openMenu('hot')">☕ نوشیدنی گرم</div>
    <div class="card" onclick="openMenu('herbal')">🌿 دمنوش</div>
    <div class="card" onclick="openMenu('cold')">🥤 نوشیدنی خنک</div>
    <div class="card" onclick="openMenu('tea')">🫖 سرویس چای</div>
    <div class="card" onclick="openMenu('food')">🍲 غذاها</div>
</div>

<!-- بستنی -->
<div class="menu" id="ice">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>بستنی و آیس پک</h2>
<ul>
<li><span>معجون</span><span>۲۰۰</span></li>
<li><span>بستنی معجون</span><span>۱۴۰</span></li>
<li><span>بستنی سنتی</span><span>۹۵</span></li>
<li><span>بستنی میوه ای</span><span>۹۵</span></li>
<li><span>فالوده خالی</span><span>۶۵</span></li>
<li><span>فالوده بستنی</span><span>۹۵</span></li>
<li><span>آیس معجون</span><span>۱۳۰</span></li>
<li><span>آیس نوتلا</span><span>۱۱۰</span></li>
<li><span>آیس شکلات</span><span>۱۱۰</span></li>
<li><span>آیس انبه</span><span>۱۰۰</span></li>
<li><span>آیس توت فرنگی</span><span>۱۰۰</span></li>
<li><span>آیس طالبی</span><span>۱۰۰</span></li>
<li><span>آیس وانیلی</span><span>۱۰۰</span></li>
<li><span>آیس نسکافه</span><span>۱۰۰</span></li>
<li><span>آیس آناناس</span><span>۱۰۰</span></li>
<li><span>آفوگاتو با بستنی</span><span>۸۵</span></li>
</ul>
</div>

<!-- کیک -->
<div class="menu" id="cake">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>کیک‌ها</h2>
<ul>
<li><span>کیک شکلاتی</span><span>۸۰</span></li>
<li><span>کاپ کیک</span><span>۴۵</span></li>
<li><span>رولت</span><span>۵۰</span></li>
</ul>
</div>

<!-- نوشیدنی گرم -->
<div class="menu" id="hot">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>نوشیدنی گرم</h2>
<ul>
<li><span>قهوه ترک</span><span>۵۰</span></li>
<li><span>اسپرسو تک</span><span>۴۵</span></li>
<li><span>اسپرسو دبل</span><span>۶۰</span></li>
<li><span>ماکیاتو</span><span>۷۰</span></li>
<li><span>قهوه یونانی</span><span>۷۰</span></li>
<li><span>آمریکانو</span><span>۷۵</span></li>
<li><span>لاته</span><span>۱۰۰</span></li>
<li><span>لاته کاراملی</span><span>۹۰</span></li>
<li><span>کافه میکس با کارامل</span><span>۹۰</span></li>
<li><span>موکا</span><span>۷۰</span></li>
<li><span>شیر قهوه</span><span>۹۰</span></li>
<li><span>نسکافه</span><span>۸۰</span></li>
<li><span>هات چاکلت</span><span>۸۰</span></li>
<li><span>شیر نسکافه</span><span>۹۰</span></li>
<li><span>کاپوچینو</span><span>۹۰</span></li>
<li><span>شیر کاکائو</span><span>۵۰</span></li>
</ul>
</div>

<!-- دمنوش -->
<div class="menu" id="herbal">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>سرویس دمنوش</h2>
<ul>
<li><span>لیمو و چای سبز</span><span>۹۰</span></li>
<li><span>گل گاو زبان</span><span>۱۰۰</span></li>
<li><span>بهار نارنج و گل محمدی</span><span>۱۰۰</span></li>
<li><span>سیب و دارچین</span><span>۱۰۰</span></li>
<li><span>آویشن</span><span>۱۰۰</span></li>
<li><span>عناب</span><span>۹۰</span></li>
<li><span>گل بنفش</span><span>۹۰</span></li>
<li><span>چای ترش</span><span>۱۰۰</span></li>
<li><span>زنجبیل و دارچین</span><span>۱۲۰</span></li>
<li><span>بابونه اسطوخدوس</span><span>۱۰۰</span></li>
</ul>
</div>

<!-- نوشیدنی خنک -->
<div class="menu" id="cold">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>نوشیدنی خنک</h2>
<ul>
<li><span>شربت پرتقال</span><span>۵۰</span></li>
<li><span>شربت آناناس</span><span>۶۰</span></li>
<li><span>شربت آلبالو</span><span>۶۰</span></li>
<li><span>موهیتو</span><span>۸۰</span></li>
<li><span>خاکشیر</span><span>۶۰</span></li>
<li><span>تخم شربتی و زعفران</span><span>۷۰</span></li>
<li><span>شیر موز معجون</span><span>۱۰۰</span></li>
<li><span>شیر پسته با بستنی</span><span>۱۱۰</span></li>
<li><span>شیر موز</span><span>۶۵</span></li>
<li><span>شیر موز بستنی</span><span>۹۰</span></li>
<li><span>شیر موز قهوه</span><span>۹۰</span></li>
<li><span>آب هویج</span><span>۵۰</span></li>
<li><span>آب هویج بستنی</span><span>۸۰</span></li>
<li><span>آب طالبی</span><span>۷۰</span></li>
<li><span>آب طالبی بستنی</span><span>۹۰</span></li>
<li><span>آب انبه</span><span>۹۰</span></li>
<li><span>آب انبه بستنی</span><span>۱۱۰</span></li>
</ul>
</div>

<!-- سرویس چای -->
<div class="menu" id="tea">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>سرویس چای</h2>
<ul>
<li><span>دو نفره</span><span>۱۲۰</span></li>
<li><span>سه نفره</span><span>۱۸۰</span></li>
<li><span>پنج نفره</span><span>۳۰۰</span></li>
<li><span>هفت نفره</span><span>۴۲۰</span></li>
<li><span>چای ماسالا</span><span>۸۰</span></li>
</ul>
</div>

<!-- غذا -->
<div class="menu" id="food">
<span class="back" onclick="goBack()">بازگشت</span>
<h2>غذاها</h2>
<ul>
<li><span>دیزی</span><span>۳۲۰</span></li>
<li><span>حلیم</span><span>۱۳۰</span></li>
<li><span>آش رشته</span><span>۱۳۰</span></li>
<li><span>آش دوغ</span><span>۱۲۰</span></li>
<li><span>بلال</span><span>۹۰</span></li>
<li><span>ذرت مکزیکی</span><span>۹۰</span></li>
</ul>
</div>

<script>
function openMenu(id){
    document.getElementById("cats").style.display="none";
    document.querySelectorAll(".menu").forEach(m=>m.style.display="none");
    document.getElementById(id).style.display="block";
}
function goBack(){
    document.querySelectorAll(".menu").forEach(m=>m.style.display="none");
    document.getElementById("cats").style.display="grid";
}
</script>

</body>
</html>
