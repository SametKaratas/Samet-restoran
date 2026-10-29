# Ajanlarla Çalışan Restoran

Bugün Claude Code ile kendi restoranımızı kuracağız. Restoranı birbirine iş devreden yapay zeka ajanları işletecek; biz restoranın **Patron**u olacağız.

Küçükten büyüğe gideceğiz: önce restoranı açacak, sonra ajanları tek tek işe alacak, en sonda hepsini birlikte çalıştıracağız.

## Adımlar

| Adım | Ne yapacağız |
|---|---|
| **0 · Restoranı açacağız** | Restoranın kartını yazacağız: konsept, masalar, saatler |
| **1 · Rezervasyon ajanı** | İlk ajanımızı ve defterini birlikte kuracağız |
| **2 · Şef ajanı** | Tahtada anlaşıp ikinci ajanı kendimiz kuracağız; iki ajan arasında bilgiyi elle taşıyacağız |
| **3 · Müdür** | Ortak el kitabını (`CLAUDE.md`) birlikte yazacağız; ajanlar arasındaki bilgiyi artık Müdür taşıyacak |
| **4 · Tedarik ajanı** | Satın alma limitini koyup üçüncü ajanı tamamen kendimiz kuracağız; bütün ekibi birlikte deneyeceğiz |

Her adımda Claude'a vereceğimiz promptlar `promptlar.md` dosyasında. Her adımın sonunda değişiklikleri kaydedip GitHub'a göndereceğiz.

## Repoda neler var

| Dosya | Ne işe yarar |
|---|---|
| `README.md` | Bu dosya |
| `promptlar.md` | Her adımda Claude'a vereceğimiz promptlar |
| `defterler/tedarikciler.md` | Manav, kasap, balık hali, market, bakkal ve özel ürün tedarikçisi; ürün grupları ve fiyat aralıkları. 4. adımda Tedarik ajanı kullanacak. |

Geri kalan her şeyi biz kuracağız.
