# Koşul İşlemleri

## 1. Koşul İşlemleri Nedir?

Algoritmalarda bazen bir işlemin gerçekleşmesi için belirli bir şartın sağlanması gerekir.

Örneğin:

> Bir kişinin yaşı 18 veya daha büyükse "Reşit" yazdır.

Burada bilgisayarın kontrol etmesi gereken bir durum vardır:

```text
Yaş >= 18
```

Bu durumun sonucu iki şekilde olabilir:

```text
Doğru (True)
```

veya

```text
Yanlış (False)
```

Koşul işlemleri, bu tür durumlara göre algoritmanın farklı işlemler gerçekleştirmesini sağlar.

---

## 2. Koşulun Temel Mantığı

Koşullu bir algoritmanın temel yapısı:

```text
Girdi
  ↓
Koşulu kontrol et
  ↓
 ┌───────────────┐
 │               │
DOĞRU          YANLIŞ
 │               │
 ↓               ↓
İşlem 1        İşlem 2
```

Örneğin:

```text
Yaş >= 18 ?
```

Eğer sonuç doğruysa:

```text
"Reşit"
```

yazdırılabilir.

Yanlışsa:

```text
"Reşit değil"
```

yazdırılabilir.

---

## 3. `if` Nedir?

Programlamada koşul belirtmek için sık kullanılan yapılardan biri `if` ifadesidir.

`if`, Türkçede kabaca:

> Eğer

anlamına gelir.

Örneğin:

```text
EĞER yaş >= 18 İSE
    "Reşit" yazdır
```

Burada:

```text
yaş >= 18
```

koşuldur.

Koşul doğruysa işlem gerçekleştirilir.

---

## 4. `else` Nedir?

`else`, koşulun yanlış olduğu durumda ne yapılacağını belirtmek için kullanılır.

Türkçede:

> Değilse / aksi durumda

anlamına gelir.

Örneğin:

```text
EĞER yaş >= 18 İSE
    "Reşit" yazdır
DEĞİLSE
    "Reşit değil" yazdır
```

Burada iki farklı durum vardır:

| Koşul     | Sonuç       |
| --------- | ----------- |
| Yaş >= 18 | Reşit       |
| Yaş < 18  | Reşit değil |

---

## 5. Karşılaştırma Operatörleri

Koşullarda iki değeri karşılaştırmak için karşılaştırma operatörleri kullanılır.

### Eşittir

```text
=
```

Örneğin:

```text
puan = 100
```

Bir değerin başka bir değere eşit olup olmadığını kontrol etmek için kullanılır.

---

### Büyük

```text
>
```

Örneğin:

```text
puan > 50
```

Puanın 50'den büyük olup olmadığını kontrol eder.

---

### Küçük

```text
<
```

Örneğin:

```text
puan < 50
```

Puanın 50'den küçük olup olmadığını kontrol eder.

---

### Büyük veya Eşit

```text
>=
```

Örneğin:

```text
yaş >= 18
```

Yaşın 18 veya daha büyük olup olmadığını kontrol eder.

---

### Küçük veya Eşit

```text
<=
```

Örneğin:

```text
yaş <= 18
```

Yaşın 18 veya daha küçük olup olmadığını kontrol eder.

---

### Eşit Değil

```text
!=
```

Örneğin:

```text
şifre != "1234"
```

Şifrenin `1234` değerine eşit olup olmadığını kontrol eder.

---

## 6. Karşılaştırma Örnekleri

Örneğin:

```text
sayı = 10
```

olsun.

Şu koşulların sonuçlarına bakalım:

```text
sayı > 5
```

Sonuç:

```text
Doğru
```

Çünkü 10, 5'ten büyüktür.

---

```text
sayı < 5
```

Sonuç:

```text
Yanlış
```

Çünkü 10, 5'ten küçük değildir.

---

```text
sayı >= 10
```

Sonuç:

```text
Doğru
```

Çünkü 10, 10'a eşittir.

---

```text
sayı != 10
```

Sonuç:

```text
Yanlış
```

Çünkü sayı 10'a eşittir.

---

## 7. Basit Bir Koşul Algoritması

### Problem

Kullanıcının girdiği sayının pozitif olup olmadığını kontrol eden bir algoritma oluşturulacaktır.

### Girdi

* Bir sayı

### Koşul

```text
Sayı > 0
```

### Algoritma

```text
1. Başla
2. Sayıyı al
3. Sayı 0'dan büyük mü kontrol et
4. Büyükse "Pozitif sayı" yazdır
5. Değilse "Pozitif sayı değil" yazdır
6. Bitir
```

### Sözde Kod

```text
BAŞLA

sayı değerini al

EĞER sayı > 0 İSE
    "Pozitif sayı" yazdır
DEĞİLSE
    "Pozitif sayı değil" yazdır

BİTİR
```

---

## 8. Koşulun Sonucunu Düşünmek

Bir algoritmada koşulu yazmak kadar, koşulun her iki durumda ne yapacağını düşünmek de önemlidir.

Örneğin:

```text
EĞER puan >= 50 İSE
    "Başarılı"
DEĞİLSE
    "Başarısız"
```

Burada iki ihtimal vardır:

```text
Puan = 70
↓
70 >= 50
↓
Doğru
↓
Başarılı
```

Başka bir durumda:

```text
Puan = 40
↓
40 >= 50
↓
Yanlış
↓
Başarısız
```

Bu nedenle algoritmanın farklı girdiler karşısında nasıl davranacağını önceden düşünmek gerekir.

---

## 9. Koşul İşlemlerinde Temel Soru

Bir problem gördüğümüzde artık şu soruyu da sormalıyız:

> **Bu problemde bir karar verilmesi gerekiyor mu?**

Örneğin:

> İki sayıyı topla.

Burada herhangi bir karar yoktur.

```text
Sayı1 + Sayı2
```

Ancak:

> Sayı pozitifse "Pozitif", değilse "Pozitif değil" yazdır.

Burada karar verilmesi gerekir.

```text
Sayı > 0 ?
```

Bu nedenle koşul yapısı kullanılır.

---

## 10. Doğrusal Algoritma ve Koşullu Algoritma

### Doğrusal algoritma

İşlemler sırayla ilerler:

```text
Girdi
 ↓
İşlem
 ↓
İşlem
 ↓
Çıktı
```

### Koşullu algoritma

Algoritma bir noktada karar verir:

```text
Girdi
 ↓
Koşul
 ↓
 ┌───────┴───────┐
DOĞRU           YANLIŞ
 ↓                 ↓
İşlem 1           İşlem 2
 └───────┬─────────┘
         ↓
       Çıktı
```

Bu fark, koşullu algoritmaları anlamak açısından önemlidir.

---

## 11. Günlük Hayattan Örnek

Koşul mantığı yalnızca bilgisayar programlarında bulunmaz.

Örneğin:

> Eğer hava yağmurluysa şemsiye al.

Bunu algoritmik şekilde düşünürsek:

```text
Hava yağmurlu mu?
        ↓
   ┌────┴────┐
  EVET      HAYIR
   ↓          ↓
Şemsiye     Şemsiye
al           alma
```

Burada da bir koşul ve bu koşula bağlı iki farklı davranış vardır.

---

## Genel Sonuç

Bu bölümde:

* Koşul kavramını
* `if` mantığını
* `else` mantığını
* Karşılaştırma operatörlerini
* Doğru ve yanlış sonuçlarını
* Koşullu algoritmanın yapısını
* Karar verilmesi gereken problemleri

inceledik.

Temel mantık:

```text
BİR DURUMU KONTROL ET
        ↓
   DOĞRU MU?
   ↙       ↘
 EVET      HAYIR
  ↓          ↓
İşlem 1    İşlem 2
```

Koşul işlemlerinin temel amacı:

> **Bir durumun sonucuna göre algoritmanın hangi yolu izleyeceğine karar vermektir.**

**Eğitim kapsamında bireysel öğrenme ve uygulama çalışmasıdır.**
