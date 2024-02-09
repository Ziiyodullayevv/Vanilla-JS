# Loops: while and for

---

**Looplar bir xil kodni bir necha marta takrorlash usulidir.**

### While

```
let i = 0;
while (i < 3) { // shows 0, then 1, then 2
alert( i );
i++;
}
```

**Loop tanasining bitta bajarilishi iteratsiya deb ataladi . Yuqoridagi misoldagi halqa uchta takrorlashni amalga oshiradi.**

```
let i = 3;
while (i) { // when i becomes 0, the condition becomes falsy, and the loop stops
  alert( i );
  i--;
}
```

### Bir chiziqli tana uchun jingalak qavslar kerak emas

```
let i = 3;
while (i) alert(i--);
```

### “do...while” tsikli

```
do {
  // loop body
} while (condition);
```

**Loop avval tanani bajaradi, keyin holatni tekshiradi va haqiqat bo'lsa ham, uni qayta-qayta bajaradi.**

```
let i = 0;
do {
  alert( i );
  i++;
} while (i < 3);
```

**Sintaksisning bu shakli faqat shartning to'g'ri bo'lishidan qat'i nazar, tsiklning tanasi kamida bir marta bajarilishini xohlaganingizda ishlatilishi kerak**

### "For" tsikli

```
for (begin; condition; step) {
  // ... loop body ...
}
```

### Keling, for bayonotni qisman ko'rib chiqaylik:

```
for (let i = 0; i < 3; i++) { // shows 0, then 1, then 2
  alert(i);
}
```

**boshlanishi let i = 0 Loopga kirgandan keyin bir marta bajariladi.**
**holat i < 3 Har bir sikl iteratsiyasidan oldin tekshiriladi. Agar noto'g'ri bo'lsa, tsikl to'xtaydi.**
**tanasi alert(i) Vaziyat haqiqat bo'lganda qayta-qayta ishlaydi.**
**qadam i++ Har bir iteratsiyada tanadan keyin bajariladi.**

```
let i = 0; // we have i already declared and assigned

for (; i < 3; i++) { // no need for "begin"
  alert( i ); // 0, 1, 2
}
```

```
for (;;) {
  // repeats without limits
}
```

```
for (let i = 0; i < 10; i++) {

  // if true, skip the remaining part of the body
  if (i % 2 == 0) continue;

  alert(i); // 1, then 3, 5, 7, 9
}
```

### LabelName

```
outer: for (let i = 0; i < 3; i++) {

  for (let j = 0; j < 3; j++) {

    let input = prompt(`Value at coords (${i},${j})`, '');

    // if an empty string or canceled, then break out of both loops
    if (!input) break outer; // (*)

    // do something with the value...
  }
}

alert('Done!');
```
