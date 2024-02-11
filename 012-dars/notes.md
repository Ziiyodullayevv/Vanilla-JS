# Objects

---

**Ob'ektni imzolangan fayllarga ega kabinet sifatida tasavvur qilishimiz mumkin. Har bir ma'lumot bo'lagi kalit yordamida o'z faylida saqlanadi. Faylni nomi bo'yicha topish yoki faylni qo'shish/o'chirish oson**

```
let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax
```

_Mulkni olib tashlash uchun biz deleteoperatordan foydalanishimiz mumkin:_

```
delete user.age;
```

_Biz ko'p so'zli xususiyat nomlaridan ham foydalanishimiz mumkin, ammo keyin ularni keltirish kerak:_

```
let user = {
  name: "John",
  age: 30,
  "likes birds": true  // multiword property name must be quoted
};
```

### Kvadrat qavslar

_Ko'p so'zli xususiyatlar uchun nuqta kirish ishlamaydi:_

```
// this would give a syntax error
user.likes birds = true
```

**JavaScript buni tushunmaydi. Biz murojaat qilamiz, deb o'ylaydi ''user.likesva'' kutilmaganda yuz berganda sintaksis xatosi beradi birds.**

_Har qanday satr bilan ishlaydigan muqobil "kvadrat qavs yozuvi" mavjud:_

```
let user = {};

// set
user["likes birds"] = true;

// get
alert(user["likes birds"]); // true

// delete
delete user["likes birds"];
```

```
let key = "likes birds";

// same as user["likes birds"] = true;
user[key] = true;
```

_Nuqta belgisini shunga o'xshash tarzda ishlatib bo'lmaydi:_

```
let user = {
  name: "John",
  age: 30
};

let key = "name";
alert( user.key ) // undefined
```

**Kvadrat qavslar nuqta belgilaridan ko'ra kuchliroqdir. Ular har qanday xususiyat nomlari va o'zgaruvchilarga ruxsat beradi. Lekin ularni yozish ham qiyinroq.**

```
function makeUser(name, age) {
  return {
    name: name,
    age: age,
    // ...other properties
  };
}

let user = makeUser("John", 30);
alert(user.name); // John
```

```
function makeUser(name, age) {
  return {
    name, // same as name: name
    age,  // same as age: age
    // ...
  };
}
```

_Mavjud bo'lmagan xususiyatni o'qish faqat qaytib keladi undefined. Shunday qilib, biz mulk mavjudligini osongina tekshirishimiz mumkin:_

```
let user = {};

alert( user.noSuchProperty === undefined ); // true means "no such property"
```

**Buning uchun maxsus operator ham mavjud**

`"key" in object`

```
let user = { name: "John", age: 30 };

alert( "age" in user ); // true, user.age exists
alert( "blabla" in user ); // false, user.blabla doesn't exist
```

```
let user = { age: 30 };

let key = "age";
alert( key in user ); // true, property "age" exists
```

### Nima uchun inoperator mavjud? solishtirish kifoya emasmi undefined ga?

**Xo'sh, ko'pincha undefined bilan tekshirish yaxshi ishlaydi. Lekin boshqa bir holat mavjud.**

_Bu ob'ekt xususiyati undefined bolganda:_

```
let obj = {
  test: undefined
};

alert( obj.test ); // it's undefined, so - no such property?

alert( "test" in obj ); // true, the property does exist!
```

### "for..in" tsikli

```
for (key in object) {
  // executes the body for each key among object properties
}
```

```
let user = {
  name: "John",
  age: 30,
  isAdmin: true
};

for (let key in user) {
  // keys
  alert( key );  // name, age, isAdmin
  // values for the keys
  alert( user[key] ); // John, 30, true
}
```

**hunday qilib, telefon kodlari bilan bog'liq muammoni hal qilish uchun biz kodlarni butun son bo'lmagan qilib "aldashimiz" mumkin. Har bir koddan oldin ortiqcha "+"belgisini qo'shish kifoya.**

```
let codes = {
  "+49": "Germany",
  "+41": "Switzerland",
  "+44": "Great Britain",
  // ..,
  "+1": "USA"
};

for (let code in codes) {
  alert( +code ); // 49, 41, 44, 1
}
```
