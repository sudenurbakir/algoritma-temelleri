# Koşullu İfade Akışı

## 1. Koşullu İfade Akışı Nedir?

Koşullu ifade akışı, bir algoritmanın belirli koşulların sonuçlarına göre hangi adımları izleyeceğini ifade eder.

Bir algoritma her zaman aynı yolu izlemek zorunda değildir. Koşulun sonucuna göre farklı işlemler gerçekleştirebilir.

Örneğin, bir sayının pozitif olup olmadığını kontrol eden algoritmada:

* Koşul doğruysa pozitif mesajı gösterilir.
* Koşul yanlışsa diğer olasılıklar değerlendirilir.

Bu sayede algoritma, farklı durumlara uygun sonuçlar üretebilir.

## 2. Koşullu İfadelerin Akış Mantığı

Koşullu ifadeler genellikle üç temel bölümden oluşur:

* **if:** İlk koşulu kontrol eder.
* **else if:** İlk koşul sağlanmadığında başka bir koşulu kontrol eder.
* **else:** Önceki koşulların hiçbiri sağlanmadığında çalışır.

Bir koşul doğru olduğunda ilgili işlem gerçekleştirilir. Koşul yanlış olduğunda ise algoritma diğer seçeneğe ilerler.

## 3. AND Operatörü ile Koşullu İfade Akışı

AND operatörü, birden fazla koşulun birlikte değerlendirilmesini sağlar.

**Örnek: Sınav Başarı Kontrolü**

Bir öğrencinin başarılı sayılması için hem sınav notunun en az 50 olması hem de devam oranının en az %70 olması gerektiğini düşünelim.

**Koşullar:**

* Sınav notu >= 50
* Devam oranı >= 70

**Sözde kod:**

```text
BAŞLA

    sınav notunu al
    devam oranını al

    EĞER sınav notu >= 50 VE devam oranı >= 70 İSE
        "Başarılı" yazdır
    DEĞİLSE
        "Başarısız" yazdır

BİTİR
```

Bu algoritmada iki koşul birlikte değerlendirilir. İkisinin de doğru olması durumunda öğrenci başarılı kabul edilir.

## 4. Koşullu İfade Akışının Adımları

Bir koşullu algoritmanın akışını aşağıdaki sırayla inceleyebiliriz:

1. Algoritma başlar.
2. Gerekli girdiler alınır.
3. Koşul veya koşullar değerlendirilir.
4. Koşulun sonucuna göre ilgili işlem gerçekleştirilir.
5. Algoritma tamamlanır.

**Örnek akış:**

```text
       (BAŞLA)
          |
          v
   / Not ve devam al /
          |
          v
   < Not >= 50 VE
     devam >= 70? >
       /       \
    Evet       Hayır
      |          |
      v          v
 "Başarılı"  "Başarısız"
      |          |
      v          v
    (BİTİR)   (BİTİR)
```

## Kısa Özet

* Koşullu ifade akışı, algoritmanın koşullara göre izleyeceği yolu belirler.
* Koşulun doğru veya yanlış olması, algoritmanın hangi adıma ilerleyeceğini etkiler.
* AND operatörü birden fazla koşulun birlikte değerlendirilmesini sağlar.
* Akış şemaları, koşullu ifadelerin işleyişini görselleştirmeye yardımcı olur.
* Doğru bir akışta tüm olası durumların nasıl sonuçlanacağı belirlenmelidir.

