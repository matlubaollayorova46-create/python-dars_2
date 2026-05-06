# python-dars_2
Virtual muhit nima
Pythondagi virtual muhit - bu sizning kompyuteringizdagi izolyatsiya qilingan muhit bo'lib, u yerda siz Python loyihalaringizni ishga tushirishingiz va sinab ko'rishingiz mumkin.

Bu sizga boshqa loyihalarga yoki asl Python o'rnatilishiga xalaqit bermasdan loyihaga xos bog'liqliklarni boshqarish imkonini beradi.

Virtual muhitni har bir Python loyihasi uchun alohida konteyner deb tasavvur qiling. Har bir konteyner:

O'zining Python tarjimoniga ega
O'rnatilgan paketlarning o'ziga xos to'plamiga ega
Boshqa virtual muhitlardan ajratilgan
Xuddi shu paketning turli versiyalariga ega bo'lishi mumkin
Virtual muhitlardan foydalanish muhim, chunki:

Loyihalar o'rtasidagi paket versiyalaridagi ziddiyatlarning oldini oladi
Loyihalarni yanada ko'chma va takrorlanadigan qiladi
Python o'rnatish tizimingizni toza saqlaydi
Pythonning turli versiyalari bilan sinovdan o'tkazishga imkon beradi
Virtual muhit yaratish
venvPython virtual muhitlarni yaratish uchun o'rnatilgan modulga ega .

Kompyuteringizda virtual muhit yaratish uchun buyruq satrini oching va loyihangizni yaratmoqchi bo'lgan papkaga o'ting, so'ngra ushbu buyruqni kiriting:

MisolO'zingizning Python serveringizni oling
Quyidagi nomli virtual muhit yaratish uchun ushbu buyruqni bajaring myfirstproject:

DerazalarmacOS/Linux
C:\Users\Your Name> python -m venv myfirstproject
Bu virtual muhitni o'rnatadi va quyidagi kabi pastki papkalar va fayllarga ega "myfirstproject" nomli papka yaratadi:

Natija
Fayl/papka tuzilishi quyidagicha ko'rinadi:

myfirstproject
  Include
  Lib
  Scripts
  .gitignore
  pyvenv.cfg
Virtual muhitni faollashtirish
Virtual muhitdan foydalanish uchun uni quyidagi buyruq bilan faollashtirishingiz kerak:

Misol
Virtual muhitni faollashtirish:

DerazalarmacOS/Linux
C:\Users\Your Name> myfirstproject\Scripts\activate
Faollashtirilgandan so'ng, sizning so'rovingiz endi faol muhitda ishlayotganingizni ko'rsatish uchun o'zgaradi:

Natija
Virtual muhit faol bo'lganda buyruq satri quyidagicha ko'rinadi:

DerazalarmacOS/Linux
(myfirstproject) C:\Users\Your Name>

REKLAMALARNI OLIB TASHLASH

O'rnatish paketlari
Virtual muhitingiz faollashtirilgandan so'ng, siz unga dan foydalanib paketlarni o'rnatishingiz mumkin pip.

Biz "cowsay" deb nomlangan paketni o'rnatamiz:

Misol
Virtual muhitda 'cowsay' ni o'rnating:

DerazalarmacOS/Linux
(myfirstproject) C:\Users\Your Name> pip install cowsay
Natija
'cowsay' faqat virtual muhitda o'rnatiladi:

Collecting cowsay
  Downloading cowsay-6.1-py3-none-any.whl.metadata (5.6 kB)
Downloading cowsay-6.1-py3-none-any.whl (25 kB)
Installing collected packages: cowsay
Successfully installed cowsay-6.1

[notice] A new release of pip is available: 25.0.1 -> 25.1.1
[notice] To update, run: python.exe -m pip install --upgrade pip

REKLAMALARNI OLIB TASHLASH

Paketdan foydalanish
Endi virtual muhitingizga "cowsay" moduli o'rnatilgandan so'ng, keling, undan gapiradigan sigirni ko'rsatish uchun foydalanaylik.

test.pyKompyuteringizda chaqiriladigan fayl yarating . Uni xohlagan joyingizga joylashtirishingiz mumkin, lekin men uni papka bilan bir xil joyga joylashtiraman - papkadamyfirstproject emas , balki bir xil joyga.

Faylni oching va unga quyidagi uchta qatorni qo'ying:

Misol
Ikki qator qo'ying test.py:

test.py
import cowsay

cowsay.cow("Good Mooooorning!")
Keyin, virtual muhitda bo'lganingizda faylni ishga tushirishga harakat qiling:

Misol
test.pyVirtual muhitda bajaring :

DerazalarmacOS/Linux
(myfirstproject) C:\Users\Your Name> python test.py
Natijada, sizning terminalingizda sigir paydo bo'ladi:

Natija
"Cowsay" modulining maqsadi siz bergan har qanday ma'lumotni aytadigan sigirni chizishdir:

  _________________
| Good Mooooorning! |
  =================
                 \
                  \
                    ^__^
                    (oo)\_______
                    (__)\       )\/\
                        ||----w |
                        ||     ||

Virtual muhitni o'chirish
Virtual muhitni o'chirish uchun quyidagi buyruqdan foydalaning:

Misol
Virtual muhitni o'chiring:

DerazalarmacOS/Linux
(myfirstproject) C:\Users\Your Name> deactivate
Natijada, siz endi odatiy buyruq satri interfeysiga qaytdingiz:

Natija
Oddiy buyruq satri interfeysi:

DerazalarmacOS/Linux
C:\Users\Your Name>
Agar faylni virtual muhitdan tashqarida ishga tushirishga harakat qilsangiz test.py, "cowsay" yo'qligi sababli xatolik yuzaga keladi. U faqat virtual muhitda o'rnatilgan:

Misol
test.pyVirtual muhitdan tashqarida bajaring :

DerazalarmacOS/Linux
C:\Users\Your Name> python test.py
Natija
Xato, chunki 'cowsay' yo'q:

Traceback (most recent call last):
  File "C:\Users\Your Name\test.py", line 1, in <module>
    import cowsay
ModuleNotFoundError: No module named 'cowsay'
Eslatma: Virtual muhit myfirstprojecthali ham mavjud, u shunchaki faollashtirilmagan. Agar siz virtual muhitni yana faollashtirsangiz, faylni ishga tushirishingiz mumkin test.py va diagramma ko'rsatiladi.

Virtual muhitni o'chirish
Virtual muhit bilan ishlashning yana bir yaxshi tomoni shundaki, agar siz uni biron sababga ko'ra o'chirmoqchi bo'lsangiz, unga bog'liq boshqa loyihalar bo'lmaydi va faqat belgilangan virtual muhitdagi modullar va fayllar o'chiriladi.

Virtual muhitni o'chirish uchun siz shunchaki uning barcha mazmuni bilan papkani o'chirishingiz mumkin. Yoki to'g'ridan-to'g'ri fayl tizimida yoki buyruq satri interfeysidan quyidagicha foydalanishingiz mumkin:

Misol
myfirstprojectBuyruq satri interfeysidan o'chirish :

DerazalarmacOS/Linux
C:\Users\Your Name> rmdir /s /q myfirstproject
