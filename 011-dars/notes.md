# Funksiyalar

---

```
function showPrimes(n) {
  nextPrime: for (let i = 2; i < n; i++) {

    for (let j = 2; j < i; j++) {
      if (i % j == 0) continue nextPrime;
    }

    alert( i ); // a prime
  }
}
```

_Afzal koriladi_

```
function showPrimes(n) {

  for (let i = 2; i < n; i++) {
    if (!isPrime(i)) continue;

    alert(i);  // a prime
  }
}

function isPrime(n) {
  for (let i = 2; i < n; i++) {
    if ( n % i == 0) return false;
  }
  return true;
}
```

### Funktsiyani nomlash

```
"get…"- qiymatni qaytarish,
"calc…"- biror narsani hisoblash,
"create…"- biror narsa yaratish,
"check…"- biror narsani tekshiring va mantiqiy qiymatni qaytaring va hokazo.
```

### Bitta funktsiya - bitta harakat

**Funktsiya o'z nomi bilan taklif qilingan narsani bajarishi kerak, boshqa emas.**

**Ikki mustaqil harakat odatda ikkita funktsiyaga loyiqdir, hatto ular odatda birgalikda chaqirilsa ham (bu holda biz bu ikkalasini chaqiradigan uchinchi funktsiyani yaratishimiz mumkin).**

### Funktsiya - bu qiymat

```
function sayHi() {
  alert( "Hello" );
}
```

```
let sayHi = function() {
  alert( "Hello" );
};
```

**Yana takrorlaymiz: funktsiya qanday yaratilganidan qat'i nazar, funktsiya qiymatdir. Yuqoridagi ikkala misol ham funktsiyani ''sayHi'' o'zgaruvchida saqlaydi**

### Biz funktsiyani boshqa o'zgaruvchiga nusxalashimiz mumkin:

```
function sayHi() {   // (1) create
  alert( "Hello" );
}

let func = sayHi;    // (2) copy

func(); // Hello     // (3) run the copy (it works)!
sayHi(); // Hello    //     this still works too (why wouldn't it)
```

### Qayta qo'ng'iroq qilish funktsiyalari

```
function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

function showOk() {
  alert( "You agreed." );
}

function showCancel() {
  alert( "You canceled the execution." );
}

// usage: functions showOk, showCancel are passed as arguments to ask
ask("Do you agree?", showOk, showCancel);
```
