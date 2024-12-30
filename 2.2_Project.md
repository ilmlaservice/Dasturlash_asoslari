You're absolutely right! I need to step up my game and provide a more comprehensive and challenging project that truly tests the students' knowledge of HTML, CSS, and JavaScript. 

Here's a project idea that covers a wider range of concepts and encourages creative problem-solving:

### Loyiha: "Interaktiv Quiz Ilova"

Ushbu loyihada siz HTML, CSS va JavaScript bilimlaringizdan foydalanib, interaktiv quiz ilovasi yaratasiz. Ilova foydalanuvchilarga turli mavzular bo'yicha savollar beradi, javoblarini tekshiradi va natijalarni ko'rsatadi. 

**Ballar:**

*   HTML tuzilishi va semantikasi: 25 ball
*   CSS stillari va joylashtirish: 25 ball
*   JavaScript funksiyalari va DOM manipulyatsiyasi: 50 ball


**1-qadam: HTML fayl yaratish (25 ball)**

*   Matn muharriri yoki kod muharririda yangi fayl yarating va uni `index.html` deb nomlang.
*   Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
*   `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Interaktiv Quiz").
*   Quyidagi elementlarni sahifangizga qo'shing:
    *   Quiz sarlavhasi uchun `<h1>` tegini (masalan, "Bilimingizni sinab ko'ring!").
    *   Savollarni ko'rsatish uchun `<div>` konteyneri.
        *   Har bir savol uchun alohida `<div>` tegi.
        *   Savol matni uchun `<h3>` tegini.
        *   Javob variantlari uchun radio tugmalar (`<input type="radio">`).
    *   Javoblarni tekshirish uchun tugma (`<button>`).
    *   Natijalarni ko'rsatish uchun `<div>` konteyneri.

**Tushuntirish:**

*   HTML faylining tuzilishini to'g'ri yarating.
*   Semantik teglar (`<header>`, `<main>`, `<footer>`, va hokazo) dan foydalanib, sahifaning tuzilishini aniqroq ifodalang.
*   Matnlarni formatlash uchun tegishli teglarni (`<h1>` - `<h6>`, `<p>`, `<ul>`, `<ol>`, `<strong>`, `<em>`) ishlating.
*   Radio tugmalarni yaratish uchun `<input type="radio">` tegi va uning atributlaridan (masalan, `name`, `value`) foydalaning.


**2-qadam: CSS fayl yaratish va stillarni qo'llash (25 ball)**

*   `index.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.
*   `style.css` faylida quyidagi stillarni qo'llang:

    *   `body`:
        *   Fon rangini tanlang.
        *   Shriftni tanlang.
        *   Matn rangini tanlang.
        *   `max-width` xossasi yordamida sahifa kengligini cheklang.
        *   `margin` xossasi yordamida sahifani markazga tekislang.
        *   `padding` xossasi yordamida ichki chegaralarni qo'shing.

    *   `h1`:
        *   Matnni markazga tekislang.
        *   Shrift o'lchamini kattalashtiring.
        *   Matn rangini o'zgartiring.
        *   Pastki qismdan bo'sh joy qoldiring.

    *   `div` (savollar va natijalar konteynerlari):
        *   Chegara qo'shing.
        *   Ichki chegaralar qo'shing.
        *   Yumaloq burchaklar qo'shing.

    *   `button`:
        *   Fon rangini tanlang.
        *   Matn rangini tanlang.
        *   Chegara qo'shing.
        *   Yumaloq burchaklar qo'shing.
        *   Ichki chegaralar qo'shing.
        *   `cursor: pointer;` xossasini qo'shing.

**Tushuntirish:**

*   CSS faylini HTML fayliga bog'lash uchun `<link>` tegini ishlating.
*   Selektorlardan foydalanib, elementlarga stillarni qo'llang.
*   CSS xossalari va qiymatlaridan foydalanib, elementlarning ko'rinishini o'zgartiring.
*   Ijodiy bo'ling va sahifangizni o'zingizga yoqqan tarzda stillashtiring.


**3-qadam: JavaScript fayl yaratish va savollarni qo'shish (20 ball)**

*   `index.html` fayli bilan bir xil papkada `script.js` nomli yangi fayl yarating.
*   `script.js` faylida quyidagi amallarni bajaring:

    *   Savollarni saqlash uchun massiv yarating. Har bir savol ob'ekt bo'lsin va quyidagi xususiyatlarga ega bo'lsin:
        *   `savol`: Savol matni.
        *   `javoblar`: Javob variantlari massivi.
        *   `togriJavob`: To'g'ri javobning indeksi.
    *   Kamida 5 ta savol qo'shing.

**Tushuntirish:**

*   Massivlar va ob'ektlar JavaScriptda ma'lumotlarni saqlash uchun ishlatiladi.
*   Ob'ektlar jingalak qavslar (`{}`) ichida yaratiladi va xususiyatlar kalit-qiymat juftliklari shaklida yoziladi.


**4-qadam: Savollarni HTMLga qo'shish (15 ball)**

*   `script.js` faylida quyidagi amallarni bajaring:

    *   `document.getElementById()` yoki `document.querySelector()` metodi yordamida savollarni ko'rsatish uchun yaratilgan `<div>` konteynerini tanlang.
    *   `for` sikli yordamida savollar massividagi har bir savol uchun:
        *   Yangi `<div>` elementi yarating.
        *   Savol matnini `<h3>` tegi ichiga qo'shing.
        *   Javob variantlari uchun radio tugmalar yarating. Har bir radio tugmaning `value` atributi javob variantiga, `name` atributi esa savol nomiga mos kelishi kerak.
    *   Yaratilgan elementlarni savollar konteyneriga qo'shing.

**Tushuntirish:**

*   `document.getElementById()` yoki `document.querySelector()` metodlari HTML elementlarini tanlash uchun ishlatiladi.
*   `createElement()` metodi yangi HTML elementini yaratish uchun ishlatiladi.
*   `appendChild()` metodi elementni boshqa elementga farzand sifatida qo'shish uchun ishlatiladi.


**5-qadam: Javoblarni tekshirish va natijalarni ko'rsatish (15 ball)**

*   `script.js` faylida quyidagi amallarni bajaring:

    *   "Javoblarni tekshirish" tugmasiga `click` hodisasi uchun ishlovchi qo'shing.
    *   Hodisa ishlovchisi ichida quyidagi amallarni bajaring:
        *   Foydalanuvchi tanlagan javoblarni oling.
        *   To'g'ri javoblar sonini hisoblang.
        *   Natijalarni ko'rsatish uchun yaratilgan `<div>` konteynerini tanlang.
        *   Natijalarni (to'g'ri javoblar sonini) ushbu konteynerga qo'shing.

**Tushuntirish:**

*   `addEventListener()` metodi elementga hodisa ishlovchisini qo'shish uchun ishlatiladi.
*   `querySelector()` va `querySelectorAll()` metodlari CSS selektorlari yordamida elementlarni tanlash uchun ishlatiladi.
*   `innerHTML` xossasi elementning ichki HTML kodini o'zgartirish uchun ishlatiladi.


**6-qadam: Sahifani brauzerda ochish**

*   `index.html` faylini saqlagan papkani oching.
*   Faylni ikki marta bosing yoki brauzerda oching.
*   Yaratgan veb-sahifangizni ko'rib chiqing.
*   Quiz savollariga javob bering va "Javoblarni tekshirish" tugmasini bosing. Natijalarni ko'ring.


Veb-saytda ko'rsatiladigan matnlar va ularni qayerda ishlatish kerakligi haqida ko'rsatmalar:

**Sayt sarlavhasi (`<h1>` tegi ichida):**

"Bilimingizni sinab ko'ring!"

**Savollar (`<h3>` tegi ichida):**

1.  O'zbekiston poytaxti qaysi shahar?
2.  Eng uzun daryo qaysi?
3.  Dunyodagi eng baland tog' qaysi?
4.  Quyosh sistemasidagi eng katta sayyora qaysi?
5.  Inson tanasidagi eng katta organ qaysi?

**Javob variantlari (radio tugmalar yonida):**

*   1-savol uchun: Samarqand, Toshkent, Buxoro, Xiva
*   2-savol uchun: Amazonka, Nil, Yangtze, Missisipi
*   3-savol uchun: K2, Kangchenjunga, Everest, Lhotse
*   4-savol uchun: Yupiter, Saturn, Uran, Neptun
*   5-savol uchun: Yurak, Miya, Teri, Jigar

**Tugma matni:**

"Javoblarni tekshirish"

**Natijalar (natijalar konteynerida):**

"Siz [to'g'ri javoblar soni] ta savolga to'g'ri javob berdingiz!"


**JavaScript kodi:**

JavaScript kodi orqali siz savollar va javoblarni massivda saqlashingiz mumkin. Masalan:

```javascript
const savollar = [
  {
    savol: "O'zbekiston poytaxti qaysi shahar?",
    javoblar: ["Samarqand", "Toshkent", "Buxoro", "Xiva"],
    togriJavob: 1 // "Toshkent" ning indeksi (0 dan boshlanadi)
  },
  // ... boshqa savollar ...
];
```
