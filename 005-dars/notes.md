# Data Types

---

### Numbers

_Oddiy raqamlardan tashqari, ushbu ma'lumotlar turiga tegishli "maxsus raqamli qiymatlar" ham mavjud:_

`Infinity, -Infinityva NaN.`

**Infinitymatematik Infinity ∞ ni ifodalaydi. Bu har qanday raqamdan kattaroq bo'lgan maxsus qiymat.**

_Biz uni nolga bo'lish natijasida olishimiz mumkin:_

`alert( 1 / 0 ); // Infinity`

```
alert( NaN + 1 ); // NaN
alert( 3 * NaN ); // NaN
alert( "not a number" / 2 - 1 ); // NaN
```

### BigInt

**JavaScript-da “raqam” turi manfiylardan kattaroq (bu ) yoki undan kichik butun son qiymatlarini ishonchli tarzda ifodalay olmaydi .**

`(253-1)9007199254740991-(253-1)`

```
console.log(9007199254740991 + 1); // 9007199254740992
console.log(9007199254740991 + 2); // 9007199254740992
```

```
// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;
```

### Null

**JavaScript-da nullba'zi boshqa tillardagi kabi "mavjud bo'lmagan ob'ektga havola" yoki "null ko'rsatgich" emas.**

**Bu shunchaki "hech narsa", "bo'sh" yoki "qiymat noma'lum" ni ifodalovchi maxsus qiymat.**

## Undefined

**Maxsus qiymat undefinedham alohida turadi. Xuddi ga o'xshab o'ziga xos tur yaratadi null.**

**Ma'nosi undefined"qiymat belgilanmagan".**

`let age;// undefinded`

```
typeof undefined // "undefined"

typeof 0 // "number"

typeof 10n // "bigint"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol("id") // "symbol"

typeof Math // "object"  (1)

typeof null // "object"  (2)

typeof alert // "function"  (3)
```

**typeof "null" //object. Bu JavaScript-ning dastlabki kunlaridan kelib chiqqan va muvofiqlik uchun saqlangan rasman tan olingan xato. Albatta, null ob'ekt emas. Bu o'zining alohida turiga ega bo'lgan maxsus qiymatdir.**
