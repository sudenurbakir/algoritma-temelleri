# Else If ve İç İçe Koşullar

## 1. Else If Nedir?

Bir algoritmada birden fazla koşulu sırayla kontrol etmemiz gerekebilir. Bu durumda `else if` (değilse eğer) yapısını kullanabiliriz.

* **if:** İlk koşulu kontrol eder.
* **else if:** Önceki koşul sağlanmadığında başka bir koşulu kontrol eder.
* **else:** Önceki koşulların hiçbiri sağlanmadığında çalışır.

### Örnek: Sınav Notunu Değerlendirme

Bir öğrencinin sınav notuna göre başarı durumunu belirleyen bir algoritma düşünelim.

| Not         | Sonuç  |
| ----------- | ------ |
| 85 ve üzeri | Pekiyi |
| 70–84       | İyi    |
| 50–69       | Geçti  |
| 50'nin altı | Kaldı  |

**Algoritmanın adımları:**

1. Öğrencinin notunu al.
2. Not 85 veya üzerindeyse "Pekiyi" yazdır.
3. Değilse, not 70 veya üzerindeyse "İyi" yazdır.
4. Değilse, not 50 veya üzerindeyse "Geçti" yazdır.
5. Hiçbir koşul sağlanmıyorsa "Kaldı" yazdır.

**Sözde kod:**

```text
BAŞLA

    not değerini al

    EĞER not >= 85 İSE
        "Pekiyi" yazdır

    DEĞİLSE EĞER not >= 70 İSE
        "İyi" yazdır

    DEĞİLSE EĞER not >= 50 İSE
        "Geçti" yazdır

    DEĞİLSE
        "Kaldı" yazdır

BİTİR
```

### Koşulların Sırası Neden Önemlidir?

Koşulları doğru sırayla kontrol etmek gerekir.

Örneğin ilk koşul olarak `not >= 50` yazarsak 90 alan bir öğrenci de bu koşulu sağlayacağı için doğrudan "Geçti" sonucunu alabilir.

Bu nedenle örneğimizde en yüksek not aralığından başlayarak ilerliyoruz.

**Önemli:** `else if` yapısında koşullar sırayla kontrol edilir. İlk doğru koşul bulunduğunda ilgili işlem gerçekleştirilir ve diğer koşullar atlanır.

---

## 2. İç İçe Koşullar Nedir?

İç içe koşullar, bir koşulun içerisinde başka bir koşul kullanılmasıdır.

Bazı durumlarda ikinci koşulu kontrol edebilmek için önce başka bir koşulun sağlanması gerekir.

### Örnek: Üyelik Kontrolü

Bir sisteme giriş yapmak isteyen kişinin önce 18 yaşında veya daha büyük olması, ardından aktif üyeliğe sahip olması gerektiğini düşünelim.

**Algoritmanın adımları:**

1. Kullanıcının yaşını al.
2. Yaşı 18 veya üzerindeyse üyelik durumunu kontrol et.
3. Üyelik aktifse "Giriş başarılı" mesajını göster.
4. Üyelik aktif değilse "Üyeliğiniz aktif değil" mesajını göster.
5. Kullanıcı 18 yaşından küçükse "Yaş koşulu sağlanmadı" mesajını göster.

**Sözde kod:**

```text
BAŞLA

    yaş değerini al

    EĞER yaş >= 18 İSE

        üyelik durumunu al

        EĞER üyelik aktif İSE
            "Giriş başarılı" yazdır
        DEĞİLSE
            "Üyeliğiniz aktif değil" yazdır
        BİTİR

    DEĞİLSE
        "Yaş koşulu sağlanmadı" yazdır

BİTİR
```

Burada üyelik kontrolü, yalnızca yaş koşulu sağlandığında gerçekleştiriliyor. Yani ikinci koşul, ilk koşulun içinde yer alıyor.

---

## 3. Else If ile İç İçe Koşullar Arasındaki Fark

| Else If                                              | İç İçe Koşullar                                                  |
| ---------------------------------------------------- | ---------------------------------------------------------------- |
| Birden fazla koşulu sırayla kontrol eder.            | Bir koşulun içinde başka bir koşul kontrol edilir.               |
| Alternatif durumları değerlendirmek için kullanılır. | Bir işlemin başka bir koşula bağlı olduğu durumlarda kullanılır. |
| Örneğin not aralıklarını belirlemek.                 | Örneğin yaş koşulu sağlanınca üyeliği kontrol etmek.             |

## 4. Kısa Özet

* **if:** Bir koşulu kontrol eder.
* **else if:** Önceki koşul sağlanmadığında yeni bir koşulu kontrol eder.
* **else:** Hiçbir koşul sağlanmadığında çalışır.
* **İç içe koşul:** Bir koşulun içerisinde başka bir koşul bulunmasıdır.
* Koşulların sırası, algoritmanın doğru sonuç üretmesi açısından önemlidir.

**Unutma:** Else if, alternatifler arasında seçim yapmamızı; iç içe koşullar ise birbirine bağlı kararlar oluşturmamızı sağlar.
