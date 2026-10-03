# AND ile Çoklu Koşullar

## 1. Çoklu Koşul Nedir?

Bir algoritmada bazen yalnızca iki değil, üç veya daha fazla koşulu aynı anda kontrol etmemiz gerekebilir.

Birden fazla koşulun tamamının doğru olması gerekiyorsa AND (VE) operatörünü kullanabiliriz.

Örneğin bir kişinin bir etkinliğe katılabilmesi için şu üç koşulu sağlaması gerektiğini düşünelim:

* Kayıt yaptırmış olması.
* Yaşının en az 18 olması.
* Katılım ücretini ödemiş olması.

Bu üç koşulun da doğru olması durumunda kişi etkinliğe katılabilir.

## 2. Birden Fazla Koşulun Birlikte Kullanılması

AND operatörü birden fazla koşulu birleştirebilir.

**Örnek: Etkinliğe Katılım Kontrolü**

| Kayıtlı mı? | Yaş 18 veya üzeri mi? | Ödeme yapıldı mı? | Katılabilir mi? |
| ----------- | --------------------- | ----------------- | --------------- |
| Evet        | Evet                  | Evet              | Evet            |
| Evet        | Evet                  | Hayır             | Hayır           |
| Evet        | Hayır                 | Evet              | Hayır           |
| Hayır       | Evet                  | Evet              | Hayır           |

Tablodaki ilk satırda bütün koşullar doğrudur. Diğer satırlarda en az bir koşul yanlış olduğu için katılım onaylanmaz.

Üç koşulun tamamının doğru olması gerektiğinden AND operatörü kullanılır.

## 3. Sözde Kod ile Çoklu Koşul

Aynı örneği bir algoritma haline getirelim.

```text
BAŞLA

    kayıt durumunu al
    yaş değerini al
    ödeme durumunu al

    EĞER kayıtlı = Evet
    VE yaş >= 18
    VE ödeme yapıldı = Evet İSE

        "Etkinliğe katılabilirsiniz" yazdır

    DEĞİLSE
        "Katılım koşulları sağlanmadı" yazdır

BİTİR
```

Bu algoritmada üç koşul birlikte kontrol edilir. Üçü de doğru olduğunda olumlu sonuç üretilir.

## 4. AND ile Koşulları Değerlendirme

Birden fazla AND operatörü kullanıldığında da aynı temel kural geçerlidir.

Örneğin:

```text
A VE B VE C
```

ifadesinin doğru olması için A, B ve C koşullarının tamamı doğru olmalıdır.

| A      | B      | C      | A VE B VE C |
| ------ | ------ | ------ | ----------- |
| Doğru  | Doğru  | Doğru  | Doğru       |
| Doğru  | Doğru  | Yanlış | Yanlış      |
| Doğru  | Yanlış | Doğru  | Yanlış      |
| Yanlış | Doğru  | Doğru  | Yanlış      |

Diğer olası kombinasyonlarda da en az bir koşul yanlışsa sonuç yanlış olur.

## 5. Çoklu Koşullarda Dikkat Edilmesi Gerekenler

* Her koşulun neyi kontrol ettiği açık olmalıdır.
* Bütün koşulların sağlanmasının gerçekten gerekli olup olmadığı belirlenmelidir.
* Koşullardan birinin yanlış olması durumunda algoritmanın ne yapacağı tanımlanmalıdır.
* Çok sayıda koşul kullanıldığında ifadelerin anlaşılır olması için koşullar ayrı ayrı incelenmelidir.

## 6. Kısa Özet

* Çoklu koşullar, birden fazla şartın birlikte değerlendirilmesini sağlar.
* AND operatörü ikiden fazla koşulu birleştirebilir.
* Bütün koşullar doğru olduğunda sonuç doğrudur.
* Koşullardan biri bile yanlış olduğunda sonuç yanlıştır.
* Çoklu koşullarda her koşulun ne anlama geldiği açıkça tanımlanmalıdır.

**Not:** Birden fazla koşulun tamamının sağlanması gerekiyorsa AND operatörünü kullanabiliriz.
