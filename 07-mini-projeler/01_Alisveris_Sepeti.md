# Alışveriş Sepeti

Bu mini projede algoritma kursunda daha önce öğrendiğim **değişken, matematiksel işlemler, koşul ve döngü** konularını bir arada tekrar ettim.

Önceki uygulamalarda bu konuları daha küçük örneklerle görmüştüm. Burada ise birkaç konunun aynı problem içerisinde nasıl birlikte çalıştığını görmeye çalıştım.

---

## 1. Problem

Basit bir alışveriş sepetinin toplam tutarını hesaplamak istiyorum.

Kullanıcı sepete birkaç ürün ekleyecek ve her ürünün fiyatını girecek.

Program da girilen ürün fiyatlarını toplayarak sepetin toplam tutarını gösterecek.

Örneğin:

```text
100 TL
150 TL
50 TL
```

girildiğinde:

```text
100 + 150 + 50 = 300 TL
```

sonucuna ulaşılır.

---

## 2. Daha Önce Öğrendiğim Bilgilerle İlişkisi

Bu örnekte daha önce öğrendiğim birkaç konuyu tekrar kullanıyorum.

### Değişken

Bilgileri saklamak için değişkenlere ihtiyacım var.

Örneğin:

```text
toplam
ürün sayısı
ürün fiyatı
```

### Matematiksel İşlem

Ürün fiyatlarını toplamak için toplama işlemini kullanıyorum.

```text
toplam = toplam + ürün fiyatı
```

### Döngü

Birden fazla ürün olduğu için aynı işlemi tekrar etmem gerekiyor.

Her seferinde:

```text
ürün fiyatını al
toplama ekle
```

işlemini yapıyorum.

### Koşul

Sepette hiç ürün olup olmadığını kontrol etmek için koşul kullanabilirim.

---

## 3. Toplam Değişkeninin Çalışması

Burada daha önce öğrendiğim **biriktirme mantığını** tekrar kullanıyorum.

Başlangıçta:

```text
toplam = 0
```

olarak belirliyorum.

İlk ürünün fiyatı 100 TL olsun:

```text
toplam = 0 + 100
toplam = 100
```

İkinci ürün 150 TL:

```text
toplam = 100 + 150
toplam = 250
```

Üçüncü ürün 50 TL:

```text
toplam = 250 + 50
toplam = 300
```

Sonuçta:

```text
toplam = 300
```

oluyor.

Burada özellikle daha önce öğrendiğim:

```text
toplam = toplam + sayı
```

mantığını tekrar etmiş oldum.

---

## 4. Döngünün Kullanılması

Ürün sayısı arttığında her ürünü ayrı ayrı yazmak yerine döngü kullanabilirim.

Örneğin 3 ürün varsa:

```text
1. tekrar → 100 TL → toplam = 100
2. tekrar → 150 TL → toplam = 250
3. tekrar → 50 TL → toplam = 300
```

Burada döngünün yaptığı şey aslında çok basit:

```text
Ürün fiyatını al
↓
Toplama ekle
↓
Tekrar et
```

Bu şekilde aynı işlemi tekrar tekrar yapabiliyorum.

---

## 5. Koşulun Kullanılması

Daha önce öğrendiğim koşul mantığını da burada kullanabilirim.

Örneğin ürün sayısını kontrol edebilirim:

```text
EĞER ürün sayısı > 0 İSE
    toplam tutarı göster
DEĞİLSE
    "Sepet boş." yazdır
```

Böylece iki farklı durum oluşuyor:

```text
Ürün varsa → Toplam tutarı göster
Ürün yoksa → Sepet boş mesajı göster
```

Bu da daha önce öğrendiğim **if / else** mantığının tekrar kullanılması oluyor.

---

## 6. Algoritmanın Adımları

Benim için algoritmanın sıralaması şu şekilde:

1. Toplamı 0 olarak belirle.
2. Ürün sayısını al.
3. Ürün sayısı kadar tekrar et.
4. Ürün fiyatını al.
5. Ürün fiyatını toplamın üzerine ekle.
6. Ürün sayısını kontrol et.
7. Ürün varsa toplam tutarı göster.
8. Ürün yoksa sepetin boş olduğunu göster.
9. Bitir.

---

## 7. Sözde Kod

```text
BAŞLA

    toplam = 0

    ürün sayısını al

    Ürün sayısı kadar TEKRARLA

        ürün fiyatını al
        toplam = toplam + ürün fiyatı

    EĞER ürün sayısı > 0 İSE

        toplam tutarı yazdır

    DEĞİLSE

        "Sepet boş." yazdır

BİTİR
```

---

## 8. Gerçek Sayılarla Örnek

Ürün sayısının 3 olduğunu düşünelim.

### 1. ürün

```text
100 TL
```

```text
toplam = 0 + 100
toplam = 100
```

### 2. ürün

```text
150 TL
```

```text
toplam = 100 + 150
toplam = 250
```

### 3. ürün

```text
50 TL
```

```text
toplam = 250 + 50
toplam = 300
```

Sonuç:

```text
Sepet toplamı = 300 TL
```

---

## 9. Bu Uygulamada Tekrar Ettiklerim

Bu mini projede daha önce öğrendiğim konuları şu şekilde tekrar ettim:

| Öğrendiğim konu    | Bu projede kullanımı                       |
| ------------------ | ------------------------------------------ |
| Değişken           | `toplam`, `ürün sayısı`, `ürün fiyatı`     |
| Matematiksel işlem | Ürün fiyatlarını toplamak                  |
| Döngü              | Birden fazla ürünü tekrar tekrar almak     |
| Koşul              | Sepette ürün olup olmadığını kontrol etmek |
| `if / else`        | Farklı durumlara göre sonuç göstermek      |

---

## 10. Kendi Notum

Bu örnekte benim için en önemli kısım:

```text
toplam = toplam + ürün fiyatı
```

ifadesinin döngü içerisinde tekrar edilmesi.

Her döngüde yeni ürünün fiyatı mevcut toplamın üzerine ekleniyor.

Yani mantık:

```text
0
↓
0 + 100 = 100
↓
100 + 150 = 250
↓
250 + 50 = 300
```

şeklinde ilerliyor.

