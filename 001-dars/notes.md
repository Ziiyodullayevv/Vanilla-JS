### Skriptlardan oldin va keyin comment yozish:

**Haqiqatan ham qadimiy kitoblar va qo'llanmalarda siz _script_ teglar ichida sharhlarni topishingiz mumkin, masalan:**

`<script type="text/javascript"><!--...--></script>`

**Ushbu hiyla zamonaviy JavaScript-da qo'llanilmaydi. Ushbu sharhlar _script_ tegni qanday qayta ishlashni bilmagan eski brauzerlardan yashiradi. So'nggi 15 yil ichida chiqarilgan brauzerlarda bunday muammo bo'lmaganligi sababli, bunday sharh haqiqatan ham eski kodni aniqlashga yordam beradi.**

### ES6 To'liq URL manzilini ham berishimiz mumkin. Masalan:

`<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js"></script>`

### Bir nechta skriptlarni biriktirish uchun bir nechta teglardan foydalaning:

`<script src="/js/script1.js"></script>`

`<script src="/js/script2.js"></script>`

### Yodda tuting:

**Qoidaga ko'ra, HTMLga faqat eng oddiy skriptlar qo'yiladi.
Alohida faylning afzalligi shundaki, brauzer uni yuklab oladi va keshda saqlaydi .
Xuddi shu skriptga havola qilingan boshqa sahifalar uni yuklab olish o'rniga keshdan oladi, shuning uchun fayl aslida bir marta yuklab olinadi.
Bu trafikni kamaytiradi va sahifalarni tezroq qiladi.**
