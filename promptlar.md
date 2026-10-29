# Promptlar

Her promptu Claude Code'a olduğu gibi kopyalayıp yapıştıracağız. Köşeli parantezli yerleri kendimiz dolduracağız.

Ajanların ve defterlerin içeriğine **biz** karar vereceğiz. Bu yüzden onları yazdırırken Claude'a soru sordurup cevapları biz vereceğiz; cevaplarımızı tahtada birlikte aldığımız kararlardan getireceğiz.

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

_Ajanı ve defterini tahtadaki kararlara göre birlikte yazacağız. Önce defter, sonra ajan. Sonra ajanı deneyeceğiz._

### Prompt 1.1 · Defteri yazdıralım
> `defterler/rezervasyonlar.md` adında Rezervasyon ajanının defterini oluşturacağız. Bana şunları sor: defterin sahibi kim, hangi bölümleri olacak, her bölümde hangi sütunlar olacak.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 1.2 · Ajanı yazdıralım
> `.claude/agents/rezervasyon.md` dosyasında Rezervasyon ajanını oluşturacağız. Bana şu altı bölümü sor: açıklama (hangi işlerde çağrılacak), görev ve kurallar, okuduğu bilgi, kendi defteri, yetki, sınır.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

_Ajan ekranda görünmezse oturumu kapatıp yeniden açacağız._

> **Saatler:** Aşağıdaki promptlardaki saatleri kendi restoranımızın açılış ve son oturma saatine göre değiştireceğiz. Köşeli parantezdeki notlara bakalım.

### Prompt 1.3 · İlk rezervasyon
> Ayşe Yılmaz aradı: bu akşam [açılıştan 2 saat sonra] için 4 kişilik masa istiyor.

### Prompt 1.4 · Yoğun bir akşam
> Bu akşam için gelen talepler:
> - Mert Kaya, [açılış saati], 2 kişi
> - Selin Demir, [açılıştan 30 dk sonra], 6 kişi
> - Can Aydın, [açılıştan 1 saat sonra], 2 kişi
> - Deniz Arslan, [açılıştan 1,5 saat sonra], 4 kişi
> - Ece Şahin, [son oturmadan 30 dk önce], 3 kişi
> - Burak Öz, [son oturmadan 45 dk sonra], 2 kişi

### Prompt 1.5 · Büyük grup
> Bir şirket aradı: bu akşam [açılıştan 1 saat sonra] 12 kişilik bir yemek için yer istiyorlar.

### Prompt 1.6 · Kaydedip gönderelim
> Değişiklikleri "Rezervasyon ajanı işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] Ajan dosyasındaki her kural tahtadaki bir karardan geliyor; Claude kendinden bir şey eklemedi.
- [ ] Ekranda Rezervasyon ajanının çalıştığını gösteren bir satır var; işi ana oturum yapmadı.
- [ ] Masalar tahtadaki kurallarımıza göre verildi; aynı masaya çakışan rezervasyon yok.
- [ ] Burak Öz'ün ve şirketin talebinde ajan tahtadaki kurallarımıza ve sınırımıza göre davrandı.
- [ ] GitHub'da "Rezervasyon ajanı işe başladı" kaydı görünüyor.

---

## Adım 2 · Şef ajanı

_Şef'i ve defterini tahtadaki kararlara göre kendimiz yazacağız. Tahtadaki iki sorunun cevabına göre Rezervasyon'u da güncelleyeceğiz. Sonra iki ajanı sırayla çalıştıracağız._

### Prompt 2.1 · Şef'in defteri
> `defterler/menu.md` adında Şef'in defterini oluşturacağız. Bana şunları sor: defterin sahibi kim, hangi bölümleri olacak, her bölümde neler yazacak.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 2.2 · Şef ajanı
> `.claude/agents/sef.md` dosyasında Şef ajanını oluşturacağız. Bana şu yedi bölümü sor: açıklama, görev ve kurallar, okuduğu bilgi, kendi defteri, yetki, sınır, rapor.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 2.3 · Rezervasyon'u güncelleyelim
> Rezervasyon ajanını tahtadaki kararlarımıza göre güncelleyeceğiz. Bana sor: ajana hangi yeni görev ekleniyor, raporu nasıl olacak, defterinde değişen bir şey var mı.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 2.4 · Kişi tahmini
> Bu akşamın kişi tahminini yap.

### Prompt 2.5 · Menü ve porsiyon planı
> Şef, bu akşam [bir önceki adımda çıkan kişi sayısı] kişi bekliyoruz. Menüyü, reçeteleri ve bu akşamın porsiyon planını hazırla.

_Köşeli parantezi bir önceki raporun içinden biz dolduracağız._

### Prompt 2.6 · Kaydedip gönderelim
> Değişiklikleri "Şef işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] İki ajan dosyasındaki her kural tahtadaki bir karardan geliyor.
- [ ] `defterler/menu.md`'de konseptimize uygun bir menü ve tahtada kararlaştırdığımız bölümler var.
- [ ] Menüde `restoran.md`'de "olmasın" dediğimiz bir şey yok.
- [ ] Her ajan sadece kendi defterini değiştirdi.
- [ ] İki ajanın raporu tahtada anlaştığımız formatta.

---

## Adım 3 · Müdür

_`CLAUDE.md` dosyasını tahtadaki kararlara göre birlikte yazacağız. Sonra **yeni bir oturum açıp** iki ajanı Müdür'e bırakacağız._

### Prompt 3.1 · El kitabını yazdıralım
> Reponun en üstünde `CLAUDE.md` adında restoranın ortak el kitabını oluşturacağız. Bana şu beş bölümü sor: roller, defter sahipleri, ortak kurallar, Müdür'ün kuralları, zincirler. Ortak kurallara aldığımız bir şey ajan dosyalarında da yazıyorsa, oradan çıkarıp çıkarmayacağımı bana sor.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

_Dosya yazılınca bu oturumu kapatıp **yeni bir oturum** açacağız._

### Prompt 3.2 · Akşam hazırlığı
> Saat 12:00. Bu akşamın hazırlığını başlat.

_Arada hiçbir şey yazmayacağız; ekranda hangi ajanların, hangi sırayla çalıştığını izleyeceğiz._

### Prompt 3.3 · Bir grup talebi
> Bir doğum günü grubu aradı: bu akşam [açılıştan 2 saat sonra] 10 kişi gelmek istiyorlar.

### Prompt 3.4 · Kaydedip gönderelim
> Değişiklikleri "Müdür işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] 3.2'de ajanlar sırayla çalıştı; aradaki bilgiyi biz taşımadık.
- [ ] Müdür tahtada yazdığımız kurallara uydu: neyi kendisi yaptı, neyi devretti?
- [ ] 3.3'te Müdür tahtadaki kurallarımıza göre davrandı.
- [ ] Birden fazla dosyada tekrar eden bir kural kalmadı.

---

## Adım 4 · Tedarik ajanı

_Bu adımı tamamen kendimiz yapacağız. Önce Patron olarak satın alma limitimizi restoran kartına ekleyeceğiz. Sonra Tedarik'in kutularını kendimiz dolduracak, ajanı ve defterini yazdıracak, el kitabını güncelleyeceğiz. En sonda bütün ekibi birlikte deneyeceğiz._

### Prompt 4.1 · Satın alma limiti
> `restoran.md`'ye "Satın alma" başlığı ekle: Tedarik tek siparişte en fazla [20.000 ₺]'ye kendisi karar verir, üstü Patron onayı ister.

_Limiti kendi restoranımıza göre değiştirebiliriz. Bu dosyanın sahibi biziz; bu yüzden değişikliği biz istiyoruz._

### Prompt 4.2 · Tedarik'in defteri
> `defterler/siparisler.md` adında Tedarik ajanının defterini oluşturacağız. Bana şunları sor: defterin sahibi kim, hangi bölümleri olacak, her bölümde hangi sütunlar olacak.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 4.3 · Tedarik ajanı
> `.claude/agents/tedarik.md` dosyasında Tedarik ajanını oluşturacağız. Bana şu bölümleri sor: açıklama, görev ve kurallar, okuduğu bilgi, kendi defteri, yetki, sınır, rapor.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 4.4 · El kitabını güncelleyelim
> `CLAUDE.md`'yi yeni ajana göre güncelleyeceğiz. Bana sor: hangi bölümlere ne ekleniyor, zincirlerde neler değişiyor, yeni bir zincir gerekiyor mu.
>
> **Çalışma kuralı:** İçeriğe ben karar vereceğim, sen sadece yazacaksın. Soruları sırayla, her seferinde bir tane sor. Sadece soruyu sor; öneri, örnek ya da seçenek verme. Cevabım belirsizse netleştirmek için yeniden sor, boşluğu kendin doldurma. Cevaplarımda olmayan hiçbir kural ekleme. Bitince dosyayı oluştur, sonra her bölümün hangi cevabımdan geldiğini bana kısaca göster.

### Prompt 4.5 · Tam zincir
> Saat 12:00. Bu akşamın hazırlığını başlat.

### Prompt 4.6 · Büyük alım
> Hafta sonu için iki akşamın malzemesini bugünden sipariş et.

### Prompt 4.7 · Teslimat sorunu
> [Siparişte tutarı en yüksek tedarikçi] aradı: bu akşam teslimat yapamıyor.

_Köşeli parantezi kendi restoranımızın siparişine bakıp dolduracağız._

### Prompt 4.8 · Kaydedip gönderelim
> Değişiklikleri "Tedarik işe başladı" mesajıyla kaydet ve GitHub'a gönder.

**Kontrol**
- [ ] `restoran.md`'de satın alma limiti var.
- [ ] Tedarik'in dosyasındaki her kural kendi kararımızdan geliyor.
- [ ] 4.5'te yeni ajan zincirde yer aldı ve sonunda Patron'a özet geldi.
- [ ] Siparişteki miktarlar Şef'in defterindeki bilgilerden hesaplandı.
- [ ] 4.6 ve 4.7'de ekip koyduğumuz limite, sınırlara ve zincirlere göre davrandı.
- [ ] Her ajan sadece kendi defterine yazdı.
