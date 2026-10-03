# Döngü ve Koşul Birlikte

## 1. Döngü ve Koşul Neden Birlikte Kullanılır?

Döngüler bir işlemi tekrar etmemizi sağlar.

Koşullar ise belirli bir duruma göre karar vermemizi sağlar.

Bazı problemlerde hem tekrar yapmak hem de her tekrarda bir koşulu kontrol etmek gerekir.

Bu durumda döngü ve koşul birlikte kullanılabilir.

Örneğin 1'den 10'a kadar olan sayıları inceleyip sadece çift olanları yazdırmak istediğimizi düşünelim.

Burada:

* **Döngü:** 1'den 10'a kadar olan sayıları tek tek kontrol eder.
* **Koşul:** Sayının çift olup olmadığını kontrol eder.
* **Çıktı:** Koşulu sağlayan sayılar yazdırılır.

---

## 2. Basit Bir Örnek

1'den 10'a kadar olan sayılar arasından çift olanları bulalım.

**Algoritmanın adımları:**

1. 1'den başla.
2. Sayıyı kontrol et.
3. Sayının 2'ye tam bölünüp bölünmediğine bak.
4. Çiftse ekrana yazdır.
5. Bir sonraki sayıya geç.
6. 10'a kadar aynı işlemi tekrarla.

**Sözde kod:**

```text
BAŞLA

    1'den 10'a kadar tekrarla

        EĞER sayı 2'ye tam bölünüyorsa
            sayıyı yazdır

BİTİR
```

**Çıktı:**

```text
2
4
6
8
10
```

Burada döngü, sayıları sırayla kontrol ederken koşul hangi sayıların ekrana yazdırılacağını belirler.

---

## 3. Döngünün İçindeki Koşul

Bu örnekte koşul döngünün içerisinde bulunmaktadır.

Mantık şu şekildedir:

```text
DÖNGÜ BAŞLA
      ↓
  Sayıyı al
      ↓
  Çift mi?
    /    \
  Evet   Hayır
   ↓       ↓
 Yazdır   Geç
   \       /
    \     /
   Sonraki sayı
      ↓
DÖNGÜ DEVAM
```

Yani her tekrar sırasında koşul yeniden kontrol edilir.

Örneğin:

* 1 → çift değil → yazdırma
* 2 → çift → yazdır
* 3 → çift değil → yazdırma
* 4 → çift → yazdır
* ...

Bu işlem 10'a ulaşana kadar devam eder.

---

## 4. Döngü İçinde Birden Fazla Koşul

Bir döngünün içerisinde birden fazla koşul da kullanılabilir.

Örneğin 1'den 10'a kadar olan sayıları kontrol ederek:

* Çift sayıları "Çift"
* Tek sayıları "Tek"

olarak belirtmek istediğimizi düşünelim.

**Sözde kod:**

```text
BAŞLA

    1'den 10'a kadar tekrarla

        EĞER sayı 2'ye tam bölünüyorsa
            "Çift" yazdır

        DEĞİLSE
            "Tek" yazdır

BİTİR
```

**Çıktı mantığı:**

```text
1 → Tek
2 → Çift
3 → Tek
4 → Çift
5 → Tek
...
10 → Çift
```

Burada döngü tekrar sayısını kontrol ederken, `if / else` yapısı her sayının sonucunu belirler.

---

## 5. While Döngüsü ile Koşul

Koşullar yalnızca `for` döngüsüyle değil, `while` döngüsüyle de birlikte kullanılabilir.

Örneğin kullanıcıdan alınan sayıları kontrol ettiğimizi düşünelim.

```text
BAŞLA

    sayı = 1

    SAYI 10'DAN KÜÇÜK OLDUĞU SÜRECE

        EĞER sayı çift ise
            sayıyı yazdır

        sayı = sayı + 1

BİTİR
```

Burada:

* `while` mantığı → işlemin ne zamana kadar devam edeceğini belirler.
* `if` mantığı → her sayı için hangi işlemin yapılacağını belirler.

Yani iki farklı karar mekanizması birlikte çalışır.

---

## 6. Döngü + Koşul Mantığını Günlük Hayatta Düşünmek

Bu yapıyı günlük hayattan da düşünebiliriz.

Örneğin bir sepette 10 ürün olduğunu düşünelim.

Her ürün için:

1. Ürünü incele.
2. Ürün stokta mı kontrol et.
3. Stokta ise listeye ekle.
4. Sonraki ürüne geç.
5. Tüm ürünler kontrol edilene kadar devam et.

Burada:

**Döngü:**

> Tüm ürünleri sırayla kontrol et.

**Koşul:**

> Ürün stokta mı?

**İşlem:**

> Stokta ise listeye ekle.

Bu nedenle döngü ve koşullar gerçek problemlerde birlikte kullanılabilir.

---

## 7. Kısa Özet

* Döngü, işlemlerin tekrar edilmesini sağlar.
* Koşul, her tekrar sırasında karar verilmesini sağlar.
* Bir koşul döngünün içerisinde kullanılabilir.
* Her döngü tekrarında koşul yeniden değerlendirilebilir.
* `for` ve `while` döngüleri koşullarla birlikte kullanılabilir.
* Döngü ve koşul birlikte kullanıldığında daha karmaşık problemler çözülebilir.

**NOT:**

> **Döngü = Kaç kez veya ne zamana kadar tekrar edeceğim?**

> **Koşul = Her tekrarda neye karar vereceğim?**
