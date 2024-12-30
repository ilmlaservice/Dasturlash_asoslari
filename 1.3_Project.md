### Loyiha: "Sayohat Agentligi Veb-sayti"

Ushbu loyihada siz HTML va CSS bilimlaringizdan foydalanib, sayohat agentligi uchun veb-sayt yaratasiz. Saytda agentlik haqida ma'lumot, xizmatlar ro'yxati, sayohat turlari, mijozlarning fikr-mulohazalari va kontakt ma'lumotlari bo'lishi kerak.

**Ballar:**

*   HTML tuzilishi va semantikasi: 30 ball
*   CSS stillari va joylashtirish: 40 ball
*   Ijodiy dizayn va foydalanuvchi tajribasi: 30 ball

**1-qadam: HTML fayl yaratish (30 ball)**

*   Matn muharriri yoki kod muharririda yangi fayl yarating va uni `index.html` deb nomlang. (**1 ball**)
*   Faylga asosiy HTML tuzilishini qo'shing: (**3 ball**)
    *   `<!DOCTYPE html>` deklaratsiyasini qo'shing.
    *   `<html lang="uz">` tegini qo'shing.
    *   `<head>` tegi ichida:
        *   `<meta charset="UTF-8">` tegini qo'shing.
        *   `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Sayohat Agentligi").
        *   CSS faylini bog'lash uchun `<link>` tegini qo'shing.
    *   `<body>` tegi ichida sahifa kontentini joylashtiring.

*   **Header qismi:** (**4 ball**)
    *   `<header>` tegini ichida:
        *   Agentlik logotipi uchun `<img>` tegi qo'shing. `src` atributida logotip rasmining manzilini, `alt` atributida esa rasmning tavsifini ko'rsating.
        *   Agentlik nomi uchun `<h1>` tegini qo'shing va ichiga agentlik nomini yozing (masalan, "Sayohat Dunyosi").

*   **Navigatsiya qismi:** (**7 ball**)
    *   `<nav>` tegi ichida:
        *   Tartibsiz ro'yxat (`<ul>`) yarating.
        *   Har bir menyu elementi uchun ro'yxat elementi (`<li>`) yarating.
        *   Har bir `<li>` tegi ichida havola (`<a>`) yarating va `href` atributida tegishli sahifa manzilini ko'rsating. Hozircha barcha havolalarga `#` belgisini qo'yishingiz mumkin.
        *   Menyu elementlari quyidagicha bo'lsin: Bosh sahifa, Xizmatlar, Sayohatlar, Fikrlar, Aloqa.

*   **Asosiy qism (`<main>`):** (**15 ball**)
    *   Agentlik haqida ma'lumot beruvchi `<section>` tegini yarating. (**2 ball**)
        *   Ichida sarlavha (`<h2>`) sifatida "Biz haqimizda" matnini yozing.
        *   Xatboshilar (`<p>`) ichida agentlik haqida qisqacha ma'lumot bering. Masalan, "Sayohat Dunyosi agentligi 2010-yildan buyon O'zbekiston bo'ylab sayohatlar tashkil qilib kelmoqda. Biz sizga eng yaxshi mehmonxonalar, gidlar va transport xizmatlarini taklif etamiz. Biz bilan sayohat qilish - bu unutilmas tajriba!"

    *   Xizmatlar ro'yxati uchun `<section>` tegini yarating. (**3 ball**)
        *   Ichida sarlavha (`<h2>`) sifatida "Xizmatlarimiz" matnini yozing.
        *   Tartiblangan ro'yxat (`<ol>`) yarating va ichida quyidagi xizmatlarni ko'rsating: Aviachiptalar bron qilish, Mehmonxonalar bron qilish, Ekskursiyalar tashkil qilish, Transport xizmatlari, Viza olishda yordam.

    *   Sayohat turlari uchun `<section>` tegini yarating. (**6 ball**)
        *   Ichida sarlavha (`<h2>`) sifatida "Sayohat turlari" matnini yozing.
        *   Har bir sayohat turi uchun alohida `<article>` tegi yarating. 
        *   Har bir `<article>` ichida:
            *   Sayohat nomi uchun `<h3>` tegini ishlating (masalan, "Samarqand", "Buxoro", "Xiva").
            *   Tavsifi uchun `<p>` tegini ishlating.
            *   Rasmi uchun `<img>` tegini ishlating. `src` atributida rasm manzilini, `alt` atributida esa rasmning tavsifini ko'rsating.

    *   Mijozlarning fikr-mulohazalari uchun `<section>` tegini yarating. (**4 ball**)
        *   Ichida sarlavha (`<h2>`) sifatida "Mijozlarimiz fikri" matnini yozing.
        *   Har bir fikr uchun alohida `<article>` tegi yarating. 
        *   Har bir `<article>` ichida:
            *   Mijoz ismi uchun `<h4>` tegini ishlating.
            *   Fikr matni uchun `<p>` tegini ishlating.

*   **Footer qismi:** (**4 ball**)
    *   `<footer>` tegi ichida:
        *   Agentlikning manzili, telefon raqami va email manzili uchun alohida `<p>` teglari qo'shing.
        *   Mualliflik huquqi haqida ma'lumotni `<p>` tegi ichida ko'rsating (masalan, "&copy; 2024 Sayohat Dunyosi").


**2-qadam: CSS fayl yaratish va asosiy stillarni qo'llash (20 ball)**

*   `index.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating. (**2 ball**)
*   `style.css` faylida quyidagi stillarni qo'llang: (**18 ball**)

    *   `body`:
        *   Fon rangini `#f4f4f4` ga o'rnating.
        *   Shriftni `'Open Sans', sans-serif` ga o'rnating.
        *   Matn rangini `#333` ga o'rnating.
        *   `max-width` xossasini `960px` ga o'rnating.
        *   `margin` xossasini `0 auto` ga o'rnating.
        *   `padding` xossasini `20px` ga o'rnating.

    *   `h1`, `h2`:
        *   Matnni markazga tekislang (`text-align: center`).
        *   Pastki qismdan 20px bo'sh joy qoldiring (`margin-bottom: 20px`).


**3-qadam: Navigatsiya menyusi stilini qo'llash (15 ball)**

*   `style.css` faylida quyidagi stillarni qo'llang:

    *   `nav`: (**3 ball**)
        *   Fon rangini `#333` ga o'rnating.
        *   Ichki chegaralarni 10px ga o'rnating (`padding: 10px`).
        *   Burchaklarni 5px radiusda yumaloqlang (`border-radius: 5px`).

    *   `nav ul`: (**6 ball**)
        *   Markerlarni olib tashlang (`list-style: none`).
        *   Tashqi chegaralarni olib tashlang (`margin: 0`).
        *   Ichki chegaralarni olib tashlang (`padding: 0`).
        *   Flexbox yordamida elementlarni gorizontal joylashtiring (`display: flex`).
        *   Elementlar orasidagi bo'shliqni teng taqsimlang (`justify-content: space-around`).

    *   `nav a`: (**6 ball**)
        *   Rangini oq rangga o'zgartiring (`color: #fff`).
        *   Ostiga chizilgan chiziqni olib tashlang (`text-decoration: none`).
        *   Ichki chegaralarni 8px yuqoridan va pastdan, 15px chapdan va o'ngdan qilib o'rnating (`padding: 8px 15px`).



**4-qadam: Sayohat turlari stilini qo'llash (15 ball)**

*   `style.css` faylida quyidagi stillarni qo'llang:

    *   `article`: (**9 ball**)
        *   Fon rangini oq rangga o'zgartiring (`background-color: #fff`).
        *   1 piksel qalinlikdagi och kulrang chegara qo'shing (`border: 1px solid #ddd`).
        *   Ichki chegaralarni 20px ga o'rnating (`padding: 20px`).
        *   Pastki qismdan 20px bo'sh joy qoldiring (`margin-bottom: 20px`).
        *   Burchaklarni 5px radiusda yumaloqlang (`border-radius: 5px`).

    *   `article img`: (**6 ball**)
        *   Kenglikni 100% qilib o'rnating (`width: 100%`).
        *   Balandlikni avtomatik o'lchab o'rnating (`height: auto`).
        *   Burchaklarni 5px radiusda yumaloqlang (`border-radius: 5px`).



**5-qadam: Qolgan elementlarga stillarni qo'llash (20 ball)**

*   `style.css` faylida quyidagi stillarni qo'llang:

    *   `p` (paragraflar) uchun: (**4 ball**)
        *   Satrlar orasidagi masofani 1.6 ga o'rnating.

    *   `ol` (tartiblangan ro'yxatlar) uchun: (**4 ball**)
        *   Markerlarni ro'yxat ichida ko'rsating.

    *   `footer` (pastki qism) uchun: (**12 ball**)
        *   Fon rangini quyuq kulrangga o'zgartiring.
        *   Matn rangini oq rangga o'zgartiring.
        *   Matnni markazga tekislang.
        *   Ichki chegaralarni 20 pikselga o'rnating.
        *   Yuqoridan 30 piksel bo'sh joy qoldiring.

**6-qadam: Sahifani brauzerda ochish**

*   `index.html` faylini saqlagan papkani oching.
*   Faylni ikki marta bosing yoki brauzerda oching.
*   Yaratgan veb-sahifangizni ko'rib chiqing.


Eslatma: Loyihada ishlatiladigan rasmlar (`logo.png`, `samarqand.jpg`, `buxoro.jpg`, `xiva.jpg`) ni o'zingiz topib qo'yishingiz kerak bo'ladi.