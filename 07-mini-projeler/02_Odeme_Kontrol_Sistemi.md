# Ödeme Kontrol Sistemi

Bu mini projede daha önce öğrendiğim **koşul, mantıksal operatörler ve AND (`&&`)** konularını tekrar ediyorum.

Önceki derslerde birden fazla koşulun aynı anda doğru olması gerektiğinde AND operatörünü kullanmayı öğrenmiştim. Burada bunu basit bir ödeme kontrolü üzerinden tekrar ediyorum.

---

## 1. Problem

Bir alışverişte ödemenin başarılı olup olmadığını kontrol etmek istiyorum.

Ödemenin başarılı olması için iki koşulun da sağlanması gerekiyor:

1. Bir ödeme yöntemi seçilmiş olmalı.
2. Ödeme işleminin durumu başarılı olmalı.

Yani iki koşul da doğruysa ödeme başarılı kabul edilecek.

---

## 2. Koşullar

İlk koşul:

```text id="q5t3cm"
ödeme yöntemi seçilmiş mi?
```

İkinci koşul:

```text id="0j7e6f"
ödeme başarılı mı?
```

İki koşulun da doğru olması gerekiyor.

Bunu daha önce öğrendiğim AND mantığıyla şöyle düşünebilirim:

```text id="q0o7d8"
Ödeme yöntemi seçildi
        &&
Ödeme başarılı
        ↓
Ödeme tamamlandı
```

---

## 3. AND Mantığını Hatırlama

AND'de iki koşulun da doğru olması gerekiyor.

| Koşul 1 | Koşul 2 | Sonuç  |
| ------- | ------- | ------ |
| Doğru   | Doğru   | Doğru  |
| Doğru   | Yanlış  | Yanlış |
| Yanlış  | Doğru   | Yanlış |
| Yanlış  | Yanlış  | Yanlış |

Bu nedenle ödeme kontrolünde:

```text id="kcc2a7"
Ödeme yöntemi var
+
Ödeme başarılı
```

olmadan işlemi başarılı kabul etmiyorum.

---

## 4. Gerçek Örneklerle

### Örnek 1

Ödeme yöntemi seçilmiş:

```text id="4g7j2s"
EVET
```

Ödeme başarılı:

```text id="w3a5d4"
EVET
```

İki koşul da doğru.

```text id="v6avh6"
EVET && EVET
```

Sonuç:

```text id="5q6s9x"
Ödeme başarılı.
```

---

### Örnek 2

Ödeme yöntemi seçilmiş:

```text id="c1y1h5"
EVET
```

Ödeme başarılı:

```text id="k6ym2q"
HAYIR
```

Kontrol:

```text id="q3x8p4"
EVET && HAYIR
```

Sonuç yanlış olur.

Bu nedenle:

```text id="b3o4p9"
Ödeme başarısız.
```

---

### Örnek 3

Ödeme yöntemi seçilmemiş:

```text id="e2v0g6"
HAYIR
```

Ödeme başarılı:

```text id="j3l6t2"
EVET
```

Kontrol:

```text id="x8k5v4"
HAYIR && EVET
```

Sonuç yine yanlış.

Bu nedenle:

```text id="m1x4v9"
Ödeme başarısız.
```

---

## 5. Algoritmanın Adımları

1. Başla.
2. Ödeme yönteminin seçilip seçilmediğini kontrol et.
3. Ödeme durumunu kontrol et.
4. İki koşul da doğruysa ödeme başarılı sonucunu göster.
5. Koşullardan en az biri yanlışsa ödeme başarısız sonucunu göster.
6. Bitir.

---

## 6. Sözde Kod

```text id="qv4x1c"
BAŞLA

    ödeme yönteminin seçilip seçilmediğini kontrol et
    ödeme durumunu kontrol et

    EĞER ödeme yöntemi seçilmiş
    VE ödeme başarılı İSE

        "Ödeme başarılı." yazdır

    DEĞİLSE

        "Ödeme başarısız." yazdır

BİTİR
```

---

## 7. Mantığı Daha Basit Düşünürsem

Buradaki temel soru şu:

> **İki şartın da aynı anda gerçekleşmesi gerekiyor mu?**

Cevap evetse AND mantığını düşünüyorum.

Bu örnekte:

```text id="wq2bcm"
Ödeme yöntemi var mı?
        +
Ödeme başarılı mı?
```

İkisine de **evet** demem gerekiyor.

```text id="0r7f2j"
EVET + EVET → Başarılı
```

Ama herhangi bir tanesi bile hayırsa:

```text id="3d2k8z"
Başarısız
```

oluyor.

---

## 8. Bu Projede Tekrar Ettiklerim

| Öğrendiğim konu | Bu projede kullanımı                          |
| --------------- | --------------------------------------------- |
| Değişken        | Ödeme bilgilerini tutmak                      |
| Koşul           | Ödeme durumunu kontrol etmek                  |
| AND             | İki koşulun aynı anda doğru olmasını sağlamak |
| `if / else`     | Başarılı veya başarısız sonucunu belirlemek   |
| True / False    | Koşulların doğru veya yanlış olması           |

---

## 9. Kendi Notum

Bu örnekte benim için en önemli nokta **AND mantığını tekrar görmek** oldu.

Daha önce öğrendiğim gibi:

> **AND kullanıldığında bütün koşulların doğru olması gerekir.**

Ödeme örneğinde:

```text id="w7k1m9"
Ödeme yöntemi seçildi
AND
Ödeme başarılı
```

iki koşul da doğruysa:

```text id="e6x5p2"
Ödeme başarılı
```

sonucuna ulaşıyorum.

Koşullardan biri bile yanlışsa:

```text id="z0h5rm"
Ödeme başarısız
```

oluyor.

Bu nedenle burada yeni bir konu öğrenmekten çok, daha önce öğrendiğim **AND + koşul** mantığını gerçek bir problem üzerinde tekrar etmiş oldum.
