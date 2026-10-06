# Alışveriş Hesaplama

Bu uygulamada bir alışverişin toplam tutarını hesaplayacağız ve belirli bir tutarın üzerinde alışveriş yapılırsa **indirim uygulayacağız**.

Bu uygulamada daha önce öğrendiğimiz:

* Değişkenler
* Hesaplama
* Koşullar
* `if / else`
* Girdi → İşlem → Çıktı

mantıklarını birlikte kullanacağız.

---

## 1. Problem

Bir müşterinin alışveriş tutarı hesaplanacak.

Kurallarımız:

* Alışveriş tutarı **500 TL veya üzerindeyse %10 indirim**
* 500 TL'nin altındaysa **indirim yok**

Örneğin:

```text
Alışveriş tutarı = 800 TL
```

800 TL, 500 TL'den büyük olduğu için %10 indirim uygulanır.

İndirim:

```text
800 × 10 / 100 = 80 TL
```

Ödenecek tutar:

```text
800 - 80 = 720 TL
```

---

## 2. Girdi - İşlem - Çıktı

### Girdi

Kullanıcıdan:

```text
alışveriş tutarı
```

alınır.

### İşlem

Önce tutarın 500 TL veya üzeri olup olmadığı kontrol edilir.

Eğer 500 TL veya üzerindeyse:

```text
indirim = tutar × 10 / 100
```

hesaplanır.

Daha sonra:

```text
ödenecek tutar = tutar - indirim
```

hesaplanır.

Eğer tutar 500 TL'nin altındaysa indirim uygulanmaz.

---

## 3. Adım Adım Örnek

Alışveriş tutarı:

```text
800 TL
```

### Adım 1 — Tutarı kontrol et

```text
800 >= 500
```

Sonuç:

```text
DOĞRU
```

Bu nedenle indirim uygulanır.

### Adım 2 — İndirimi hesapla

```text
800 × 10 / 100 = 80
```

İndirim:

```text
80 TL
```

### Adım 3 — Ödenecek tutarı hesapla

```text
800 - 80 = 720
```

Sonuç:

```text
Ödenecek tutar = 720 TL
```

---

## 4. İndirim Olmayan Durum

Şimdi alışveriş tutarı:

```text
350 TL
```

olsun.

Kontrol:

```text
350 >= 500
```

Sonuç:

```text
YANLIŞ
```

Bu nedenle indirim uygulanmaz.

Ödenecek tutar:

```text
350 TL
```

olur.

---

## 5. Algoritmanın Adımları

1. Başla.
2. Alışveriş tutarını al.
3. Tutarın 500 TL veya üzeri olup olmadığını kontrol et.
4. Eğer 500 TL veya üzerindeyse %10 indirim hesapla.
5. İndirimi alışveriş tutarından çıkar.
6. Eğer 500 TL'nin altındaysa indirim uygulama.
7. Ödenecek tutarı ekrana yazdır.
8. Bitir.

---

## 6. Sözde Kod

```text
BAŞLA

    alışveriş tutarını al

    EĞER tutar >= 500 İSE

        indirim = tutar × 10 / 100
        ödenecek tutar = tutar - indirim

    DEĞİLSE

        ödenecek tutar = tutar

    ödenecek tutarı yazdır

BİTİR
```

---

## 7. Gerçek Sayılarla Algoritmanın Çalışması

Örneğin:

```text
tutar = 650 TL
```

Kontrol:

```text
650 >= 500 → DOĞRU
```

İndirim:

```text
650 × 10 / 100 = 65
```

Ödenecek tutar:

```text
650 - 65 = 585
```

Sonuç:

```text
Ödenecek tutar = 585 TL
```

---

## 8. Algoritmanın Genel Mantığı

Bu uygulamada algoritmanın akışı şöyle:

```text
Alışveriş tutarını al
        ↓
Tutar >= 500 ?
     /       \
   EVET     HAYIR
    ↓          ↓
%10 indirim   İndirim yok
    ↓          ↓
Ödenecek tutarı hesapla
        ↓
      Sonucu yazdır
```

Burada önemli olan nokta, **koşulun hesaplamanın hangi kısmının yapılacağını belirlemesi**.

Yani koşul sadece "başarılı/başarısız" gibi bir sonuç üretmek zorunda değil.

Bir hesaplamanın **yapılıp yapılmayacağına da karar verebilir.**

---

### Değişken

```text
tutar
indirim
ödenecek tutar
```

### Hesaplama

```text
indirim = tutar × 10 / 100
```

### Koşul

```text
EĞER tutar >= 500
```

### Karar

```text
İndirim uygula
veya
İndirim uygulama
```

---

## Kısa Özet

Bu algoritmanın temel mantığı:

**Tutarı al → Koşulu kontrol et → Gerekirse indirim hesapla → Ödenecek tutarı bul → Sonucu yazdır**

şeklindedir.

Bu uygulama, daha önce öğrendiğimiz konuların bir araya gelmeye başladığı ilk örneklerden biridir.
