# Kartlar

Her kartı Claude Code'a olduğu gibi kopyalayıp yapıştıracağız. Köşeli parantezli yerleri kendimiz dolduracağız.

---

## Adım 0 · Restoranı açacağız

### Kart 0.1 · Repoyu tanıyalım
> Bu repoda ne var? Her dosyanın ne işe yaradığını kısaca anlat.

### Kart 0.2 · Restoran kartını yazalım
> Bu repoda `restoran.md` adında bir restoran kartı oluşturalım. Bana şu dört başlığı sırayla, her seferinde bir soru sorarak doldur:
>
> 1. **Kimlik:** restoranın adı, konsepti (mutfak türü), semti, fiyat seviyesi
> 2. **Kapasite:** kaç masa var, her masa kaç kişilik
> 3. **Zaman:** açılış ve kapanış saati, son oturma saati, bir masa ortalama ne kadar dolu kalır
> 4. **Şef'ten beklenti:** menüde mutlaka olmasını istediklerim ve istemediklerim
>
> Masaları sorarken en az bir masanın 6 kişilik olması ve toplam kapasitenin 30–40 kişi arasında kalması gerektiğini hatırlat.
>
> Dosyanın en üstüne şunu yaz: "Bu dosyanın sahibi Patron'dur. Ajanlar bu dosyayı okur, değiştirmez."
>
> Bütün cevaplarımı aldıktan sonra dosyayı yaz ve bana göster.

### Kart 0.3 · Kaydedip gönderelim
> Değişiklikleri "Restoran açıldı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] `restoran.md` dört başlığı da içeriyor.
- [ ] En üstte sahiplik satırı var.
- [ ] En az bir 6 kişilik masa var; toplam kapasite 30–40 kişi arasında.
- [ ] GitHub'daki repomuzda "Restoran açıldı" kaydı görünüyor.

---

## Adım 1 · Rezervasyon ajanı

_Ajanı ve defterini birlikte yazacağız. Aşağıdaki kartlar, ajanı yazdıktan sonra onu denemek için._

> **Saatler:** Kartlardaki saatleri kendi restoranımızın açılış ve son oturma saatine göre değiştireceğiz. Köşeli parantezdeki notlara bakalım.

### Kart 1.1 · İlk rezervasyon
> Ayşe Yılmaz aradı: bu akşam [açılıştan 2 saat sonra] için 4 kişilik masa istiyor.

### Kart 1.2 · Yoğun bir akşam
> Bu akşam için gelen talepler:
> - Mert Kaya, [açılış saati], 2 kişi
> - Selin Demir, [açılıştan 30 dk sonra], 6 kişi
> - Can Aydın, [açılıştan 1 saat sonra], 2 kişi
> - Deniz Arslan, [açılıştan 1,5 saat sonra], 4 kişi
> - Ece Şahin, [son oturmadan 30 dk önce], 3 kişi
> - Burak Öz, [son oturmadan 45 dk sonra], 2 kişi

### Kart 1.3 · Büyük grup
> Bir şirket aradı: bu akşam [açılıştan 1 saat sonra] 12 kişilik bir yemek için yer istiyorlar.

### Kart 1.4 · Kaydedip gönderelim
> Değişiklikleri "Rezervasyon ajanı işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] Ekranda Rezervasyon ajanının çalıştığını gösteren bir satır var; işi ana oturum yapmadı.
- [ ] Her rezervasyon kişi sayısına uyan bir masaya yazıldı; aynı masaya çakışan rezervasyon yok.
- [ ] Burak Öz'ün talebi kabul edilmedi, başka bir saat önerildi.
- [ ] 12 kişilik grup için deftere bir şey yazılmadı; Patron'a sorulması istendi.
- [ ] GitHub'da "Rezervasyon ajanı işe başladı" kaydı görünüyor.
