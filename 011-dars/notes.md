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
