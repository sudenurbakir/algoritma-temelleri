# Not Değerlendirme

Bu uygulamada, kullanıcının girdiği nota göre öğrencinin **başarılı veya başarısız** olduğunu belirleyen basit bir algoritma oluşturacağız.

## 1. Problem

Bir öğrencinin sınav notu giriliyor.

* Not **50 veya üzerindeyse** → Başarılı
* Not **50'nin altındaysa** → Başarısız

Program, bu bilgiye göre sonucu ekrana yazdıracak.

---

## 2. Girdi - İşlem - Çıktı

### Girdi

Kullanıcıdan:

* Öğrencinin sınav notu

alınır.

### İşlem

Girilen not kontrol edilir:

```text
Eğer not >= 50 ise
    Başarılı
Değilse
    Başarısız
```

### Çıktı

Ekrana:

* Başarılı
  veya
* Başarısız

yazdırılır.

---

## 3. Örnek

Öğrencinin notu:

```text
75
```

Kontrol:

```text
75 >= 50 → DOĞRU
```

Sonuç:

```text
Başarılı
```

Başka bir örnek:

```text
35
```

Kontrol:

```text
35 >= 50 → YANLIŞ
```

Sonuç:

```text
Başarısız
```

---

## 4. Algoritmanın Adımları

1. Başla.
2. Öğrencinin notunu al.
3. Notun 50 veya daha büyük olup olmadığını kontrol et.
4. Eğer 50 veya daha büyükse "Başarılı" yazdır.
5. Değilse "Başarısız" yazdır.
6. Bitir.

---

## 5. Sözde Kod 

```text
BAŞLA

    notu al

    EĞER not >= 50 İSE
        "Başarılı" yazdır
    DEĞİLSE
        "Başarısız" yazdır

BİTİR
```

---

## Kısa Özet

Bu uygulamada:

* Kullanıcıdan veri aldık.
* Bir koşul oluşturduk.
* Koşulu kontrol ettik.
* Doğruysa bir sonuç,
* Yanlışsa başka bir sonuç verdik.

Yani:

**Girdi → Koşul → Karar → Çıktı**
