<details>
<summary>
HTML Hujjatining Asosiy Strukturasi
</summary>

Har bir HTML hujjat quyidagi asosiy strukturaga ega:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Sahifa sarlavhasi</title>
</head>
<body>

  <h1>Bu sarlavha</h1>
  <p>Bu xatboshi.</p>

</body>
</html>
```

Keling, bu strukturadagi har bir elementni batafsil ko'rib chiqamiz:

* **`<!DOCTYPE html>`:** Bu deklaratsiya veb-brauzerga hujjatning HTML5 standartida yozilganligini bildiradi.
* **`<html lang="uz">`:** Bu teg HTML hujjatning boshlanishini bildiradi. `lang="uz"` atributi sahifaning tili o'zbekcha ekanligini ko'rsatadi.
* **`<head>`:** Bu bo'limda sahifa haqida meta-ma'lumotlar, jumladan sahifa sarlavhasi, CSS stillari va JavaScript kodlari joylashtiriladi. Bu ma'lumotlar brauzerda ko'rsatilmaydi, lekin sahifaning ishlashi uchun muhimdir.
    * **`<meta charset="UTF-8">`:** Bu teg sahifaning kodlash standarti UTF-8 ekanligini bildiradi. UTF-8 standarti o'zbek tilidagi barcha belgilarni to'g'ri ko'rsatish imkonini beradi.
    * **`<title>Sahifa sarlavhasi</title>`:** Bu teg sahifaning sarlavhasini belgilaydi. Sarlavha brauzerning tabida yoki oynasining sarlavha satrida ko'rsatiladi.
* **`<body>`:** Bu bo'limda sahifaning asosiy tarkibi, ya'ni foydalanuvchilar brauzerda ko'radigan barcha elementlar joylashtiriladi.
    * **`<h1>Bu sarlavha</h1>`:** Bu teg sarlavha yaratish uchun ishlatiladi. HTMLda `<h1>` dan `<h6>` gacha bo'lgan oltita sarlavha darajasi mavjud.
    * **`<p>Bu xatboshi.</p>`:** Bu teg xatboshi yaratish uchun ishlatiladi.

### Teglar va Elementlar

HTMLda ko'plab teglar mavjud. Keling, ba'zi asosiy teglarni ko'rib chiqamiz va ularning qanday ishlatilishini misollar bilan ko'rsatamiz:

* **Sarlavhalar:** `<h1>` dan `<h6>` gacha bo'lgan teglar sarlavhalar yaratish uchun ishlatiladi.

```html
<h1>Bu eng katta sarlavha</h1>
<h2>Bu kichikroq sarlavha</h2>
<h3>Bu undan ham kichikroq sarlavha</h3>
```

* **Xatboshilar:** `<p>` tegi xatboshilar yaratish uchun ishlatiladi.

```html
<p>Bu birinchi xatboshi.</p>
<p>Bu ikkinchi xatboshi.</p>
```

* **Rasmlar:** `<img>` tegi rasmlarni veb-sahifaga qo'shish uchun ishlatiladi.

```html
<img src="rasm.jpg" alt="Rasmning tavsifi">
```

Bu misolda, `src` atributi rasm faylining manzilini, `alt` atributi esa rasmning tavsifini ko'rsatadi.

* **Havolalar:** `<a>` tegi havolalar yaratish uchun ishlatiladi.

```html
<a href="https://kun.uz">Kun.uz saytiga o'tish</a>
```

Bu misolda, `href` atributi havolaning manzilini ko'rsatadi. Havolani bosganda, foydalanuvchi Kun.uz saytiga o'tadi.

* **Ro'yxatlar:** `<ul>`, `<ol>` va `<li>` teglari ro'yxatlar yaratish uchun ishlatiladi.

```html
<ul>
  <li>Olma</li>
  <li>Anor</li>
  <li>Uzum</li>
</ul>

<ol>
  <li>Birinchi</li>
  <li>Ikkinchi</li>
  <li>Uchinchi</li>
</ol>
```

Bu misolda, `<ul>` tegi tartibsiz ro'yxatni, `<ol>` tegi tartibli ro'yxatni, `<li>` tegi esa ro'yxat elementini bildiradi.

### Atributlar

Atributlar teglarga qo'shimcha ma'lumot berish uchun ishlatiladi. Keling, ba'zi asosiy atributlarni ko'rib chiqamiz:

* **`class`:** Bu atribut elementga CSS stillarini qo'llash uchun ishlatiladi.

```html
<p class="qizil-matn">Bu xatboshi qizil rangda bo'ladi.</p>
```

* **`id`:** Bu atribut elementga noyob identifikator berish uchun ishlatiladi.

```html
<div id="asosiy-kontent">Bu asosiy kontent.</div>
```

* **`style`:** Bu atribut elementga inline CSS stillarini qo'llash uchun ishlatiladi.

```html
<p style="color: blue;">Bu xatboshi ko'k rangda bo'ladi.</p>
```

Bu misollar HTML asoslarini tushunishga yordam beradi degan umiddaman. Keyingi darslarda biz HTMLning boshqa jihatlarini, jumladan semantik teglar, formlar va jadvallarni ko'rib chiqamiz.

### O'qituvchi boshchiligidagi loyiha: "Mening maktabim" (to'liq)

**1-qadam: Yangi HTML hujjat yaratish**

Avvalgi kabi, yangi HTML hujjat yarating va uni `maktab.html` deb nomlang. Asosiy HTML tuzilishini qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Mening maktabim</title>
</head>
<body>

</body>
</html>
```

**2-qadam: Sarlavha va kirish qismini qo'shish**

* `<body>` teglari ichida `<h1>` tegi yordamida sahifa sarlavhasini qo'shing. Masalan, "Mening maktabim".
* Maktabingiz haqida qisqacha ma'lumot beruvchi xatboshilar (`<p>`) yozing. Masalan, maktabingizning nomi, manzili, qachon tashkil etilgani va boshqalar.

```html
<body>

  <h1>Mening maktabim</h1>
  <p>Men 1-umumta'lim maktabida o'qiyman. Maktabimiz Samarqand shahrida joylashgan.</p>
  <p>Maktabimiz 1991-yilda tashkil etilgan.</p>

</body>
```

**3-qadam: Maktab rasmini qo'shish**

* Endi maktabingizning rasmini qo'shamiz. Buning uchun `<img>` tegini ishlatamiz.
* `src` atributida rasm faylining manzilini ko'rsating. Masalan, agar rasm fayli `maktab_rasmi.jpg` deb nomlangan va `maktab.html` fayli bilan bir xil papkada joylashgan bo'lsa, `src="maktab_rasmi.jpg"` deb yozasiz.
* `alt` atributida rasmning tavsifini ko'rsating. Bu atribut rasm ko'rsatilmasa (masalan, internet aloqasi yo'q bo'lsa) yoki ko'zi ojiz foydalanuvchilar uchun ekran o'quvchi dasturlar tomonidan ishlatiladi.

```html
<img src="maktab_rasmi.jpg" alt="Maktabimizning rasmi">
```

**4-qadam: Maktab haqida batafsil ma'lumot qo'shish**

* Maktabingizning veb-sayti yoki ijtimoiy tarmoqdagi sahifasi bormi? Agar bo'lsa, uning havolasini qo'shing. Buning uchun `<a>` tegini ishlating. Havolaning manzilini `href` atributida ko'rsating.

```html
<p>Maktabimiz haqida batafsil ma'lumotni <a href="https://maktab.uz">bu yerda</a> olishingiz mumkin.</p>
```

* Maktabingizda qanday fanlar o'qitiladi? Ularning ro'yxatini tuzing. Buning uchun tartibsiz ro'yxat (`<ul>`, `<li>`) dan foydalaning.

```html
<p>Maktabimizda quyidagi fanlar o'qitiladi:</p>
<ul>
  <li>Ona tili</li>
  <li>Matematika</li>
  <li>Fizika</li>
  <li>Kimyo</li>
  <li>Biologiya</li>
  <li>Tarix</li>
</ul>
```

* Maktabingizda qanday to'garaklar bor? Ularning ro'yxatini tuzing va har bir to'garak haqida qisqacha ma'lumot bering. Buning uchun tartibli ro'yxat (`<ol>`, `<li>`) dan foydalaning.

```html
<p>Maktabimizda quyidagi to'garaklar faoliyat yuritadi:</p>
<ol>
  <li>Shaxmat to'garagi - bu yerda o'quvchilar shaxmat o'ynashni o'rganadilar va musobaqalarda qatnashadilar.</li>
  <li>Rasm to'garagi - bu yerda o'quvchilar rasm chizishni o'rganadilar.</li>
  <li>Sport to'garagi - bu yerda o'quvchilar turli xil sport turlari bilan shug'ullanadilar.</li>
</ol>
```

**5-qadam: Sahifani brauzerda ochish**

* `maktab.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

**Tushuntirish:**

Bu loyihada biz HTMLning asosiy elementlaridan foydalanib, maktab haqida ma'lumotlarni o'z ichiga olgan veb-sahifa yaratdik. `<img>` tegi rasm qo'shish uchun, `<a>` tegi havola yaratish uchun, `<ul>` va `<ol>` teglari esa tartibsiz va tartibli ro'yxatlar yaratish uchun ishlatildi.

Ushbu loyihani o'zingizning maktabingiz haqidagi ma'lumotlar bilan to'ldiring. O'zingizga yoqqan boshqa elementlarni ham qo'shishingiz mumkin. Masalan, maktabingizning direktori haqida ma'lumot, maktabingizning qo'shimcha rasmlari va boshqalar.


### Mustaqil loyiha: "Mening sevimli mashg'ulotlarim"

Ushbu loyihada siz HTML bilimlaringizdan foydalanib, sevimli mashg'ulotlaringiz haqida veb-sahifa yaratasiz. 

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `mashgulotlar.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Mening sevimli mashg'ulotlarim").


**2-qadam: Sahifa tarkibini yaratish**

* Quyidagi elementlarni sahifangizga qo'shing:
    * `<h1>` tegi bilan sahifa sarlavhasini qo'shing (masalan, "Mening sevimli mashg'ulotlarim").
    * O'zingiz haqingizda qisqacha ma'lumot beruvchi bir nechta xatboshilar (`<p>`) yozing. 
    * Har bir sevimli mashg'ulotingiz uchun:
        * `<div>` tegi yordamida alohida bo'lim yarating.
        * `<h2>` tegi bilan mashg'ulot nomini sarlavha qiling.
        * Mashg'ulot haqida ma'lumot beruvchi xatboshilar (`<p>`) yozing.
        * Mashg'ulot bilan bog'liq rasm qo'shing (`<img>`). Rasm faylining manzilini va rasmning tavsifini tegishli atributlarda ko'rsating.
    * Mashg'ulotlaringiz haqida qo'shimcha ma'lumot olish uchun foydali havolalar ro'yxatini yarating. Havolalarni yaratish uchun `<a>` tegini ishlating.
    * Mashg'ulotlaringiz bilan bog'liq biror ro'yxat yarating. Ro'yxatni tartibli yoki tartibsiz (`<ol>` yoki `<ul>`) shaklida taqdim eting.


**Tushuntirish:**

* Masalan, siz kitob o'qishni yaxshi ko'rsangiz, quyidagicha bo'lim yaratishingiz mumkin:
    * `<div>` tegini oching.
    * Ichida `<h2>` tegi bilan "Kitob o'qish" deb yozing.
    * Kitob o'qish haqida bir nechta xatboshilar yozing. Masalan: "Men bo'sh vaqtimda kitob o'qishni yaxshi ko'raman. Kitoblar menga yangi bilimlar olishga va dunyoqarashimni kengaytirishga yordam beradi. Ayniqsa, tarixiy romanlar va fantastika janridagi kitoblarni o'qishni yoqtiraman".
    * Xatboshilardan keyin kitob o'qish bilan bog'liq rasm qo'shing. Buning uchun `<img>` tegini ishlating. Rasm faylining manzilini `src` atributida, rasmning tavsifini esa `alt` atributida ko'rsating. Masalan, `src="kitob.jpg"` va `alt="Kitob o'qiyotgan odam"`.
    * `<div>` tegini yoping.
* Agar sizda bir nechta sevimli kitoblar bo'lsa, ularning ro'yxatini tartibsiz ro'yxat shaklida ko'rsatishingiz mumkin. Buning uchun `<ul>` va `<li>` teglaridan foydalaning.


**3-qadam: Sahifani brauzerda ochish**

* `mashgulotlar.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

</details>


<details>
<summary>
HTML Jadvallar va Formalar
</summary>

Veb-sahifalarni yaratishda ma'lumotlarni tartibli va tushunarli ko'rsatish, shuningdek, foydalanuvchilar bilan o'zaro aloqada bo'lish juda muhim. HTML tili bizga bu maqsadlar uchun jadvallar va formalar kabi kuchli vositalarni taqdim etadi.

### Jadvallar bilan ishlash

Jadvallar ma'lumotlarni satr va ustunlarga ajratilgan holda strukturaviy tarzda taqdim etish imkonini beradi. Bu esa ma'lumotlarni oson o'qish, tahlil qilish va tushunishni ta'minlaydi. Jadvallarni kundalik hayotda ham tez-tez uchratamiz: dars jadvali, poyezdlar jadvali, mahsulotlar ro'yxati va boshqalar.

HTMLda jadvallarni yaratish uchun bir nechta teglar qo'llaniladi:

* **`<table>`**: Jadvalning asosiy konteyneri. Barcha jadval elementlari shu teg ichida joylashtiriladi.
    ```html
    <table>
      
    </table>
    ```

* **`<tr>`**: Jadvaldagi satrni (row) ifodalaydi.
    ```html
    <table>
      <tr>
          
      </tr>
    </table>
    ```

* **`<td>`**: Jadvaldagi katakchani (data cell) ifodalaydi. Har bir katakcha ma'lumotning bir qismini o'z ichiga oladi.
    ```html
    <table>
      <tr>
        <td>Olma</td>
        <td>5000 so'm</td>
      </tr>
    </table>
    ```

* **`<th>`**: Jadvaldagi sarlavha katakchasini (header cell) ifodalaydi. Sarlavha katakchalari odatda qalin shriftda ko'rsatiladi va ustun yoki satr uchun nom vazifasini bajaradi.
    ```html
    <table>
      <tr>
        <th>Mahsulot</th>
        <th>Narxi</th>
      </tr>
    </table>
    ```

**Jadvallarni Strukturaviy Tuzish**

Jadvallarni yanada tushunarli va foydalanuvchilarga qulay qilish uchun ularni quyidagi qismlarga ajratish mumkin:

* **`<caption>`**: Jadvalga sarlavha qo'yish uchun ishlatiladi. Sarlavha jadvalning tepasida joylashadi va uning mazmunini qisqacha ifodalaydi. Misol uchun, "O'quvchilar ro'yxati", "Mahsulotlar narxlari" va hokazo.
    ```html
    <table>
      <caption>O'quvchilar ro'yxati</caption>
      ...
    </table>
    ```

* **`<thead>`**: Jadvalning sarlavha qismini belgilaydi. Bu qismda ustun nomlari yoki boshqa sarlavha ma'lumotlari joylashtiriladi. Misol uchun, "Ism", "Familiya", "Yoshi" kabi ustun nomlari.
    ```html
    <table>
      <thead>
        <tr>
          <th>Ism</th>
          <th>Familiya</th>
          <th>Yoshi</th>
        </tr>
      </thead>
      ...
    </table>
    ```

* **`<tbody>`**: Jadvalning asosiy qismini belgilaydi. Bu qismda jadvalning ma'lumotlari satr va ustunlarga ajratilgan holda joylashtiriladi. Misol uchun, o'quvchilarning ismi, familiyasi va yoshi haqidagi ma'lumotlar.
    ```html
    <table>
      <tbody>
        <tr>
          <td>Ali</td>
          <td>Valiyev</td>
          <td>20</td>
        </tr>
        ...
      </tbody>
    </table>
    ```

* **`<tfoot>`**: Jadvalning pastki qismini belgilaydi. Bu qismda jadvalga oid xulosa ma'lumotlari, masalan, jami yoki o'rtacha qiymatlar ko'rsatilishi mumkin. Misol uchun, jadvaldagi barcha o'quvchilarning o'rtacha yoshi.
    ```html
    <table>
      <tfoot>
        <tr>
          <td colspan="2">Jami:</td>
          <td>45</td>
        </tr>
      </tfoot>
    </table>
    ```

**Katakchalarni Birlashtirish**

Ba'zan jadval katakchalarini bir nechta ustun yoki satrga yoyish kerak bo'ladi. Buning uchun `colspan` va `rowspan` atributlaridan foydalanish mumkin. 

* **`colspan`**: Katakchani gorizontal ravishda, ya'ni bir nechta ustunga yoyadi. Misol uchun, jadvalning birinchi satrida "Ism va Familiya" bitta katakchada joylashishi uchun `colspan="2"` atributidan foydalanish mumkin.
    ```html
    <table>
      <tr>
        <th colspan="2">Ism va Familiya</th>
        <th>Yoshi</th>
      </tr>
      ...
    </table>
    ```

* **`rowspan`**: Katakchani vertikal ravishda, ya'ni bir nechta satrga yoyadi. Misol uchun, jadvalning birinchi ustunida "1-guruh" nomi ikkita satrga yoyilishi uchun `rowspan="2"` atributidan foydalanish mumkin.
    ```html
    <table>
      <tr>
        <th rowspan="2">Guruh</th>
        <th>Ism</th>
        <th>Familiya</th>
      </tr>
      <tr>
        <td>Ali</td>
        <td>Valiyev</td>
      </tr>
    </table>
    ```

**Jadvallarni Formatlash**

Jadvallarni vizual jihatdan jozibador qilish va ma'lumotlarni yanada tushunarli qilish uchun CSS stillaridan foydalanish mumkin. CSS yordamida jadvallarning chegaralarini, fon rangini, shriftlarini va boshqa xususiyatlarini o'zgartirish mumkin.


### Formalar bilan ishlash

Formalar foydalanuvchilar bilan o'zaro aloqada bo'lishning asosiy vositalaridan biridir. Ular orqali foydalanuvchilar ma'lumotlarni kiritishlari, so'rovlar yuborishlari, fikr-mulohazalarini bildirishlari va boshqa ko'p narsalarni qilishlari mumkin.

HTMLda formalarni yaratish uchun `<form>` tegi ishlatiladi. Formada turli xil elementlar bo'lishi mumkin:

* **`<form>`**: Formani belgilaydi. Formadagi barcha elementlar shu teg ichida joylashtiriladi.
    ```html
    <form>
        
    </form>
    ```

* **`<input>`**: Turli xil ma'lumotlarni kiritish uchun ishlatiladi. `type` atributi yordamida input maydonining turini belgilash mumkin. Eng ko'p ishlatiladigan turlari:
    * `text`: Matn kiritish uchun. Misol uchun, ism, familiya, manzil va hokazo.
        ```html
        <input type="text" name="ism" placeholder="Ismingizni kiriting">
        ```
    * `password`: Parolni maxfiy kiritish uchun.
        ```html
        <input type="password" name="parol" placeholder="Parolni kiriting">
        ```
    * `email`: Email manzilini kiritish uchun.
        ```html
        <input type="email" name="email" placeholder="Emailingizni kiriting">
        ```
    * `number`: Raqam kiritish uchun. Misol uchun, yosh, telefon raqami va hokazo.
        ```html
        <input type="number" name="yosh" min="18" max="100">
        ```
    * `date`: Sanani tanlash uchun.
        ```html
        <input type="date" name="tug'ilgan_kun">
        ```
    * `radio`: Bir nechta variantdan birini tanlash uchun. Misol uchun, jinsni tanlashda.
        ```html
        <input type="radio" name="jins" value="erkak"> Erkak
        <input type="radio" name="jins" value="ayol"> Ayol
        ```
    * `checkbox`: Bir nechta variantni tanlash uchun. Misol uchun, qiziqishlarni tanlashda.
        ```html
        <input type="checkbox" name="qiziqishlar" value="sport"> Sport
        <input type="checkbox" name="qiziqishlar" value="musiqa"> Musiqa
        ```
    * `file`: Faylni yuklash uchun. Misol uchun, rasm, hujjat va hokazo.
        ```html
        <input type="file" name="fayl">
        ```
    * `submit`: Formani yuborish uchun.
        ```html
        <input type="submit" value="Yuborish">
        ```
    * `reset`: Formani tozalash uchun.
        ```html
        <input type="reset" value="Tozalash">
        ```
    * `hidden`: Foydalanuvchiga ko'rinmaydigan ma'lumotlarni yuborish uchun.
        ```html
        <input type="hidden" name="user_id" value="123">
        ```

* **`<textarea>`**: Ko'p qatorli matn kiritish uchun ishlatiladi. Misol uchun, xabar yoki sharh yozishda.
    ```html
    <textarea name="xabar" rows="5" cols="40"></textarea>
    ```

* **`<select>`**: Bir nechta variantdan birini tanlash uchun ishlatiladi. `<option>` tegi yordamida variantlarni belgilash mumkin. Misol uchun, shaharni tanlashda.
    ```html
    <select name="shahar">
      <option value="toshkent">Toshkent</option>
      <option value="samarqand">Samarqand</option>
      <option value="buxoro">Buxoro</option>
    </select>
    ```

* **`<label>`**: Input maydonlariga yorliq qo'yish uchun ishlatiladi.
    ```html
    <label for="ism">Ismingiz:</label>
    <input type="text" id="ism" name="ism">
    ```

**Formalarni Yuborish**

Formalarni yuborish uchun `action` va `method` atributlaridan foydalaniladi.

* **`action`**: Formani qaysi manzilga yuborish kerakligini belgilaydi. Odatda bu serverdagi skript faylining manzili bo'ladi.
* **`method`**: Formani qanday usulda yuborish kerakligini belgilaydi. Eng ko'p ishlatiladigan usullari:
    * `GET`: Ma'lumotlar URL manziliga qo'shiladi.
    * `POST`: Ma'lumotlar alohida so'rov bilan yuboriladi.

Umid qilamanki, bu batafsil ma'lumot va kod namunalari jadvallar va formalarni chuqurroq tushunishga yordam berdi. Ularni to'g'ri ishlatish orqali veb-sahifalarni yanada foydali va interaktiv qilish mumkin.


Xop bo'ladi, loyihani to'liq taqdim etaman va forma qismini bosqichlarga ajrataman.

### O'qituvchi boshchiligidagi loyiha: "Kutubxona katalogi"

Bu loyihada biz HTML bilimlarimizdan foydalanib, kutubxona katalogi jadvalini va yangi kitob qo'shish uchun formani yaratuvchi veb-sahifa yaratamiz.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating (masalan, Notepad, Sublime Text, VS Code).
* Faylni `kutubxona.html` deb nomlang va saqlang.
* Faylga quyidagi asosiy HTML tuzilishini qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Kutubxona katalogi</title>
</head>
<body>

</body>
</html>
```

**2-qadam: Jadvalni yaratish**

* `<body>` teglari ichida `<table>` tegini qo'shing.
* Jadvalga sarlavha qo'shing (`<caption>`). Masalan, "Kutubxona katalogi".
* Jadval sarlavhasini yaratish uchun `<thead>` tegini, so'ngra `<tr>` tegini va har bir ustun uchun `<th>` tegini qo'shing. Masalan, "№", "Kitob nomi", "Muallifi", "Nashr yili" va "Mavjudligi".

```html
<table>
  <caption>Kutubxona katalogi</caption>
  <thead>
    <tr>
      <th>№</th>
      <th>Kitob nomi</th>
      <th>Muallifi</th>
      <th>Nashr yili</th>
      <th>Mavjudligi</th>
    </tr>
  </thead>
  
</table>
```

**3-qadam: Jadvalga ma'lumotlarni qo'shish**

* Jadvalning asosiy qismini yaratish uchun `<tbody>` tegini qo'shing.
* Har bir kitob uchun `<tr>` tegini va har bir ma'lumot uchun `<td>` tegini qo'shing.
* Birinchi ustunda kitobning tartib raqamini ko'rsating.
* Ikkinchi ustunda kitob nomini ko'rsating.
* Uchinchi ustunda kitob muallifini ko'rsating.
* To'rtinchi ustunda kitob nashr etilgan yilni ko'rsating.
* Beshinchi ustunda kitobning mavjudligini ko'rsating ("Ha" yoki "Yo'q").

```html
<tbody>
  <tr>
    <td>1</td>
    <td>Alpomish</td>
    <td>Xalq og'zaki ijodi</td>
    <td>1980</td>
    <td>Ha</td>
  </tr>
  <tr>
    <td>2</td>
    <td>O'tkan kunlar</td>
    <td>Abdulla Qodiriy</td>
    <td>1925</td>
    <td>Ha</td>
  </tr>
  </tbody>
```

**4-qadam: Jadvalga qo'shimcha elementlar qo'shish**

* Jadvalning pastki qismini yaratish uchun `<tfoot>` tegini qo'shing.
* `<tfoot>` ichida `<tr>` va `<td>` teglaridan foydalanib, jadvalga oid xulosa ma'lumotlarini qo'shing. Masalan, "Jami kitoblar soni:".
* `colspan` atributidan foydalanib, "Jami kitoblar soni:" katakchasini bir nechta ustunga yoying.

```html
<tfoot>
  <tr>
    <td colspan="4">Jami kitoblar soni:</td>
    <td>2</td>
  </tr>
</tfoot>
```

**5-qadam: Formani yaratish**

* Jadvaldan keyin `<form>` tegini qo'shing.
* Formaga sarlavha qo'shing (`<h2>`). Masalan, "Yangi kitob qo'shish".

```html
<h2>Yangi kitob qo'shish</h2>
<form>

</form>
```

**6-qadam: Input maydonlarini qo'shish**

* Kitob nomi uchun matn maydoni (`<input type="text">`) qo'shing.
* Muallifi uchun matn maydoni (`<input type="text">`) qo'shing.
* Nashr yili uchun raqam maydoni (`<input type="number">`) qo'shing.
* Mavjudligi uchun radio tugmalar (`<input type="radio">`) qo'shing. "Ha" va "Yo'q" variantlarini yarating.

```html
<label for="kitob_nomi">Kitob nomi:</label><br>
<input type="text" id="kitob_nomi" name="kitob_nomi"><br><br>
<label for="muallifi">Muallifi:</label><br>
<input type="text" id="muallifi" name="muallifi"><br><br>
<label for="nashr_yili">Nashr yili:</label><br>
<input type="number" id="nashr_yili" name="nashr_yili"><br><br>
<label for="mavjudligi">Mavjudligi:</label><br>
<input type="radio" id="ha" name="mavjudligi" value="ha">
<label for="ha">Ha</label><br>
<input type="radio" id="yoq" name="mavjudligi" value="yoq">
<label for="yoq">Yo'q</label><br><br>
```

**7-qadam: Yuborish tugmasini qo'shish**

* Formaga yuborish tugmasini (`<input type="submit">`) qo'shing.

```html
<input type="submit" value="Qo'shish">
```

**8-qadam: Sahifani brauzerda ochish**

* `kutubxona.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

**Tushuntirish:**

Bu loyihada biz HTMLning jadval va forma elementlaridan foydalanib, kutubxona katalogi jadvalini va yangi kitob qo'shish uchun formani yaratdik. Formada turli xil input turlaridan foydalandik: matn maydoni, raqam maydoni va radio tugmalar.

Ushbu loyihani o'zingiz xohlagan kitoblar ro'yxati bilan to'ldiring. Formadagi "Qo'shish" tugmasi hozircha hech qanday funksiyani bajarmaydi, chunki biz hali JavaScriptni o'rganmadik. Keyingi darslarda JavaScript yordamida formani qanday qilib ishga tushirishni o'rganamiz.


### Mustaqil loyiha: "Mening kundalik ishlarim"

Ushbu loyihada siz HTML bilimlaringizdan foydalanib, kundalik ishlaringizni rejalashtiruvchi veb-sahifa yaratasiz. Sahifada jadval va forma bo'lishi kerak.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `kundalik.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Mening kundalik ishlarim").


**2-qadam: Sahifa tarkibini yaratish**

* Quyidagi elementlarni sahifangizga qo'shing:
    * `<h1>` tegi bilan sahifa sarlavhasini qo'shing (masalan, "Mening kundalik ishlarim").
    * Kundalik ishlaringizni rejalashtirish uchun jadval yarating (`<table>`). Jadvalda quyidagi ustunlar bo'lishi kerak:
        * "Vaqt"
        * "Dushanba"
        * "Seshanba"
        * "Chorshanba"
        * "Payshanba"
        * "Juma"
        * "Shanba"
        * "Yakshanba"
    * Jadvalga kamida 5 ta satr qo'shing va har bir satrda vaqt oralig'ini (masalan, "08:00 - 09:00") va haftaning har bir kuni uchun rejalashtirilgan ishlarni yozing.
    * Jadvaldan keyin yangi ish qo'shish uchun forma yarating (`<form>`). Formada quyidagi input maydonlari bo'lishi kerak:
        * Kunni tanlash uchun ochiladigan ro'yxat (`<select>`). Haftaning barcha kunlarini ro'yxatga qo'shing.
        * Vaqtni kiritish uchun matn maydoni (`<input type="text">`).
        * Ishni kiritish uchun matn maydoni (`<input type="text">`).
    * Formaga yuborish tugmasini (`<input type="submit">`) qo'shing.


**Tushuntirish:**

* **Jadvalni yaratish:**
    * Jadval yaratish uchun `<table>` tegini ishlatasiz.
    * Jadvalni sarlavha (`<thead>`), asosiy qism (`<tbody>`) va pastki qism (`<tfoot>`) ga ajratish uchun tegishli teglarni ishlating.
    * Jadval sarlavhasida (`<thead>`) haftaning kunlarini ustunlar sifatida ko'rsatish uchun `<th>` tegini ishlating.
    * Jadvalning asosiy qismida (`<tbody>`) har bir satr (`<tr>`) uchun vaqt oralig'ini va haftaning har bir kuni uchun rejalashtirilgan ishlarni katakchalar (`<td>`) ga yozing.
    * Jadvalning pastki qismida (`<tfoot>`) agar kerak bo'lsa, qo'shimcha ma'lumotlarni (masalan, "Jami ishlar soni") ko'rsatishingiz mumkin.

* **Formani yaratish:**
    * Formani yaratish uchun `<form>` tegini ishlatasiz.
    * Formada input maydonlariga yorliqlar qo'yish uchun `<label>` tegini ishlating.
    * Kunni tanlash uchun `<select>` tegini va uning ichida haftaning har bir kuni uchun `<option>` tegini ishlating.
    * Vaqtni va ishni kiritish uchun `<input type="text">` maydonlarini ishlating.
    * Formaga yuborish tugmasini qo'shish uchun `<input type="submit">` tegini ishlating.

* **Eslatma:** Formadagi "Yuborish" tugmasi hozircha hech qanday funksiyani bajarmaydi, chunki biz hali JavaScriptni o'rganmadik. Keyingi darslarda JavaScript yordamida formani qanday qilib ishga tushirishni o'rganamiz.


**3-qadam: Sahifani brauzerda ochish**

* `kundalik.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.


</details>

<details>
<summary>
HTML Semantik Teglar va Atributlar
</summary>

Veb-sahifalarni yaratishda nafaqat kontentni ko'rsatish, balki uni ma'no jihatidan ham to'g'ri tuzish muhim ahamiyatga ega. Buning uchun HTML bizga semantik teglar va atributlarni taqdim etadi. Semantik teglar veb-sahifaning tuzilishini va mazmunini aniqroq ifodalashga yordam beradi, atributlar esa teglarga qo'shimcha ma'lumotlarni qo'shish imkonini beradi. Bu esa brauzerlar, qidiruv tizimlari va ekran o'quvchi dasturlar uchun sahifaning mazmunini yaxshiroq tushunish imkonini beradi, shuningdek, veb-sahifalarni yanada qulay va optimallashtirilgan qiladi.

### Semantik Teglar

Semantik teglar sahifaning turli qismlarini ma'no jihatidan ajratish uchun ishlatiladi. Ba'zi asosiy semantik teglar:

* **`<header>`**: Sahifa yoki bo'limning sarlavha qismini belgilaydi. Odatda sayt nomi, navigatsiya menyusi va boshqa kirish ma'lumotlari joylashtiriladi.
    ```html
    <header>
      <h1>Sayt nomi</h1>
      <nav>
        <ul>
          <li><a href="#">Bosh sahifa</a></li>
          <li><a href="#">Biz haqimizda</a></li>
          <li><a href="#">Aloqa</a></li>
        </ul>
      </nav>
    </header>
    ```

* **`<nav>`**: Navigatsiya havolalarini o'z ichiga oladi. Odatda menyu yaratish uchun ishlatiladi.
    ```html
    <nav>
      <ul>
        <li><a href="#">Bosh sahifa</a></li>
        <li><a href="#">Biz haqimizda</a></li>
        <li><a href="#">Aloqa</a></li>
      </ul>
    </nav>
    ```

* **`<main>`**: Sahifaning asosiy kontentini belgilaydi. Har bir sahifada faqat bitta `<main>` tegi bo'lishi kerak.
    ```html
    <main>
      <article>
        <h2>Maqola sarlavhasi</h2>
        <p>Maqola matni...</p>
      </article>
    </main>
    ```

* **`<article>`**: Mustaqil kontentni belgilaydi. Masalan, blog posti, yangiliklar maqolasi yoki forumdagi xabar.
    ```html
    <article>
      <h2>Maqola sarlavhasi</h2>
      <p>Maqola matni...</p>
    </article>
    ```

* **`<aside>`**: Asosiy kontentga bevosita aloqador bo'lmagan kontentni belgilaydi. Masalan, yon panel, reklama yoki tegishli havolalar.
    ```html
    <aside>
      <h2>Tegishli havolalar</h2>
      <ul>
        <li><a href="#">Havola 1</a></li>
        <li><a href="#">Havola 2</a></li>
      </ul>
    </aside>
    ```

* **`<footer>`**: Sahifa yoki bo'limning pastki qismini belgilaydi. Odatda mualliflik huquqi, aloqa ma'lumotlari va boshqa qo'shimcha ma'lumotlar joylashtiriladi.
    ```html
    <footer>
      <p>&copy; 2024 Sayt nomi</p>
    </footer>
    ```

* **`<section>`**: Sahifaning mantiqiy bo'limini belgilaydi. Masalan, "Kirish", "Xizmatlar", "Aloqa" kabi bo'limlar.
    ```html
    <section>
      <h2>Xizmatlar</h2>
      <p>Bizning xizmatlarimiz ro'yxati...</p>
    </section>
    ```

### Atributlar

Atributlar HTML teglariga qo'shimcha ma'lumot berish uchun ishlatiladi. Ular tegning ochilish qismida yoziladi va `atribut="qiymat"` formatida bo'ladi.

Ba'zi asosiy atributlar:

* **`class`**: Elementga CSS stillarini qo'llash uchun ishlatiladi. Bir nechta elementga bir xil stillarni qo'llash uchun ishlatiladi.
    ```html
    <p class="qizil-matn">Bu xatboshi qizil rangda bo'ladi.</p>
    ```

* **`id`**: Elementga noyob identifikator berish uchun ishlatiladi. Sahifada faqat bitta elementda ma'lum bir `id` bo'lishi mumkin. JavaScript orqali elementlarga murojaat qilish uchun ishlatiladi.
    ```html
    <div id="asosiy-kontent">Bu asosiy kontent.</div>
    ```

* **`title`**: Element haqida qo'shimcha ma'lumot berish uchun ishlatiladi. Foydalanuvchi sichqoncha kursorini element ustiga olib borganda, bu ma'lumot tooltip shaklida ko'rsatiladi.
    ```html
    <a href="#" title="Kun.uz saytiga o'tish">Kun.uz</a>
    ```

* **`lang`**: Elementning tilini belgilaydi. Masalan, `<p lang="uz">` o'zbek tilidagi xatboshini belgilaydi.
    ```html
    <p lang="uz">Bu xatboshi o'zbek tilida.</p>
    ```

* **`data-*`**: Elementga maxsus ma'lumotlarni saqlash uchun ishlatiladi. JavaScript orqali bu ma'lumotlarga murojaat qilish mumkin.
    ```html
    <div data-user-id="123">Foydalanuvchi ma'lumotlari</div>
    ```

Semantik teglar va atributlarni to'g'ri ishlatish orqali veb-sahifalarni yanada tushunarli, qulay va optimallashtirilgan qilish mumkin.

### O'qituvchi boshchiligidagi loyiha: "Shaxsiy blog"

Ushbu loyihada biz birgalikda HTML bilimlarimizdan foydalanib, semantik teglar yordamida shaxsiy blog sahifasini yaratamiz. Men har bir qadamni tushuntirib beraman va siz meni kuzatib, kodni yozasiz.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating (masalan, Notepad, Sublime Text, VS Code).
* Faylni `blog.html` deb nomlang va saqlang.
* Faylga quyidagi asosiy HTML tuzilishini qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Mening blogim</title>
</head>
<body>

</body>
</html>
```

**2-qadam: Sahifa sarlavhasini yaratish**

* `<body>` teglari ichida `<header>` tegini qo'shing.
* `<header>` tegi ichida `<h1>` tegi bilan blogingiz nomini yozing. Masalan, "Mening blogim".
* Blogingiz haqida qisqacha ma'lumot beruvchi xatboshini (`<p>`) qo'shing.

```html
<header>
  <h1>Mening blogim</h1>
  <p>Bu mening shaxsiy blogim, bu yerda men o'z fikrlarim, tajribalarim va qiziqishlarim bilan o'rtoqlashaman.</p>
</header>
```

**3-qadam: Navigatsiya menyusini yaratish**

* `<header>` tegi ichida `<nav>` tegini qo'shing.
* `<nav>` tegi ichida tartibsiz ro'yxat (`<ul>`) yarating.
* Ro'yxat elementlari (`<li>`) sifatida blogingizdagi turli bo'limlarga havolalar (`<a>`) qo'shing. Masalan, "Bosh sahifa", "Maqolalar", "Loyihalar", "Aloqa".

```html
<nav>
  <ul>
    <li><a href="#">Bosh sahifa</a></li>
    <li><a href="#">Maqolalar</a></li>
    <li><a href="#">Loyihalar</a></li>
    <li><a href="#">Aloqa</a></li>
  </ul>
</nav>
```

**4-qadam: Asosiy kontentni yaratish**

* `<header>` tegi dan keyin `<main>` tegini qo'shing.
* `<main>` tegi ichida `<article>` tegini qo'shing.
* `<article>` tegi ichida maqola sarlavhasini (`<h2>`) va maqola matnini (`<p>`) yozing.

```html
<main>
  <article>
    <h2>Mening birinchi maqolam</h2>
    <p>Bu mening blogimdagi birinchi maqolam. Bu yerda men ... haqida yozmoqchiman.</p>
  </article>
</main>
```

**5-qadam: Yon panelni yaratish**

* `<main>` tegi dan keyin `<aside>` tegini qo'shing.
* `<aside>` tegi ichida tegishli havolalar yoki boshqa qo'shimcha ma'lumotlarni joylashtiring.

```html
<aside>
  <h2>Tegishli havolalar</h2>
  <ul>
    <li><a href="#">Havola 1</a></li>
    <li><a href="#">Havola 2</a></li>
  </ul>
</aside>
```

**6-qadam: Sahifa pastki qismini yaratish**

* `<aside>` tegi dan keyin `<footer>` tegini qo'shing.
* `<footer>` tegi ichida mualliflik huquqi haqida ma'lumotni (`<p>`) yozing.

```html
<footer>
  <p>&copy; 2024 Mening blogim</p>
</footer>
```

**7-qadam: Sahifani brauzerda ochish**

* `blog.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

**Tushuntirish:**

Bu loyihada biz HTMLning semantik teglaridan foydalanib, shaxsiy blog sahifasini yaratdik. `<header>`, `<nav>`, `<main>`, `<article>`, `<aside>` va `<footer>` teglaridan foydalanib, sahifaning tuzilishini va mazmunini aniqroq ifodaladik.

Ushbu loyihani o'zingizning blogingiz ma'lumotlari bilan to'ldiring. Maqolalar, loyihalar va boshqa bo'limlarga o'zingizning kontentingizni qo'shing.


### Mustaqil loyiha: "Mening sevimli shaxrim"

Ushbu loyihada siz HTML bilimlaringizdan foydalanib, sevimli shahringiz haqida veb-sahifa yaratasiz. Sahifada semantik teglar va atributlardan foydalaning.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `shahar.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Mening sevimli shaxrim").


**2-qadam: Sahifa tarkibini yaratish**

* Quyidagi elementlarni sahifangizga qo'shing:
    * Sahifa sarlavhasi uchun `<header>` tegini ishlating. Sarlavhada shahar nomi (`<h1>`) va shahar haqida qisqacha ma'lumot (`<p>`) bo'lishi kerak.
    * Navigatsiya menyusi uchun `<nav>` tegini ishlating. Menyuda shaharning turli joylari haqida ma'lumot beruvchi bo'limlarga havolalar (`<a>`) bo'lishi kerak. Masalan, "Tarixi", "Diqqatga sazovor joylar", "Madaniyati", "Rasmlar".
    * Sahifaning asosiy kontenti uchun `<main>` tegini ishlating. Asosiy kontentda shahar haqida batafsil ma'lumot beruvchi bo'limlar (`<section>`) bo'lishi kerak. Har bir bo'limda sarlavha (`<h2>`) va matn (`<p>`) bo'lishi kerak.
    * Qo'shimcha ma'lumotlar uchun `<aside>` tegini ishlating. Qo'shimcha ma'lumotlarda shahar haqida qiziqarli faktlar, statistik ma'lumotlar yoki shahar bilan bog'liq mashhur shaxslar haqida ma'lumotlar bo'lishi mumkin.
    * Sahifa pastki qismi uchun `<footer>` tegini ishlating. Pastki qismda mualliflik huquqi haqida ma'lumot va shaharning rasmiy veb-saytiga havola bo'lishi mumkin.
    * Shaharning rasmlarini qo'shing (`<img>`). Rasmlarga tavsif (`alt`) atributini qo'shishni unutmang.
    * Tegishli atributlardan foydalaning. Masalan, `lang` atributidan foydalanib, sahifaning tilini belgilang.


**Tushuntirish:**

* Semantik teglarni to'g'ri ishlatishga e'tibor bering. Har bir teg o'z maqsadiga muvofiq ishlatilishi kerak.
* Sahifaning tuzilishini mantiqiy qismlarga ajrating. Masalan, shahar tarixi, diqqatga sazovor joylari, madaniyati va boshqalar uchun alohida bo'limlar yarating.
* Atributlardan foydalanib, teglarga qo'shimcha ma'lumotlarni qo'shing. Masalan, `class` atributidan foydalanib, CSS stillarini qo'llashingiz mumkin.
* Rasmlarga tavsif (`alt`) atributini qo'shishni unutmang. Bu atribut rasm ko'rsatilmasa (masalan, internet aloqasi yo'q bo'lsa) yoki ko'zi ojiz foydalanuvchilar uchun ekran o'quvchi dasturlar tomonidan ishlatiladi.


**3-qadam: Sahifani brauzerda ochish**

* `shahar.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.
</details>