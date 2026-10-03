## 1. Döngü Nedir?

Döngü, bir algoritmada belirli bir işlemin veya işlem grubunun birden fazla kez tekrarlanmasını sağlayan yapıdır.

Bazı problemlerde aynı işlemi tekrar tekrar gerçekleştirmemiz gerekir. Her tekrar için ayrı bir komut yazmak yerine döngüler kullanabiliriz.

Örneğin, 1'den 5'e kadar olan sayıları ekrana yazdırmak istediğimizi düşünelim. Her sayı için ayrı bir komut yazmak yerine bir döngü kullanarak bu işlemi gerçekleştirebiliriz.

## 2. Döngüler Neden Kullanılır?

Döngülerin temel amacı, tekrar eden işlemleri daha kolay ve düzenli bir şekilde gerçekleştirmektir.

Döngü kullanmanın başlıca avantajları şunlardır:

* Tekrar eden işlemleri tek bir yapı içerisinde toplar.
* Gereksiz kod tekrarını azaltır.
* Algoritmaların daha kısa ve anlaşılır olmasını sağlar.
* Belirli sayıda veya bir koşul sağlandığı sürece işlem yapılmasına olanak tanır.

## 3. Günlük Hayattan Döngü Örneği

Bir kitabın 10 sayfasını sırayla okumak istediğimizi düşünelim.

Her sayfayı okuduktan sonra bir sonraki sayfaya geçeriz. Bu işlem, 10 sayfa tamamlanana kadar devam eder.

Bu örnekte:

* **Başlangıç:** İlk sayfadan okumaya başlamak.
* **Tekrarlanan işlem:** Bir sayfayı okumak.
* **Koşul:** Okunacak sayfa sayısının 10'dan küçük veya eşit olması.
* **Bitiş:** 10 sayfa okunduğunda işlemi durdurmak.

Bu işlem, döngü mantığının günlük hayattaki basit bir örneğidir.

## 4. Basit Bir Döngü Örneği

1'den 5'e kadar olan sayıları ekrana yazdıran bir algoritma oluşturalım.

**Algoritmanın adımları:**

1. Sayacı 1 olarak başlat.
2. Sayacın 5'ten küçük veya eşit olup olmadığını kontrol et.
3. Koşul doğruysa sayacı ekrana yazdır.
4. Sayacı 1 artır.
5. Koşulu yeniden kontrol et.
6. Koşul yanlış olduğunda döngüyü bitir.

**Sözde kod:**

```text
BAŞLA

    sayaç = 1

    sayaç <= 5 OLDUĞU SÜRECE
        sayacı yazdır
        sayaç = sayaç + 1

BİTİR
```

**Çıktı:**

```text
1
2
3
4
5
```

Bu örnekte aynı yazdırma işlemi, sayaç 5'e ulaşana kadar tekrarlanır.

## 5. Döngülerde Sayaç ve Koşul

Döngüleri anlamak için iki önemli kavramı bilmemiz gerekir.

**Sayaç:** Döngünün kaçıncı tekrarda olduğunu takip etmek için kullanılan değişkendir.

**Koşul:** Döngünün devam edip etmeyeceğini belirleyen ifadedir.

Örneğimizde sayaç 1'den başlar ve her tekrarda 1 artar. Sayaç 5'i geçtiğinde koşul yanlış olur ve döngü sona erer.

Her döngüde sayaç bulunması zorunlu değildir. Bazı döngüler bir koşul doğru olduğu sürece devam eder.

## 6. Döngü Türleri

Programlamada yaygın olarak kullanılan iki döngü türü vardır:

| Döngü | Kullanım amacı                                                    |
| ----- | ----------------------------------------------------------------- |
| For   | Tekrar sayısının önceden bilindiği durumlarda sıkça kullanılır.   |
| While | Bir koşul doğru olduğu sürece işlemi tekrarlamak için kullanılır. |

Her iki döngü de tekrar eden işlemleri gerçekleştirebilir. Aralarındaki temel fark, tekrarların nasıl kontrol edildiğidir.

## 7. Sonsuz Döngü Nedir?

Bir döngünün durmasını sağlayan koşul hiçbir zaman yanlış olmazsa döngü sürekli çalışabilir. Bu duruma sonsuz döngü denir.

Örneğin, sayaç her tekrarda artırılmasına rağmen koşulun sürekli doğru kalacağı şekilde belirlenmesi, döngünün bitmemesine neden olabilir.

Bu nedenle döngüler tasarlanırken bitiş koşulunun doğru belirlenmesi önemlidir.

## 8. Kısa Özet

* Döngüler, tekrar eden işlemleri gerçekleştirmek için kullanılır.
* Kod tekrarını azaltır ve algoritmaları daha düzenli hâle getirir.
* Sayaç, tekrar sayısını takip etmek için kullanılabilir.
* Koşul, döngünün devam edip etmeyeceğini belirler.
* For ve while, yaygın olarak kullanılan iki döngü türüdür.
* Bitiş koşulu doğru belirlenmezse sonsuz döngü oluşabilir.

