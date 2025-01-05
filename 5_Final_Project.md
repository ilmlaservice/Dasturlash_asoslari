<details>
<summary>
1-qadam: Ma'lumotlar bazasini yaratish
</summary>

*   **Ma'lumotlar bazasiga ulanish:** (5 ball)
    *   `sqlite3` modulini import qiling.
    *   `sqlite3.connect()` funksiyasi yordamida ma'lumotlar bazasiga ulaning. Ma'lumotlar bazasi fayli nomini "auksion.db" deb nomlang.
    *   Kursor yarating.

**Tushuntirish:**

*   Loyihangiz boshida `import sqlite3` deb yozing. Bu qator `sqlite3` modulini import qiladi, bu modul Python'da SQLite ma'lumotlar bazasi bilan ishlash imkonini beradi.
*   `sqlite3.connect('auksion.db')` funksiyasini chaqiring. Bu funksiya `auksion.db` nomli faylga ulanishni qaytaradi. Agar bu fayl mavjud bo'lmasa, u avtomatik ravishda yaratiladi.
*   O'zgaruvchi yarating va unga ulanishni saqlang. Masalan, `ulanish = sqlite3.connect('auksion.db')`.
*   `ulanish.cursor()` funksiyasini chaqiring. Bu funksiya kursor ob'ektini qaytaradi. Kursor ma'lumotlar bazasi bilan ishlash, ya'ni SQL so'rovlarini bajarish va natijalarni olish uchun ishlatiladi.
*   O'zgaruvchi yarating va unga kursorni saqlang. Masalan, `kursor = ulanish.cursor()`.

*   **Foydalanuvchilar jadvalini yaratish:** (5 ball)
    *   `foydalanuvchilar` jadvalini yarating.
    *   Jadvalda quyidagi ustunlar bo'lsin:
        *   `id`: Butun son, asosiy kalit (`INTEGER PRIMARY KEY`).
        *   `foydalanuvchi_nomi`: Matn (`TEXT`).
        *   `parol`: Matn (`TEXT`).

**Tushuntirish:**

*   `kursor.execute()` metodi yordamida SQL so'rovlarini bajaring.
*   Jadval yaratish uchun `CREATE TABLE` SQL buyrug'idan foydalaning.
*   Jadval nomini va ustunlar ro'yxatini ko'rsating.
*   Har bir ustun uchun nom va ma'lumot turini belgilang.
*   `INTEGER` butun sonlar uchun, `TEXT` matnlar uchun ishlatiladi.
*   `PRIMARY KEY` kalit so'zidan foydalanib, har bir jadval uchun asosiy kalitni belgilang. Masalan, `foydalanuvchilar` jadvalini yaratish uchun quyidagi kodni yozing:

    ```python
    kursor.execute('''CREATE TABLE IF NOT EXISTS foydalanuvchilar
                  (id INTEGER PRIMARY KEY, foydalanuvchi_nomi TEXT, parol TEXT)''')
    ```

    Bu yerda `IF NOT EXISTS` qismi jadval allaqachon mavjud bo'lsa, xatolik chiqarmaslik uchun ishlatiladi.

*   **Mahsulotlar jadvalini yaratish:** (10 ball)
    *   `mahsulotlar` jadvalini yarating.
    *   Jadvalda quyidagi ustunlar bo'lsin:
        *   `id`: Butun son, asosiy kalit (`INTEGER PRIMARY KEY`).
        *   `nomi`: Matn (`TEXT`).
        *   `tavsifi`: Matn (`TEXT`).
        *   `boshlangich_narx`: O'nlik son (`REAL`).
        *   `hozirgi_narx`: O'nlik son (`REAL`).
        *   `sotish_muddati`: Sana va vaqt (`DATETIME`).
        *   `sotuvchi_id`: Butun son, `foydalanuvchilar` jadvalidagi `id` ustuniga bog'langan (`INTEGER`).

**Tushuntirish:**

*   Jadvallar orasidagi bog'liqlikni yaratish uchun tegishli ustunlarni qo'shing. Masalan, `mahsulotlar` jadvalidagi `sotuvchi_id` ustuni `foydalanuvchilar` jadvalidagi `id` ustuniga bog'langan. Bu degani, har bir mahsulot ma'lum bir foydalanuvchi tomonidan qo'yilgan.


*   **Takliflar jadvalini yaratish:** (10 ball)
    *   `takliflar` jadvalini yarating.
    *   Jadvalda quyidagi ustunlar bo'lsin:
        *   `id`: Butun son, asosiy kalit (`INTEGER PRIMARY KEY`).
        *   `mahsulot_id`: Butun son, `mahsulotlar` jadvalidagi `id` ustuniga bog'langan (`INTEGER`).
        *   `foydalanuvchi_id`: Butun son, `foydalanuvchilar` jadvalidagi `id` ustuniga bog'langan (`INTEGER`).
        *   `narx`: O'nlik son (`REAL`).
        *   `vaqt`: Sana va vaqt (`DATETIME`).

**Tushuntirish:**

*   Jadvallar orasidagi bog'liqlikni yaratish uchun tegishli ustunlarni qo'shing. Masalan, `takliflar` jadvalidagi `mahsulot_id` ustuni `mahsulotlar` jadvalidagi `id` ustuniga bog'langan. Bu degani, har bir taklif ma'lum bir mahsulotga tegishli.
</details>



<details>
<summary>
2-qadam: Flask ilovasini yaratish va asosiy route'larni aniqlash (10 ball)
</summary>



* Flask ilovasini yarating.
* Asosiy route (`/`) uchun funksiya yarating. Bu funksiya hozircha oddiygina "Salom!" xabarini qaytarsin.
* `/register` va `/login` route'lari uchun funksiyalar yarating. Bu funksiyalar ham hozircha oddiygina xabar qaytarsin (masalan, "Bu ro'yxatdan o'tish sahifasi" va "Bu kirish sahifasi").

**Tushuntirish:**

*   `from flask import Flask` kodi bilan Flask klassini import qiling.
*   `app = Flask(__name__)` kodi bilan Flask ilovasini yarating. `__name__` o'zgaruvchisi joriy modul nomini bildiradi.
*   `@app.route('/')` dekoratori yordamida asosiy route (`/`) uchun funksiya yarating. Bu funksiya foydalanuvchi saytning asosiy manziliga kirganda bajariladi.
*   Xuddi shunday, `@app.route('/register')` va `@app.route('/login')` dekoratorlari yordamida ro'yxatdan o'tish va kirish sahifalari uchun funksiyalar yarating.
*   Funksiyalar ichida `return` operatori yordamida matn qaytaring. Masalan, `return "Salom!"`.

Bu bosqichda biz Flask ilovasining asosiy strukturasini yaratamiz va asosiy route'larni aniqlaymiz. Keyingi bosqichlarda bu route'larga to'liq funksionallik qo'shamiz.
**3-qadam: Ro'yxatdan o'tish sahifasini yaratish (20 ball)**

*  `/register` route'i uchun funksiya yarating.
*  Funksiya `GET` va `POST` metodlarini qabul qilsin.
*  **`GET` so'rovi uchun:**
    *   Ro'yxatdan o'tish formasini ko'rsatuvchi HTML shablonini yarating (`register.html`).
    *   Shablonda foydalanuvchi nomi va parol uchun `input` maydonlarini yarating (`type="text"` va `type="password"`).
    *   Formaga "Ro'yxatdan o'tish" tugmasini qo'shing (`<button type="submit">`).
    *   `render_template()` funksiyasi yordamida shablonni render qiling.
*  **`POST` so'rovi uchun:**
    *   Forma ma'lumotlarini oling (`request.form`).
    *   Foydalanuvchi nomini va parolni ma'lumotlar bazasiga saqlang (`INSERT INTO foydalanuvchilar`).
        *   Yangi foydalanuvchi yaratish uchun SQL buyrug'ini `kursor.execute()` metodi yordamida bajaring.
        *   Ma'lumotlar bazasida o'zgarishlarni saqlash uchun `ulanish.commit()` funksiyasini chaqiring.
    *   Foydalanuvchini `/` route'iga yo'naltiring (`redirect('/')`).

**Tushuntirish:**

*   `@app.route('/register', methods=['GET', 'POST'])` dekoratori yordamida route'ni yarating. Bu dekorator `/register` manziliga kelgan so'rovlarni ushbu funksiya bilan bog'laydi va funksiyaning `GET` va `POST` metodlarini qabul qilishini bildiradi.
*   `if request.method == 'POST':` sharti yordamida so'rov metodini tekshiring. Agar foydalanuvchi ro'yxatdan o'tish formasini yuborsa, `request.method` "POST" qiymatiga ega bo'ladi.
*   `request.form` ob'ektidan foydalanib, formadan ma'lumotlarni oling. Masalan, foydalanuvchi nomini olish uchun `request.form['foydalanuvchi_nomi']` deb yozing.
*   `INSERT INTO` SQL buyrug'i yordamida yangi foydalanuvchini ma'lumotlar bazasiga qo'shing. `kursor.execute()` metodi yordamida SQL buyrug'ini bajaring. Masalan:

    ```python
    kursor.execute("INSERT INTO foydalanuvchilar (foydalanuvchi_nomi, parol) VALUES (?, ?)", (foydalanuvchi_nomi, parol))
    ```

*   `redirect()` funksiyasi yordamida foydalanuvchini boshqa sahifaga yo'naltiring. `redirect('/')` kodi foydalanuvchini asosiy sahifaga yo'naltiradi.  

</details>


<details>
<summary>
3-qadam: Ro'yxatdan o'tish sahifasini yaratish (20 ball)
</summary>



*  `/register` route'i uchun funksiya yarating.
*  Funksiya `GET` va `POST` metodlarini qabul qilsin.
*  **`GET` so'rovi uchun:**
    *   Ro'yxatdan o'tish formasini ko'rsatuvchi HTML shablonini yarating (`register.html`).
    *   Shablonda foydalanuvchi nomi va parol uchun `input` maydonlarini yarating (`type="text"` va `type="password"`).
    *   Formaga "Ro'yxatdan o'tish" tugmasini qo'shing (`<button type="submit">`).
    *   `render_template()` funksiyasi yordamida shablonni render qiling.
*  **`POST` so'rovi uchun:**
    *   Forma ma'lumotlarini oling (`request.form`).
    *   Foydalanuvchi nomini va parolni ma'lumotlar bazasiga saqlang (`INSERT INTO foydalanuvchilar`).
        *   Yangi foydalanuvchi yaratish uchun SQL buyrug'ini `kursor.execute()` metodi yordamida bajaring.
        *   Ma'lumotlar bazasida o'zgarishlarni saqlash uchun `ulanish.commit()` funksiyasini chaqiring.
    *   Foydalanuvchini `/` route'iga yo'naltiring (`redirect('/')`).

**Tushuntirish:**

*   `@app.route('/register', methods=['GET', 'POST'])` dekoratori yordamida route'ni yarating. Bu dekorator `/register` manziliga kelgan so'rovlarni ushbu funksiya bilan bog'laydi va funksiyaning `GET` va `POST` metodlarini qabul qilishini bildiradi.
*   `if request.method == 'POST':` sharti yordamida so'rov metodini tekshiring. Agar foydalanuvchi ro'yxatdan o'tish formasini yuborsa, `request.method` "POST" qiymatiga ega bo'ladi.
*   `request.form` ob'ektidan foydalanib, formadan ma'lumotlarni oling. Masalan, foydalanuvchi nomini olish uchun `request.form['foydalanuvchi_nomi']` deb yozing.
*   `INSERT INTO` SQL buyrug'i yordamida yangi foydalanuvchini ma'lumotlar bazasiga qo'shing. `kursor.execute()` metodi yordamida SQL buyrug'ini bajaring. Masalan:

    ```python
    kursor.execute("INSERT INTO foydalanuvchilar (foydalanuvchi_nomi, parol) VALUES (?, ?)", (foydalanuvchi_nomi, parol))
    ```

*   `redirect()` funksiyasi yordamida foydalanuvchini boshqa sahifaga yo'naltiring. `redirect('/')` kodi foydalanuvchini asosiy sahifaga yo'naltiradi.


</details>



<details>
<summary>
4-qadam: Kirish sahifasini yaratish (20 ball)
</summary>



*   `/login` route'i uchun funksiya yarating.
*   Funksiya `GET` va `POST` metodlarini qabul qilsin.
*   **`GET` so'rovi uchun:**
    *   Kirish formasini ko'rsatuvchi HTML shablonini yarating (`login.html`).
    *   Shablonda foydalanuvchi nomi va parol uchun `input` maydonlarini yarating (`type="text"` va `type="password"`).
    *   Formaga "Kirish" tugmasini qo'shing (`<button type="submit">`).
    *   `render_template()` funksiyasi yordamida shablonni render qiling.
*   **`POST` so'rovi uchun:**
    *   Forma ma'lumotlarini oling (`request.form`).
    *   Foydalanuvchi nomini va parolni ma'lumotlar bazasidagi ma'lumotlar bilan solishtiring (`SELECT` buyrug'i yordamida).
        *   `kursor.execute()` metodi yordamida SQL so'rovini bajaring. Masalan:

            ```python
            kursor.execute("SELECT * FROM foydalanuvchilar WHERE foydalanuvchi_nomi = ?", (foydalanuvchi_nomi,))
            ```
        *   `fetchone()` metodi yordamida natijani oling. Bu metod natijalar to'plamidan birinchi qatorni qaytaradi.

    *   Agar foydalanuvchi topilsa va parol to'g'ri bo'lsa, foydalanuvchini `/` route'iga yo'naltiring (`redirect('/')`).
    *   Aks holda, xato xabarini ko'rsating. Masalan, `flash("Noto'g'ri foydalanuvchi nomi yoki parol")` funksiyasidan foydalanishingiz mumkin.


**Tushuntirish:**

*   **Route yaratish:** `@app.route('/login', methods=['GET', 'POST'])` dekoratori yordamida `/login` route'i uchun funksiya yarating. Bu dekorator `/login` manziliga kelgan so'rovlarni ushbu funksiya bilan bog'laydi. `methods=['GET', 'POST']` qismi esa bu funksiyaning `GET` va `POST` metodlarini qabul qilishini bildiradi.

*   **`GET` so'rovi:**
    *   `GET` so'rovi odatda veb-sahifani serverdan olish uchun ishlatiladi. Bizning holatda, foydalanuvchi `/login` manziliga kirganda, server unga kirish formasini ko'rsatishi kerak.
    *   Kirish formasini yaratish uchun HTML faylini yarating (masalan, `templates` papkasida `login.html` faylini).
    *   Bu faylda foydalanuvchi nomi va parol uchun `input` maydonlarini yarating. `input` tegining `type` atributi "text" yoki "password" bo'lishi mumkin.
    *   Formaga "Kirish" tugmasini qo'shing. Bu tugma bosilganda, formadagi ma'lumotlar serverga `POST` so'rovi bilan yuboriladi.
    *   `render_template()` funksiyasi yordamida HTML shablonini render qiling. Bu funksiya shablon faylini o'qiydi va undagi o'zgaruvchilarni almashtirib, HTML kodini qaytaradi.

*   **`POST` so'rovi:**
    *   `POST` so'rovi odatda serverga ma'lumotlarni yuborish uchun ishlatiladi. Bizning holatda, foydalanuvchi kirish formasini yuborganda, foydalanuvchi nomi va parol serverga `POST` so'rovi bilan yuboriladi.
    *   `request.method == 'POST'` sharti yordamida so'rov metodini tekshiring. Agar so'rov `POST` metodi bilan bo'lsa, demak foydalanuvchi formadagi ma'lumotlarni yuborgan.
    *   `request.form` ob'ektidan foydalanib, formadan ma'lumotlarni oling. Masalan, foydalanuvchi nomini olish uchun `request.form['foydalanuvchi_nomi']` deb yozing.
    *   `SELECT` SQL buyrug'i yordamida foydalanuvchini ma'lumotlar bazasidan qidiring. `kursor.execute()` metodi yordamida SQL so'rovini bajaring. Masalan:

        ```python
        kursor.execute("SELECT * FROM foydalanuvchilar WHERE foydalanuvchi_nomi = ?", (foydalanuvchi_nomi,))
        ```

        Bu yerda `?` belgisi o'rniga `foydalanuvchi_nomi` o'zgaruvchisining qiymati qo'yiladi. Bu SQL injection hujumlaridan himoya qilish uchun ishlatiladi.
    *   `fetchone()` metodi yordamida natijani oling. Bu metod natijalar to'plamidan birinchi qatorni qaytaradi. Agar foydalanuvchi topilmasa, `fetchone()` `None` qiymatini qaytaradi.

    *   Agar foydalanuvchi topilsa va parol to'g'ri bo'lsa:
        *   Foydalanuvchi sessiyasini yarating. Sessiya - bu foydalanuvchi haqidagi ma'lumotlarni serverda saqlash mexanizmi. Bu foydalanuvchi keyingi so'rovlarda ham tizimga kirganligini eslab qolish uchun kerak. Flaskda sessiyalar bilan ishlash uchun `session` ob'ektidan foydalaniladi. Masalan, foydalanuvchi ID'sini sessiyaga saqlash uchun `session['user_id'] = user[0]` deb yozishingiz mumkin. Bu yerda `user[0]` foydalanuvchi haqidagi ma'lumotlarni o'z ichiga olgan kortej (tuple) ning birinchi elementi, ya'ni foydalanuvchi ID'si.
        *   Foydalanuvchini `/` route'iga yo'naltiring (`redirect('/')`).

    *   Aks holda:
        *   Xato xabarini ko'rsating. Masalan, `flash("Noto'g'ri foydalanuvchi nomi yoki parol")` funksiyasidan foydalanishingiz mumkin. `flash()` funksiyasi xabarni keyingi so'rovda ko'rsatish uchun sessiyaga saqlaydi.


</details>


<details>
<summary>
5-qadam: Mahsulotlar ro'yxatini ko'rsatish (10 ball)
</summary>

*   `/` (asosiy sahifa) route'i uchun funksiya yarating.
*   Ma'lumotlar bazasidan mahsulotlar ro'yxatini oling (`SELECT` buyrug'i yordamida).
*   `fetchall()` metodi yordamida natijalarni ro'yxat shaklida oling.
*   Mahsulotlarni ko'rsatuvchi HTML shablonini yarating (`index.html`).
    *   Shablonda `for` sikli yordamida mahsulotlar ro'yxatini ko'rsating.
    *   Har bir mahsulot uchun uning nomi, tavsifi, hozirgi narxi va rasmini ko'rsating.
    *   Har bir mahsulot uchun mahsulot sahifasiga olib boruvchi havola yarating. Havola manzili `/mahsulot/<id>` bo'lishi kerak.
*   `render_template()` funksiyasi yordamida HTML shablonini render qiling va unga mahsulotlar ro'yxatini uzating.

**Tushuntirish:**

*   **Route yaratish:** `@app.route('/')` dekoratori yordamida asosiy route (`/`) uchun funksiya yarating. Bu funksiya foydalanuvchi saytning asosiy manziliga kirganda bajariladi.

*   **Ma'lumotlar bazasidan ma'lumotlarni olish:**
    *   `kursor.execute()` metodi yordamida SQL so'rovini bajaring. `SELECT` buyrug'idan foydalanib, `mahsulotlar` jadvalidan barcha mahsulotlarni oling. Masalan:

        ```python
        kursor.execute("SELECT * FROM mahsulotlar")
        ```

    *   `fetchall()` metodi yordamida natijalarni oling. Bu metod barcha natijalarni ro'yxat shaklida qaytaradi. Har bir element kortej (tuple) bo'lib, u mahsulot haqidagi ma'lumotlarni o'z ichiga oladi. Masalan:

        ```python
        mahsulotlar = kursor.fetchall()
        ```

*   **HTML shablonini yaratish:**
    *   `templates` papkasida `index.html` faylini yarating.
    *   Bu faylda `for` sikli yordamida mahsulotlar ro'yxatini ko'rsating. Jinja shablon tizimida `for` sikli quyidagicha yoziladi:

        ```html
        {% for mahsulot in mahsulotlar %}
          ...
        {% endfor %}
        ```

    *   Har bir mahsulot uchun uning nomi, tavsifi, hozirgi narxi va rasmini ko'rsating. Mahsulot haqidagi ma'lumotlarni olish uchun `mahsulot` o'zgaruvchisidan foydalaning. Masalan, mahsulot nomini ko'rsatish uchun `{{ mahsulot[1] }}` deb yozing (bu yerda `1` - mahsulot nomini o'z ichiga olgan kortejning indeksi).
    *   Har bir mahsulot uchun mahsulot sahifasiga olib boruvchi havola yarating. Havola manzili `/mahsulot/<id>` bo'lishi kerak. Masalan:

        ```html
        <a href="/mahsulot/{{ mahsulot[0] }}">{{ mahsulot[1] }}</a> 
        ```

        Bu yerda `mahsulot[0]` - mahsulot ID'sini o'z ichiga olgan kortejning indeksi.

*   **Shablonni render qilish:**
    *   `render_template()` funksiyasi yordamida HTML shablonini render qiling va unga mahsulotlar ro'yxatini uzating. Masalan:

        ```python
        return render_template('index.html', mahsulotlar=mahsulotlar)
        ```

</details>



<details>
<summary>
6-qadam: Mahsulot qo'shish (10 ball)
</summary>



Endi, foydalanuvchilar uchun mahsulotlarni qo'shish funksiyasini amalga oshiramiz.

*   `/mahsulot_qoshish` route'i uchun `GET` va `POST` metodlarini qabul qiluvchi funksiya yarating.
*   **`GET` so'rovi uchun:**
    *   Mahsulot qo'shish formasini ko'rsatuvchi HTML shablonini yarating (`mahsulot_qoshish.html`).
    *   Shablonda mahsulot nomi, tavsifi, boshlang'ich narxi, sotish muddati va rasm uchun `input` maydonlarini yarating.
        *   Matn kiritish uchun `type="text"` atributini ishlating.
        *   Raqam kiritish uchun `type="number"` atributini ishlating.
        *   Sana va vaqtni kiritish uchun `type="datetime-local"` atributini ishlating.
        *   Fayl yuklash uchun `type="file"` atributini ishlating.
    *   `render_template()` funksiyasi yordamida shablonni render qiling.
*   **`POST` so'rovi uchun:**
    *   Forma ma'lumotlarini oling (`request.form`).
    *   Yangi mahsulotni ma'lumotlar bazasiga qo'shing (`INSERT INTO mahsulotlar`).
        *   Yangi mahsulot yaratish uchun SQL buyrug'ini `kursor.execute()` metodi yordamida bajaring.
        *   Ma'lumotlar bazasida o'zgarishlarni saqlash uchun `ulanish.commit()` funksiyasini chaqiring.
    *   Foydalanuvchini asosiy sahifaga yo'naltiring (`redirect('/')`).

**Tushuntirish:**

*   **Route yaratish:** `@app.route('/mahsulot_qoshish', methods=['GET', 'POST'])` dekoratori yordamida route'ni yarating. Bu dekorator `/mahsulot_qoshish` manziliga kelgan so'rovlarni ushbu funksiya bilan bog'laydi. `methods=['GET', 'POST']` qismi esa bu funksiyaning `GET` va `POST` metodlarini qabul qilishini bildiradi.

*   **`GET` so'rovi:**
    *   `GET` so'rovi odatda veb-sahifani serverdan olish uchun ishlatiladi. Bizning holatda, foydalanuvchi `/mahsulot_qoshish` manziliga kirganda, server unga mahsulot qo'shish formasini ko'rsatishi kerak.
    *   Mahsulot qo'shish formasini yaratish uchun HTML faylini yarating (masalan, `templates` papkasida `mahsulot_qoshish.html` faylini).
    *   Bu faylda mahsulot nomi, tavsifi, boshlang'ich narxi, sotish muddati va rasm uchun `input` maydonlarini yarating.
    *   `render_template()` funksiyasi yordamida HTML shablonini render qiling. Bu funksiya shablon faylini o'qiydi va undagi o'zgaruvchilarni almashtirib, HTML kodini qaytaradi.

*   **`POST` so'rovi:**
    *   `POST` so'rovi odatda serverga ma'lumotlarni yuborish uchun ishlatiladi. Bizning holatda, foydalanuvchi mahsulot qo'shish formasini yuborganda, formadagi ma'lumotlar serverga `POST` so'rovi bilan yuboriladi.
    *   `request.method == 'POST'` sharti yordamida so'rov metodini tekshiring. Agar so'rov `POST` metodi bilan bo'lsa, demak foydalanuvchi formadagi ma'lumotlarni yuborgan.
    *   `request.form` ob'ektidan foydalanib, formadan ma'lumotlarni oling. Masalan, mahsulot nomini olish uchun `request.form['nomi']` deb yozing.
    *   `INSERT INTO` SQL buyrug'i yordamida yangi mahsulotni ma'lumotlar bazasiga qo'shing. `kursor.execute()` metodi yordamida SQL buyrug'ini bajaring.
    *   `redirect()` funksiyasi yordamida foydalanuvchini boshqa sahifaga yo'naltiring. `redirect('/')` kodi foydalanuvchini asosiy sahifaga yo'naltiradi.


</details>


<details>
<summary>
7-qadam: Mahsulot sahifasini yaratish (10 ball)
</summary>

Endi, har bir auksion buyumi uchun alohida sahifalar yarataylik, ularda buyum tafsilotlarini ko'rsatamiz va foydalanuvchilarga takliflar berishga ruxsat beramiz.

*   `/mahsulot/<id>` route'i uchun funksiya yarating. Bu yerda `<id>` mahsulotning identifikatorini bildiradi.
*   Ma'lumotlar bazasidan berilgan `id` ga ega mahsulotni oling (`SELECT` buyrug'i yordamida).
    *   `kursor.execute()` metodi yordamida SQL so'rovini bajaring. `id` parametrini so'rovga berish uchun `?` belgisidan foydalaning. Masalan:

        ```python
        kursor.execute("SELECT * FROM mahsulotlar WHERE id = ?", (id,))
        ```
    *   `fetchone()` metodi yordamida natijani oling. Bu metod natijalar to'plamidan birinchi qatorni qaytaradi.

*   `JOIN` operatoridan foydalanib, mahsulotga tegishli takliflarni oling.
    *   `kursor.execute()` metodi yordamida SQL so'rovini bajaring. `JOIN` operatoridan foydalanib, `takliflar` jadvalini `mahsulotlar` jadvaliga bog'lang. Masalan:

        ```python
        kursor.execute("SELECT * FROM takliflar WHERE mahsulot_id = ?", (id,))
        ```
    *   `fetchall()` metodi yordamida barcha takliflarni oling.

*   Mahsulotni ko'rsatuvchi HTML shablonini yarating (`mahsulot.html`).
    *   Shablonda mahsulot haqida ma'lumotlarni (nomi, tavsifi, rasmi, hozirgi narxi) ko'rsating.
    *   Takliflar ro'yxatini ko'rsating. Har bir taklif uchun foydalanuvchi nomi va taklif narxini ko'rsating.
    *   Taklif berish uchun forma yarating. Formada taklif narxi uchun `input` maydoni bo'lishi kerak.
*   `render_template()` funksiyasi yordamida HTML shablonini render qiling va unga mahsulot va takliflar haqida ma'lumotlarni uzating.

**Tushuntirish:**

*   **Dinamik route yaratish:** `@app.route('/mahsulot/<int:id>')` dekoratori yordamida route'ni yarating. Bu yerda `<int:id>` dinamik qism bo'lib, u mahsulotning ID'sini ifodalaydi. `int:` qismi esa bu qiymatni butun songa aylantiradi.
*   **Ma'lumotlar bazasidan ma'lumotlarni olish:** `SELECT` SQL buyrug'idan foydalanib, ma'lumotlar bazasidan mahsulot haqida ma'lumotlarni oling. `WHERE` shartidan foydalanib, berilgan ID'ga ega mahsulotni tanlang.
*   **Takliflarni olish:** `JOIN` operatoridan foydalanib, mahsulotga tegishli takliflarni oling.
*   **Shablonni render qilish:** `render_template()` funksiyasi yordamida HTML shablonini render qiling. Bu funksiya shablon faylini o'qiydi va undagi o'zgaruvchilarni almashtirib, HTML kodini qaytaradi.
*   **O'zgaruvchilarni uzatish:** `render_template()` funksiyasiga ikkinchi va undan keyingi argumentlar sifatida shablonga uzatiladigan o'zgaruvchilarni bering. Masalan, `return render_template('mahsulot.html', mahsulot=mahsulot, takliflar=takliflar)`


</details>



<details>
<summary>
8-qadam: Taklif berish (10 ball)
</summary>

Bu bosqich foydalanuvchilarga auksion buyumlariga takliflar berishga imkon berishga qaratilgan.

*   `/mahsulot/<id>/taklif` route'i uchun `POST` metodi bilan ishlovchi funksiya yarating.
*   Forma ma'lumotlarini oling (`request.form`).
    * Foydalanuvchi kiritgan taklif narxini `request.form` ob'ektidan oling.
*   Yangi taklifni ma'lumotlar bazasiga qo'shing (`INSERT INTO takliflar`).
    * `kursor.execute()` metodi yordamida SQL buyrug'ini bajaring.
    * Ma'lumotlar bazasida o'zgarishlarni saqlash uchun `ulanish.commit()` funksiyasini chaqiring.
*   Agar taklif narxi hozirgi narxdan katta bo'lsa, mahsulotning hozirgi narxini yangilang (`UPDATE mahsulotlar`).
    * `if` shartidan foydalanib, taklif narxini mahsulotning hozirgi narxi bilan solishtiring.
    * Agar taklif narxi katta bo'lsa, `UPDATE` SQL buyrug'i yordamida mahsulotning hozirgi narxini yangilang.
    * `kursor.execute()` metodi yordamida SQL buyrug'ini bajaring.
    * Ma'lumotlar bazasida o'zgarishlarni saqlash uchun `ulanish.commit()` funksiyasini chaqiring.
*   Foydalanuvchini mahsulot sahifasiga yo'naltiring (`redirect('/mahsulot/<id>')`).

**Tushuntirish:**

*   **Route yaratish:** `@app.route('/mahsulot/<int:id>/taklif', methods=['POST'])` dekoratori yordamida route'ni yarating. Bu yerda `<int:id>` dinamik qism bo'lib, u mahsulotning ID'sini ifodalaydi. `int:` qismi esa bu qiymatni butun songa aylantiradi. `methods=['POST']` qismi esa bu funksiyaning faqat `POST` so'rovlarini qabul qilishini bildiradi.
*   **Ma'lumotlarni olish:** `request.form` ob'ektidan foydalanib, foydalanuvchi kiritgan taklif narxini oling.
*   **Taklifni saqlash:** `INSERT INTO` SQL buyrug'i yordamida yangi taklifni `takliflar` jadvaliga qo'shing.
*   **Narxni yangilash:** `if` shartidan foydalanib, taklif narxini mahsulotning hozirgi narxi bilan solishtiring. Agar taklif narxi katta bo'lsa, `UPDATE` SQL buyrug'i yordamida `mahsulotlar` jadvalidagi mahsulotning hozirgi narxini yangilang.
*   **Yo'naltirish:** `redirect()` funksiyasi yordamida foydalanuvchini mahsulot sahifasiga qayta yo'naltiring.


</details>



<details>
<summary>
9-qadam: Frontend qismini yaratish (10 ball)
</summary>

Endi biz ilovamizning frontend qismiga o'tamiz. Bu bosqichda siz HTML, CSS va JavaScript bilimlaringizdan foydalanib, auksion veb-sayti uchun foydalanuvchi interfeysi yaratasiz.

*   **HTML tuzilishini yaratish:**
    *   Har bir sahifa uchun alohida HTML fayl yarating (masalan, `index.html`, `register.html`, `login.html`, `mahsulot_qoshish.html`, `mahsulot.html`).
    *   Sahifalar tuzilishini yaratish uchun HTML teglaridan foydalaning.
    *   Semantik teglar (`<header>`, `<nav>`, `<main>`, `<article>`, `<aside>`, `<footer>`) dan foydalanib, sahifalarni mantiqiy qismlarga ajrating.
    *   Matnlarni formatlash uchun tegishli teglarni (`<h1>` - `<h6>`, `<p>`, `<ul>`, `<ol>`, `<strong>`, `<em>`) ishlating.
    *   Rasmlarni qo'shish uchun `<img>` tegi va uning atributlaridan (masalan, `src`, `alt`) foydalaning.
    *   Havolalar yaratish uchun `<a>` tegi va uning `href` atributidan foydalaning.
    *   Formalarni yaratish uchun `<form>` tegi va uning ichida `input`, `textarea`, `button` kabi teglarni ishlating.

*   **CSS stillarini qo'llash:**
    *   `style.css` faylida sahifa elementlariga stillarni qo'llang.
    *   CSS selektorlaridan foydalanib, elementlarga stillarni qo'llang.
    *   CSS xossalari va qiymatlaridan foydalanib, elementlarning ko'rinishini o'zgartiring.
    *   Ranglar, shriftlar, chegaralar, fon rasmlari va boshqa stillarni qo'llang.
    *   Sahifalarni turli xil ekran o'lchamlarida to'g'ri ko'rsatish uchun media so'rovlardan foydalaning.

*   **JavaScript funksiyalarini yozish:**
    *   Foydalanuvchi interfeysi logikasini boshqarish uchun JavaScript kodini yozing.
    *   `fetch()` API'si yordamida backend API'siga so'rovlar yuboring va javoblarni qayta ishlang.
    *   Masalan, ro'yxatdan o'tish formasini yuborish, mahsulot qo'shish, taklif berish va boshqa amallarni bajarish uchun JavaScript kodini yozing.
    *   DOM (Document Object Model) bilan ishlashni o'rganing. DOM yordamida siz veb-sahifa elementlarini dinamik ravishda o'zgartirishingiz mumkin.

**Tushuntirish:**

*   Frontend qismi foydalanuvchi bilan o'zaro aloqada bo'ladigan veb-saytning ko'rinadigan qismidir.
*   HTML, CSS va JavaScript - bu frontend yaratish uchun ishlatiladigan asosiy texnologiyalar.
*   HTML sahifa tuzilishini, CSS sahifa stilini, JavaScript esa sahifa logikasini belgilaydi.
*   `fetch()` API'si veb-serverga (backendga) so'rovlar yuborish va javoblarni olish uchun ishlatiladi.
*   DOM (Document Object Model) - bu veb-sahifaning ob'ektga yo'naltirilgan modeli. U HTML hujjatni daraxt shaklida tasavvur qiladi, bu yerda har bir element tugun (node) hisoblanadi. JavaScript yordamida DOMga kirish va uni o'zgartirish mumkin.

Bu bosqichda siz o'zingizning ijodiy yechimlaringizni qo'llab, auksion veb-saytini yanada jozibador va funksional qilishingiz mumkin.

</details>



<details>
<summary>
10-qadam: Ilovani ishga tushirish va sinab ko'rish
</summary>



Endi biz yaratgan onlayn auksion ilovamizni ishga tushirib, uning to'g'ri ishlashini tekshirib ko'ramiz.

* `app.run(debug=True)` funksiyasi yordamida ilovani ishga tushiring.
* Brauzerda `http://127.0.0.1:5000/` manziliga kiring.
* Veb-saytning barcha funksiyalarini sinab ko'ring:
    * Ro'yxatdan o'tish va kirish.
    * Mahsulot qo'shish.
    * Mahsulotlar ro'yxatini ko'rish.
    * Mahsulot sahifasini ko'rish.
    * Taklif berish.

**Tushuntirish:**

*   `app.run()` funksiyasi Flask ilovasini ishga tushiradi.
*   `debug=True` parametri disk raskadrovka rejimini yoqadi. Bu rejimda kodda xatolik bo'lsa, brauzerda xato haqida batafsil ma'lumot ko'rsatiladi.
*   Ilovani ishga tushirgandan so'ng, brauzerda `http://127.0.0.1:5000/` manziliga kiring. Bu sizning ilovangizning asosiy sahifasi bo'ladi.
*   Veb-saytning barcha funksiyalarini sinab ko'ring va ularning to'g'ri ishlashini tekshiring.
*   Agar xatoliklar topsangiz, ularni tuzating.
*   Kodni toza va tushunarli qilib yozing.
*   Kodga izoh (comment) lar qo'shing.

Bu yakuniy bosqichda siz yaratgan ilovangizni sinab ko'rasiz va uni takomillashtirasiz.

</details>

