# Mantıksal Operatörler

## 1. Mantıksal Operatörler Nedir?

Bir algoritmada bazen tek bir koşulu kontrol etmek yeterli olmaz.
Birden fazla koşulu birlikte değerlendirmek gerekebilir.

Örneğin:

> Kullanıcının yaşı 18 veya daha büyük **ve** üyeliği aktif olmalı.

Burada iki farklı koşul vardır:

```text
Yaş >= 18
Üyelik = Aktif
```

Bu koşulları birlikte değerlendirmek için **mantıksal operatörler** kullanılır.

Temel mantıksal operatörler:

* `VE (AND)`
* `VEYA (OR)`
* `DEĞİL (NOT)`

---

# 2. VE (AND)

`VE`, iki veya daha fazla koşulun **aynı anda doğru olmasını** ister.

Örneğin:

```text
Yaş >= 18
VE
Üyelik = Aktif
```

Bu durumda iki koşulun da doğru olması gerekir.

### Doğruluk Tablosu

| Koşul 1 | Koşul 2 | Sonuç  |
| ------- | ------- | ------ |
| Doğru   | Doğru   | Doğru  |
| Doğru   | Yanlış  | Yanlış |
| Yanlış  | Doğru   | Yanlış |
| Yanlış  | Yanlış  | Yanlış |

Yani `VE` mantığında:

> **Hepsi doğruysa sonuç doğrudur.**

---

# 3. VEYA (OR)

`VEYA`, koşullardan **en az birinin doğru olması** durumunda doğru sonuç verir.

Örneğin:

```text
Ödeme = Kredi Kartı
VEYA
Ödeme = Havale
```

Kullanıcı bu iki ödeme yönteminden herhangi birini seçmişse koşul sağlanır.

### Doğruluk Tablosu

| Koşul 1 | Koşul 2 | Sonuç  |
| ------- | ------- | ------ |
| Doğru   | Doğru   | Doğru  |
| Doğru   | Yanlış  | Doğru  |
| Yanlış  | Doğru   | Doğru  |
| Yanlış  | Yanlış  | Yanlış |

Yani `VEYA` mantığında:

> **En az bir koşul doğruysa sonuç doğrudur.**

---

# 4. DEĞİL (NOT)

`DEĞİL`, bir koşulun sonucunu tersine çevirir.

Başka bir ifadeyle:

```text
Doğru → Yanlış
Yanlış → Doğru
```

Örneğin:

```text
Üyelik aktif
```

koşulu doğruysa:

```text
DEĞİL üyelik aktif
```

ifadesi yanlış olur.

### Doğruluk Tablosu

| Koşul  | NOT Sonucu |
| ------ | ---------- |
| Doğru  | Yanlış     |
| Yanlış | Doğru      |

---

# 5. VE ve VEYA Arasındaki Fark

Bu iki operatör sık sık karıştırılabilir.

### VE

İki koşulun da doğru olması gerekir.

```text
A VE B
```

```text
A = Doğru
B = Doğru

Sonuç = Doğru
```

---

### VEYA

Koşullardan birinin doğru olması yeterlidir.

```text
A VEYA B
```

```text
A = Doğru
B = Yanlış

Sonuç = Doğru
```

Kısaca:

```text
VE   → Hepsi doğru olmalı
VEYA → En az biri doğru olmalı
```

---

# 6. Günlük Hayattan Örnekler

Mantıksal operatörleri günlük hayattan düşünmek konuyu daha kolay anlamayı sağlar.

### VE

> Sinemaya girmek için biletin **VE** kimliğin olmalı.

Burada iki koşulun da sağlanması gerekir.

```text
Bilet var mı? → Evet
Kimlik var mı? → Evet

Sonuç → Girebilir
```

---

### VEYA

> Ödeme kredi kartı **VEYA** banka kartı ile yapılabilir.

Burada iki seçenekten herhangi biri yeterlidir.

```text
Kredi kartı → Evet
Banka kartı → Hayır

Sonuç → Ödeme yapılabilir
```

---

### DEĞİL

> Hesap aktif **değilse** işlem yapılamaz.

Burada mevcut durumun tersi kontrol edilmektedir.

```text
Hesap aktif mi?
      ↓
    DEĞİL
      ↓
Hesap aktif değil
```

---

# 7. Birden Fazla Mantıksal Operatör Kullanmak

Daha karmaşık problemlerde birden fazla mantıksal operatör aynı algoritmada kullanılabilir.

Örneğin:

> Kullanıcının yaşı 18 veya daha büyük **ve** hesabı aktif **veya** yönetici yetkisine sahip olmalı.

Burada:

```text
Yaş >= 18
VE
Hesap aktif
VEYA
Yönetici yetkisi
```

gibi birden fazla koşul bulunmaktadır.

Bu tür durumlarda koşulların nasıl gruplanacağı önemlidir.

Bu nedenle karmaşık koşullar oluştururken ifadeyi küçük parçalara ayırmak daha anlaşılırdır.

---

# 8. Koşulları Parçalara Ayırmak

Karmaşık bir koşulu doğrudan düşünmek yerine parçalara ayırabiliriz.

Örneğin:

```text
Yaş >= 18
```

birinci koşul olsun.

```text
Hesap aktif
```

ikinci koşul olsun.

```text
Yönetici
```

üçüncü koşul olsun.

Daha sonra bunların arasındaki mantıksal ilişkiyi belirleriz.

Bu yaklaşım algoritmanın daha kolay anlaşılmasını sağlar.

---

# 9. Doğruluk Tablosu Neden Kullanılır?

Birden fazla koşul olduğunda hangi durumda hangi sonucun ortaya çıkacağını görmek zorlaşabilir.

Doğruluk tabloları bu noktada yardımcı olur.

Örneğin `VE` için:

| A      | B      | A VE B |
| ------ | ------ | ------ |
| Doğru  | Doğru  | Doğru  |
| Doğru  | Yanlış | Yanlış |
| Yanlış | Doğru  | Yanlış |
| Yanlış | Yanlış | Yanlış |

Bu tablo bize `VE` operatörünün nasıl çalıştığını açık şekilde gösterir.

---

# 10. Algoritmik Düşünme Açısından

Mantıksal operatörler algoritmanın **karar verme kapasitesini artırır.**

Tek koşul:

```text
Koşul
 ↓
Karar
```

Birden fazla koşul:

```text
Koşul 1
   +
Koşul 2
   ↓
Mantıksal operatör
   ↓
Karar
```

Örneğin:

```text
Yaş >= 18
VE
Üyelik aktif
```

ifadesi algoritmaya iki farklı bilgiyi birlikte değerlendirme imkânı verir.

---

# 11. Temel Mantık

Mantıksal operatörleri şu şekilde hatırlayabiliriz:

```text
VE
↓
Her iki koşul da doğru olmalı


VEYA
↓
En az bir koşul doğru olmalı


DEĞİL
↓
Sonucu tersine çevirir
```

---

# Genel Özet

Bu bölümde:

* Mantıksal operatörlerin ne olduğunu
* `VE (AND)` operatörünü
* `VEYA (OR)` operatörünü
* `DEĞİL (NOT)` operatörünü
* Doğruluk tablolarını
* Birden fazla koşulun birlikte değerlendirilmesini

öğrendik.

Temel yapı:

```text
KOŞULLAR
   ↓
Mantıksal operatör
   ↓
Doğru / Yanlış
   ↓
Karar
```

En önemli üç kural:

```text
VE   → Hepsi doğru olmalı
VEYA → En az biri doğru olmalı
NOT  → Sonucu tersine çevirir
```

**Eğitim kapsamında bireysel öğrenme ve uygulama çalışmasıdır.**
