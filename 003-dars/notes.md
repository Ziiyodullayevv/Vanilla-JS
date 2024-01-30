# The modern mode, "use strict"

**Uzoq vaqt davomida JavaScript moslik muammosisiz rivojlandi. Tilga yangi funksiyalar qo‘shildi, eski funksiya esa o‘zgarmadi.**

**Bu mavjud kodni hech qachon buzmaslikning foydasiga ega edi. Ammo salbiy tomoni shundaki, JavaScript yaratuvchilari tomonidan qilingan har qanday xato yoki nomukammal qaror tilda abadiy qolib ketgan.**

**Bu 2009 yilgacha ECMAScript 5 (ES5) paydo bo'lgunga qadar shunday edi. U tilga yangi xususiyatlarni qo'shdi va mavjudlarini o'zgartirdi. Eski kodning ishlashini ta'minlash uchun bunday o'zgartirishlarning aksariyati sukut bo'yicha o'chirilgan. Siz ularni maxsus direktiva bilan aniq yoqishingiz kerak: "use strict".**

**Agar u skriptning yuqori qismida joylashgan bo'lsa, butun skript "zamonaviy" usulda ishlaydi.**

**U ko'pgina brauzerlarda, ya'ni Firefox va Chrome brauzerlarida ishlaydi.**

**Agar bunday bo'lmasa, masalan, eski brauzerda, ni ta'minlashning yomon, ammo ishonchli usuli bor use strict. Uni shunday o'ramga soling:**

```
(function() {
  'use strict';

  // ...your code here...
})()
```

**Zamonaviy JavaScript "classlar" va "modullar" ni qo'llab-quvvatlaydi. Ular "use strict"ni avtomatik ravishda yoqadi. Shunday qilib, agar biz ulardan foydalansak, uni qo'shishimiz shart emas .**


