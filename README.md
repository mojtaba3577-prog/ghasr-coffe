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
    background:linear-gradient(135deg,#f6efe4,#e8dcc8);
    color:#3b2a1a;
}

/* عنوان بدون کادر */
.title{
    text-align:center;
    padding:22px 10px 10px;
    font-size:20px;
    font-weight:bold;
    color:#7a4e2d;
    letter-spacing:1px;
}

/* کارت‌های صفحه اصلی */
.categories{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:14px;
    padding:16px;
}
.card{
    background:linear-gradient(145deg,#fff7ec,#e7d3a3);
    border-radius:16px;
    padding:26px 10px;
    text-align:center;
    font-size:14px;
    box-shadow:0 6px 16px rgba(90,60,30,.25);
    cursor:pointer;
    transition:.25s;
}
.card:hover{
    transform:scale(1.03);
    background:linear-gradient(145deg,#f5e6c8,#d9b873);
}

/* صفحه منو */
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
    background:linear-gradient(145deg,#c8a45c,#8b5e2f);
    color:#fff;
    padding:7px 14px;
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

<!-- منوها (همون قبلی، بدون تغییر محتوا) -->
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
