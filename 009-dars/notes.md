# Logical operators

---

**JavaScript-da to'rtta mantiqiy operator mavjud: ||(OR), &&(VA), !(NOT), ??(Nullish Coalescing).**

### || Operatori

```
alert( true || true );   // true
alert( false || true );  // true
alert( true || false );  // true
alert( false || false ); // false
```

_Agar operand mantiqiy bo'lmasa, u baholash uchun mantiqiyga aylantiriladi._

```
if (1 || 0) { // works just like if( true || false )
  alert( 'truthy!' );
}
```

```
let hour = 9;

if (hour < 10 || hour > 18) {
  alert( 'The office is closed.' );
}
```

```
let firstName = "";
let lastName = "";
let nickName = "SuperCoder";

alert( firstName || lastName || nickName || "Anonymous"); // SuperCoder
```

### && Operatori

```
alert( true && true );   // true
alert( false && true );  // false
alert( true && false );  // false
alert( false && false ); // false
```

```
let hour = 12;
let minute = 30;

if (hour == 12 && minute == 30) {
  alert( 'The time is 12:30' );
}
```

_Natija avval 1 keyin esa 2 chiqadi:_

```
alert( alert(1) || 2 || alert(3) );
// birinchi alert(1) dan undefined qaytadi
```

### Important

**AND && ustunligi OR || dan yuqori**
**AND && operatorining ustuvorligi OR || dan yuqori.**

**Shunday qilib, a && b || kodi c && d, asosan, && iboralari qavs ichida bo'lgani bilan bir xil: (a && b) || (c && d).**
