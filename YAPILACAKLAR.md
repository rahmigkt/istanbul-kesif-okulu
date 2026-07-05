# İstanbul Keşif Okulu — Yapılacaklar Listesi

Bu dosya, projenin canlı, kalıcı yapılacaklar listesidir. Her oturumda güncellenir.
Son güncelleme: 2026-07-05

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
- [x] Site-içi bildirim sistemi (kayıt, mazeret gönderimi, mazeret onay/red)
- [x] Admin: öğrenci arama/filtreleme, dondurma, silme, CSV dışa aktarma
- [x] Admin: yeni eğitmen/yönetici hesabı oluşturma ekranı

---

## 🔴 RESMİ İŞLEM GEREKTİRENLER (şimdilik bekletiliyor — kullanıcı talebiyle)
Bunlar bir kurum/hesap/sözleşme gerektirdiği için öncelik dışı bırakıldı:
- [ ] Gerçek ödeme tahsilatı (iyzico / PayTR / Stripe sözleşmesi + entegrasyon)
- [ ] KVKK VERBİS kaydı (resmi devlet kaydı — hukuki danışmanlık önerilir)
- [ ] Şirket/vakıf resmi vergi & fatura entegrasyonu

## 🟡 SIRADAKI ÖNCELİKLER (üzerinde çalışılıyor / önerilen sıra)
- [ ] **E-posta bildirimleri** — şu an sadece site-içi bildirim var, gerçek e-posta göndermek için
      bir e-posta servisi (Resend/SendGrid) hesabı + API anahtarı gerekiyor (Supabase/Netlify/GitHub gibi ücretsiz kurulabilir)
- [ ] KVKK aydınlatma metni + açık rıza onay kutusu (kayıt formunda — resmi kayıt değil, sadece metin/onay kutusu)
- [ ] Kullanım Şartları / Gizlilik Politikası sayfası (metin olarak, hukuki danışmanlık olmadan taslak)
- [ ] Şifremi unuttum / şifre sıfırlama akışı
- [ ] İletişim formu / telefon / WhatsApp hattı (footer'a)
- [ ] SSS (Sıkça Sorulan Sorular) bölümü
- [ ] Eğitmen profil fotoğrafları + gerçek özgeçmişler

## 🟢 SONRAKİ AŞAMA (daha büyük işler)
- [ ] Öğrenci kendi bilgilerini güncelleyebilme (profil düzenleme)
- [ ] Veli onay mekanizması (18 yaş altı öğrenciler için)
- [ ] Toplu öğrenci içe aktarma (Excel'den 1000 öğrenci)
- [ ] Toplu e-posta / duyuru gönderme (admin panelinden)
- [ ] Fatura/makbuz otomatik oluşturma
- [ ] Gelir/muhasebe raporu (admin dashboard'da grafik)
- [ ] Aktivite/denetim kaydı (kim ne zaman değiştirdi)
- [ ] SEO (Google'da bulunabilirlik), sosyal medya paylaşım kartları
- [ ] Google Analytics / ziyaretçi istatistiği
- [ ] Oturum zaman aşımı, 2 adımlı doğrulama (admin için)
- [ ] Site editörü şifresinin panelden değiştirilebilmesi (şu an sabit kodlanmış)
- [ ] Eğitmenin kendi şifresini değiştirmesi

## 🐛 BİLİNEN HATALAR / KONTROL EDİLMESİ GEREKENLER
- [ ] Bir öğrenci kaydında e-posta adresi bozuk görünüyor (`hrahmi@xn--gmailcom-w0a` gibi punycode'a
      dönüşmüş) — muhtemelen kayıt formunda e-posta girilirken bir encoding sorunu. İncelenmeli.
- [ ] Yoğun trafik testi yapılmadı (1000 öğrenci aynı anda giriş yaparsa davranış bilinmiyor)
- [ ] Supabase otomatik yedekleme ayarları kontrol edilmedi

---

## Nasıl kullanılır
Yeni bir sohbette bu dosyayı okuyup devam edebilirsiniz: "istanbul-kesif-okulu deposundaki
YAPILACAKLAR.md dosyasına bak, oradan devam edelim" demeniz yeterli.
