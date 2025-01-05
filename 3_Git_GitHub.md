<details>
<summary>
Git va GitHub bilan Versiyalarni Boshqarish
</summary>

Dasturiy ta'minotni ishlab chiqishda kodni yozishdan tashqari, uni samarali boshqarish, o'zgarishlarni kuzatib borish va xatolarni tuzatish juda muhim. Buning uchun versiyalarni boshqarish tizimlari (Version Control Systems - VCS) ishlatiladi. Git eng mashhur va keng tarqalgan VCS hisoblanadi. GitHub esa Git asosida ishlaydigan veb-xizmat bo'lib, u kodni saqlash, loyihalar ustida hamkorlik qilish va boshqa ko'plab imkoniyatlarni taqdim etadi.

### 1-qism: Git va GitHub bilan tanishuv

**Versiyalarni boshqarish nima?**

Tasavvur qiling, siz bir insho yozyapsiz. Siz inshoga o'zgartirishlar kiritasiz, yangi qismlar qo'shasiz, ba'zi qismlarni o'chirasiz. Lekin keyin sizga inshoning oldingi versiyasi kerak bo'lib qoladi. Agar siz har bir o'zgartirishdan keyin inshoning nusxasini alohida faylda saqlamasangiz, bu juda qiyin bo'ladi.

Versiyalarni boshqarish tizimlari aynan shu muammoni hal qiladi. Ular fayllardagi barcha o'zgarishlarni kuzatib boradi va istalgan vaqtda oldingi versiyalarga qaytish imkonini beradi. Bu xuddi fayllaringiz uchun "vaqt mashinasi" ga o'xshaydi.

**Git nima?**

Git - bu tarqatilgan versiyalarni boshqarish tizimi. Bu degani, kodning barcha tarixi har bir ishlab chiquvchining kompyuterida saqlanadi. Bu esa internetga ulanmasdan ham kod bilan ishlash imkonini beradi.

**GitHub nima?**

GitHub - bu Git asosida ishlaydigan veb-xizmat. U kodni saqlash, loyihalar ustida hamkorlik qilish, kodni ko'rib chiqish (code review), xatolarni kuzatib borish (issue tracking) va boshqa ko'plab imkoniyatlarni taqdim etadi. GitHub - bu dasturchilar uchun ijtimoiy tarmoqqa o'xshaydi, bu yerda ular o'zlarining kodlarini baham ko'rishlari, boshqa dasturchilarning kodlarini ko'rishlari va birgalikda loyihalar ustida ishlashlari mumkin.

**Gitning asosiy tushunchalari**

* **Repozitoriya (repository):** Kod fayllari va ularning tarixi saqlanadigan joy. Repozitoriya - bu kodning "uyi" dir. Uning ichida kodning barcha fayllari, papkalari va o'zgarishlar tarixi saqlanadi.
* **Kommit (commit):** Koddagi o'zgarishlarni saqlash. Har bir kommitga xabar (message) yoziladi, bu o'zgarish haqida ma'lumot beradi. Kommit - bu koddagi o'zgarishlarni saqlashning asosiy usuli. Har bir kommit kodning ma'lum bir vaqtdagi "suratiga" o'xshaydi.
* **Tarmoq (branch):** Kodning asosiy versiyasidan alohida nusxasi. Tarmoqlar yangi funksiyalarni ishlab chiqish yoki xatolarni tuzatish uchun ishlatiladi. Tarmoqlar - bu kodning turli versiyalarini parallel ravishda ishlab chiqish imkonini beradi.
* **Birlashtirish (merge):** Ikkita tarmoqni birlashtirish. Birlashtirish - bu ikkita tarmoqdagi o'zgarishlarni bitta tarmoqqa qo'shish jarayoni.

**Git buyruqlari**

Git bilan ishlash uchun buyruq satri (command line) dan foydalaniladi. Buyruq satri - bu kompyuter bilan matnli buyruqlar orqali muloqot qilish imkonini beruvchi dastur. Ba'zi asosiy Git buyruqlari:

* **`git init`:** Yangi repozitoriya yaratish. Bu buyruq joriy papkada yangi Git repozitoriyasini yaratadi.
* **`git add`:** Fayllarni repozitoriyaga qo'shish. Bu buyruq fayllarni repozitoriyaga qo'shish uchun ishlatiladi. Masalan, `git add index.html` buyrug'i `index.html` faylini repozitoriyaga qo'shadi. `git add .` buyrug'i esa joriy papkadagi barcha fayllarni repozitoriyaga qo'shadi.
* **`git commit -m "Xabar"`:** O'zgarishlarni kommit qilish. Bu buyruq koddagi o'zgarishlarni saqlash uchun ishlatiladi. `-m` parametri kommitga xabar qo'shish uchun ishlatiladi. Masalan, `git commit -m "Birinchi kommit"` buyrug'i o'zgarishlarni "Birinchi kommit" xabari bilan saqlaydi.
* **`git status`:** Repozitoriyaning holatini ko'rish. Bu buyruq repozitoriyada qanday fayllar o'zgartirilganligini, qaysi fayllar qo'shilganligini va boshqa ma'lumotlarni ko'rsatadi.
* **`git log`:** Kommitlar tarixini ko'rish. Bu buyruq repozitoriyadagi barcha kommitlarni, ularning xabarlarini, mualliflarini va vaqtlarini ko'rsatadi.
* **`git branch`:** Tarmoqlar bilan ishlash. Bu buyruq tarmoqlar yaratish, o'chirish va boshqa amallarni bajarish uchun ishlatiladi.
* **`git checkout`:** Tarmoqlar orasida almashish. Bu buyruq bir tarmoqdan boshqa tarmoqqa o'tish uchun ishlatiladi.
* **`git merge`:** Tarmoqlarni birlashtirish. Bu buyruq ikkita tarmoqni birlashtirish uchun ishlatiladi.
* **`git push`:** O'zgarishlarni uzoq repozitoriyaga yuborish (masalan, GitHubga). Bu buyruq lokal repozitoriyadagi o'zgarishlarni uzoq repozitoriyaga yuborish uchun ishlatiladi.
* **`git pull`:** Uzoq repozitoriyadan o'zgarishlarni olish. Bu buyruq uzoq repozitoriyadagi o'zgarishlarni lokal repozitoriyaga olish uchun ishlatiladi.
* **`git clone`:** Uzoq repozitoriyaning nusxasini olish. Bu buyruq uzoq repozitoriyaning nusxasini lokal kompyuterga olish uchun ishlatiladi.

**Misol: Veb-sayt yaratish**

```bash
# Yangi repozitoriya yaratish
git init 

# Barcha fayllarni repozitoriyaga qo'shish
git add . 

# O'zgarishlarni kommit qilish
git commit -m "Birinchi kommit" 

# Fayllarga o'zgartirishlar kiritish (masalan, index.html ga yangi kontent qo'shish)

# O'zgartirilgan fayllarni repozitoriyaga qo'shish
git add index.html 

# Yangi o'zgarishlarni kommit qilish
git commit -m "Yangi kontent qo'shildi" 

# Kommitlar tarixini ko'rish
git log 
```

Bu misolda biz quyidagi amallarni bajardik:

* `git init`: Joriy papkada yangi Git repozitoriyasini yaratdik.
* `git add .`: Joriy papkadagi barcha fayllarni repozitoriyaga qo'shdik.
* `git commit -m "Birinchi kommit"`: Koddagi o'zgarishlarni "Birinchi kommit" xabari bilan saqladik.
* `git add index.html`: `index.html` fayliga kiritilgan o'zgarishlarni repozitoriyaga qo'shdik.
* `git commit -m "Yangi kontent qo'shildi"`: Yangi o'zgarishlarni "Yangi kontent qo'shildi" xabari bilan saqladik.
* `git log`: Repozitoriyadagi barcha kommitlarni, ularning xabarlarini, mualliflarini va vaqtlarini ko'rdik.


**Git va GitHubni amalda qo'llash**

Git va GitHub dasturiy ta'minotni ishlab chiqishda juda muhim vositalardir. Ular kodni samarali boshqarish, o'zgarishlarni kuzatib borish, xatolarni tuzatish va loyihalar ustida hamkorlik qilish imkonini beradi.

### 2-qism: O'qituvchi boshchiligidagi loyiha: "Veb-saytni GitHubda saqlash"

Ushbu loyihada biz birgalikda oddiy veb-sayt yaratamiz va uni GitHubda saqlaymiz. Men har bir qadamni tushuntirib beraman va siz meni kuzatib, kodni yozasiz.

**1-qadam: GitHubda repozitoriya yaratish**

* GitHub.com saytiga kiring va akkauntingizga kiring.
* Yangi repozitoriya yaratish uchun "New" tugmasini bosing.
* Repozitoriya nomini kiriting (masalan, "mening-saytim").
* "Create repository" tugmasini bosing.

**2-qadam: Lokal kompyuteringizda papka yaratish**

* Kompyuteringizda yangi papka yarating va uni "mening-saytim" deb nomlang.
* Bu papka sizning veb-sayt fayllaringizni saqlaydi.

**3-qadam: Papkani Git repozitoriyasiga aylantirish**

* Buyruq satrini oching va `cd` buyrug'i yordamida "mening-saytim" papkasiga o'ting.
* `git init` buyrug'ini bajaring. Bu buyruq papkani Git repozitoriyasiga aylantiradi.

**4-qadam: Veb-sayt fayllarini yaratish**

* "mening-saytim" papkasida `index.html` va `style.css` fayllarini yarating.
* `index.html` fayliga oddiy HTML kodini yozing.
* `style.css` fayliga CSS stillarini yozing.

**5-qadam: Fayllarni repozitoriyaga qo'shish**

* Buyruq satrida `git add index.html style.css` buyrug'ini bajaring. Bu buyruq fayllarni repozitoriyaga qo'shish uchun ishlatiladi.

**6-qadam: O'zgarishlarni kommit qilish**

* Buyruq satrida `git commit -m "Birinchi kommit"` buyrug'ini bajaring. Bu buyruq koddagi o'zgarishlarni saqlash uchun ishlatiladi. `-m` parametri kommitga xabar qo'shish uchun ishlatiladi.

**7-qadam: Lokal repozitoriyangizni GitHubdagi repozitoriya bilan bog'lash**

* GitHubdagi repozitoriya sahifasiga o'ting.
* "Code" tabida "HTTPS" ni tanlang va repozitoriya URL manzilini nusxalang.
* Buyruq satrida `git remote add origin <repozitoriya URL manzili>` buyrug'ini bajaring. Bu buyruq lokal repozitoriyangizni GitHubdagi repozitoriya bilan bog'laydi.

**8-qadam: O'zgarishlarni GitHubga yuborish**

* Buyruq satrida `git push -u origin main` buyrug'ini bajaring. Bu buyruq lokal repozitoriyadagi o'zgarishlarni GitHubdagi repozitoriyaga yuboradi.

**9-qadam: Veb-saytingizni GitHub Pagesda joylashtirish**

* GitHubdagi repozitoriya sahifasiga o'ting.
* "Settings" tabiga o'ting.
* "Pages" bo'limida "Source" ni "main" ga o'rnating.
* "Save" tugmasini bosing.

Endi sizning veb-saytingiz GitHub Pagesda joylashtirildi va uni internetda ko'rish mumkin.

Bu loyihada biz GitHubda repozitoriya yaratishni, lokal repozitoriya yaratishni, fayllarni qo'shishni, kommit qilishni, uzoq repozitoriyaga o'zgarishlarni yuborishni va veb-saytni GitHub Pagesda joylashtirishni o'rgandik.

### 3-qism: Mustaqil loyiha: "Mening blogim"

Ushbu loyihada siz Git va GitHubdan foydalanib, shaxsiy blogingizni yaratasiz va uni GitHubda saqlaysiz. Siz yangi repozitoriya yaratasiz, fayllarni qo'shasiz, o'zgarishlarni kommit qilasiz va o'zgarishlarni GitHubga yuborasiz.

**Vazifalar:**

1. **GitHubda repozitoriya yaratish:**

    * GitHub akkauntingizga kiring.
    * Yangi repozitoriya yaratish uchun "New" tugmasini bosing.
    * Repozitoriya nomini kiriting (masalan, "mening-blogim").
    * "Create repository" tugmasini bosing.

**Tushuntirish:**

*   GitHub - bu kodni saqlash va versiyalarni boshqarish uchun ishlatiladigan veb-xizmat.
*   Repozitoriya - bu sizning loyihalaringiz uchun "konteyner" dir. Uning ichida kod fayllari, rasmlar, hujjatlar va boshqa fayllar saqlanadi.


2. **Lokal kompyuteringizda papka yaratish va uni Git repozitoriyasiga aylantirish:**

    * Kompyuteringizda yangi papka yarating va uni "mening-blogim" deb nomlang.
    * Buyruq satrini oching va `cd` buyrug'i yordamida "mening-blogim" papkasiga o'ting.
    * `git init` buyrug'ini bajaring.

**Tushuntirish:**

*   `git init` buyrug'i papkani Git repozitoriyasiga aylantiradi. Bu degani, endi Git ushbu papkadagi fayllardagi o'zgarishlarni kuzatib boradi.


3. **Blog fayllarini yaratish va ularni repozitoriyaga qo'shish:**

    * "mening-blogim" papkasida blog fayllarini yarating. Masalan, `index.html` va `style.css` fayllarini yaratishingiz mumkin.
    * `index.html` fayliga blogingizning HTML kodini yozing.
    * `style.css` fayliga blogingizning CSS stillarini yozing.
    * `git add index.html style.css` buyrug'ini bajaring.

**Tushuntirish:**

*   `git add` buyrug'i fayllarni repozitoriyaga qo'shish uchun ishlatiladi.


4. **O'zgarishlarni kommit qilish:**

    * `git commit -m "Birinchi kommit"` buyrug'ini bajaring.

**Tushuntirish:**

*   `git commit` buyrug'i koddagi o'zgarishlarni saqlash uchun ishlatiladi.
*   `-m` parametri kommitga xabar qo'shish uchun ishlatiladi. Xabar o'zgarishlar haqida qisqacha ma'lumot berishi kerak.


5. **Blogingizga o'zgartirishlar kiritish:**

    * `index.html` va `style.css` fayllariga o'zgartirishlar kiriting. Masalan, yangi blog post qo'shing yoki stilini o'zgartiring.
    * `git add .` va `git commit -m "Blog yangilandi"` buyruqlarini bajaring.

**Tushuntirish:**

*   `.` belgisi joriy papkadagi barcha o'zgartirilgan fayllarni anglatadi.


6. **O'zgarishlarni GitHubga yuborish:**

    * `git remote add origin <repozitoriya URL manzili>` buyrug'i yordamida lokal repozitoriyangizni GitHubdagi repozitoriya bilan bog'lang.
    * `git push -u origin main` buyrug'i yordamida o'zgarishlarni GitHubga yuboring.

**Tushuntirish:**

*   `git remote add origin` buyrug'i lokal repozitoriyangizni uzoq repozitoriya bilan bog'laydi.
*   `git push` buyrug'i o'zgarishlarni uzoq repozitoriyaga yuboradi.


Ushbu loyiha orqali siz Git va GitHub bilan ishlashni mustaqil ravishda mashq qilasiz.
</details>


<details>
<summary>
Git Tarmoqlari (Branches)
</summary>

Git tarmoqlari - bu loyihaning turli versiyalarini parallel ravishda ishlab chiqish imkonini beruvchi kuchli vosita. Ular yordamida siz asosiy kodga ta'sir qilmasdan yangi funksiyalarni qo'shishingiz, xatolarni tuzatishingiz va tajriba o'tkazishingiz mumkin.

### 1-qism: Git tarmoqlari bilan tanishuv

**Tarmoq nima?**

Git repozitoriyasini daraxt deb tasavvur qiling. Asosiy tarmoq (odatda `main` yoki `master` deb ataladi) bu daraxtning asosiy tanasidir. Tarmoqlar esa bu tanadan o'sib chiqadigan shoxlarga o'xshaydi. Har bir tarmoq kodning alohida versiyasini o'z ichiga oladi.

**Nima uchun tarmoqlardan foydalanish kerak?**

Tarmoqlar quyidagi hollarda foydali bo'ladi:

* **Yangi funksiyalarni ishlab chiqish:** Yangi funksiyalarni asosiy kodga ta'sir qilmasdan alohida tarmoqda ishlab chiqish mumkin.
* **Xatolarni tuzatish:** Kodda xatolik topilsa, uni tuzatish uchun alohida tarmoq yaratish mumkin.
* **Tajriba o'tkazish:** Kodda tajriba o'tkazish yoki yangi g'oyalarni sinab ko'rish uchun alohida tarmoq yaratish mumkin.

**Tarmoqlar bilan ishlash**

Git tarmoqlari bilan ishlash uchun quyidagi buyruqlardan foydalaniladi:

* **`git branch`:** Tarmoqlar ro'yxatini ko'rish. Joriy tarmoq yonida yulduzcha (`*`) belgisi bilan ko'rsatiladi.

```bash
git branch
```

* **`git branch <tarmoq nomi>`:** Yangi tarmoq yaratish.

```bash
git branch yangi-funksionallik
```

Bu buyruq "yangi-funksionallik" nomli yangi tarmoq yaratadi.

* **`git checkout <tarmoq nomi>`:** Boshqa tarmoqqa o'tish.

```bash
git checkout yangi-funksionallik
```

Bu buyruq "yangi-funksionallik" tarmog'iga o'tadi.

* **`git merge <tarmoq nomi>`:** Boshqa tarmoqni joriy tarmoqqa birlashtirish.

```bash
git checkout main
git merge yangi-funksionallik
```

Bu buyruqlar avval `main` tarmog'iga o'tadi, keyin "yangi-funksionallik" tarmog'ini `main` tarmog'iga birlashtiradi.

* **`git branch -d <tarmoq nomi>`:** Tarmoqni o'chirish.

```bash
git branch -d yangi-funksionallik
```

Bu buyruq "yangi-funksionallik" tarmog'ini o'chiradi.

**Tarmoqlar bilan ishlash misoli**

```bash
# "yangi-funksionallik" nomli yangi tarmoq yaratish
git branch yangi-funksionallik 

# Yangi tarmoqqa o'tish
git checkout yangi-funksionallik 

# Kodda o'zgarishlar kiritish (masalan, yangi funksiya qo'shish)
# ...

# O'zgartirilgan fayllarni repozitoriyaga qo'shish
git add . 

# O'zgarishlarni kommit qilish
git commit -m "Yangi funksiya qo'shildi" 

# Asosiy tarmoqqa qaytish
git checkout main

# "yangi-funksionallik" tarmog'ini asosiy tarmoqqa birlashtirish
git merge yangi-funksionallik
```

Bu misolda biz quyidagi amallarni bajardik:

1.  **`git branch yangi-funksionallik`:** "yangi-funksionallik" nomli yangi tarmoq yaratdik. Bu buyruq yangi tarmoq yaratadi, lekin joriy tarmoqni o'zgartirmaydi.
2.  **`git checkout yangi-funksionallik`:** "yangi-funksionallik" tarmog'iga o'tdik. Bu buyruq joriy tarmoqni o'zgartiradi. Endi siz ushbu tarmoqda o'zgarishlar kiritishingiz mumkin.
3.  **Kodda o'zgarishlar kiritish:** Yangi tarmoqda kodda o'zgarishlar kiritdik. Bu o'zgarishlar faqat "yangi-funksionallik" tarmog'iga ta'sir qiladi, asosiy tarmoq o'zgarishsiz qoladi.
4.  **`git add .`:** Barcha o'zgartirilgan fayllarni repozitoriyaga qo'shdik.
5.  **`git commit -m "Yangi funksiya qo'shildi"`:** O'zgarishlarni "Yangi funksiya qo'shildi" xabari bilan saqladik.
6.  **`git checkout main`:** Asosiy tarmoqqa qaytdik.
7.  **`git merge yangi-funksionallik`:** "yangi-funksionallik" tarmog'ini asosiy tarmoqqa birlashtirdik. Bu buyruq "yangi-funksionallik" tarmog'idagi barcha o'zgarishlarni asosiy tarmoqqa qo'shadi.


**Git tarmoqlari - bu kodni samarali boshqarish va loyihalar ustida hamkorlik qilish uchun juda muhim vositadir.**


### 2-qism: O'qituvchi boshchiligidagi loyiha: "Veb-saytni yangilash"

Ushbu loyihada biz birgalikda oddiy veb-saytni yangilaymiz va Git tarmoqlaridan foydalanib o'zgarishlarni boshqaramiz. Men har bir qadamni tushuntirib beraman va siz meni kuzatib, kodni yozasiz.

**1-qadam: Veb-sayt fayllarini tayyorlash**

* Agar oldingi "Veb-saytni GitHubda saqlash" loyihasida yaratilgan veb-sayt fayllari mavjud bo'lsa, ulardan foydalaning. 
* Aks holda, yangi papka yarating va unda `index.html` va `style.css` fayllarini yarating.
* `index.html` fayliga oddiy HTML kodini yozing.
* `style.css` fayliga CSS stillarini yozing.

**2-qadam: Git repozitoriyasini yaratish va fayllarni qo'shish**

* Buyruq satrini oching va veb-sayt fayllari joylashgan papkaga o'ting.
* `git init` buyrug'ini bajaring.
* `git add .` buyrug'i yordamida barcha fayllarni repozitoriyaga qo'shing.
* `git commit -m "Birinchi kommit"` buyrug'i yordamida o'zgarishlarni kommit qiling.

**3-qadam: Yangi tarmoq yaratish**

* `git branch yangi-dizayn` buyrug'i yordamida "yangi-dizayn" nomli yangi tarmoq yarating.

**4-qadam: Yangi tarmoqqa o'tish**

* `git checkout yangi-dizayn` buyrug'i yordamida "yangi-dizayn" tarmog'iga o'ting.

**5-qadam: Veb-sayt dizaynini o'zgartirish**

* `style.css` faylida CSS stillarini o'zgartirib, veb-sayt dizaynini yangilang. Masalan, fon rangini, shriftlarni yoki elementlar joylashuvini o'zgartirishingiz mumkin.

**6-qadam: O'zgarishlarni yangi tarmoqda saqlash**

* `git add style.css` buyrug'i yordamida o'zgartirilgan faylni repozitoriyaga qo'shing.
* `git commit -m "Yangi dizayn qo'shildi"` buyrug'i yordamida o'zgarishlarni kommit qiling.

**7-qadam: Asosiy tarmoqqa qaytish**

* `git checkout main` buyrug'i yordamida asosiy tarmoqqa qayting.

**8-qadam: Ikkala tarmoqdagi fayllarni taqqoslash**

* Brauzerda `index.html` faylini oching va ikkala tarmoqdagi dizaynni solishtiring. Buning uchun `git checkout yangi-dizayn` va `git checkout main` buyruqlaridan foydalanib, tarmoqlar orasida almashing.

**9-qadam: Yangi tarmoqni asosiy tarmoqqa birlashtirish**

* `git merge yangi-dizayn` buyrug'i yordamida "yangi-dizayn" tarmog'ini asosiy tarmoqqa birlashtiring.

**10-qadam: O'zgarishlarni GitHubga yuborish**

* `git push origin main` buyrug'i yordamida o'zgarishlarni GitHubga yuboring.

Bu loyihada biz yangi tarmoq yaratishni, tarmoqqa o'tishni, o'zgarishlarni kommit qilishni, tarmoqlarni birlashtirishni va o'zgarishlarni GitHubga yuborishni o'rgandik.

Albatta, tushuntirishlarni qisqaroq jumlalar bilan berishga harakat qilaman, lekin ma'nosini saqlab qolaman.

### 3-qism: Mustaqil loyiha: "Portfolio saytini yangilash"

Ushbu loyihada siz Git tarmoqlaridan foydalanib, portfolio saytingizni yangilaysiz. Yangi funksiyalar yoki bo'limlar qo'shishda tarmoqlardan foydalanish kodni xavfsiz saqlashga va asosiy loyihaga xalaqit bermasdan ishlashga yordam beradi. 

**Vazifalar:**

1. **Portfolio sayt fayllarini tayyorlash:**

    * Oldingi "Veb-saytni GitHubda saqlash" loyihasida yaratilgan portfolio sayt fayllari mavjud bo'lsa, ulardan foydalaning. 
    * Aks holda, yangi papka yarating (`index.html` va `style.css` fayllarini yarating).
    * `index.html` fayliga portfolio saytingizning HTML kodini yozing. 
    * `style.css` fayliga CSS stillarini yozing.

**Tushuntirish:**

* Portfolio sayt - o'zingizning ishlaringizni namoyish qilish uchun veb-sayt. 
* Agar oldingi loyihadan fayllar bo'lmasa, yangi HTML va CSS fayllarini yarating. HTML faylida sayt tuzilishi va kontentini yarating. CSS faylida esa saytning ko'rinishini belgilang.


2. **Git repozitoriyasini yaratish va fayllarni qo'shish:**

    * Buyruq satrini oching va portfolio sayt fayllari joylashgan papkaga o'ting (`cd` buyrug'i yordamida).
    * `git init` buyrug'ini bajaring.
    * `git add .` buyrug'i yordamida barcha fayllarni repozitoriyaga qo'shing.
    * `git commit -m "Birinchi kommit"` buyrug'i yordamida o'zgarishlarni kommit qiling.

**Tushuntirish:**

* `cd` buyrug'i fayllar joylashgan papkaga o'tish uchun.
* `git init` buyrug'i papkani Git repozitoriyasiga aylantiradi. 
* `git add .` buyrug'i barcha fayllarni repozitoriyaga qo'shadi.
* `git commit -m "Xabar"` buyrug'i o'zgarishlarni saqlaydi. Xabar o'zgarishlar haqida ma'lumot beradi.


3. **Yangi tarmoq yaratish va unga o'tish:**

    * `git branch yangi-bolim` buyrug'i yordamida "yangi-bolim" nomli yangi tarmoq yarating.
    * `git checkout yangi-bolim` buyrug'i yordamida yangi tarmoqqa o'ting.

**Tushuntirish:**

*   `git branch <tarmoq nomi>` buyrug'i yangi tarmoq yaratadi. Tarmoq nomi o'zgarishlarni aks ettirishi kerak.
*   `git checkout <tarmoq nomi>` buyrug'i boshqa tarmoqqa o'tish uchun. Yangi tarmoqda kiritilgan o'zgarishlar asosiy tarmoqqa ta'sir qilmaydi.


4. **Yangi bo'lim qo'shish:**

    * `index.html` faylida yangi bo'lim yarating. 
    * `style.css` faylida yangi bo'lim uchun CSS stillarini yozing.
    * `git add index.html style.css` buyrug'i yordamida o'zgartirilgan fayllarni repozitoriyaga qo'shing.
    * `git commit -m "Yangi bo'lim qo'shildi"` buyrug'i yordamida o'zgarishlarni kommit qiling.

**Tushuntirish:**

* Yangi bo'lim qo'shish uchun HTML va CSS bilimlaringizdan foydalaning.
* `git add` buyrug'i o'zgartirilgan fayllarni repozitoriyaga qo'shadi.
* `git commit` buyrug'i o'zgarishlarni saqlaydi. Kommit xabarida nima o'zgarganligini tushuntiring.


5. **Asosiy tarmoqqa qaytish va yangi bo'limni birlashtirish:**

    * `git checkout main` buyrug'i yordamida asosiy tarmoqqa qayting.
    * `git merge yangi-bolim` buyrug'i yordamida "yangi-bolim" tarmog'ini asosiy tarmoqqa birlashtiring.

**Tushuntirish:**

*   `git checkout main` buyrug'i asosiy tarmoqqa qaytish uchun.
*   `git merge <tarmoq nomi>` buyrug'i boshqa tarmoqni joriy tarmoqqa birlashtirish uchun.


6. **O'zgarishlarni GitHubga yuborish:**

    * `git push origin main` buyrug'i yordamida o'zgarishlarni GitHubga yuboring.

**Tushuntirish:**

*   `git push` buyrug'i o'zgarishlarni uzoq repozitoriyaga yuboradi.


Ushbu loyiha orqali siz Git tarmoqlaridan foydalanib, kodni samarali boshqarishni o'rganasiz.
</details>