# While Döngüsü

## 1. While Döngüsü Nedir?

While döngüsü, belirli bir koşul doğru olduğu sürece bir veya birden fazla işlemi tekrar eden döngü yapısıdır.

For döngüsünden farklı olarak while döngüsünde tekrar sayısının önceden bilinmesi gerekmez. Döngünün devam edip etmeyeceğini belirleyen temel unsur koşuldur.

Örneğin, kullanıcı doğru şifreyi girene kadar tekrar şifre isteyen bir algoritmada while döngüsü kullanılabilir.

## 2. While Döngüsünün Çalışma Mantığı

While döngüsünün temelinde iki önemli unsur bulunur:

* **Koşul:** Döngünün devam edip etmeyeceğini belirler.
* **Tekrarlanan işlem:** Koşul doğru olduğu sürece gerçekleştirilen işlemdir.

While döngüsü çalışmaya başlamadan önce koşul kontrol edilir.

* Koşul doğruysa döngünün içindeki işlemler gerçekleştirilir.
* İşlemler tamamlandığında koşul yeniden kontrol edilir.
* Koşul yanlış olduğunda döngü sona erer.

Koşul başlangıçta yanlışsa döngünün içindeki işlemler hiç çalışmayabilir.

## 3. While Döngüsü Örneği

1'den 5'e kadar olan sayıları ekrana yazdıralım.

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

Bu örnekte sayaç her tekrarda 1 artırılır. Sayaç 5'i geçtiğinde koşul yanlış olur ve döngü sona erer.

## 4. While Döngüsünde Koşulun Önemi

While döngüsünde koşulun doğru belirlenmesi gerekir. Çünkü döngünün devam edip etmeyeceği bu koşula bağlıdır.

Örneğin, aşağıdaki algoritmayı inceleyelim:

```text
BAŞLA

    sayaç = 1

    sayaç <= 3 OLDUĞU SÜRECE
        sayacı yazdır

BİTİR
```

Bu örnekte sayaç artırılmadığı için değer sürekli 1 olarak kalır. Dolayısıyla koşul her zaman doğru olur ve döngü sona ermez.

Bu duruma **sonsuz döngü** denir.

Döngünün tamamlanabilmesi için koşulun bir noktada yanlış olmasını sağlayacak bir değişiklik yapılmalıdır.

## 5. For ve While Döngüsü Arasındaki Fark

| For döngüsü                                               | While döngüsü                                                                |
| --------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Belirli sayıdaki tekrarlar için sıkça kullanılır.         | Bir koşul doğru olduğu sürece çalışır.                                       |
| Tekrar sayısı genellikle önceden bellidir.                | Tekrar sayısı önceden bilinmeyebilir.                                        |
| Başlangıç, koşul ve artış çoğunlukla birlikte tanımlanır. | Koşul kontrolü ön plandadır.                                                 |
| Sayı aralıkları üzerinde işlem yapmak için kullanışlıdır. | Kullanıcı girdisi veya değişen durumlara bağlı tekrarlar için kullanışlıdır. |

Her iki döngü de uygun şekilde tasarlandığında aynı işlemi gerçekleştirebilir.

## 6. While Döngüsünün Kullanım Alanları

While döngüsü özellikle şu durumlarda kullanılabilir:

* Kullanıcı doğru bir bilgi girene kadar tekrar istemek.
* Belirli bir koşul sağlanana kadar işlem yapmak.
* Bir sayacın belirli bir değere ulaşmasını beklemek.
* Kullanıcı işlemi sonlandırana kadar menüyü tekrar göstermek.
* Bir işlemin sonucuna göre tekrara devam etmek.

## 7. Kısa Özet

* While döngüsü, bir koşul doğru olduğu sürece çalışır.
* Koşul her tekrardan önce kontrol edilir.
* Koşul başlangıçta yanlışsa döngü hiç çalışmayabilir.
* Koşulun yanlış olmasını sağlayan bir değişiklik yapılmazsa sonsuz döngü oluşabilir.
* For ve while döngüleri benzer işlemleri gerçekleştirebilir ancak kullanım amaçları farklı olabilir.

**Unutma:** While döngüsünde önemli olan tekrar sayısı değil, döngünün devam etmesini sağlayan koşuldur.
