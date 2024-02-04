# Comparisons

---

### String taqqoslash

**Satrlar harfma-harf taqqoslanadi.**

```
alert( 'Z' > 'A' ); // true
alert( 'Glow' > 'Glee' ); // true
alert( 'Bee' > 'Be' ); // true
```

_Ikki qatorni solishtirish algoritmi oddiy:_

**Ikkala satrning birinchi belgisini solishtiring.**
**Agar birinchi satrning birinchi belgisi boshqa satrdan kattaroq (yoki kichik) bo'lsa, birinchi qator ikkinchisidan kattaroq (yoki kamroq) bo'ladi. Biz tugatdik.**
**Aks holda, agar ikkala satrning birinchi belgilari bir xil bo'lsa, ikkinchi belgilarni bir xil tarzda solishtiring.**
**Ikkala satrning oxirigacha takrorlang.**
**Agar ikkala satr bir xil uzunlikda tugasa, ular tengdir. Aks holda, uzunroq satr kattaroq bo'ladi.**

### Haqiqiy lug'at emas, balki Unicode tartibi

**Yuqorida keltirilgan taqqoslash algoritmi taxminan lug'atlar yoki telefon kitoblarida qo'llaniladigan algoritmga teng, ammo u mutlaqo bir xil emas.**

**Katta harf "A" kichik harf "a"ga teng emas. Qaysi biri kattaroq? Kichik harf "a". Nega? Chunki kichik harf JavaScript ishlatadigan ichki kodlash jadvalida kattaroq indeksga ega (Unicode). Buning aniq tafsilotlari va oqibatlariga Strings bobida qaytamiz.**

### Boolean is the result

```
alert( 2 > 1 );  // true (correct)
alert( 2 == 1 ); // false (wrong)
alert( 2 != 1 ); // true (correct)

let result = 5 > 4; // assign the result of the comparison
alert( result ); // true
```

### Comparison of different types

```
alert( '2' > 1 ); // true, string '2' becomes a number 2
alert( '01' == 1 ); // true, string '01' becomes a number 1

alert( true == 1 ); // true
alert( false == 0 ); // true
```

### Qiziqarli natija

_Ehtimol, bir vaqtning o'zida:_

**Ikki qiymat teng.**

**Ulardan biri true mantiqiy, ikkinchisi esa false mantiqiy.**

_Masalan:_

```
let a = 0;
alert( Boolean(a) ); // false

let b = "0";
alert( Boolean(b) ); // true

alert(a == b); // true!
```

**JavaScript nuqtai nazaridan, bu natija juda normaldir. Tenglik tekshiruvi qiymatlarni raqamli konvertatsiya yordamida o'zgartiradi (shuning uchun "0" 0ga aylanadi), aniq Boolean konvertatsiya esa boshqa qoidalar to'plamidan foydalanadi.**

### Null va undefined bilan taqqoslash

```
alert( null === undefined ); // false
alert( null == undefined ); // true

alert( null > 0 );  // (1) false
alert( null == 0 ); // (2) false
alert( null >= 0 ); // (3) true
```

### Strange result: null vs 0

```
alert( null > 0 );  // (1) false
alert( null == 0 ); // (2) false
alert( null >= 0 ); // (3) true
```

**Matematik jihatdan, bu g'alati. Oxirgi natijada aytilishicha, "null noldan katta yoki teng", shuning uchun yuqoridagi taqqoslashlardan birida u to'g'ri bo'lishi kerak, lekin ikkalasi ham noto'g'ri.**

**Sababi tenglikni tekshirish == va taqqoslash > < >= <= boshqacha ishlaydi. Taqqoslash nullni raqamga aylantirib, uni 0 deb hisoblaydi. Shuning uchun (3) null >= 0 rost va (1) null > 0 noto‘g‘ri.**

**Boshqa tomondan, undefined va null uchun == tenglik tekshiruvi shunday aniqlanadiki, hech qanday konvertatsiyasiz ular bir-biriga tenglashadi va boshqa hech narsaga teng kelmaydi. Shuning uchun (2) null == 0 noto'g'ri.**

```
5 > 4
"apple" > "pineapple"
"2" > "12"
undefined == null
undefined === null
null == "\n0\n" // false;
null === +"\n0\n" //false;
```
