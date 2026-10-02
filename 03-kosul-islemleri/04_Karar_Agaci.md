# Karar Ağacı

## 1. Karar Ağacı Nedir?

Karar ağacı, bir problemdeki koşulları ve bu koşullara bağlı olarak gerçekleşen işlemleri görsel veya adım adım gösteren bir yapıdır.

Bir algoritmanın hangi koşulda hangi yolu izleyeceğini anlamamızı sağlar.

Karar ağaçlarında genellikle şu adımlar bulunur:

* **Başlangıç:** Algoritmanın başladığı nokta.
* **Koşul:** Doğru veya yanlış olarak değerlendirilen ifade.
* **İşlem:** Koşulun sonucuna göre gerçekleştirilen adım.
* **Çıktı:** Algoritmanın ürettiği sonuç.
* **Bitiş:** Algoritmanın tamamlandığı nokta.

## 2. Karar Ağacı Nasıl Çalışır?

Bir karar ağacında koşullar sırayla değerlendirilir. Her koşulun sonucuna göre farklı bir yol izlenebilir.

### Örnek: Bir Sayının Pozitif veya Negatif Olduğunu Belirleme

Kullanıcıdan alınan bir sayının pozitif, negatif veya sıfır olduğunu belirleyen bir algoritma düşünelim.

**Algoritmanın adımları:**

1. Kullanıcıdan bir sayı al.
2. Sayının sıfırdan büyük olup olmadığını kontrol et.
3. Büyükse pozitif olduğunu belirt.
4. Büyük değilse sıfırdan küçük olup olmadığını kontrol et.
5. Küçükse negatif, değilse sıfır olduğunu belirt.

**Sözde kod:**

```text
BAŞLA

    sayı değerini al

    EĞER sayı > 0 İSE
        "Pozitif" yazdır

    DEĞİLSE EĞER sayı < 0 İSE
        "Negatif" yazdır

    DEĞİLSE
        "Sıfır" yazdır

BİTİR
```

## 3. Karar Ağacı ve Akış Şeması

Karar ağacı, koşullara göre oluşan seçenekleri gösterir. Akış şeması ise algoritmanın başlangıçtan bitişe kadar izlediği yolu standart şekillerle gösterir.

Akış şemalarında yaygın olarak kullanılan şekiller şunlardır:

| Şekil           | Anlamı             |
| --------------- | ------------------ |
| Oval            | Başlangıç ve bitiş |
| Dikdörtgen      | İşlem              |
| Paralelkenar    | Girdi ve çıktı     |
| Eşkenar dörtgen | Karar veya koşul   |
| Ok              | Akış yönü          |

### Örnek Akış Şeması

Bir sayının pozitif, negatif veya sıfır olduğunu belirleyen algoritmanın akışı:

```text
       (BAŞLA)
          |
          v
    / Sayıyı al /
          |
          v
     < sayı > 0? >
       /      \
    Evet      Hayır
      |         |
      v         v
 "Pozitif"  < sayı < 0? >
               /      \
            Evet      Hayır
              |         |
              v         v
         "Negatif"   "Sıfır"
              |         |
              v         v
           (BİTİR)   (BİTİR)
```

Bu örnekte ilk koşul doğruysa algoritma doğrudan pozitif sonucuna ulaşır. İlk koşul yanlışsa ikinci koşul kontrol edilir.

## 4. Karar Ağacının Önemi

Karar ağaçları, bir problemin farklı olasılıklarını görmemizi sağlar.

Özellikle şu konularda yararlıdır:

* Birden fazla koşulun bulunduğu problemleri anlamak.
* Koşulların hangi sırayla değerlendirileceğini belirlemek.
* Her olası durumda hangi işlemin yapılacağını görmek.
* Algoritmadaki eksik veya hatalı kararları fark etmek.
* Karmaşık problemleri daha küçük karar adımlarına ayırmak.

## 5. Kısa Özet

* Karar ağacı, koşullara göre izlenen yolları gösterir.
* Her koşulun sonucuna göre algoritma farklı bir yoldan ilerleyebilir.
* Akış şeması, algoritmanın işleyişini görsel olarak ifade eder.
* Eşkenar dörtgen kararları, dikdörtgen işlemleri, paralelkenar ise girdi ve çıktıları gösterir.
* Doğru bir karar ağacı, olası durumları ve bu durumların sonuçlarını açıkça göstermelidir.

**Unutma:** Karar ağacının temel amacı, bir algoritmanın hangi durumda hangi kararı verdiğini anlaşılır hâle getirmektir.
