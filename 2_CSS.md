<details>
<summary>
CSS Stillash Asoslari
</summary>


Veb-sahifalar faqatgina matn va rasmlardan iborat bo'lmasligi kerak. Ular chiroyli, jozibador va foydalanuvchilar uchun qulay bo'lishi kerak. Buning uchun bizga CSS (Cascading Style Sheets) yordam beradi. CSS yordamida veb-sahifalarning ranglarini, shriftlarini, joylashuvini va boshqa ko'plab xususiyatlarini o'zgartirish mumkin.

### 1-qism: CSS bilan tanishuv

CSS stillarini HTMLga uch xil usulda qo'shish mumkin:

1. **Tashqi fayl (External CSS):** Bu usulda CSS stillari alohida faylda saqlanadi va HTML hujjatga `<link>` tegi yordamida ulanadi. Bu usul eng keng tarqalgan va tavsiya etilgan usul hisoblanadi. Chunki u kodni tartibli saqlashga va bir nechta HTML hujjatlarda bir xil CSS stillaridan foydalanishga imkon beradi.

    ```html
    <!DOCTYPE html>
    <html lang="uz">
    <head>
      <meta charset="UTF-8">
      <title>Mening sahifam</title>
      <link rel="stylesheet" href="style.css">
    </head>
    <body>
    
    </body>
    </html>
    ```

2. **Ichki stil (Internal CSS):** Bu usulda CSS stillari HTML hujjatning `<head>` qismida `<style>` teglari ichida yoziladi. Bu usul faqat bitta HTML hujjatda ishlatiladigan stillar uchun qulay.

    ```html
    <!DOCTYPE html>
    <html lang="uz">
    <head>
      <meta charset="UTF-8">
      <title>Mening sahifam</title>
      <style>
        body {
          background-color: lightblue;
        }
      </style>
    </head>
    <body>
    
    </body>
    </html>
    ```

3. **Inline stil (Inline CSS):** Bu usulda CSS stillari to'g'ridan-to'g'ri HTML tegida `style` atributi sifatida yoziladi. Bu usul faqat bitta elementga stil berish uchun ishlatiladi va kamdan-kam hollarda tavsiya etiladi.

    ```html
    <!DOCTYPE html>
    <html lang="uz">
    <head>
      <meta charset="UTF-8">
      <title>Mening sahifam</title>
    </head>
    <body>
    
      <p style="color: blue;">Bu xatboshi ko'k rangda bo'ladi.</p>
    
    </body>
    </html>
    ```


### CSS Selektorlari

CSS selektorlari HTML elementlarini tanlash uchun ishlatiladi. Ular CSS qoidalarining qaysi elementlarga qo'llanilishini belgilaydi.

Ba'zi asosiy selektorlar:

* **Element selektori:** Element nomiga ko'ra elementlarni tanlaydi. Masalan, `p` barcha `<p>` elementlarini tanlaydi.
    ```css
    p {
      color: red;
    }
    ```

* **ID selektori:** Elementning `id` atributiga ko'ra elementni tanlaydi. `#` belgisi bilan boshlanadi. Masalan, `#asosiy-kontent` `id="asosiy-kontent"` bo'lgan elementni tanlaydi.
    ```css
    #asosiy-kontent {
      background-color: lightgray;
    }
    ```

* **Class selektori:** Elementning `class` atributiga ko'ra elementlarni tanlaydi. `.` belgisi bilan boshlanadi. Masalan, `.qizil-matn` `class="qizil-matn"` bo'lgan barcha elementlarni tanlaydi.
    ```css
    .qizil-matn {
      color: red;
    }
    ```

* **Universal selektor:** Barcha elementlarni tanlaydi. `*` belgisi bilan ifodalanadi.
    ```css
    * {
      margin: 0;
      padding: 0;
    }
    ```

* **Guruhlash:** Bir nechta selektorni vergul bilan ajratib, ularga bir xil stillarni qo'llash mumkin.
    ```css
    h1, h2, h3 {
      font-family: sans-serif;
    }
    ```

### CSS Xossalari va Qiymatlari

CSS xossalari elementlarning ko'rinishini o'zgartirish uchun ishlatiladi. Har bir xossa o'z qiymatiga ega.

Ba'zi asosiy xossalar:

* **`color`**: Matn rangini o'zgartiradi.
    ```css
    p {
      color: blue;
    }
    ```

* **`background-color`**: Elementning fon rangini o'zgartiradi.
    ```css
    body {
      background-color: lightgray;
    }
    ```

* **`font-family`**: Shrift turini o'zgartiradi.
    ```css
    h1 {
      font-family: Arial, sans-serif;
    }
    ```

* **`font-size`**: Shrift o'lchamini o'zgartiradi.
    ```css
    p {
      font-size: 16px;
    }
    ```

* **`text-align`**: Matnni tekislashni o'zgartiradi (`left`, `center`, `right`).
    ```css
    h2 {
      text-align: center;
    }
    ```

* **`margin`**: Elementning tashqi chegarasini o'zgartiradi.
    ```css
    div {
      margin: 20px;
    }
    ```

* **`padding`**: Elementning ichki chegarasini o'zgartiradi.
    ```css
    p {
      padding: 10px;
    }
    ```

CSS yordamida veb-sahifalarni xohlagancha stillash mumkin. Bu esa ularni chiroyli, jozibador va foydalanuvchilar uchun qulay qilish imkonini beradi.

Ha, tushunarli. Keling, CSS qismini batafsilroq qilib, faqat darsda ko'rsatilgan CSS xususiyatlaridan foydalanamiz.

### 2-qism: O'qituvchi boshchiligidagi loyiha: Fotogalereya (kengaytirilgan)

Ushbu loyihada biz CSS yordamida oddiy fotogalereya yaratamiz. Rasmlarni joylashtirish, ularga chegara va soya qo'shish, shuningdek, matnni formatlashni o'rganamiz.

**1-qadam: HTML fayl yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating.
* Faylni `fotogalereya.html` deb nomlang va saqlang.
* Quyidagi HTML kodni faylga qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Fotogalereya</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <h1>Mening fotogalereyam</h1>

  <div class="galereya">
    <img src="rasm1.jpg" alt="Rasm 1">
    <img src="rasm2.jpg" alt="Rasm 2">
    <img src="rasm3.jpg" alt="Rasm 3">
  </div>

</body>
</html>
```

Bu kodda biz uchta rasmni o'z ichiga olgan `div` elementini yaratdik. `class="galereya"` atributi keyinchalik CSS yordamida ushbu elementni stillash uchun ishlatiladi. Shuningdek, sahifa sarlavhasi uchun `<h1>` tegini qo'shdik.

**2-qadam: CSS fayl yaratish**

* `fotogalereya.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Sahifa fon rangini o'zgartirish**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
body {
  background-color: lightblue;
}
```

Bu kod sahifaning fon rangini och ko'k rangga o'zgartiradi.

**4-qadam: Sarlavhani formatlash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
h1 {
  text-align: center;
  font-family: Arial, sans-serif;
  color: darkblue;
}
```

Bu kod sarlavhani markazga tekislaydi, shrift turini Arial ga o'zgartiradi va rangini to'q ko'k rangga o'zgartiradi.

**5-qadam: Rasmlarni joylashtirish**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.galereya {
  display: flex;
  justify-content: space-around;
  margin-top: 20px;
}
```

Bu kod `galereya` klassidagi elementlar uchun `flex` xususiyatini qo'lladi. Bu rasmlarni bir qatorda yonma-yon joylashtirishga imkon beradi. `justify-content: space-around;` xususiyati rasmlar orasidagi bo'shliqni teng taqsimlaydi. `margin-top: 20px;` xususiyati rasmlarni sarlavhadan 20px pastga tushiradi.

**6-qadam: Rasmlarga stil berish**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.galereya img {
  width: 300px;
  height: 200px;
  border: 5px solid black;
  box-shadow: 10px 10px 5px gray;
}
```

Bu kod `galereya` klassidagi elementlar ichidagi barcha `img` elementlarini tanlaydi. Biz bu yerda rasmlarning kengligi va balandligini, chegara qalinligi va rangini, shuningdek, soya xususiyatlarini o'zgartirdik.

**7-qadam: Sahifani brauzerda ochish**

* `fotogalereya.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

**Tushuntirish:**

Bu loyihada biz CSS yordamida oddiy fotogalereya yaratdik. `display: flex;` xususiyati yordamida rasmlarni bir qatorda joylashtirdik. `border` va `box-shadow` xususiyatlari yordamida rasmlarga chegara va soya qo'shdik. Shuningdek, sahifa fon rangini, sarlavha stilini va rasmlar orasidagi bo'shliqni o'zgartirdik.

Ushbu loyihani o'zingizning rasmlaringiz bilan to'ldiring. Rasmlar sonini va ularning xususiyatlarini o'zgartirishingiz mumkin. CSS yordamida fotogalereyani xohlagancha stillash mumkin.

### 3-qism: Mustaqil loyiha: "Motivatsion Poster"

Ushbu loyihada siz CSS bilimlaringizdan foydalanib, motivatsion poster yaratasiz. Posteringizda ilhomlantiruvchi iqtibos, muallif nomi va orqa fon rasmi bo'lishi kerak. Ranglar, shriftlar va matn xususiyatlarini qo'llab, posteringizni jozibador va ta'sirli qiling.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `poster.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Motivatsion Poster").
* Quyidagi elementlarni sahifangizga qo'shing:
    * Poster konteyneri uchun `<div>` tegi.
    * Ilhomlantiruvchi iqtibos uchun `<blockquote>` tegi.
    * Muallif nomi uchun `<cite>` tegi.

**2-qadam: CSS fayl yaratish**

* `poster.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Sahifa stilini qo'llash**

* `style.css` faylida `body` selektoridan foydalaning.
* Sahifa fon rangini `#f0f0f0` (och kulrang) ga o'zgartiring.

**Tushuntirish:**

Bu yerda biz `body` selektori yordamida butun sahifa uchun stillarni belgilayapmiz. `background-color` xossasi fon rangini o'zgartirish uchun ishlatiladi.

**4-qadam: Poster konteyneri stilini qo'llash**

* `style.css` faylida `div` selektoridan foydalaning.
* Konteynerga `600px` kenglik bering.
* Konteynerga fon rasmi qo'shing. Fon rasmi sifatida ilhomlantiruvchi rasmni tanlang.
* Fon rasmini takrorlamaslikni belgilang (`background-repeat: no-repeat;`).
* Fon rasmini konteyner o'lchamiga moslab cho'zing (`background-size: cover;`).
* Konteyner ichida 30 piksel bo'sh joy qoldiring (`padding: 30px;`).
* Konteynerni sahifa bo'ylab markazga tekislang (`margin: 50px auto;`).

**Tushuntirish:**

`div` selektori yordamida biz poster konteyneri uchun stillarni belgilaymiz. `background-image` xossasi fon rasmini qo'shish uchun ishlatiladi. `background-repeat`, `background-size` xossalari esa fon rasmining takrorlanishini va o'lchamini boshqaradi. `padding` xossasi elementning ichki chegaralarini belgilaydi. `margin` xossasi esa elementning tashqi chegaralarini belgilaydi.

**5-qadam: Iqtibos stilini qo'llash**

* `style.css` faylida `blockquote` selektoridan foydalaning.
* Iqtibos uchun `2em` shrift o'lchamini tanlang.
* Iqtibos rangini `#fff` (oq) ga o'zgartiring.
* Iqtibos matnini kursiv qiling (`font-style: italic;`).
* Iqtibos matniga `2px 2px 4px #000` (qora) soya qo'shing.
* Iqtibosning pastki qismidan 20 piksel bo'sh joy qoldiring (`margin-bottom: 20px;`).

**Tushuntirish:**

`blockquote` selektori yordamida biz iqtibos uchun stillarni belgilaymiz. `font-size` xossasi matn o'lchamini o'zgartirish, `color` xossasi matn rangini o'zgartirish, `font-style` xossasi esa matn stilini o'zgartirish uchun ishlatiladi.

**6-qadam: Muallif nomi stilini qo'llash**

* `style.css` faylida `cite` selektoridan foydalaning.
* Muallif nomi uchun `1.5em` shrift o'lchamini tanlang.
* Muallif nomi rangini `#e67e22` (to'q sariq) ga o'zgartiring.
* Muallif nomini o'ng tomonga tekislang (`text-align: right;`).

**Tushuntirish:**

`cite` selektori yordamida biz muallif nomi uchun stillarni belgilaymiz. `text-align` xossasi matnni tekislash uchun ishlatiladi.

**7-qadam: Sahifani brauzerda ochish**

* `poster.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

Ushbu loyihada biz CSSning ranglar va matn xususiyatlaridan foydalanib, motivatsion poster yaratdik. Bu posterda ilhomlantiruvchi iqtibos, muallif nomi va orqa fon rasmi mavjud. Siz ushbu maketni asos qilib, o'zingizning posterlaringizni yaratishingiz mumkin.

</details>

<details>
<summary>
CSS Ranglar va Matn Xususiyatlari
</summary>


## CSS Ranglar va Matn Xususiyatlari

Veb-sahifalarni yanada jozibador va o'qilishi oson qilish uchun CSS yordamida ranglar va matn xususiyatlarini boshqarish juda muhim. Bu darsda biz ranglarni qo'llashning turli usullari va matnni formatlash uchun asosiy CSS xususiyatlarini ko'rib chiqamiz.


### 1-qism: Ranglar va Matn Stillari bilan tanishuv

CSS sizga veb-sahifalaringizdagi elementlarning rangini va matn ko'rinishini o'zgartirishga imkon beradi. Bu orqali siz o'zingizning dizayningizni yaratishingiz, ma'lumotlarni ta'kidlashingiz va foydalanuvchi tajribasini yaxshilashingiz mumkin.

**Ranglarni belgilash**

CSSda ranglarni belgilashning bir necha yo'li mavjud:

* **Rang nomlari:**  Bu eng oddiy usul. Siz shunchaki ingliz tilidagi rang nomini yozasiz, masalan, `red`, `blue`, `green`, `black`, `white`, `orange`, `purple` va hokazo.

```css
h1 {
  color: red; /* Sarlavha qizil rangda bo'ladi */
}

p {
  color: blue; /* Paragraf ko'k rangda bo'ladi */
}
```

* **Hex kodlari:** Bu usulda ranglar `#` belgisi va oltita belgidan iborat kod bilan ifodalanadi. Har bir belgi 0 dan 9 gacha bo'lgan raqam yoki A dan F gacha bo'lgan harf bo'lishi mumkin. Masalan, `#ff0000` qizil rangni, `#0000ff` ko'k rangni, `#00ff00` yashil rangni ifodalaydi.

```css
body {
  background-color: #f0f0f0; /* Sahifa foni och kulrang rangda bo'ladi */
}

a {
  color: #007bff; /* Havolalar ko'k rangda bo'ladi */
}
```

* **RGB qiymatlari:** Bu usulda ranglar qizil (Red), yashil (Green) va ko'k (Blue) ranglarning aralashmasi sifatida ifodalanadi. Har bir rang uchun 0 dan 255 gacha bo'lgan qiymat beriladi. Masalan, `rgb(255, 0, 0)` qizil rangni, `rgb(0, 0, 255)` ko'k rangni, `rgb(0, 255, 0)` yashil rangni ifodalaydi.

```css
.box {
  background-color: rgb(255, 165, 0); /* Quti foni to'q sariq rangda bo'ladi */
}

.text {
  color: rgb(128, 0, 128); /* Matn binafsha rangda bo'ladi */
}
```

* **RGBA qiymatlari:** Bu usul RGB ga o'xshash, lekin qo'shimcha ravishda rangning shaffoflik darajasini ham belgilash imkonini beradi. Shaffoflik qiymati 0 dan 1 gacha bo'lishi mumkin, bu yerda 0 to'liq shaffoflikni, 1 esa to'liq shaffof emaslikni bildiradi. Masalan, `rgba(255, 0, 0, 0.5)` yarim shaffof qizil rangni ifodalaydi.

```css
.overlay {
  background-color: rgba(0, 0, 0, 0.5); /* Qoplama yarim shaffof qora rangda bo'ladi */
}

.highlight {
  background-color: rgba(255, 255, 0, 0.7); /* Ta'kidlangan matn yarim shaffof sariq rangda bo'ladi */
}
```

* **HSL va HSLA qiymatlari:** Bu usulda ranglar rang burchagi (Hue), to'yinganlik (Saturation) va yorqinlik (Lightness) bilan ifodalanadi. HSL qiymatlariga qo'shimcha ravishda, HSLA qiymatlari rangning shaffoflik darajasini ham belgilash imkonini beradi.

```css
.button {
  background-color: hsl(120, 100%, 50%); /* Tugma yashil rangda bo'ladi */
}

.link {
  color: hsla(240, 100%, 50%, 0.8); /* Havola yarim shaffof ko'k rangda bo'ladi */
}
```

**Matn xususiyatlari**

CSSda matnni formatlash uchun ko'plab xususiyatlar mavjud. Ular yordamida siz matnning shriftini, o'lchamini, stilini, rangini, hizalamasini va boshqa ko'plab xususiyatlarini o'zgartirishingiz mumkin.

* **`color`:** Matn rangini o'zgartiradi. Yuqorida ko'rsatilgan rang belgilash usullaridan foydalanishingiz mumkin.

```css
p {
  color: #333; /* Matn quyuq kulrang rangda bo'ladi */
}
```

* **`font-family`:** Matn shriftini o'zgartiradi. Siz shrift nomini yoki shrift oilasini ko'rsatishingiz mumkin.

```css
h1 {
  font-family: "Times New Roman", serif; /* Sarlavha Times New Roman shriftida bo'ladi */
}

p {
  font-family: Arial, sans-serif; /* Paragraf Arial shriftida bo'ladi */
}
```

* **`font-size`:** Matn o'lchamini o'zgartiradi. Siz piksel (`px`), em yoki foiz (`%`) kabi o'lchov birliklaridan foydalanishingiz mumkin.

```css
h2 {
  font-size: 24px; /* Sarlavha 24 piksel o'lchamda bo'ladi */
}

p {
  font-size: 1.2em; /* Paragraf hozirgi shrift o'lchamiga nisbatan 1.2 barobar katta bo'ladi */
}
```

* **`font-weight`:** Matn qalinligini o'zgartiradi. Siz `normal`, `bold`, `bolder`, `lighter` yoki 100 dan 900 gacha bo'lgan raqamlarni ishlatishingiz mumkin.

```css
strong {
  font-weight: bold; /* Matn qalin bo'ladi */
}

.thin {
  font-weight: 300; /* Matn ingichka bo'ladi */
}
```

* **`font-style`:** Matn stilini o'zgartiradi. Siz `normal`, `italic` yoki `oblique` qiymatlaridan foydalanishingiz mumkin.

    * `normal`: Matn oddiy ko'rinishda bo'ladi (qiyshaytirilmagan).
    * `italic`: Matn kursiv ko'rinishda bo'ladi.
    * `oblique`: Matn qiyshiq ko'rinishda bo'ladi. `italic` ga o'xshash, lekin ba'zi shriftlarda farq qilishi mumkin.

```css
.normal-text {
  font-style: normal; 
}

.italic-text {
  font-style: italic; 
}

.oblique-text {
  font-style: oblique; 
}
```

* **`text-align`:** Matnni tekislashni o'zgartiradi. 

    * `left`: Matn chap tomonga tekislanadi.
    * `center`: Matn markazga tekislanadi.
    * `right`: Matn o'ng tomonga tekislanadi.
    * `justify`: Matn ikki tomonga tekislanadi (har ikki chekkaga to'g'ri keladi).

```css
.left-align {
  text-align: left; 
}

.center-align {
  text-align: center;
}

.right-align {
  text-align: right;
}

.justify-align {
  text-align: justify; 
}
```

* **`text-decoration`:** Matnga chiziq qo'shish yoki olib tashlash uchun ishlatiladi. 

    * `none`: Hech qanday chiziq qo'shilmaydi.
    * `underline`: Matn ostiga chiziq qo'shiladi.
    * `overline`: Matn ustiga chiziq qo'shiladi.
    * `line-through`: Matn ustidan chiziq chiziladi (o'chirilgan matn effekti).

```css
.no-decoration {
  text-decoration: none; 
}

.underline-text {
  text-decoration: underline; 
}

.overline-text {
  text-decoration: overline; 
}

.line-through-text {
  text-decoration: line-through; 
}
```

* **`text-transform`:** Matnning katta-kichik harflarini o'zgartiradi. 

    * `none`: Harflar o'zgartirilmaydi.
    * `uppercase`: Barcha harflar katta bo'ladi.
    * `lowercase`: Barcha harflar kichik bo'ladi.
    * `capitalize`: Har bir so'zning birinchi harfi katta bo'ladi.

```css
.no-transform {
  text-transform: none; 
}

.uppercase-text {
  text-transform: uppercase; 
}

.lowercase-text {
  text-transform: lowercase; 
}

.capitalize-text {
  text-transform: capitalize; 
}
```

* **`line-height`:** Satrlar orasidagi masofani o'zgartiradi. Siz raqam, foiz yoki o'lchov birliklaridan foydalanishingiz mumkin.

```css
p {
  line-height: 1.5; /* Satrlar orasidagi masofa 1.5 barobar oshiriladi */
}
```

* **`letter-spacing`:** Harflar orasidagi masofani o'zgartiradi.

```css
h2 {
  letter-spacing: 2px; /* Harflar orasidagi masofa 2 pikselga oshiriladi */
}
```

* **`word-spacing`:** So'zlar orasidagi masofani o'zgartiradi.

```css
p {
  word-spacing: 5px; /* So'zlar orasidagi masofa 5 pikselga oshiriladi */
}
```

Bu xususiyatlarni birgalikda ishlatib, matnni xohlagancha formatlash va sahifalaringizni yanada jozibador qilish mumkin.

Keling, "She'r formati" loyihasi uchun 2-qismni qayta ko'rib chiqamiz.

### 2-qism: O'qituvchi boshchiligidagi loyiha: "She'r formati"

Ushbu loyihada biz CSS yordamida veb-sahifada she'rni chiroyli formatlaymiz. Matn rangini, shrift turini, o'lchamini, stilini, tekislashni va boshqa xususiyatlarini o'zgartirib, she'rga o'zgacha ko'rinish beramiz.

**1-qadam: HTML fayl yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating.
* Faylni `sher.html` deb nomlang va saqlang.
* Quyidagi HTML kodni faylga qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>She'r</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <h1>Yulduzli tun</h1>

  <p>
    Osmonda yulduzlar miltillaydi,<br>
    Oy nuri sochib, jilvalaydi.<br>
    Yuragim qo'shiq aytmoqda,<br>
    Sevgi haqida so'zlamoqda.
  </p>

  <p>
    Daraxtlar shivirlaydi mayin,<br>
    Shamol esa esaydi sayin.<br>
    Bu tun sehrli, go'zal,<br>
    Yulduzlar bilan to'la osmon.
  </p>

</body>
</html>
```

Oddiy HTML fayl yaratdik. `<h1>` tegi she'r sarlavhasi uchun, `<p>` teglari esa she'r misralari uchun ishlatilgan. `<br>` tegi har bir misrani yangi qatorga o'tkazish uchun ishlatilgan.


**2-qadam: CSS fayl yaratish**

* `sher.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

CSS stillarini yozish uchun alohida fayl yaratdik. Bu fayl HTML faylimizga ulanadi va unda yozilgan stillar veb-sahifamizning ko'rinishini o'zgartiradi.

**3-qadam: Sahifa stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
body {
  background-color: #f7f3e8; /* Och bej rang */
  font-family: Georgia, serif;
  color: #333; /* To'q kulrang */
  line-height: 1.8;
}
```

Sahifaning fon rangini och bej rangga o'zgartiramiz, matn uchun `Georgia` shriftini tanlaymiz (agar mavjud bo'lmasa, `serif` shrift ishlatiladi), matn rangini to'q kulrangga o'rnatamiz va satrlar orasidagi masofani oshiramiz.

**4-qadam: Sarlavha stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
h1 {
  text-align: center;
  font-size: 3em;
  color: #a52a2a; /* To'q qizil rang */
  margin-bottom: 20px;
}
```

Sarlavhani sahifaning markaziga joylashtiramiz, shrift o'lchamini kattalashtiramiz, rangini to'q qizilga o'zgartiramiz va sarlavha ostiga bo'sh joy qo'shamiz.

**5-qadam: Xatboshi stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
p {
  font-size: 1.2em;
  text-indent: 30px;
  margin-bottom: 20px;
}
```

Xatboshilarning shrift o'lchamini kattalashtiramiz, har bir xatboshining birinchi qatorini ichkariga siljitamiz (bu she'r formatlashda keng tarqalgan usul) va xatboshilar ostiga bo'sh joy qo'shamiz.

**6-qadam: Sahifani brauzerda ochish**

* `sher.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

### 3-qism: Mustaqil loyiha: "Mening Sevimli Mashg'ulotim"

Ushbu loyihada siz CSS bilimlaringizdan foydalanib, sevimli mashg'ulotingiz haqida veb-sahifa yaratasiz. Sahifada mashg'ulotingiz nomi, tavsifi, rasmlari va boshqa ma'lumotlar bo'lishi kerak. Orqa fon rasmlarini, chegaralarni va boshqa CSS xususiyatlarini qo'llab, sahifani jozibador qiling.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `mashgulot.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Mening Sevimli Mashg'ulotim").
* Quyidagi elementlarni sahifangizga qo'shing:
    * Mashg'ulotingiz nomi uchun `<h1>` tegini.
    * Mashg'ulotingiz haqida qisqacha ma'lumot uchun `<p>` tegini.
    * Mashg'ulotingiz bilan bog'liq rasmlar uchun bir nechta `<img>` tegi.
    * Agar kerak bo'lsa, qo'shimcha ma'lumotlar uchun `<div>` teglari ichida sarlavhalar (`<h2>`) va xatboshilar (`<p>`) dan foydalaning.

**2-qadam: CSS fayl yaratish**

* `mashgulot.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Sahifa stilini qo'llash**

* `style.css` faylida `body` selektoridan foydalaning.
* Sahifa fon rangini `#f5f5f5` (juda och kulrang) ga o'zgartiring.
* Matn rangini `#333` (quyuq kulrang) ga o'zgartiring.
* Sahifa uchun `'Roboto', sans-serif` shrift turini tanlang.
* Sahifaga fon rasmi qo'shing. Fon rasmi sifatida mashg'ulotingizga mos rasmni tanlang.
* Fon rasmini takrorlamaslikni belgilang (`background-repeat: no-repeat;`).
* Fon rasmini sahifaning o'ng yuqori burchagiga joylashtiring (`background-position: top right;`).
* Fon rasmini asl o'lchamida saqlang (`background-size: contain;`).

**Tushuntirish:**

Bu yerda biz `body` selektori yordamida butun sahifa uchun stillarni belgilayapmiz. `background-color` xossasi yordamida sahifa fon rangini juda och kulrangga (`#f5f5f5`) o'zgartiramiz. `color` xossasi yordamida matn rangini quyuq kulrangga (`#333`) o'rnatamiz. `font-family` xossasi yordamida matn uchun `'Roboto'` shriftini tanlaymiz, agar u foydalanuvchining kompyuterida mavjud bo'lmasa, `sans-serif` shriftlar oilasidan boshqa shrift ishlatiladi. `background-image` xossasi yordamida sahifaga fon rasmi qo'shamiz. `background-repeat`, `background-position` va `background-size` xossalari esa fon rasmining takrorlanishini, joylashuvini va o'lchamini boshqaradi.

**4-qadam: Sarlavha stilini qo'llash**

* `style.css` faylida `h1` selektoridan foydalaning.
* Sarlavha uchun `2.5em` shrift o'lchamini tanlang.
* Sarlavha rangini `#e74c3c` (qizil) ga o'zgartiring.
* Sarlavha matniga `2px 2px 4px #888888` soya qo'shing.
* Sarlavhaga `3px dashed #e74c3c` (qizil) chegara qo'shing.
* Sarlavhaning pastki qismidan 20 piksel bo'sh joy qoldiring (`margin-bottom: 20px;`).

**Tushuntirish:**

Bu yerda biz `h1` selektori yordamida sahifa sarlavhasi uchun stillarni belgilayapmiz. `font-size: 2.5em;` xossasi sarlavha shriftini hozirgi shrift o'lchamiga nisbatan 2.5 barobar kattalashtiradi. `color: #e74c3c;` xossasi sarlavha rangini qizilga o'zgartiradi. `text-shadow: 2px 2px 4px #888888;` xossasi sarlavha matniga soya qo'shadi. `border: 3px dashed #e74c3c;` xossasi sarlavhaga 3 piksel qalinlikdagi, nuqtali chiziqli (`dashed`) va qizil rangli chegara qo'shadi. `margin-bottom: 20px;` xossasi sarlavha ostiga 20 piksel bo'sh joy qoldiradi.

**5-qadam: Rasm stilini qo'llash**

* `style.css` faylida `img` selektoridan foydalaning.
* Rasmlarga `4px double #2980b9` (ko'k) chegara qo'shing.
* Rasmlarga `5px 5px 10px #7f8c8d` (quyuq kulrang) soya qo'shing.
* Rasmlarni sahifa bo'ylab markazga tekislang (`display: block; margin: 0 auto;`).
* Rasmlarning maksimal kengligini `300px` qilib belgilang.
* Rasmlarga 15 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 15px;`).
* Rasmlar orasida 20 piksel bo'sh joy qoldiring (`margin-bottom: 20px;`).

**Tushuntirish:**

Bu yerda biz `img` selektori yordamida sahifadagi barcha rasmlar uchun stillarni belgilayapmiz. `border: 4px double #2980b9;` xossasi rasmlarga 4 piksel qalinlikdagi, ikki chiziqli (`double`) va ko'k rangli (`#2980b9`) chegara qo'shadi. `box-shadow: 5px 5px 10px #7f8c8d;` xossasi rasmlarga soya qo'shadi. Bu yerda soya o'ngga va pastga 5 pikselga siljiydi, tarqalish radiusi 10 piksel va rangi quyuq kulrang (`#7f8c8d`). `display: block; margin: 0 auto;` xossalari rasmlarni sahifa bo'ylab markazga tekislaydi. `max-width: 300px;` xossasi rasmlarning maksimal kengligini 300 piksel qilib belgilaydi. `border-radius: 15px;` xossasi rasmlarga 15 piksel radiusli yumaloq burchaklar qo'shadi. `margin-bottom: 20px;` xossasi har bir rasm ostiga 20 piksel bo'sh joy qo'shadi.

**6-qadam: Xatboshi stilini qo'llash**

* `style.css` faylida `p` selektoridan foydalaning.
* Xatboshilar uchun `1.1em` shrift o'lchamini va `'Georgia', serif` shrift turini belgilang.
* Xatboshilarning birinchi qatorini 20 piksel ichkariga siljiting (`text-indent: 20px;`).
* Satrlar orasidagi masofani `1.5` ga o'rnating (`line-height: 1.5;`).

**Tushuntirish:**

Bu yerda biz `p` selektori yordamida barcha xatboshilar uchun stillarni belgilayapmiz. `font-size: 1.1em;` xossasi xatboshi shriftini biroz kattalashtiradi. `font-family: 'Georgia', serif;` xossasi xatboshilar uchun `'Georgia'` shriftini tanlaydi, agar u foydalanuvchining kompyuterida mavjud bo'lmasa, `serif` shriftlar oilasidan boshqa shrift ishlatiladi. `text-indent: 20px;` xossasi xatboshilarning birinchi qatorini 20 piksel ichkariga siljitadi. `line-height: 1.5;` xossasi satrlar orasidagi masofani oshiradi, bu esa matnni o'qishni osonlashtiradi.

**7-qadam: Qo'shimcha elementlarga stillarni qo'llash**

* Agar siz qo'shimcha elementlardan (masalan, `div`, `ul`, `ol`) foydalangan bo'lsangiz, ularga ham o'zingiz xohlagan stillarni qo'llang.
* Orqa fon rangini, chegara stilini, matn xususiyatlarini va boshqa CSS xususiyatlarini o'zgartirishingiz mumkin.

**8-qadam: Sahifani brauzerda ochish**

* `mashgulot.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

</details>



<details>
<summary>
CSS Orqa Fon va Chegara Xususiyatlari
</summary>


Veb-sahifalarni yanada jozibador va professional ko'rinishga keltirish uchun CSS yordamida orqa fon va chegara xususiyatlarini boshqarish juda muhim. Bu darsda biz elementlarning orqa fon rangini, rasmini, takrorlanishini va boshqa xususiyatlarini, shuningdek, chegara stillarini, qalinligini, rangini va radiusini o'zgartirishni o'rganamiz.

You're absolutely right! I missed explaining the `border-width` property values in detail. I'll make sure to provide complete explanations for all properties this time.

Here's the revised "Orqa Fon va Chegara Xususiyatlari" lesson with more descriptive explanations and examples:

## CSS Orqa Fon va Chegara Xususiyatlari

Veb-sahifalarni yanada jozibador va professional ko'rinishga keltirish uchun CSS yordamida orqa fon va chegara xususiyatlarini boshqarish juda muhim. Bu darsda biz elementlarning orqa fon rangini, rasmini, takrorlanishini va boshqa xususiyatlarini, shuningdek, chegara stillarini, qalinligini, rangini va radiusini batafsil o'rganamiz.


### 1-qism: Orqa Fon va Chegara Stillari bilan tanishuv

Orqa fon va chegaralar veb-sahifalarning ko'rinishini yaxshilash va foydalanuvchi tajribasini oshirish uchun muhim rol o'ynaydi. Ular yordamida siz sahifalaringizni yanada jozibador, tushunarli va professional qilishingiz mumkin.

**Orqa fon xususiyatlari**

CSSda elementlarning orqa fonini boshqarish uchun quyidagi xususiyatlardan foydalanish mumkin:

* **`background-color`:** Elementning orqa fon rangini o'rnatadi. Ranglarni nomlari (`red`, `blue`, `green`), hex kodlari (`#ff0000`, `#0000ff`, `#008000`), RGB/RGBA qiymatlari (`rgb(255, 0, 0)`, `rgba(0, 0, 255, 0.5)`) yoki HSL/HSLA qiymatlari bilan belgilash mumkin.

    ```css
    body {
      background-color: lightblue; /* Sahifa fonini och ko'k rangga o'zgartirish */
    }

    h1 {
      background-color: #f0f0f0; /* Sarlavha fonini och kulrang rangga o'zgartirish */
    }

    .box {
      background-color: rgb(255, 0, 0); /* Quti fonini qizil rangga o'zgartirish */
    }

    .container {
      background-color: rgba(0, 128, 0, 0.5); /* Konteyner fonini yarim shaffof yashil rangga o'zgartirish */
    }
    ```

* **`background-image`:** Elementning orqa foniga rasm qo'shadi. Rasm URL manzili `url()` funksiyasi ichida ko'rsatiladi. 

    Masalan, agar sizning rasmingiz `fon.jpg` deb nomlangan va CSS fayli bilan bir xil papkada joylashgan bo'lsa, quyidagi kodni ishlatishingiz mumkin:

    ```css
    body {
      background-image: url("fon.jpg"); /* Sahifa foniga fon.jpg rasmini qo'shish */
    }
    ```

    Agar rasm veb-saytda joylashgan bo'lsa, rasmning to'liq URL manzilini ko'rsatishingiz kerak:

    ```css
    .card {
      background-image: url("https://example.com/rasm.png"); /* Card klassiga ega elementlarga rasm qo'shish */
    }
    ```

* **`background-repeat`:** Orqa fon rasmining takrorlanishini boshqaradi.

    * `repeat`: Rasmni gorizontal va vertikal takrorlaydi (standart qiymat). Agar rasm kichik bo'lsa, u butun fonni to'ldirguncha gorizontal va vertikal yo'nalishlarda takrorlanadi.
    * `repeat-x`: Rasmni faqat gorizontal takrorlaydi. Rasm faqat gorizontal o'q bo'yicha takrorlanadi, vertikal o'q bo'yicha esa cho'zilmaydi.
    * `repeat-y`: Rasmni faqat vertikal takrorlaydi. Rasm faqat vertikal o'q bo'yicha takrorlanadi, gorizontal o'q bo'yicha esa cho'zilmaydi.
    * `no-repeat`: Rasmni takrorlamaydi. Rasm faqat bir marta, element fonida, ko'rsatiladi.

    ```css
    body {
      background-image: url("naqsh.png");
      background-repeat: repeat-x; /* Naqshni faqat gorizontal takrorlash */
    }
    ```

* **`background-position`:** Orqa fon rasmining joylashuvini boshqaradi. Siz `top`, `bottom`, `left`, `right`, `center` kalit so'zlaridan, foizlardan yoki piksellardan foydalanishingiz mumkin.

    * `top left`: Rasmni elementning yuqori chap burchagiga joylashtiradi.
    * `center`: Rasmni elementning markaziga joylashtiradi.
    * `20% 80%`: Rasmni elementning kengligining 20% va balandligining 80% masofasida joylashtiradi.
    * `10px 50px`: Rasmni elementning chap chegarasidan 10 piksel va yuqori chegarasidan 50 piksel masofada joylashtiradi.

    ```css
    .banner {
      background-image: url("banner.jpg");
      background-position: center top; /* Rasmni yuqori markazga joylashtirish */
    }

    .logo {
      background-image: url("logo.png");
      background-position: 10px 20px; /* Rasmni chapdan 10px, yuqoridan 20px masofada joylashtirish */
    }
    ```

* **`background-size`:** Orqa fon rasmining o'lchamini boshqaradi.

    * `cover`: Rasmni elementni to'liq qoplash uchun cho'zadi, rasmning nisbati saqlanadi. Rasm elementning butun maydonini qoplashi uchun kerakli darajada kattalashtiriladi yoki kichraytiriladi, lekin rasmning asl nisbati saqlanib qoladi.
    * `contain`: Rasmni element ichida to'liq ko'rsatish uchun o'lchamini o'zgartiradi, rasmning nisbati saqlanadi. Rasm element ichida to'liq ko'rinishi uchun kerakli darajada kattalashtiriladi yoki kichraytiriladi, lekin rasmning asl nisbati saqlanib qoladi.
    * Foizlar: Rasmning kengligi va balandligini element o'lchamiga nisbatan foizlarda belgilaydi. Masalan, `background-size: 50% 100%;` rasmning kengligini element kengligining 50% iga, balandligini esa element balandligiga teng qiladi.
    * Piksellar: Rasmning kengligi va balandligini piksellarda belgilaydi. Masalan, `background-size: 32px 32px;` rasm o'lchamini 32x32 piksel qiladi.

    ```css
    .hero {
      background-image: url("hero.jpg");
      background-size: cover; /* Rasmni elementni to'liq qoplash uchun cho'zish */
    }

    .icon {
      background-image: url("icon.png");
      background-size: 32px 32px; /* Rasm o'lchamini 32x32 piksel qilish */
    }
    ```

* **`background-attachment`:** Orqa fon rasmining sahifa bilan birga siljishini yoki siljimasligini boshqaradi.

    * `scroll`: Rasm sahifa bilan birga siljiydi (standart qiymat). Bu odatiy holat, ya'ni sahifa pastga siljiganida fon rasmi ham birga siljiydi.
    * `fixed`: Rasm sahifa bilan birga siljimaydi, o'z o'rnida qoladi. Sahifa pastga siljiganida fon rasmi o'z o'rnida qoladi, bu esa "parallax" effektiga o'xshaydi.

    ```css
    body {
      background-image: url("fon.jpg");
      background-attachment: fixed; /* Fon rasmini sahifa bilan birga siljitmaslik */
    }
    ```

* **`background`:** Yuqoridagi barcha orqa fon xususiyatlarini bir qatorda belgilash imkonini beradi. Bu qisqacha yozuv usuli barcha orqa fon xususiyatlarini bitta qatorda belgilashga imkon beradi.

    ```css
    .element {
      background: lightblue url("rasm.jpg") no-repeat center center / cover fixed;
    }
    ```

**Chegara xususiyatlari**

CSSda elementlarning chegaralarini boshqarish uchun quyidagi xususiyatlardan foydalanish mumkin:

* **`border-width`:** Chegara qalinligini o'rnatadi. Siz `thin`, `medium`, `thick` kalit so'zlaridan yoki piksellardan foydalanishingiz mumkin.

    * `thin`: Ingichka chegara (odatda 1px).
    * `medium`: O'rtacha qalinlikdagi chegara (odatda 3px).
    * `thick`: Qalin chegara (odatda 5px).

    ```css
    p {
      border-width: 2px; /* Xatboshilarga 2 piksel qalinlikdagi chegara qo'shish */
    }

    .box {
      border-width: thin; /* Box klassiga ega elementlarga ingichka chegara qo'shish */
    }
    ```

* **`border-style`:** Chegara stilini o'rnatadi.

    * `none`: Chegara yo'q (standart qiymat).
    * `solid`: To'g'ri chiziq.
    * `dotted`: Nuqtali chiziq.
    * `dashed`: Chiziqli chiziq.
    * `double`: Ikkita chiziq.
    * `groove`: 3D ko'rinishdagi chiziq (ichkariga botiq).
    * `ridge`: 3D ko'rinishdagi chiziq (tashqariga botiq).
    * `inset`: Ichkariga bo'rtib chiqqan ko'rinishdagi chegara.
    * `outset`: Tashqariga bo'rtib chiqqan ko'rinishdagi chegara.

    ```css
    div {
      border-style: dotted; /* Div elementiga nuqtali chegara qo'shish */
    }

    .container {
      border-style: double; /* Konteynerga ikkita chiziqdan iborat chegara qo'shish */
    }
    ```

* **`border-color`:** Chegara rangini o'rnatadi. Ranglarni nomlari, hex kodlari, RGB/RGBA qiymatlari yoki HSL/HSLA qiymatlari bilan belgilash mumkin.

    ```css
    img {
      border-color: red; /* Rasmlarga qizil rangli chegara qo'shish */
    }

    a {
      border-color: #007bff; /* Havolalarga ko'k rangli chegara qo'shish */
    }
    ```

* **`border-radius`:** Chegaralarning burchaklarini yumaloq qiladi. Piksellar yoki foizlar bilan belgilanadi.

    ```css
    button {
      border-radius: 10px; /* Tugmalarning burchaklarini 10 pikselga yumaloqlash */
    }

    .box {
      border-radius: 50%; /* Box klassiga ega elementlarning burchaklarini to'liq yumaloqlash (doira shaklida) */
    }
    ```

* **`border`:** Yuqoridagi barcha chegara xususiyatlarini bir qatorda belgilash imkonini beradi.

    ```css
    div {
      border: 2px solid blue; /* Div elementiga 2 piksel qalinlikdagi ko'k rangli chegara qo'shish */
    }
    ```

* **Alohida chegaralar:** Har bir chegara uchun alohida xususiyatlarni belgilash mumkin (`border-top`, `border-right`, `border-bottom`, `border-left`).

    ```css
    div {
      border-top: 5px solid red; /* Div elementining yuqori chegarasini 5 piksel qalinlikdagi qizil rangli qilish */
      border-left: 2px dashed green; /* Div elementining chap chegarasini 2 piksel qalinlikdagi yashil rangli va chiziqli qilish */
    }
    ```

Bu xususiyatlarni birgalikda ishlatib, elementlarning orqa fonini va chegaralarini xohlagancha stillash mumkin. Bu esa veb-sahifalarni yanada jozibador va professional ko'rinishga keltirish imkonini beradi.

### 2-qism: O'qituvchi boshchiligidagi loyiha: "Sayohat blogi"

Ushbu loyihada biz CSS yordamida sayohat blogi uchun veb-sahifa yaratamiz. Sahifada sarlavha, xatboshilar, rasm va yon panel bo'ladi. Biz orqa fon rasmlarini, chegaralarni va boshqa CSS xususiyatlarini qo'llab, sahifani jozibador qilamiz.

**1-qadam: HTML fayl yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating.
* Faylni `sayohat.html` deb nomlang va saqlang.
* Quyidagi HTML kodni faylga qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Sayohat blogi</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>Sayohat sarguzashtlari</h1>
  </header>

  <main>
    <article>
      <h2>Samarqandga sayohat</h2>
      <p>Samarqand - tarixiy va madaniy boyliklarga boy shahar. Bu yerda Registon maydoni, Bibixonim masjidi, Go'ri Amir maqbarasi kabi ko'plab diqqatga sazovor joylarni ko'rish mumkin.</p>
      <img src="samarqand.jpg" alt="Samarqand">
      <p>Samarqand oshxonasi ham o'ziga xos. Bu yerda palov, norin, manti kabi milliy taomlarni tatib ko'rishni unutmang.</p>
    </article>
  </main>

  <aside>
    <h2>Tegishli havolalar</h2>
    <ul>
      <li><a href="#">Samarqand haqida ma'lumot</a></li>
      <li><a href="#">Samarqand mehmonxonalari</a></li>
    </ul>
  </aside>

</body>
</html>
```

**2-qadam: CSS fayl yaratish**

* `sayohat.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Sahifa stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
body {
  background-image: url("fon.jpg"); 
  background-repeat: no-repeat; 
  background-size: cover; 
  font-family: Arial, sans-serif;
  color: #333; 
  margin: 0;
}
```

Sahifa foniga `fon.jpg` rasmini qo'shamiz, uni takrorlamasdan butun sahifani qoplash uchun cho'zamiz. Shriftni `Arial` ga, matn rangini to'q kulrangga o'rnatamiz va standart tashqi chegaralarni olib tashlaymiz.

**4-qadam: Sarlavha (header) stilini qo'llash**

```css
header {
  background-color: rgba(255, 255, 255, 0.8); 
  padding: 20px;
  text-align: center;
}
```

`header` elementiga yarim shaffof oq fon qo'shamiz va ichki chegaralarni 20 pikselga o'rnatamiz. Sarlavha matnini markazga tekislaymiz.

**5-qadam: Sarlavha (h1) stilini qo'llash**

```css
h1 {
  margin: 0;
}
```

`h1` elementining standart tashqi chegaralarini olib tashlaymiz.

**6-qadam: Asosiy kontent (main) stilini qo'llash**

```css
main {
  width: 70%;
  margin: 20px auto;
  padding: 20px;
  background-color: #fff; 
  border-radius: 10px; 
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); 
}
```

`main` elementining kengligini 70% qilib cheklaymiz va uni sahifa bo'ylab markazga joylashtiramiz. Ichki chegaralarni 20 pikselga o'rnatamiz, fon rangini oqqa o'zgartiramiz, burchaklarni 10 pikselga yumaloqlaymiz va soya qo'shamiz.

**7-qadam: Maqola rasmi (article img) stilini qo'llash**

```css
article img {
  width: 100%;
  height: auto;
  margin-bottom: 20px;
}
```

`article` elementi ichidagi rasmlarni `article` kengligi bo'yicha cho'zamiz, balandligini esa avtomatik o'lchaymiz. Rasm ostiga 20 piksel bo'sh joy qo'shamiz.

**8-qadam: Yon panel (aside) stilini qo'llash**

```css
aside {
  float: right;
  width: 25%;
  padding: 20px;
  background-color: #eee; 
  border: 1px solid #ddd; 
}
```

`aside` elementini o'ng tomonga surib qo'yamiz, kengligini 25% qilib cheklaymiz, ichki chegaralarni 20 pikselga o'rnatamiz, fon rangini och kulrangga o'zgartiramiz va 1 piksel qalinlikdagi och kulrang chegara qo'shamiz.

**9-qadam: Yon panel ro'yxati (aside ul) stilini qo'llash**

```css
aside ul {
  list-style: none;
  padding: 0;
}
```

`aside` elementi ichidagi ro'yxat markerlarini olib tashlaymiz va ichki chegaralarni olib tashlaymiz.

**10-qadam: Sahifani brauzerda ochish**

* `sayohat.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.


### 3-qism: Mustaqil loyiha: "Fotogalereya Kartochkasi"

Ushbu loyihada siz CSS bilimlaringizdan foydalanib, fotogalereya uchun kartochka yaratasiz. Kartochkada rasm, sarlavha va qisqacha tavsif bo'lishi kerak. Orqa fon rasmlarini, chegaralarni va boshqa CSS xususiyatlarini qo'llab, kartochkani jozibador qiling.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `kartochka.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Fotogalereya Kartochkasi").
* Quyidagi elementlarni sahifangizga qo'shing:
    * Kartochka konteyneri uchun `<div>` tegi.
    * Rasm uchun `<img>` tegi.
    * Sarlavha uchun `<h2>` tegini.
    * Qisqacha tavsif uchun `<p>` tegini.

**2-qadam: CSS fayl yaratish**

* `kartochka.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Kartochka konteyneri stilini qo'llash**

* `style.css` faylida `div` selektoridan foydalaning.
* Konteynerga `400px` kenglik bering.
* Konteynerga oq fon rangi (`#fff`) va `1px solid #ddd` (och kulrang) chegara bering.
* Konteynerga 10 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 10px;`).
* Konteynerni sahifa bo'ylab markazga tekislang (`margin: 50px auto;`).
* Konteyner ichida 20 piksel bo'sh joy qoldiring (`padding: 20px;`).

**Tushuntirish:**

Bu yerda biz `div` selektori yordamida kartochka konteyneri uchun stillarni belgilayapmiz. `width` xossasi elementning kengligini belgilaydi. `background-color` xossasi fon rangini, `border` xossasi chegara stilini, `border-radius` xossasi esa yumaloq burchaklarni belgilaydi. `margin: 50px auto;` xossasi elementni vertikal ravishda 50 pikselga tushiradi va gorizontal ravishda markazlashtiradi. `padding` xossasi esa elementning ichki chegaralarini belgilaydi.

**4-qadam: Rasm stilini qo'llash**

* `style.css` faylida `img` selektoridan foydalaning.
* Rasmga `100%` kenglik bering.
* Rasmga 5 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 5px;`).
* Rasmning pastki qismidan 15 piksel bo'sh joy qoldiring (`margin-bottom: 15px;`).

**Tushuntirish:**

Bu yerda biz `img` selektori yordamida rasm uchun stillarni belgilaymiz. `width: 100%;` xossasi rasmni konteyner kengligi bo'yicha cho'zadi. `border-radius` xossasi yumaloq burchaklarni belgilaydi. `margin-bottom` xossasi esa rasm ostiga bo'sh joy qo'shadi.

**5-qadam: Sarlavha stilini qo'llash**

* `style.css` faylida `h2` selektoridan foydalaning.
* Sarlavha uchun `1.5em` shrift o'lchamini tanlang.
* Sarlavha rangini `#333` (quyuq kulrang) ga o'zgartiring.
* Sarlavha matnini qalin qiling (`font-weight: bold;`).
* Sarlavhaning pastki qismidan 10 piksel bo'sh joy qoldiring (`margin-bottom: 10px;`).

**Tushuntirish:**

`h2` selektori yordamida biz kartochka sarlavhasi uchun stillarni belgilaymiz. `font-size` xossasi matn o'lchamini o'zgartirish, `color` xossasi matn rangini o'zgartirish, `font-weight` xossasi esa matnni qalin qilish uchun ishlatiladi.

**6-qadam: Tavsif stilini qo'llash**

* `style.css` faylida `p` selektoridan foydalaning.
* Xatboshi uchun `1em` shrift o'lchamini va `'Arial', sans-serif` shrift turini belgilang.
* Xatboshining rangini `#666` (kulrang) ga o'zgartiring.

**Tushuntirish:**

`p` selektori yordamida biz kartochka tavsifi uchun stillarni belgilaymiz. `font-size` va `font-family` xossalari mos ravishda shrift o'lchamini va turini o'zgartirish uchun ishlatiladi.

**7-qadam: Orqa fon va chegara stillarini qo'llash**

* Yuqoridagi bosqichlarda yaratilgan elementlarga orqa fon va chegara stillarini qo'llang.
* `background-color` xossasi yordamida elementlarning fon rangini o'zgartiring.
* `background-image` xossasi yordamida elementlarga fon rasmi qo'shing.
* `border` xossasi yordamida elementlarga chegara qo'shing.
* `border-radius` xossasi yordamida elementlarga yumaloq burchaklar qo'shing.

**Tushuntirish:**

Bu yerda siz oldingi darslarda o'rgangan orqa fon va chegara xususiyatlaridan foydalanib, kartochkaning ko'rinishini yanada jozibador qilishingiz mumkin. Masalan, kartochka foniga gradient qo'shishingiz, rasmga soya qo'shishingiz yoki chegara stilini o'zgartirishingiz mumkin.

**8-qadam: Sahifani brauzerda ochish**

* `kartochka.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.

Ushbu loyihada biz CSSning orqa fon va chegara xususiyatlaridan foydalanib, fotogalereya uchun kartochka yaratdik. Bu kartochkada rasm, sarlavha va qisqacha tavsif mavjud. Siz ushbu maketni asos qilib, o'zingizning fotogalereya kartochkalaringizni yaratishingiz mumkin.

</details>



<details>
<summary>
CSS Box Model va Joylashtirish
</summary>

## CSS Box Model va Joylashtirish

Veb-sahifalar yaratishda elementlarni xohlagan joyga joylashtirish va ularning o'lchamlarini boshqarish juda muhim. Buning uchun CSS bizga **Box Model** va **joylashtirish xususiyatlari**ni taqdim etadi. 

### 1-qism: Box Model va Joylashtirish Asoslari

Tasavvur qiling, veb-sahifadagi har bir element - bu ko'rinmas quti ichida. Bu quti elementning mazmunini (matn, rasm va hokazo) o'rab turadi va uning atrofida bo'sh joylar, chegaralar va boshqa elementlar bilan o'zaro ta'sirini belgilaydi. Bu "ko'rinmas quti" **Box Model** deb ataladi.

**Box Model nima?**

CSS Box Model har bir elementni to'rtburchak quti sifatida tasavvur qiladi. Bu quti quyidagi qismlardan iborat:

* **Kontent (content):** Elementning asosiy mazmuni, masalan, matn, rasm yoki video. Bu quti ichidagi asosiy narsa.
* **Ichki chegara (padding):** Kontent atrofidagi bo'sh joy. Bu xuddi quti ichidagi yumshoq qatlamga o'xshaydi, u kontentni chegaradan himoya qiladi va chiroyli ko'rinish beradi.
* **Chegara (border):** Ichki chegaradan tashqaridagi chiziq. Bu quti devorlariga o'xshaydi, u elementni boshqa elementlardan ajratib turadi.
* **Tashqi chegara (margin):** Chegaradan tashqaridagi bo'sh joy. Bu quti atrofidagi bo'sh maydonga o'xshaydi, u elementni boshqa elementlardan uzoqlashtiradi.

Bu qismlarga turli xil CSS xususiyatlarini qo'llash orqali elementning o'lchamini va joylashuvini boshqarish mumkin.

**Box Model xususiyatlari**

* **`width` va `height`:** Elementning kengligi va balandligini belgilaydi. Bu xususiyatlar faqat kontentning o'lchamini o'rnatadi, ichki chegara, chegara va tashqi chegarani hisobga olmaydi.

```css
div {
  width: 200px; /* Kontent kengligi 200px */
  height: 100px; /* Kontent balandligi 100px */
}
```

* **`padding`:** Elementning ichki chegarasini belgilaydi. `padding-top`, `padding-right`, `padding-bottom`, `padding-left` xossalari yordamida har bir tomon uchun alohida qiymatlarni belgilash mumkin.

```css
p {
  padding: 20px; /* Barcha tomonlardan 20px ichki chegara */
}

.example {
  padding-top: 10px; /* Yuqoridan 10px ichki chegara */
  padding-right: 15px; /* O'ngdan 15px ichki chegara */
  padding-bottom: 20px; /* Pastdan 20px ichki chegara */
  padding-left: 25px; /* Chapdan 25px ichki chegara */
}
```

* **`border`:** Elementning chegarasini belgilaydi. `border-width`, `border-style`, `border-color` xossalari yordamida chegara qalinligi, stili va rangini belgilash mumkin.

```css
img {
  border-width: 3px; /* Chegara qalinligi 3px */
  border-style: solid; /* Chegara stili to'g'ri chiziq */
  border-color: blue; /* Chegara rangi ko'k */
}
```

* **`margin`:** Elementning tashqi chegarasini belgilaydi. `margin-top`, `margin-right`, `margin-bottom`, `margin-left` xossalari yordamida har bir tomon uchun alohida qiymatlarni belgilash mumkin.

```css
h1 {
  margin: 30px; /* Barcha tomonlardan 30px tashqi chegara */
}

.example {
  margin-top: 10px; /* Yuqoridan 10px tashqi chegara */
  margin-right: 15px; /* O'ngdan 15px tashqi chegara */
  margin-bottom: 20px; /* Pastdan 20px tashqi chegara */
  margin-left: 25px; /* Chapdan 25px tashqi chegara */
}
```

**Joylashtirish xususiyatlari**

CSSda elementlarni joylashtirish uchun `position` xossasidan foydalaniladi. Bu xususiyat quyidagi qiymatlarni qabul qilishi mumkin:

* **`static`:** Element hujjat oqimida odatiy joylashtiriladi. Bu standart qiymat. Boshqacha aytganda, element brauzer tomonidan avtomatik ravishda joylashtiriladi va siz uni qo'lda joylashtira olmaysiz.

* **`relative`:** Element o'zining odatiy joylashuviga nisbatan joylashtiriladi. `top`, `right`, `bottom`, `left` xossalari yordamida elementni siljitish mumkin. Element o'zining asl joylashuvini saqlab qoladi va boshqa elementlar uning asl joylashuviga qarab joylashadi.

```css
.box {
  position: relative;
  top: 20px; /* Elementni yuqoriga 20px siljitish */
  left: 30px; /* Elementni chapga 30px siljitish */
}
```

* **`absolute`:** Element o'zining eng yaqin joylashtirilgan ota elementiga nisbatan joylashtiriladi. Agar ota elementlaridan hech biri joylashtirilmagan bo'lsa, element brauzer oynasiga nisbatan joylashtiriladi. Element hujjat oqimidan chiqariladi va boshqa elementlar uning joylashuvini hisobga olmaydi.

```css
.container {
  position: relative; /* Ota elementni joylashtirish */
}

.box {
  position: absolute;
  top: 50px; /* Ota elementning yuqori chegarasidan 50px pastga joylashtirish */
  right: 100px; /* Ota elementning o'ng chegarasidan 100px chapga joylashtirish */
}
```

* **`fixed`:** Element brauzer oynasiga nisbatan joylashtiriladi va sahifa siljiganida ham o'z o'rnida qoladi. Element hujjat oqimidan chiqariladi va boshqa elementlar uning joylashuvini hisobga olmaydi.

```css
.navbar {
  position: fixed;
  top: 0; /* Brauzer oynasining yuqori chegarasiga joylashtirish */
  width: 100%; /* Navbar kengligini brauzer oynasi kengligiga tenglashtirish */
}
```

* **`sticky`:** Element odatiy joylashtiriladi, lekin ma'lum bir shart bajarilganda (masalan, sahifa ma'lum bir joyga siljiganida) `fixed` kabi ishlaydi.

```css
.sidebar {
  position: sticky;
  top: 20px; /* Brauzer oynasining yuqori chegarasidan 20px pastga joylashtirish */
}
```

**`top`, `right`, `bottom`, `left` xossalari**

Bu xossalar elementni joylashtirish uchun ishlatiladi. `position` xossasi `relative`, `absolute` yoki `fixed` qiymatlaridan biriga o'rnatilgan bo'lishi kerak.

* `top`: Elementni yuqoridan qancha masofaga joylashtirishni belgilaydi.
* `right`: Elementni o'ngdan qancha masofaga joylashtirishni belgilaydi.
* `bottom`: Elementni pastdan qancha masofaga joylashtirishni belgilaydi.
* `left`: Elementni chapdan qancha masofaga joylashtirishni belgilaydi.

**Z-indeks (z-index)**

Z-indeks xossasi elementlarning qatlamlarini boshqaradi. Yuqori z-indeksga ega bo'lgan elementlar pastki z-indeksga ega bo'lgan elementlar ustida ko'rsatiladi.

```css
.box1 {
  position: absolute;
  z-index: 1; /* box1 elementi box2 elementi ustida bo'ladi */
}

.box2 {
  position: absolute;
  z-index: 2; 
}
```

**Joylashtirish va Box Modelni birgalikda ishlatish**

Joylashtirish va Box Model xususiyatlarini birgalikda ishlatib, veb-sahifalardagi elementlarni xohlagancha joylashtirish va o'lchamlarini boshqarish mumkin. Bu esa sahifalarni yanada jozibador va foydalanuvchilar uchun qulay qilish imkonini beradi.


### 2-qism: O'qituvchi boshchiligidagi loyiha: "Interaktiv Kartochkalar"

Ushbu loyihada biz CSS Box Model va joylashtirish xususiyatlaridan foydalanib, interaktiv kartochkalar yaratamiz. Har bir kartochka rasm, sarlavha va qisqacha tavsifdan iborat bo'ladi. Kartochkalar ustiga sichqoncha olib borilganda, ularning ko'rinishi o'zgaradi (masalan, kattalashadi yoki soya qo'shiladi).

**1-qadam: HTML fayl yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating.
* Faylni `kartochkalar.html` deb nomlang va saqlang.
* Quyidagi HTML kodni faylga qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Interaktiv Kartochkalar</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="container">
    <div class="card">
      <img src="rasm1.jpg" alt="Rasm 1">
      <h3>Kartochka 1</h3>
      <p>Bu birinchi kartochka uchun qisqacha tavsif.</p>
    </div>
    <div class="card">
      <img src="rasm2.jpg" alt="Rasm 2">
      <h3>Kartochka 2</h3>
      <p>Bu ikkinchi kartochka uchun qisqacha tavsif.</p>
    </div>
    <div class="card">
      <img src="rasm3.jpg" alt="Rasm 3">
      <h3>Kartochka 3</h3>
      <p>Bu uchinchi kartochka uchun qisqacha tavsif.</p>
    </div>
  </div>

</body>
</html>
```

Bu kodda biz uchta kartochka yaratdik. Har bir kartochka `card` klassiga ega bo'lgan `div` elementi ichida joylashgan.

**2-qadam: CSS fayl yaratish**

* `kartochkalar.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Konteyner stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.container {
  display: flex;
  justify-content: space-around;
  margin-top: 50px;
}
```

Bu kod yordamida biz kartochkalarni joylashtirish uchun `container` klassiga ega bo'lgan `div` elementini stillashtiramiz. `display: flex;` xossasi elementni flex konteynerga aylantiradi. `justify-content: space-around;` xossasi elementlar orasidagi bo'shliqni teng taqsimlaydi. `margin-top: 50px;` xossasi konteynerni yuqoridan 50 pikselga tushiradi.

**4-qadam: Kartochka stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.card {
  width: 300px;
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 5px;
  transition: transform 0.2s; /* O'tish effekti qo'shish */
}
```

Bu kod yordamida biz har bir kartochka uchun stillarni belgilaymiz. `width: 300px;` xossasi kartochkaning kengligini 300 pikselga o'rnatadi. `border: 1px solid #ddd;` xossasi kartochkalarga 1 piksel qalinlikdagi och kulrang chegara qo'shadi. `padding: 20px;` xossasi kartochka ichida 20 piksel bo'sh joy qoldiradi. `border-radius: 5px;` xossasi kartochkalarga 5 piksel radiusli yumaloq burchaklar qo'shadi. `transition: transform 0.2s;` xossasi esa kartochka o'lchami o'zgarganda 0.2 sekundlik o'tish effekti qo'shadi.

**5-qadam: Kartochka hover effektini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.card:hover {
  transform: scale(1.1); /* Kartochkani 10% kattalashtirish */
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); /* Soya qo'shish */
}
```

Bu kod yordamida biz kartochka ustiga sichqoncha olib borilganda uning o'lchamini 10% ga kattalashtiramiz va soya qo'shamiz. `:hover` psevdo-klassi element ustiga sichqoncha olib borilganda stillarni qo'llash uchun ishlatiladi. `transform: scale(1.1);` xossasi elementni kattalashtirish uchun ishlatiladi. `box-shadow` xossasi esa elementga soya qo'shadi.

**6-qadam: Rasm stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.card img {
  width: 100%;
  height: auto;
  border-radius: 5px; /* Rasmlarga yumaloq burchaklar qo'shish */
  margin-bottom: 10px;
}
```

Bu kod yordamida biz kartochka ichidagi rasmlar uchun stillarni belgilaymiz. `width: 100%;` xossasi rasmni kartochka kengligi bo'yicha cho'zadi. `height: auto;` xossasi rasmning balandligini avtomatik o'lchaydi. `border-radius: 5px;` xossasi rasmlarga 5 piksel radiusli yumaloq burchaklar qo'shadi. `margin-bottom: 10px;` xossasi rasm ostiga 10 piksel bo'sh joy qo'shadi.

**7-qadam: Sahifani brauzerda ochish**

* `kartochkalar.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.
* Sichqoncha kursorini kartochkalar ustiga olib boring va ularning qanday o'zgarishini kuzating.


### 3-qism: Mustaqil loyiha: "Shaxsiy Vizitka"


Ushbu loyihada siz CSS Box Model va joylashtirish xususiyatlaridan foydalanib, o'zingizning shaxsiy vizitkangizni veb-sahifada yaratasiz. Vizitkada ismingiz, kasbingiz, kontakt ma'lumotlaringiz va rasmingiz bo'lishi kerak. Elementlarni joylashtirish, o'lchamlarini belgilash, chegaralar, ichki va tashqi chegaralarni qo'llash orqali vizitkani yarating.

**1-qadam: HTML fayl yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `vizitka.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Shaxsiy Vizitka").
* Quyidagi elementlarni sahifangizga qo'shing:
    * Vizitka konteyneri uchun `<div>` tegi.
    * Ismingiz va familiyangiz uchun `<h2>` tegini.
    * Kasbingiz uchun `<p>` tegini.
    * Kontakt ma'lumotlaringiz (telefon raqami, email manzili, ijtimoiy tarmoqlar) uchun `<ul>` tegi.
    * Rasmingiz uchun `<img>` tegi.

**2-qadam: CSS fayl yaratish**

* `vizitka.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Vizitka konteyneri stilini qo'llash**

* `style.css` faylida `div` selektoridan foydalaning.
* Konteynerga `300px` kenglik va `400px` balandlik bering.
* Konteynerga oq fon rangi (`#fff`) va `1px solid #ddd` (och kulrang) chegara bering.
* Konteynerga 10 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 10px;`).
* Konteynerni sahifa bo'ylab markazga tekislang (`margin: 50px auto;`).
* Konteyner ichida 20 piksel bo'sh joy qoldiring (`padding: 20px;`).

**Tushuntirish:**

Bu yerda biz `div` selektori yordamida vizitka konteyneri uchun stillarni belgilayapmiz. `width` va `height` xossalari elementning kengligi va balandligini belgilaydi. `background-color` xossasi fon rangini, `border` xossasi chegara stilini, `border-radius` xossasi esa yumaloq burchaklarni belgilaydi. `margin: 50px auto;` xossasi elementni vertikal ravishda 50 pikselga tushiradi va gorizontal ravishda markazlashtiradi. `padding` xossasi esa elementning ichki chegaralarini belgilaydi.

**4-qadam: Sarlavha (ism va familiya) stilini qo'llash**

* `style.css` faylida `h2` selektoridan foydalaning.
* Sarlavha uchun `2em` shrift o'lchamini tanlang.
* Sarlavha rangini `#2c3e50` (quyuq ko'k) ga o'zgartiring.
* Sarlavha matnini qalin qiling (`font-weight: bold;`).
* Sarlavhaning pastki qismidan 10 piksel bo'sh joy qoldiring (`margin-bottom: 10px;`).

**Tushuntirish:**

`h2` selektori yordamida biz vizitkadagi ism va familiya uchun stillarni belgilaymiz. `font-size` xossasi matn o'lchamini o'zgartirish, `color` xossasi matn rangini o'zgartirish, `font-weight` xossasi esa matnni qalin qilish uchun ishlatiladi.

**5-qadam: Kasb stilini qo'llash**

* `style.css` faylida `p` selektoridan foydalaning (faqat kasb uchun ishlatiladigan `<p>` tegini tanlash uchun `div p` selektoridan foydalanishingiz mumkin).
* Xatboshi uchun `1.2em` shrift o'lchamini va `'Lora', serif` shrift turini belgilang.
* Xatboshining pastki qismidan 15 piksel bo'sh joy qoldiring (`margin-bottom: 15px;`).

**Tushuntirish:**

`p` selektori yordamida biz vizitkadagi kasb uchun stillarni belgilaymiz. `font-size` va `font-family` xossalari mos ravishda shrift o'lchamini va turini o'zgartirish uchun ishlatiladi.

**6-qadam: Rasm stilini qo'llash**

* `style.css` faylida `img` selektoridan foydalaning.
* Rasmga `100px` kenglik va balandlik bering.
* Rasmga 5 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 5px;`).
* Rasmni vizitka konteynerining yuqori qismiga, markazga joylashtiring. Buning uchun `position: absolute;`, `top: 20px;` va `left: 50%; transform: translateX(-50%);` xossalaridan foydalaning.

**Tushuntirish:**

Bu yerda biz `img` selektori yordamida rasm uchun stillarni belgilaymiz. `position: absolute;` xossasi elementni hujjat oqimidan chiqarib, uni ota elementiga nisbatan joylashtirish imkonini beradi. `top: 20px;` xossasi rasmni ota elementining yuqori chegarasidan 20 piksel pastga tushiradi. `left: 50%; transform: translateX(-50%);` xossalari esa rasmni gorizontal ravishda markazlashtiradi.

**7-qadam: Kontakt ma'lumotlari stilini qo'llash**

* `style.css` faylida `ul` selektoridan foydalaning.
* Ro'yxat elementlari oldidagi markerlarni olib tashlang (`list-style: none;`).
* Ro'yxatning ichki chegaralarini olib tashlang (`padding: 0;`).
* Ro'yxat elementlari orasidagi bo'shliqni 10 pikselga o'zgartiring (`margin-bottom: 10px;`).

**Tushuntirish:**

`ul` selektori yordamida biz kontakt ma'lumotlari ro'yxati uchun stillarni belgilaymiz. `list-style: none;` xossasi ro'yxat elementlari oldidagi markerlarni olib tashlash uchun ishlatiladi. `padding: 0;` xossasi ro'yxatning ichki chegaralarini olib tashlaydi. `margin-bottom` xossasi esa ro'yxat elementlari orasiga bo'sh joy qo'shadi.

**8-qadam: Sahifani brauzerda ochish**

* `vizitka.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.


Ushbu loyihada biz Box Model va joylashtirish xususiyatlaridan foydalanib, shaxsiy vizitka yaratdik. Bu vizitkada ism, kasb, kontakt ma'lumotlari va rasm mavjud. Siz ushbu maketni asos qilib, o'zingizning shaxsiy vizitkangizni yaratishingiz mumkin.
</details>



<details>
<summary>
CSS Flexbox va Media So'rovlar
</summary>
Albatta, "Flexbox va Media So'rovlar" darsining nazariy qismini batafsilroq va tushunarli qilib, misollar va kodlar bilan boyitib beraman.



Zamonaviy veb-dizaynda sahifalar turli xil qurilmalarda (kompyuterlar, planshetlar, telefonlar) va turli o'lchamdagi ekranlarda to'g'ri ko'rinishi kerak. Buning uchun bizga **Flexbox** va **Media So'rovlar** yordam beradi.

### 1-qism: Flexbox va Media So'rovlar bilan tanishuv

**Flexbox nima?**

Flexbox (Flexible Box Layout) - bu CSSda elementlarni bir qatorda yoki ustunda moslashuvchan tarzda joylashtirish uchun mo'ljallangan modul. Flexbox yordamida elementlarni o'lchamlarini, tartibini va hizalamasini osongina boshqarish mumkin.

Flexbox sizga quyidagi imkoniyatlarni beradi:

* Elementlarni gorizontal yoki vertikal ravishda joylashtirish.
* Elementlar orasidagi bo'shliqni boshqarish.
* Elementlarni turli o'lchamdagi ekranlarda to'g'ri ko'rsatish.
* Elementlarni markazga hizala yoki boshqa hizalamalardan foydalanish.
* Elementlarning tartibini o'zgartirish.

**Flexbox atamalari**

Flexboxda ikkita asosiy tushuncha mavjud:

* **Flex konteyner:** Flexbox xususiyatlari qo'llaniladigan ota element.
* **Flex elementlar:** Flex konteyner ichidagi elementlar.


**Flex konteyner xususiyatlari**

* **`display: flex;`:** Elementni flex konteynerga aylantiradi. Bu xususiyatni qo'llaganingizdan so'ng, element ichidagi barcha elementlar flex elementlarga aylanadi.

```css
.container {
  display: flex;
}
```

* **`flex-direction`:** Flex elementlarning joylashish yo'nalishini belgilaydi.

    * `row`: Elementlar chapdan o'ngga gorizontal joylashadi (standart qiymat).
    * `column`: Elementlar yuqoridan pastga vertikal joylashadi.
    * `row-reverse`: Elementlar o'ngdan chapga gorizontal joylashadi.
    * `column-reverse`: Elementlar pastdan yuqoriga vertikal joylashadi.

```css
.container {
  display: flex;
  flex-direction: column; /* Elementlarni vertikal joylashtirish */
}
```

* **`flex-wrap`:** Flex elementlarning yangi qatorga o'tishini boshqaradi.

    * `nowrap`: Elementlar yangi qatorga o'tmaydi (standart qiymat).
    * `wrap`: Elementlar yangi qatorga o'tadi, agar ular konteynerga sig'masa.
    * `wrap-reverse`: Elementlar teskari tartibda yangi qatorga o'tadi.

```css
.container {
  display: flex;
  flex-wrap: wrap; /* Elementlarni yangi qatorga o'tkazish */
}
```

* **`justify-content`:** Flex elementlarning asosiy o'q bo'yicha hizalamasini belgilaydi. Asosiy o'q `flex-direction` xossasi bilan belgilanadi.

    * `flex-start`: Elementlar konteynerning boshidan joylashtiriladi.
    * `flex-end`: Elementlar konteynerning oxiridan joylashtiriladi.
    * `center`: Elementlar konteynerning markazida joylashtiriladi.
    * `space-between`: Elementlar orasidagi bo'shliq teng taqsimlanadi.
    * `space-around`: Elementlar atrofidagi bo'shliq teng taqsimlanadi.
    * `space-evenly`: Elementlar orasidagi va atrofidagi bo'shliq teng taqsimlanadi.

```css
.container {
  display: flex;
  justify-content: space-around; /* Elementlar atrofidagi bo'shliqni teng taqsimlash */
}
```

* **`align-items`:** Flex elementlarning ko'ndalang o'q bo'yicha hizalamasini belgilaydi. Ko'ndalang o'q asosiy o'qga perpendikulyar bo'ladi.

    * `flex-start`: Elementlar konteynerning boshidan hizalanadi.
    * `flex-end`: Elementlar konteynerning oxiridan hizalanadi.
    * `center`: Elementlar konteynerning markazida hizalanadi.
    * `stretch`: Elementlar konteyner balandligiga cho'ziladi (standart qiymat).
    * `baseline`: Elementlar matnning asosiy chizig'iga hizalanadi.

```css
.container {
  display: flex;
  align-items: center; /* Elementlarni vertikal markazga hizala */
}
```

* **`align-content`:** Bir nechta qatorli flex konteynerlarda qatorlarning hizalamasini belgilaydi.

    * `flex-start`: Qatorlar konteynerning boshidan hizalanadi.
    * `flex-end`: Qatorlar konteynerning oxiridan hizalanadi.
    * `center`: Qatorlar konteynerning markazida hizalanadi.
    * `space-between`: Qatorlar orasidagi bo'shliq teng taqsimlanadi.
    * `space-around`: Qatorlar atrofidagi bo'shliq teng taqsimlanadi.
    * `stretch`: Qatorlar konteyner balandligiga cho'ziladi (standart qiymat).

```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between; /* Qatorlar orasiga bo'sh joy qo'shish */
}
```

**Flex elementlar xususiyatlari**

* **`order`:** Flex elementlarning tartibini o'zgartiradi. Standart qiymat 0. Qancha katta raqam bo'lsa, element shuncha keyin joylashadi.

```css
.item1 {
  order: 2; /* item1 elementi item2 elementidan keyin joylashadi */
}

.item2 {
  order: 1;
}
```

* **`flex-grow`:** Flex elementlarning bo'sh joyni qanday to'ldirishini belgilaydi. Standart qiymat 0. Qancha katta raqam bo'lsa, element shuncha ko'p bo'sh joyni egallaydi.

```css
.item {
  flex-grow: 2; /* item elementi boshqa elementlardan ikki barobar ko'proq bo'sh joyni egallaydi */
}
```

* **`flex-shrink`:** Flex elementlarning bo'sh joy yetishmaganda qanday qisqarishini belgilaydi. Standart qiymat 1. 0 qiymati elementni qisqarishdan saqlaydi.

```css
.item {
  flex-shrink: 0; /* item elementi qisqarmaydi */
}
```

* **`flex-basis`:** Flex elementlarning boshlang'ich o'lchamini belgilaydi. Siz piksel (`px`), foiz (`%`) yoki boshqa o'lchov birliklaridan foydalanishingiz mumkin.

```css
.item {
  flex-basis: 200px; /* item elementining boshlang'ich kengligi 200px */
}
```

* **`align-self`:** Flex elementlarning ko'ndalang o'q bo'yicha o'z hizalamasini belgilaydi. `align-items` xossasiga o'xshash qiymatlarni qabul qiladi.

```css
.item {
  align-self: center; /* item elementi vertikal markazga hizalanadi */
}
```


**Media So'rovlar**

Media so'rovlar ekran o'lchamiga, qurilma turiga va boshqa shartlarga qarab turli xil CSS stillarini qo'llash imkonini beradi. Bu sizga veb-sahifalaringizni turli xil qurilmalarda to'g'ri ko'rsatishga yordam beradi.

Masalan, siz katta ekranlarda matnni katta qilib, kichik ekranlarda esa kichik qilishingiz mumkin. Yoki katta ekranlarda yon panelni o'ng tomonga joylashtirib, kichik ekranlarda esa yon panelni sahifa ostiga joylashtirishingiz mumkin.

Media so'rovlar `@media` qoidasi yordamida yoziladi. Bu qoida ichida shartlar va ular bajarilganda qo'llaniladigan CSS stillari ko'rsatiladi.

**Media so'rovlar sintaksisi**

```css
@media (shart) {
  /* CSS stillari */
}
```

**Shartlar**

Media so'rovlarda quyidagi shartlardan foydalanish mumkin:

* **`width` va `height`:** Ekranning kengligi va balandligi.

```css
@media (width: 768px) {
  /* Ekran kengligi 768px bo'lganda qo'llaniladigan stillar */
}
```

* **`min-width` va `min-height`:** Ekranning minimal kengligi va balandligi.

```css
@media (min-width: 1024px) {
  /* Ekran kengligi 1024px dan katta yoki teng bo'lganda qo'llaniladigan stillar */
}
```

* **`max-width` va `max-height`:** Ekranning maksimal kengligi va balandligi.

```css
@media (max-width: 768px) {
  /* Ekran kengligi 768px dan kichik bo'lganda qo'llaniladigan stillar */
}
```

* **`orientation`:** Ekranning orientatsiyasi (`portrait` yoki `landscape`).

```css
@media (orientation: landscape) {
  /* Ekran gorizontal holatda bo'lganda qo'llaniladigan stillar */
}
```

* **`media-type`:** Qurilma turi (`screen`, `print`, `speech`).

```css
@media print {
  /* Chop etish uchun qo'llaniladigan stillar */
}
```

Flexbox va media so'rovlarni birgalikda ishlatib, turli xil ekran o'lchamlarida to'g'ri ko'rinadigan moslashuvchan veb-sahifalar yaratish mumkin.

You're absolutely correct! I seem to be struggling with the format of these tutorials. I apologize for the repeated errors. 

Let me try this again, providing a 2nd part for the "Flexbox va Media So'rovlar" tutorial with a more comprehensive project and the correct format.

### 2-qism: O'qituvchi boshchiligidagi loyiha: "Moslashuvchan Veb-sayt Maketi"

Ushbu loyihada biz birgalikda CSS Flexbox va Media So'rovlar yordamida moslashuvchan veb-sayt maketi yaratamiz. Maketimizda header, navigatsiya menyusi, asosiy kontent maydoni, yon panel va footer bo'ladi. Flexbox yordamida elementlarni joylashtiramiz va media so'rovlar yordamida ekran o'lchamiga qarab ularning joylashuvini o'zgartiramiz. Men har bir qadamni tushuntirib beraman va siz meni kuzatib, kodni yozasiz.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating.
* Faylni `maket.html` deb nomlang va saqlang.
* Faylga quyidagi asosiy HTML tuzilishini qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Veb-sayt maketi</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>Veb-sayt nomi</h1>
    <nav>
      <a href="#">Bosh sahifa</a>
      <a href="#">Biz haqimizda</a>
      <a href="#">Xizmatlar</a>
      <a href="#">Aloqa</a>
    </nav>
  </header>

  <main>
    <article>
      <h2>Maqola sarlavhasi</h2>
      <p>Maqola matni...</p>
    </article>
    <article>
      <h2>Maqola sarlavhasi</h2>
      <p>Maqola matni...</p>
    </article>
  </main>

  <aside>
    <h2>Yon panel</h2>
    <p>Yon panel matni...</p>
  </aside>

  <footer>
    <p>&copy; 2024 Veb-sayt nomi</p>
  </footer>

</body>
</html>
```

Bu kodda biz veb-sayt maketi uchun oddiy HTML tuzilishini yaratdik. `header`, `nav`, `main`, `article`, `aside` va `footer` teglaridan foydalanib, sahifani asosiy qismlarga ajratdik.

**2-qadam: CSS fayl yaratish**

* `maket.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Header stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
header {
  background-color: #3498db; /* Ko'k fon */
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
```

Bu kod yordamida biz header elementini flex konteynerga aylantiramiz, fon rangini ko'k rangga o'zgartiramiz, ichki chegaralarni 20 pikselga o'rnatamiz va elementlarni vertikal markazga hizalaymiz.

**4-qadam: Navigatsiya menyusi stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
nav {
  display: flex;
}

nav a {
  color: white;
  text-decoration: none;
  margin-left: 20px;
}
```

Bu kod yordamida biz navigatsiya menyusini ham flex konteynerga aylantiramiz, havolalar rangini oq rangga o'zgartiramiz, chiziqlarni olib tashlaymiz va har bir havola chap tomonidan 20 piksel bo'sh joy qoldiramiz.

**5-qadam: Asosiy kontent va yon panel stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
main {
  display: flex;
  margin: 20px;
}

article {
  width: 70%;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
  margin-right: 20px;
}

aside {
  width: 30%;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
}
```

Bu kod yordamida biz asosiy kontent maydoni va yon panelni yonma-yon joylashtiramiz. `main` elementini flex konteynerga aylantiramiz va ichki elementlarga kenglik, ichki chegara, chegara stili va yumaloq burchaklar qo'shamiz.

**6-qadam: Footer stilini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
}
```

Bu kod yordamida biz footerga fon rangi, matn rangi, hizalama va ichki chegara qo'shamiz.

**7-qadam: Media so'rovlarini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
@media (max-width: 768px) {
  header {
    flex-direction: column;
    align-items: flex-start;
  }

  nav {
    margin-top: 20px;
  }

  main {
    flex-direction: column;
  }

  article, aside {
    width: 100%;
    margin-right: 0;
    margin-bottom: 20px;
  }
}
```

Bu kod yordamida biz media so'rovlarini qo'llaymiz. Ekran kengligi 768px dan kichik bo'lganda, header elementlarini vertikal joylashtiramiz, navigatsiya menyusini pastga tushiramiz va asosiy kontent bilan yon panelni bir-birining ostiga joylashtiramiz.

**8-qadam: Sahifani brauzerda ochish**

* `maket.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.
* Brauzer oynasining o'lchamini o'zgartirib, maketning qanday moslashishini kuzating.

### 3-qism: Mustaqil loyiha: "Moslashuvchan Navigatsiya Menyu"

Ushbu loyihada siz CSS bilimlaringizdan foydalanib, moslashuvchan navigatsiya menyusi yaratasiz. Menyuda bir nechta havolalar bo'lishi kerak va u turli ekran o'lchamlarida to'g'ri ko'rinishi kerak. Flexbox va media so'rovlar yordamida menyu elementlarini joylashtiring va ekran o'lchamiga qarab ularning joylashuvini o'zgartiring.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `menyu.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Moslashuvchan Navigatsiya Menyu").
* Quyidagi elementlarni sahifangizga qo'shing:
    * Menyu konteyneri uchun `<nav>` tegi.
    * Har bir menyu elementi uchun `<a>` tegi.

**2-qadam: CSS fayl yaratish**

* `menyu.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.

**3-qadam: Menyu konteyneri stilini qo'llash**

* `style.css` faylida `nav` selektoridan foydalaning.
* Konteynerga `#34495e` (quyuq ko'k) fon rangini bering.
* Konteynerga 60 piksel balandlik bering (`height: 60px;`).
* Konteyner ichida 20 piksel bo'sh joy qoldiring (`padding: 20px;`).

**Tushuntirish:**

Bu yerda biz `nav` selektori yordamida menyu konteyneri uchun stillarni belgilayapmiz. `background-color` xossasi fon rangini, `height` xossasi elementning balandligini, `padding` xossasi esa elementning ichki chegaralarini belgilaydi.

**4-qadam: Menyu elementlari stilini qo'llash**

* `style.css` faylida `a` selektoridan foydalaning.
* Havolalar rangini `#fff` (oq) ga o'zgartiring.
* Havolalarni bezashni olib tashlang (`text-decoration: none;`).
* Havolalar uchun `1.2em` shrift o'lchamini tanlang.
* Havolalar orasida 20 piksel bo'sh joy qoldiring (`margin: 0 20px;`).

**Tushuntirish:**

`a` selektori yordamida biz menyu elementlari (havolalar) uchun stillarni belgilaymiz. `color` xossasi matn rangini o'zgartirish, `text-decoration` xossasi matn bezaklarini olib tashlash, `font-size` xossasi esa matn o'lchamini o'zgartirish uchun ishlatiladi.

**5-qadam: Flexbox xususiyatlarini qo'llash**

* `style.css` faylida `nav` selektoridan foydalaning.
* Konteynerni flex konteynerga aylantiring (`display: flex;`).
* Flex elementlarini vertikal markazga hizala (`align-items: center;`).
* Flex elementlarini gorizontal markazga hizala (`justify-content: center;`).

**Tushuntirish:**

Bu yerda biz `nav` selektori yordamida menyu konteyneri uchun flexbox xususiyatlarini qo'llaymiz. `display: flex;` xossasi elementni flex konteynerga aylantiradi. `align-items: center;` xossasi flex elementlarini vertikal markazga hizalaydi. `justify-content: center;` xossasi esa flex elementlarini gorizontal markazga hizalaydi.

**6-qadam: Media so'rovlarini qo'llash**

* `style.css` faylida `@media` qoidasidan foydalanib, turli ekran o'lchamlari uchun stillarni belgilang.
* Masalan, ekran kengligi 768px dan kichik bo'lganda:
    * Flex elementlarini vertikal joylashtiring (`flex-direction: column;`).
    * Havolalar orasidagi bo'shliqni 10 pikselga o'zgartiring (`margin: 10px 0;`).
    * Har bir havolaning kengligini 100% qilib belgilang (`width: 100%;`).
    * Havolalarga 1 piksel qalinlikdagi och kulrang chegara qo'shing (`border: 1px solid #ddd;`).

**Tushuntirish:**

`@media` qoidasi yordamida biz ma'lum shartlar bajarilganda qo'llaniladigan stillarni belgilashimiz mumkin. Bu yerda biz `max-width: 768px` shartidan foydalanib, ekran kengligi 768px dan kichik bo'lganda menyu elementlarini vertikal joylashtiramiz va ularning stillarini o'zgartiramiz. Bu kichik ekranlarda menyuni to'g'ri ko'rsatishga yordam beradi.

**7-qadam: Sahifani brauzerda ochish**

* `menyu.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.
* Brauzer oynasining o'lchamini o'zgartirib, menyuning qanday moslashishini kuzating.

Ushbu loyihada biz Flexbox va media so'rovlaridan foydalanib, moslashuvchan navigatsiya menyusi yaratdik. Bu menyu turli xil ekran o'lchamlarida to'g'ri ko'rinadi. Siz ushbu maketni asos qilib, o'zingizning veb-saytlaringiz uchun moslashuvchan menyular yaratishingiz mumkin.

</details>



<details>
<summary>
CSS Psevdo-klasslar va Display Xususiyatlari
</summary>

CSS psevdo-klasslari va `display` xossasi veb-sahifalar yaratishda elementlarning ko'rinishini va xatti-harakatlarini dinamik tarzda o'zgartirish uchun kuchli vositalardir. Psevdo-klasslar yordamida siz foydalanuvchi harakatlariga (masalan, sichqoncha bosish, ustiga olib borish) yoki element holatiga (masalan, birinchi element, fokuslangan element) qarab stillarni qo'llashingiz mumkin. `display` xossasi esa elementning ko'rinish turini boshqaradi, masalan, blok, inline yoki umuman ko'rinmas qilish.

### 1-qism: Psevdo-klasslar va Display Xususiyatlari bilan tanishuv

**Psevdo-klasslar**

Psevdo-klasslar selektorlarga qo'shilib, elementlarning ma'lum bir holatiga yoki foydalanuvchi harakatlariga qarab stillarni qo'llash imkonini beradi. Psevdo-klasslar ikki nuqta (`:`) bilan boshlanadi.

Ba'zi asosiy psevdo-klasslar:

* **`:hover`:** Sichqoncha kursorini element ustiga olib borilganda qo'llaniladi.

```css
a:hover {
  color: red; /* Havola ustiga sichqoncha olib borilganda rangini qizilga o'zgartirish */
}
```

* **`:active`:** Sichqoncha tugmasi element ustida bosilganda qo'llaniladi.

```css
button:active {
  background-color: darkgray; /* Tugma bosilganda fon rangini quyuq kulrangga o'zgartirish */
}
```

* **`:focus`:** Element fokuslanganda (masalan, tab tugmasi bilan tanlanganda) qo'llaniladi.

```css
input:focus {
  border-color: blue; /* Input maydoni fokuslanganda chegara rangini ko'kka o'zgartirish */
}
```

* **`:first-child`:** Ota elementning birinchi farzandi bo'lgan elementga qo'llaniladi.

```css
ul li:first-child {
  font-weight: bold; /* Ro'yxatning birinchi elementini qalin qilish */
}
```

* **`:last-child`:** Ota elementning oxirgi farzandi bo'lgan elementga qo'llaniladi.

```css
ul li:last-child {
  font-style: italic; /* Ro'yxatning oxirgi elementini kursiv qilish */
}
```

* **`:nth-child(n)`:** Ota elementning n-chi farzandi bo'lgan elementga qo'llaniladi.

```css
ul li:nth-child(2) {
  color: red; /* Ro'yxatning ikkinchi elementini qizil rangda qilish */
}
```

* **`:nth-of-type(n)`:** Ota elementning ma'lum bir turdagi n-chi farzandi bo'lgan elementga qo'llaniladi.

```css
p:nth-of-type(3) {
  text-align: center; /* Uchinchi xatboshini markazga tekislash */
}
```

**`display` xossasi**

`display` xossasi elementning ko'rinish turini boshqaradi. Ba'zi asosiy qiymatlari:

* **`block`:** Element yangi qatorga o'tadi va konteynerning butun kengligini egallaydi. Masalan, `<h1>`, `<p>`, `<div>` elementlari standart ravishda `block` ko'rinishida bo'ladi.

```css
.box {
  display: block;
  width: 200px; /* Kenglikni belgilash mumkin */
  height: 100px; /* Balandlikni belgilash mumkin */
}
```

* **`inline`:** Element yangi qatorga o'tmaydi va faqat o'z mazmuni uchun kerakli joyni egallaydi. Masalan, `<span>`, `<a>`, `<strong>` elementlari standart ravishda `inline` ko'rinishida bo'ladi.

```css
.highlight {
  display: inline;
  background-color: yellow; /* Fon rangini belgilash mumkin */
  padding: 5px; /* Ichki chegara qo'shish mumkin */
}
```

* **`inline-block`:** Element `inline` kabi joylashadi, lekin `block` kabi kenglik, balandlik, ichki chegara va tashqi chegara xususiyatlarini qabul qiladi.

```css
.button {
  display: inline-block;
  padding: 10px 20px;
  background-color: blue;
  color: white;
  border-radius: 5px;
}
```

* **`none`:** Elementni sahifada ko'rinmas qiladi.

```css
.hidden {
  display: none;
}
```

* **`flex` va `grid`:** Elementlarni moslashuvchan tarzda joylashtirish uchun ishlatiladi. Bu qiymatlar alohida darslarda batafsil ko'rib chiqiladi.

Psevdo-klasslar va `display` xossasini birgalikda ishlatib, veb-sahifalarda interaktiv va dinamik elementlar yaratish mumkin.

You're absolutely right! I apologize for overlooking the `display` property in this tutorial. It seems I'm still struggling to incorporate all the necessary elements into these lessons.

Let me revise the "Interaktiv Tugmalar" project to include the `display` property and demonstrate its usage along with pseudo-classes.

### 2-qism: O'qituvchi boshchiligidagi loyiha: "Interaktiv Tugmalar" (Revised with `display`)

Ushbu loyihada biz birgalikda CSS psevdo-klasslari va `display` xossasidan foydalanib, interaktiv tugmalar yaratamiz. Tugmalar ustiga sichqoncha olib borilganda, bosilganda va fokuslanganda ularning ko'rinishi o'zgaradi. Bundan tashqari, biz `display` xossasi yordamida tugmalarning joylashuvini boshqaramiz. Men har bir qadamni tushuntirib beraman va siz meni kuzatib, kodni yozasiz.

**1-qadam: Yangi HTML hujjat yaratish va CSS faylini ulash**

* Matn muharriri yoki kod muharririda yangi fayl yarating.
* Faylni `tugmalar.html` deb nomlang va saqlang.
* Quyidagi HTML kodni faylga qo'shing:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <title>Interaktiv Tugmalar</title>
  <link rel="stylesheet" href="style.css"> 
</head>
<body>

  <button class="tugma">Tugma 1</button>
  <button class="tugma">Tugma 2</button>
  <button class="tugma">Tugma 3</button>

</body>
</html>
```

Bu kodda biz uchta tugma yaratdik. Har bir tugma `tugma` klassiga ega. Shuningdek, biz `style.css` faylini HTML hujjatimizga bog'ladik.

**2-qadam: CSS faylini yaratish va tugmalarga asosiy stil berish**

* `tugmalar.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.
* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.tugma {
  background-color: #3498db; /* Ko'k fon rangi */
  color: white;
  padding: 15px 30px;
  border: none;
  border-radius: 5px;
  cursor: pointer; /* Sichqoncha kursorini qo'l shaklida ko'rsatish */
  transition: all 0.3s ease; /* O'tish effekti qo'shish */
  display: inline-block; /* Tugmalarni inline-block elementi sifatida ko'rsatish */
  margin: 10px; /* Tugmalar orasiga bo'sh joy qo'shish */
}
```

Bu yerda biz tugmalarga asosiy stil beramiz va `display: inline-block;` xossasi yordamida ularni yonma-yon joylashtiramiz. `margin` xossasi yordamida tugmalar orasiga bo'sh joy qo'shamiz.

**3-qadam: Hover effektini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.tugma:hover {
  background-color: #2980b9; /* Quyuqroq ko'k fon rangi */
  transform: translateY(-3px); /* Tugmani 3px yuqoriga ko'tarish */
  box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2); /* Soya qo'shish */
}
```

Bu kod yordamida biz tugma ustiga sichqoncha olib borilganda uning fon rangini quyuqroq ko'k rangga o'zgartiramiz, tugmani 3px yuqoriga ko'taramiz va soya qo'shamiz.

**4-qadam: Active effektini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.tugma:active {
  background-color: #21618c; /* Yana quyuqroq ko'k fon rangi */
  transform: translateY(1px); /* Tugmani 1px pastga tushirish */
  box-shadow: none; /* Soyani olib tashlash */
}
```

Bu kod yordamida biz tugma bosilganda uning fon rangini yana quyuqroq ko'k rangga o'zgartiramiz, tugmani 1px pastga tushiramiz va soyani olib tashlaymiz.

**5-qadam: Focus effektini qo'llash**

* `style.css` fayliga quyidagi CSS kodni qo'shing:

```css
.tugma:focus {
  outline: none; /* Fokus chizig'ini olib tashlash */
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.5); /* Boshqa soya qo'shish */
}
```

Bu kod yordamida biz tugma fokuslanganda (masalan, tab tugmasi bilan tanlanganda) uning fokus chizig'ini olib tashlaymiz va boshqa soya qo'shamiz.

**6-qadam: Tugmalarning joylashuvini o'zgartirish**

* Endi biz `display` xossasining boshqa qiymatlarini sinab ko'ramiz. `style.css` faylida `.tugma` qoidasidagi `display: inline-block;` xossasini `display: block;` ga o'zgartiring.

```css
.tugma {
  /* ... boshqa stillar ... */
  display: block; /* Tugmalarni block elementi sifatida ko'rsatish */
  margin: 10px auto; /* Tugmalarni vertikal joylashtirish va gorizontal markazlash */
}
```

Endi tugmalar bir-birining ostiga joylashadi va sahifaning markazida bo'ladi.

**7-qadam: Sahifani brauzerda ochish**

* `tugmalar.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.
* Sichqoncha kursorini tugmalar ustiga olib boring, ularni bosing va tab tugmasi bilan fokuslang. Ularning qanday o'zgarishini kuzating.
* `display` xossasining qiymatini o'zgartirib, tugmalarning joylashuvini qanday o'zgarishini kuzating.

Bu loyihada biz psevdo-klasslar va `display` xossasidan foydalanib, interaktiv tugmalar yaratdik va ularning joylashuvini boshqarishni o'rgandik.

You're absolutely right! I apologize for the inconsistency in my response structure. I'll make sure to follow the structure you provided in the "Box Model va Joylashtirish" tutorial's 3rd part for this "Psevdo-klasslar va Display Xususiyatlari" self-practice project.

### 3-qism: Mustaqil loyiha: "Dinamik Profil Kartochkasi"

Ushbu loyihada siz CSS bilimlaringizdan foydalanib, dinamik profil kartochkasi yaratasiz. Kartochkada shaxsning rasmi, ismi, kasbi va qisqacha biografiyasi, shuningdek, ijtimoiy tarmoqlarga havolalar bo'lishi kerak. Psevdo-klasslar va `display` xossasidan foydalanib, kartochkaning elementlarini yashiring va sichqoncha ustiga olib borilganda ko'rsating.

**1-qadam: Yangi HTML hujjat yaratish**

* Matn muharriri yoki kod muharririda yangi fayl yarating va uni `profil.html` deb nomlang.
* Faylga asosiy HTML tuzilishini qo'shing (`<!DOCTYPE html>`, `<html lang="uz">`, `<head>`, `<title>`, `<body>`).
* `<title>` tegi ichida sahifa sarlavhasini yozing (masalan, "Dinamik Profil Kartochkasi").
* Quyidagi elementlarni sahifangizga qo'shing:
    * Kartochka konteyneri uchun `<div>` tegi.
    * Shaxsning rasmi uchun `<img>` tegi.
    * Shaxsning ismi va familiyasi uchun `<h2>` tegini.
    * Shaxsning kasbi uchun `<p>` tegi.
    * Shaxsning biografiyasi uchun yana bir `<p>` tegi.
    * Ijtimoiy tarmoqlarga havolalar uchun `<ul>` tegi va ichida har bir havola uchun `<li>` va `<a>` teglari.

**2-qadam: CSS fayl yaratish**

* `profil.html` fayli bilan bir xil papkada `style.css` nomli yangi fayl yarating.
* `style.css` faylida `div` selektoridan foydalaning.
* Konteynerga `300px` kenglik bering.
* Konteynerga oq fon rangi (`#fff`) va `1px solid #ddd` (och kulrang) chegara bering.
* Konteynerga 10 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 10px;`).
* Konteynerni sahifa bo'ylab markazga tekislang (`margin: 50px auto;`).
* Konteyner ichida 20 piksel bo'sh joy qoldiring (`padding: 20px;`).

**Tushuntirish:**

Bu yerda biz `div` selektori yordamida kartochka konteyneri uchun stillarni belgilayapmiz. `width` xossasi elementning kengligini belgilaydi. `background-color` xossasi fon rangini, `border` xossasi chegara stilini, `border-radius` xossasi esa yumaloq burchaklarni belgilaydi. `margin: 50px auto;` xossasi elementni vertikal ravishda 50 pikselga tushiradi va gorizontal ravishda markazlashtiradi. `padding` xossasi esa elementning ichki chegaralarini belgilaydi.


**3-qadam: Rasm stilini qo'llash**

* `style.css` faylida `img` selektoridan foydalaning.
* Rasmga `100%` kenglik bering.
* Rasmga 5 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 5px;`).
* Rasmning pastki qismidan 15 piksel bo'sh joy qoldiring (`margin-bottom: 15px;`).

**Tushuntirish:**

Bu yerda biz `img` selektori yordamida rasm uchun stillarni belgilaymiz. `width: 100%;` xossasi rasmni konteyner kengligi bo'yicha cho'zadi. `border-radius` xossasi yumaloq burchaklarni belgilaydi. `margin-bottom` xossasi esa rasm ostiga bo'sh joy qo'shadi.

**4-qadam: Sarlavha (ism va familiya) stilini qo'llash**

* `style.css` faylida `h2` selektoridan foydalaning.
* Sarlavha uchun `1.5em` shrift o'lchamini tanlang.
* Sarlavha rangini `#333` (quyuq kulrang) ga o'zgartiring.
* Sarlavha matnini qalin qiling (`font-weight: bold;`).
* Sarlavhaning pastki qismidan 10 piksel bo'sh joy qoldiring (`margin-bottom: 10px;`).

**Tushuntirish:**

`h2` selektori yordamida biz shaxsning ismi va familiyasi uchun stillarni belgilaymiz. `font-size` xossasi matn o'lchamini o'zgartirish, `color` xossasi matn rangini o'zgartirish, `font-weight` xossasi esa matnni qalin qilish uchun ishlatiladi.

**5-qadam: Kasb va biografiya stilini qo'llash**

* `style.css` faylida `p` selektoridan foydalaning.
* Xatboshi uchun `1em` shrift o'lchamini va `'Arial', sans-serif` shrift turini belgilang.
* Xatboshining rangini `#666` (kulrang) ga o'zgartiring.
* Biografiya xatboshisini standart holatda yashiring (`display: none;`).

**Tushuntirish:**

`p` selektori yordamida biz shaxsning kasbi va biografiyasi uchun stillarni belgilaymiz. `font-size` va `font-family` xossalari mos ravishda shrift o'lchamini va turini o'zgartirish uchun ishlatiladi. `display: none;` xossasi esa elementni sahifada ko'rinmas qiladi.

**6-qadam: Ijtimoiy tarmoqlar havolalari stilini qo'llash**

* `style.css` faylida `ul` va `li` selektorlaridan foydalaning.
* Ro'yxat elementlari oldidagi markerlarni olib tashlang (`list-style: none;`).
* Ro'yxatning ichki chegaralarini olib tashlang (`padding: 0;`).
* Havolalarni blok elementlar sifatida ko'rsating (`display: block;`).
* Havolalarga 10 piksel ichki chegara qo'shing (`padding: 10px;`).
* Havolalarga `#3498db` (ko'k) fon rangi va oq matn rangi bering.
* Havolalarga 5 piksel radiusli yumaloq burchaklar qo'shing (`border-radius: 5px;`).
* Havolalar orasida 5 piksel bo'sh joy qoldiring (`margin-bottom: 5px;`).
* Ijtimoiy tarmoqlar ro'yxatini standart holatda yashiring (`display: none;`).

**Tushuntirish:**

Bu yerda biz `ul` va `li` selektorlari yordamida ijtimoiy tarmoqlar havolalari ro'yxati uchun stillarni belgilaymiz. `display: block;` xossasi havolalarni blok elementlar sifatida ko'rsatadi, bu esa ularga kenglik va balandlik berish imkonini beradi.

**7-qadam: Hover effektini qo'llash**

* `style.css` faylida `div:hover p` va `div:hover ul` selektorlaridan foydalaning.
* Kartochka konteyneri ustiga sichqoncha olib borilganda, biografiya xatboshisini va ijtimoiy tarmoqlar ro'yxatini ko'rsating (`display: block;`).

**Tushuntirish:**

Bu yerda biz `:hover` psevdo-klassi yordamida kartochka konteyneri ustiga sichqoncha olib borilganda biografiya va ijtimoiy tarmoqlar ro'yxatini ko'rsatish uchun `display` xossasini `block` ga o'zgartiramiz.

**8-qadam: Sahifani brauzerda ochish**

* `profil.html` faylini saqlagan papkani oching.
* Faylni ikki marta bosing yoki brauzerda oching.
* Yaratgan veb-sahifangizni ko'rib chiqing.
* Sichqoncha kursorini kartochka ustiga olib boring va yashirin elementlarning qanday paydo bo'lishini kuzating.

Ushbu loyihada biz CSSning psevdo-klasslari va `display` xossasidan foydalanib, dinamik profil kartochkasi yaratdik. Bu kartochkada shaxsning rasmi, ismi, kasbi, biografiyasi va ijtimoiy tarmoqlarga havolalar mavjud. Siz ushbu maketni asos qilib, o'zingizning profil kartochkalaringizni yaratishingiz mumkin.
</details>