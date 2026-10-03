# For Döngüsü

## 1. For Döngüsü Nedir?

For döngüsü, belirli sayıda tekrar gerçekleştirmek istediğimizde sıkça kullanılan bir döngü yapısıdır.

Tekrar sayısının veya döngünün hangi değerler üzerinde çalışacağının önceden belli olduğu durumlarda kullanışlıdır.

Örneğin, 1'den 10'a kadar olan sayıları ekrana yazdırmak istediğimizde her sayı için ayrı bir komut yazmak yerine for döngüsünden yararlanabiliriz.

## 2. For Döngüsünün Çalışma Mantığı

For döngüsünün temelinde üç unsur bulunur:

* **Başlangıç değeri:** Döngünün hangi değerden başlayacağını belirler.
* **Koşul:** Döngünün devam edip etmeyeceğini belirler.
* **Artış veya azalış:** Her tekrarda değerin nasıl değişeceğini belirler.

Örneğin, 1'den 5'e kadar sayıları yazdırmak için:

* Başlangıç değeri: 1
* Koşul: Sayı 5'ten küçük veya eşit olmalı.
* Artış: Her tekrarda sayı 1 artmalı.

## 3. For Döngüsü Örneği

1'den 5'e kadar olan sayıları ekrana yazdıralım.

**Sözde kod:**

```text
BAŞLA

    1'den 5'e kadar her sayı için
        sayıyı yazdır

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

Bu örnekte döngü, 1'den başlayarak 5'e kadar her sayıyı ekrana yazdırır.

## 4. For Döngüsünde Artış ve Azalış

For döngüsü yalnızca birer birer artmak zorunda değildir. Belirlenen artış veya azalış miktarına göre de çalışabilir.

### Örnek 1: İkişer İkişer Artış

2'den 10'a kadar çift sayıları yazdıralım.

```text
BAŞLA

    2'den 10'a kadar ikişer artarak
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

Burada her tekrarda sayı 2 artırılır.

### Örnek 2: Geriye Doğru Sayma

5'ten 1'e kadar geriye doğru sayalım.

```text
BAŞLA

    5'ten 1'e kadar birer azalarak
        sayıyı yazdır

BİTİR
```

**Çıktı:**

```text
5
4
3
2
1
```

Bu örnekte sayı her tekrarda 1 azaltılır.

## 5. For Döngüsünde Tekrar Sayısı

Bir döngünün kaç kez çalışacağını belirlemek önemlidir.

Örneğin, 1'den 5'e kadar sayıları yazdıran bir for döngüsü 5 kez çalışır.

Ancak başlangıç ve bitiş değerleri değiştiğinde tekrar sayısı da değişebilir.

| Başlangıç | Bitiş | Artış | Tekrar sayısı |
| --------: | ----: | ----: | ------------: |
|         1 |     5 |     1 |             5 |
|         2 |    10 |     2 |             5 |
|         5 |     1 |    -1 |             5 |
|         1 |    10 |     1 |            10 |

Bu tabloda bitiş değerinin döngüye dahil olduğu kabul edilmiştir.

## 6. For Döngüsünün Kullanım Alanları

For döngüsü özellikle şu durumlarda kullanışlıdır:

* Belirli sayıdaki işlemleri tekrarlamak.
* Bir sayı aralığındaki değerleri incelemek.
* Bir listedeki elemanları sırayla işlemek.
* Belirli sayıda işlem gerçekleştirmek.
* Toplama ve sayma gibi tekrar gerektiren işlemleri yapmak.

## 7. Kısa Özet

* For döngüsü, belirli sayıdaki tekrarlar için sıkça kullanılır.
* Başlangıç değeri, koşul ve artış veya azalış miktarı döngünün işleyişini belirler.
* Döngüdeki değerler her tekrarda değişebilir.
* Artış veya azalış miktarı değiştirilerek farklı sayma işlemleri yapılabilir.
* Tekrar sayısı, başlangıç ve bitiş değerlerine bağlıdır.

**NOT:** For döngüsü, kaç kez tekrarlanacağı önceden belirlenebilen işlemleri düzenli bir şekilde gerçekleştirmemizi sağlar.
