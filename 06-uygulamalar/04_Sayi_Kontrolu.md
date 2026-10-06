# Sayı Kontrolü

Bu uygulamada kullanıcıdan alınan bir sayının **pozitif, negatif veya sıfır** olduğunu belirleyen bir algoritma oluşturacağız.

Bu uygulama, daha önce öğrendiğimiz **if / else if / else** mantığını tekrarı için bir örnektir.

---

## 1. Problem

Kullanıcı bir sayı girecek.

Program bu sayıyı kontrol edecek:

* Sayı **0'dan büyükse** → Pozitif
* Sayı **0'dan küçükse** → Negatif
* Sayı **0'a eşitse** → Sıfır

### Örnekler

```text
8  → Pozitif
-3 → Negatif
0  → Sıfır
```

---

## 2. Girdi - İşlem - Çıktı

### Girdi

Kullanıcıdan bir sayı alınır.

### İşlem

Sayı üç farklı durum açısından kontrol edilir.

```text
Sayı > 0
Sayı < 0
Sayı = 0
```

### Çıktı

Sayıya göre:

```text
Pozitif
Negatif
Sıfır
```

sonuçlarından biri yazdırılır.

---

## 3. Algoritmanın Mantığı

Burada üç farklı ihtimalimiz var.

Örneğin kullanıcı:

```text
-7
```

girmiş olsun.

İlk kontrol:

```text
-7 > 0 ?
```

Hayır.

İkinci kontrol:

```text
-7 < 0 ?
```

Evet.

Sonuç:

```text
Negatif
```

---

## 4. Algoritmanın Adımları

1. Başla.
2. Kullanıcıdan bir sayı al.
3. Sayının 0'dan büyük olup olmadığını kontrol et.
4. Büyükse "Pozitif" yazdır.
5. Değilse sayının 0'dan küçük olup olmadığını kontrol et.
6. Küçükse "Negatif" yazdır.
7. Hiçbiri değilse "Sıfır" yazdır.
8. Bitir.

---

## 5. Sözde Kod

```text
BAŞLA

    sayıyı al

    EĞER sayı > 0 İSE
        "Pozitif" yazdır

    DEĞİLSE EĞER sayı < 0 İSE
        "Negatif" yazdır

    DEĞİLSE
        "Sıfır" yazdır

BİTİR
```

---

## 6. Gerçek Sayılarla Adım Adım

### Örnek 1

Kullanıcı:

```text
sayı = 15
```

Kontrol:

```text
15 > 0 → DOĞRU
```

Sonuç:

```text
Pozitif
```

---

### Örnek 2

Kullanıcı:

```text
sayı = -4
```

İlk kontrol:

```text
-4 > 0 → YANLIŞ
```

İkinci kontrol:

```text
-4 < 0 → DOĞRU
```

Sonuç:

```text
Negatif
```

---

### Örnek 3

Kullanıcı:

```text
sayı = 0
```

İlk kontrol:

```text
0 > 0 → YANLIŞ
```

İkinci kontrol:

```text
0 < 0 → YANLIŞ
```

Geriye kalan durum:

```text
0 = 0
```

Sonuç:

```text
Sıfır
```

---

## 7. Burada `else if` Neden Kullanıldı?

Çünkü birden fazla ihtimalimiz var.

Mantık şu:

```text
          Sayı > 0 ?
          /       \
       EVET       HAYIR
        ↓           ↓
    Pozitif     Sayı < 0 ?
                /       \
             EVET       HAYIR
              ↓           ↓
          Negatif       Sıfır
```

Yani algoritma **ilk koşulu kontrol ediyor**, doğru değilse ikinci koşula geçiyor.

İkinci koşul da doğru değilse geriye kalan ihtimal `else` ile yakalanıyor.

---

## Kısa Özet

```text
Sayı > 0 → Pozitif
Sayı < 0 → Negatif
Sayı = 0 → Sıfır
```

Algoritmanın temel yapısı:

**Girdi → Koşulları kontrol et → Uygun sonucu seç → Çıktı**
