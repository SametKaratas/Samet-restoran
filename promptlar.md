# Promptlar

Her promptu Claude Code'a olduğu gibi kopyalayıp yapıştıracağız. Köşeli parantezli yerleri kendimiz dolduracağız.

---

## Adım 0 · Restoranı açacağız

### Prompt 0.1 · Repoyu tanıyalım
> Bu repoda ne var? Her dosyanın ne işe yaradığını kısaca anlat.

### Prompt 0.2 · Restoran kartını yazalım
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

### Prompt 0.3 · Kaydedip gönderelim
> Değişiklikleri "Restoran açıldı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] `restoran.md` dört başlığı da içeriyor.
- [ ] En üstte sahiplik satırı var.
- [ ] En az bir 6 kişilik masa var; toplam kapasite 30–40 kişi arasında.
- [ ] GitHub'daki repomuzda "Restoran açıldı" kaydı görünüyor.

---

## Adım 1 · Rezervasyon ajanı

_Ajanı ve defterini birlikte yazacağız. Aşağıdaki promptlar, ajanı yazdıktan sonra onu denemek için._

> **Saatler:** Promptlardaki saatleri kendi restoranımızın açılış ve son oturma saatine göre değiştireceğiz. Köşeli parantezdeki notlara bakalım.

### Prompt 1.1 · İlk rezervasyon
> Ayşe Yılmaz aradı: bu akşam [açılıştan 2 saat sonra] için 4 kişilik masa istiyor.

### Prompt 1.2 · Yoğun bir akşam
> Bu akşam için gelen talepler:
> - Mert Kaya, [açılış saati], 2 kişi
> - Selin Demir, [açılıştan 30 dk sonra], 6 kişi
> - Can Aydın, [açılıştan 1 saat sonra], 2 kişi
> - Deniz Arslan, [açılıştan 1,5 saat sonra], 4 kişi
> - Ece Şahin, [son oturmadan 30 dk önce], 3 kişi
> - Burak Öz, [son oturmadan 45 dk sonra], 2 kişi

### Prompt 1.3 · Büyük grup
> Bir şirket aradı: bu akşam [açılıştan 1 saat sonra] 12 kişilik bir yemek için yer istiyorlar.

### Prompt 1.4 · Kaydedip gönderelim
> Değişiklikleri "Rezervasyon ajanı işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] Ekranda Rezervasyon ajanının çalıştığını gösteren bir satır var; işi ana oturum yapmadı.
- [ ] Her rezervasyon kişi sayısına uyan bir masaya yazıldı; aynı masaya çakışan rezervasyon yok.
- [ ] Burak Öz'ün talebi kabul edilmedi, başka bir saat önerildi.
- [ ] 12 kişilik grup için deftere bir şey yazılmadı; Patron'a sorulması istendi.
- [ ] GitHub'da "Rezervasyon ajanı işe başladı" kaydı görünüyor.

---

## Adım 2 · Şef ajanı

_Şef'i ve defterini tahtadaki kararlara göre kendimiz yazacağız. Rezervasyon'a kişi tahmini görevini, iki ajana da rapor bölümünü ekleyeceğiz. Sonra zinciri elle yürüteceğiz: bilgiyi bir ajandan diğerine biz taşıyacağız._

### Prompt 2.1 · Kişi tahmini
> Rezervasyon, bu akşamın kişi tahminini yap.

### Prompt 2.2 · Menü ve porsiyon planı
> Şef, bu akşam [Rezervasyon'un raporundaki kişi sayısı] kişi bekliyoruz. Menüyü, reçeteleri ve bu akşamın porsiyon planını hazırla.

_Köşeli parantezi Rezervasyon'un raporuna bakarak biz dolduracağız._

### Prompt 2.3 · Kaydedip gönderelim
> Değişiklikleri "Şef işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] Rezervasyon'un raporunda kişi tahmini var ve rapor tahtada anlaştığımız başlıklarla yazılmış.
- [ ] `defterler/menu.md`'de konseptimize uygun menü, fiyatlar, reçeteler ve porsiyon planı var.
- [ ] Menüde "olmasın" dediğimiz bir şey yok.
- [ ] Şef sadece kendi defterini değiştirdi.
- [ ] İki ajanın raporu aynı başlıkları kullanıyor.

## Adım 3 · Müdür

_CLAUDE.md dosyasını birlikte yazacağız ve Müdür'ü işe alacağız. Rapor bölümünü iki ajan dosyasından çıkarıp CLAUDE.md'ye taşıyacağız. Sonra **yeni bir oturum açıp** Adım 2'de elle yürüttüğümüz zinciri Müdür'e bırakacağız._

### Prompt 3.1 · Akşam hazırlığı
> Saat 12:00. Bu akşamın hazırlığını başlat.

_Arada hiçbir şey yazmayacağız. Ekranda önce Rezervasyon'un, sonra Şef'in çalıştığını izleyeceğiz._

### Prompt 3.2 · Onay gereken bir talep
> Bir doğum günü grubu aradı: bu akşam [açılıştan 2 saat sonra] 10 kişi gelmek istiyorlar.

_Müdür bize seçenekleri sunup cevabımızı bekleyecek. Patron olarak kararı biz vereceğiz; Müdür kararımızı Rezervasyon'a iletecek._

### Prompt 3.3 · Kaydedip gönderelim
> Değişiklikleri "Müdür işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] 3.1'de Rezervasyon ve Şef sırayla çalıştı; aradaki bilgiyi biz taşımadık.
- [ ] Müdür defterlere kendisi yazmadı, işi ajanlara verdi.
- [ ] Sonunda Patron'a kısa bir özet geldi.
- [ ] 3.2'de Müdür deftere yazdırmadan önce bize sordu ve kararımızı Rezervasyon'a iletti.
- [ ] Rapor formatı artık sadece CLAUDE.md'de yazıyor; iki ajan dosyasında tekrar etmiyor.
