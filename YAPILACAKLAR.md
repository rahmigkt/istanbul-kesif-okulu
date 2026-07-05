# İstanbul Keşif Okulu — Yapılacaklar Listesi

Bu dosya, projenin canlı, kalıcı yapılacaklar listesidir. Her oturumda güncellenir.
Son güncelleme: 2026-07-05 (4. güncelleme — gerçek kurumsal içerik entegrasyonu)

## ✅ Bu turda tamamlananlar
- [x] "Bizans" → "Doğu Roma" terminolojisi (29 ders kaydında, veritabanında; Bizantion ancient city adı kasıtlı korundu)
- [x] Açılış sloganı: "İstanbullu Olmak, Kültürlü Olmaktır"
- [x] Sahte demo eğitmenler (Elif Demir, Mehmet Kaya, Zeynep Aydın, Can Öz) kaldırıldı
- [x] Gerçek eğitim kadrosundan 4 eğitmen hesabı eklendi (Prof. Dr. Mehmet Özsait/Modül I, Prof. Dr. Ahmet Kal'a/Modül II, Prof. Dr. İlber Ortaylı/Modül III, Doç. Dr. Engin Akyürek/Keşif Turları) — şifre: 1234
- [x] Vizyon bölümü: Amaç, Misyon, Kapsam, Hedef Kitle eklendi (gerçek kurucu belge içeriği)
- [x] Paydaşlar bölümü: 18 ek gerçek kurum/kuruluş eklendi (Kültür ve Turizm Bakanlığı, İBB, İKSV, TÜRSAB, THY, vb.)
- [x] Yeni "Akademik Kadro" bölümü: Danışma Kurulu (6 makam), Bilim Kurulu (5 isim), Eğitim Kadrosu (28 isim), Eğitim Branşları (13 alan)

## ⚠️ Kullanıcıya hatırlatma
- Bilim Kurulu/Danışma Kurulu/Eğitim Kadrosu'ndaki isimlerin **güncel onayının/bilgisinin teyit edilmesi** önerildi (belge eski olabilir) — kullanıcı bilgilendirildi, engel olmadı.
- Eğitim Kadrosu'ndaki 28 isimden sadece 4'üne gerçek fonksiyonel giriş hesabı açıldı (Özsait, Kal'a, Ortaylı, Akyürek); diğerleri sadece bilgilendirme amaçlı listelendi (hesapları yok).


---

## ✅ TAMAMLANANLAR

### Altyapı
- [x] Supabase (PostgreSQL) veritabanı kuruldu
- [x] Netlify üzerinden yayına alındı, GitHub'a bağlı otomatik deploy
- [x] Kendi domain (schoolofistanbul.com) bağlandı, SSL aktif
- [x] Site içi düzenleme modu (özel şifreyle metin/görsel/bölüm düzenleme)

### Öğrenci / Eğitmen Sistemi
- [x] Öğrenci kayıt + giriş (şifreler bcrypt ile şifrelenmiş)
- [x] Eğitmen/yönetici girişi, rol bazlı paneller (instructor/admin/siteeditor)
- [x] Ders takvimi, video gömme (YouTube izleme yüzdesi takibi dahil)
- [x] Ders/eğitmen değerlendirme (öğrenciden anonim, eğitmen kimliği görmüyor kim puanladığını)
- [x] Ödeme adımı (DEMO — gerçek tahsilat yok, bkz. "Resmi işlem gerektirenler")

### LMS/ERP Çekirdek Mantığı
- [x] GPS coğrafi çit doğrulaması (geofencing) — sahada gerçek konum kontrolü
- [x] Kontenjanlı keşif turu randevu sistemi (quota + booking)
- [x] Mazeret + video izleme çift şartlı devam mantığı
- [x] Sertifika kilidi (yoklama %100 kontrolü)
- [x] Canlı ders linki self-check-in

### Bildirimler ve Admin Yönetimi
- [x] Site-içi bildirim sistemi (kayıt, mazeret gönderimi, mazeret onay/red, iletişim mesajı)
- [x] Admin: öğrenci arama/filtreleme, dondurma, silme, CSV dışa aktarma
- [x] Admin: yeni eğitmen/yönetici hesabı oluşturma ekranı
- [x] Admin: eğitmen/yönetici şifresini sıfırlama
- [x] İletişim formu (site → admin bildirimi, admin panelinden mesajları görüntüleme)
- [x] Şifremi unuttum (öğrenci için, e-posta + doğum tarihi doğrulamasıyla)
- [x] KVKK onay kutusu (kayıt formunda, zorunlu) + Gizlilik Metni (taslak, hukuki danışmanlık uyarılı)
- [x] SSS (Sıkça Sorulan Sorular) bölümü
- [x] Kullanım Şartları sayfası (taslak, hukuki danışmanlık uyarılı)
- [x] Öğrenci kendi panelinden şifre değiştirebiliyor (mevcut şifre doğrulamalı)
- [x] `info@schoolofistanbul.com` gerçek posta kutusu Natro'da oluşturuldu ve siteye (İletişim + footer) eklendi

### 📧 E-posta durumu (kısmi)
- Natro'da 1 kutu hakkı var, `info@schoolofistanbul.com` aktif ve doğrulandı (webmail: XMail Cloud üzerinden çalışıyor)
- `bilgi@`, `kayit@`, `destek@`, `yonetim@` adresleri **oluşturulamadı** — paket sadece 1 hesap içeriyor. Ek hesap için paket yükseltmesi veya "yönlendirme (forwarder)" özelliği araştırılmalı.
- info@ adresinin Gmail'den okunup yazılması (IMAP/SMTP kurulumu) **beklemede** — kullanıcı "başka zamana" bıraktı.
- Otomatik sistem maili (kayıt onayı vb.) göndermek için henüz bir mekanizma kurulmadı — bu info@ kutusunun SMTP bilgileriyle ya da Resend gibi bir servisle yapılabilir, karar bekleniyor.


---

## 🔴 RESMİ İŞLEM GEREKTİRENLER (şimdilik bekletiliyor — kullanıcı talebiyle)
Bunlar bir kurum/hesap/sözleşme gerektirdiği için öncelik dışı bırakıldı:
- [ ] Gerçek ödeme tahsilatı (iyzico / PayTR / Stripe sözleşmesi + entegrasyon)
- [ ] KVKK VERBİS kaydı (resmi devlet kaydı — hukuki danışmanlık önerilir)
- [ ] Şirket/vakıf resmi vergi & fatura entegrasyonu
- [ ] **SMS bildirimleri** — bütçe kararı (SMS ücretli, ücretsiz kota yok) + İYS (İleti Yönetim Sistemi) kaydı gerektirir. Netgsm/İletiMerkezi önerilir. "Aklımızda olsun" notuyla bekletiliyor.

## 🟡 SIRADAKI ÖNCELİKLER
- [ ] **E-posta gönderim mekanizması** — info@ kutusunun SMTP bilgileri ile otomatik mail (kayıt onayı, mazeret sonucu vb.) gönderme kurulumu (kullanıcı ile bekliyor, "başka zamana" bırakıldı)
- [ ] Ek e-posta hesapları veya yönlendirme (kayıt@, destek@ vb.) — Natro paket yükseltmesi ya da forwarder özelliği araştırılmalı
- [ ] Eğitmen profil fotoğrafları + gerçek özgeçmişler (**kullanıcıdan gerçek bilgi/fotoğraf gerekiyor**, uydurulamaz)

## 🟢 SONRAKİ AŞAMA (daha büyük işler)
- [ ] Öğrenci kendi bilgilerini güncelleyebilme (profil düzenleme)
- [ ] Veli onay mekanizması (18 yaş altı öğrenciler için)
- [ ] Toplu öğrenci içe aktarma (Excel'den 1000 öğrenci)
- [ ] Toplu e-posta / duyuru gönderme (admin panelinden — e-posta servisi kurulunca)
- [ ] Fatura/makbuz otomatik oluşturma
- [ ] Gelir/muhasebe raporu (admin dashboard'da grafik)
- [ ] Aktivite/denetim kaydı (kim ne zaman değiştirdi)
- [ ] SEO (Google'da bulunabilirlik), sosyal medya paylaşım kartları
- [ ] Google Analytics / ziyaretçi istatistiği
- [ ] Oturum zaman aşımı, 2 adımlı doğrulama (admin için)
- [ ] Site editörü şifresinin panelden değiştirilebilmesi (şu an sabit kodlanmış)

## 🐛 BİLİNEN HATALAR / KONTROL EDİLMESİ GEREKENLER
- [ ] Bir öğrenci kaydında e-posta adresi bozuk görünüyor (`hrahmi@xn--gmailcom-w0a` gibi punycode'a
      dönüşmüş) — muhtemelen kayıt formunda e-posta girilirken bir encoding sorunu. İncelenmeli.
- [ ] Yoğun trafik testi yapılmadı (1000 öğrenci aynı anda giriş yaparsa davranış bilinmiyor)
- [ ] Supabase otomatik yedekleme ayarları kontrol edilmedi

---

## Nasıl kullanılır
Yeni bir sohbette bu dosyayı okuyup devam edebilirsiniz: "istanbul-kesif-okulu deposundaki
YAPILACAKLAR.md dosyasına bak, oradan devam edelim" demeniz yeterli.
