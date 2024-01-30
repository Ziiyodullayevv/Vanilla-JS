# Vareables

---

**O'zgaruvchi ma'lumotlar uchun "nomli xotira" dir. Biz o'zgaruvchilardan shirinliklar, tashrif buyuruvchilar va boshqa ma'lumotlarni saqlash uchun foydalanishimiz mumkin.**

_Quyidagi bayonot “message” nomli o‘zgaruvchini yaratadi (boshqacha aytganda: e’lon qiladi ):_

`let message;`

_Endi biz tayinlash operatoridan foydalanib, unga ba'zi ma'lumotlarni kiritishimiz mumkin:_

`message = 'Hello';`

_Shuningdek, biz bir qatorda bir nechta o'zgaruvchilarni e'lon qilishimiz mumkin:_

`let user = 'John', age = 25, message = 'Hello';`

**Bu qisqaroq tuyulishi mumkin, lekin biz buni tavsiya etmaymiz. Yaxshiroq o'qilishi uchun har bir o'zgaruvchiga bitta qatordan foydalaning.**

**Biz qutiga istalgan qiymatni qo'yishimiz mumkin. Shuningdek, biz uni xohlagancha o'zgartirishimiz mumkin:**

```
let message;

message = 'Hello!';

message = 'World!';
```

**Qiymat o'zgartirilganda, eski ma'lumotlar o'zgaruvchidan o'chiriladi.**

**Ikki marta e'lon qilish xatolikni keltirib chiqaradi O'zgaruvchi faqat bir marta e'lon qilinishi kerak.**

```
let message = "This";

// repeated 'let' leads to an error
let message = "That"; // SyntaxError: 'message' has already been declared
```

### O'zgaruvchilarni nomlash

_JavaScript-da o'zgaruvchilar nomlarida ikkita cheklov mavjud:_

1. Ism faqat harflar, raqamlar yoki belgilarni o'z ichiga olishi kerak.
2. Birinchi belgi raqam bo'lmasligi kerak.

**O'zgaruvchilar nomli appleva APPLEikki xil o'zgaruvchilardir.**

### Zaxiralangan nomlar

**Zaxiralangan so'zlar ro'yxati mavjud bo'lib , ularni o'zgaruvchan nom sifatida ishlatib bo'lmaydi, chunki ular tilning o'zi tomonidan qo'llaniladi.**

### use strict

**Odatda, biz uni ishlatishdan oldin o'zgaruvchini aniqlashimiz kerak. Ammo qadimgi davrlarda let dan foydalanmasdan faqat qiymatni belgilash orqali o'zgaruvchini yaratish texnik jihatdan mumkin edi. Agar biz eski skriptlar bilan moslikni saqlab qolish uchun "use strict" kiritmasak, bu hozir ham ishlaydi .**

_Bu yomon amaliyot va qattiq rejimda xatolikka olib keladi:_

```
"use strict";

num = 5; // error: num is not defined
```

### Konstantalar

**Doimiy (o'zgarmas) o'zgaruvchini e'lon qilish uchun let o'rniga const foydalaning**

`const myBirthday = '18.04.1982';`
