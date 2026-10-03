# AND (VE) Operatörü

## 1. AND Operatörü Nedir?

AND (VE) operatörü, birden fazla koşulu aynı anda kontrol etmek için kullanılır.

Birden fazla koşulun bulunduğu durumlarda, bütün koşulların doğru olması gerekiyorsa AND operatöründen yararlanırız.

**Temel kural:** AND operatöründe bütün koşullar doğruysa sonuç doğrudur. Koşullardan en az biri yanlışsa sonuç yanlıştır.

## 2. AND Operatörünün Doğruluk Tablosu

AND operatörünün nasıl çalıştığını anlamak için doğruluk tablosuna bakalım.

| A koşulu | B koşulu | A VE B |
| -------- | -------- | ------ |
| Doğru    | Doğru    | Doğru  |
| Doğru    | Yanlış   | Yanlış |
| Yanlış   | Doğru    | Yanlış |
| Yanlış   | Yanlış   | Yanlış |

Tablodan da görülebileceği gibi yalnızca iki koşulun da doğru olduğu durumda sonuç doğrudur.

## 3. Günlük Hayattan Bir Örnek

Bir kişinin sinemaya indirimli bilet alabilmesi için hem öğrenci olması hem de 25 yaşından küçük olması gerektiğini düşünelim.

Bu durumda iki koşul bulunur:

* Kişinin öğrenci olması.
* Kişinin 25 yaşından küçük olması.

İki koşul da sağlanırsa indirimli bilet alınabilir.

| Öğrenci mi? | Yaş 25'ten küçük mü? | İndirimli bilet |
| ----------- | -------------------- | --------------- |
| Evet        | Evet                 | Evet            |
| Evet        | Hayır                | Hayır           |
| Hayır       | Evet                 | Hayır           |
| Hayır       | Hayır                | Hayır           |

Bu örnekte iki koşulun da doğru olması gerektiği için AND operatörü kullanılır.

## 4. AND Operatörünün Algoritmada Kullanımı

AND operatörünü sözde kod içerisinde birden fazla koşulu birleştirmek için kullanabiliriz.

**Örnek: İndirimli Bilet Kontrolü**

```text
BAŞLA

    öğrenci durumunu al
    yaş değerini al

    EĞER öğrenci = Evet VE yaş < 25 İSE
        "İndirimli bilet alabilirsiniz" yazdır
    DEĞİLSE
        "İndirim koşulları sağlanmadı" yazdır

BİTİR
```

Bu algoritmada önce öğrencilik durumu ve yaş kontrol edilir. Her iki koşul da doğruysa indirimli bilet mesajı gösterilir. Aksi durumda indirim koşullarının sağlanmadığı belirtilir.

## 5. AND Operatörünün Kullanım Alanları

AND operatörü, birden fazla şartın aynı anda sağlanması gereken durumlarda kullanılabilir.

Örnekler:

* Bir kişinin hem kullanıcı adına hem de şifresine ilişkin kontrollerin başarılı olması.
* Bir ürünün hem stokta bulunması hem de satışa açık olması.
* Bir öğrencinin hem devam koşulunu hem de sınav notu koşulunu sağlaması.
* Bir işlemin hem yetki hem de onay koşullarını karşılaması.

Bu örneklerde ortak nokta, bütün koşulların doğru olmasının gerekmesidir.

