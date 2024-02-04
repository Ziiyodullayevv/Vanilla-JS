# Basic operators, maths

---

**Agar operator bitta operandga ega bo'lsa, _unary_ hisoblanadi.**

_Masalan:_

```
let x = 1;

x = -x;
alert( x ); // -1, unary negation was applied
```

**Agar operator ikkita operandga ega bo'lsa, _binary_ hisoblanadi. Xuddi shu minus ikkilik shaklda ham mavjud**

_Masalan:_

```
let x = 1, y = 3;
alert( y - x ); // 2, binary minus subtracts values
```

### Remainder %

```
alert( 5 % 2 ); // 1, the remainder of 5 divided by 2
alert( 8 % 3 ); // 2, the remainder of 8 divided by 3
alert( 8 % 4 ); // 0, the remainder of 8 divided by 4
```

### Exponentiation

```
alert( 2 ** 2 ); // 2² = 4
alert( 2 ** 3 ); // 2³ = 8
alert( 2 ** 4 ); // 2⁴ = 16
```

**Xuddi matematikada bo'lgani kabi, _exponentiation_ operatori ham butun son bo'lmagan sonlar uchun aniqlanadi.**

```
alert( 4 ** (1/2) ); // 2 (power of 1/2 is the same as a square root)
alert( 8 ** (1/3) ); // 2 (power of 1/3 is the same as a cubic root)
```

### Ikkilik + bilan satrlarni birlashtirish (concatenation)

```
alert( '1' + 2 ); // "12"
alert( 2 + '1' ); // "21"

let s = "my" + "string";
alert(s); // mystring
```

### Numeric conversion, unary +

```
// No effect on numbers
let x = 1;
alert( +x ); // 1

let y = -2;
alert( +y ); // -2

// Converts non-numbers
alert( +true ); // 1
alert( +"" );   // 0


let apples = "2";
let oranges = "3";

// both values converted to numbers before the binary plus
alert( +apples + +oranges ); // 5

// the longer variant
// alert( Number(apples) + Number(oranges) ); // 5
```

### Operator ustunligi

```
let a = 1;
let b = 2;

let c = 3 - (a = b + 1);

alert( a ); // 3
alert( c ); // 0
```

**Agar ifoda bir nechta operatorga ega bo'lsa, bajarilish tartibi ularning ustuvorligiga qaraydi**

_Operatirlar ustuvorlik jadvali:_

| Precedence | Name           | Sign |
| ---------- | -------------- | ---- |
| **…**      | …              | …    |
| **14**     | unary plus     | +    |
| **14**     | unary negation | -    |
| **13**     | exponentiation | \*\* |
| **12**     | multiplication | \*   |
| **12**     | division       | /    |
| **11**     | addition       | +    |
| **11**     | subtraction    | -    |
| **2**      | assignment     | =    |

