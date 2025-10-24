# 💣 Minesweeper - Klasik Mayın Tarlası

Modern web teknolojileri ile geliştirilmiş, PWA (Progressive Web App) destekli klasik Mayın Tarlası oyunu. Hem masaüstü hem de mobil cihazlarda mükemmel çalışır.

## ✨ Özellikler

### 🎮 Oyun Özellikleri
- **Klasik Minesweeper deneyimi** - Orijinal oyunun tüm kuralları
- **3 zorluk seviyesi** - Kolay (%10), Orta (%15), Zor (%25)
- **Özel boyutlar** - 5x5'ten 30x30'a kadar özelleştirilebilir
- **Gelişmiş istatistikler** - 3BV, verimlilik, deneyim puanları
- **Tahmini süre** - Oyun başında hesaplanan süre tahmini
- **Patlama efektleri** - Görsel ve ses efektleri
- **Haptic feedback** - Uzun basma sırasında titreşim (destekleyen cihazlarda)

### 📱 PWA Özellikleri
- **Offline çalışır** - İnternet olmadan oynanabilir
- **Ana ekrana eklenebilir** - Gerçek uygulama gibi
- **Hızlı yüklenir** - Cache sayesinde anında açılır
- **Tam ekran** - Tarayıcı çubuğu olmadan
- **Mobil uyumlu** - Touch kontroller

### 🎯 Kontroller
- **Tek Tık/Tap:** Hücreyi aç
- **Çift Tık/Tap:** Kapalı hücrede → Bayrak koy/kaldır | Açık hücrede → Etrafı aç
- **Sağ Tık:** Bayrak koy/kaldır (PC)
- **Uzun Bas (0.2s):** Bayrak koy/kaldır (Mobil)
- **Ayarlanabilir tap gecikmesi** - Mobil deneyim için optimize edilmiş

## 🚀 Kurulum ve Çalıştırma

### Yerel Geliştirme
```bash
# Projeyi klonlayın
git clone <repository-url>
cd minesweeper

# Basit HTTP sunucusu başlatın
# Python 3
python3 -m http.server 8000

# Node.js (npx ile)
npx serve .

# Tarayıcıda açın: http://localhost:8000/minesweeper.html
```

### PWA Olarak Yükleme

#### 📱 Android (Chrome)
1. Chrome tarayıcıda `minesweeper.html` dosyasını açın
2. Sağ üst köşedeki ⋮ (üç nokta) menüsüne tıklayın
3. **"Ana ekrana ekle"** veya **"Yükle"** seçeneğini seçin
4. Uygulama adını onaylayın
5. ✅ Ana ekranınızda artık uygulama var!

#### 🍎 iOS (Safari)
1. Safari'de `minesweeper.html` dosyasını açın
2. Alt kısımda Paylaş butonuna (📤) tıklayın
3. Aşağı kaydırın ve **"Ana Ekrana Ekle"** seçeneğini bulun
4. **"Ekle"** butonuna tıklayın
5. ✅ Ana ekranınızda artık uygulama var!

#### 💻 Masaüstü (Chrome/Edge)
1. Tarayıcıda `minesweeper.html` dosyasını açın
2. Adres çubuğunun sağında görünen yükleme ikonuna (⊕) tıklayın
3. **"Yükle"** butonuna tıklayın
4. ✅ Uygulama artık masaüstünüzde!

## 🌐 Web Sunucusunda Yayınlama

PWA'ların tam olarak çalışması için HTTPS gereklidir. İşte bazı ücretsiz seçenekler:

### Ücretsiz Hosting Seçenekleri

1. **GitHub Pages** (Önerilen)
   - Repoyu GitHub'a yükle
   - Settings > Pages > Deploy from main branch
   - Otomatik HTTPS

2. **Netlify**
   - Klasörü Netlify'a sürükle-bırak
   - Otomatik HTTPS

3. **Vercel**
   - `vercel` komutuyla deploy et
   - Otomatik HTTPS

4. **Cloudflare Pages**
   - GitHub'dan otomatik deploy
   - Ücretsiz ve hızlı

## 🎮 Nasıl Oynanır

### Temel Kurallar
- **Hedef:** Tüm mayınları bayraklayarak veya mayınsız hücreleri açarak kazanın
- **Sayılar:** Etrafındaki mayın sayısını gösterir
- **İpucu:** İlk tıklamanız asla mayın olmaz

### Kontroller
- **Tek Tık/Tap:** Hücreyi aç
- **Çift Tık/Tap:** 
  - Kapalı hücrede → Bayrak koy/kaldır
  - Açık hücrede → Etrafı aç (Chord işlemi)
- **Sağ Tık:** Bayrak koy/kaldır (PC)
- **Uzun Bas (0.2s):** Bayrak koy/kaldır (Mobil)

### Zorluk Seviyeleri
- **Kolay:** 10x10, 10 mayın (%10)
- **Orta:** 10x10, 15 mayın (%15)
- **Zor:** 10x10, 25 mayın (%25)
- **Özel:** 5x5'ten 30x30'a kadar özelleştirilebilir

## 📊 İstatistikler ve Analiz

### Temel İstatistikler
- Oyunlar oynandı
- Kazanılan oyunlar
- Kaybedilen oyunlar
- Kazanma oranı
- En iyi süre

### Gelişmiş İstatistikler (3BV Sistemi)
- **3BV (Board Benchmark Value):** Tahtayı çözmek için gereken minimum tıklama sayısı
- **3BV/s:** Saniyedeki 3BV değeri (hız göstergesi)
- **Verimlilik:** 3BV / Toplam Sol Tıklama oranı
- **Deneyim:** Oyun performansınıza göre kazanılan yıldız sayısı
- **Tahmini süre:** Oyun başında hesaplanan süre tahmini

## 🔧 Teknik Detaylar

### Kullanılan Teknolojiler
- **HTML5** - Semantic markup
- **CSS3** - Modern styling, animations, responsive design
- **Vanilla JavaScript** - Framework-free, performant
- **PWA** - Service Worker, Web App Manifest
- **LocalStorage** - Offline data persistence

### Dosya Yapısı
```
minesweeper/
├── minesweeper.html      # Ana oyun dosyası
├── manifest.json         # PWA manifest
├── service-worker.js     # Service Worker (PWA)
├── explosion.mp3         # Patlama ses efekti
├── PWA_KURULUM.md        # PWA kurulum rehberi
└── README.md            # Bu dosya
```

### Özellikler
- **Responsive Design** - Mobil ve masaüstü uyumlu
- **Touch Optimized** - Mobil dokunma kontrolleri
- **Offline First** - İnternet olmadan çalışır
- **Performance** - Hızlı yükleme ve çalışma
- **Accessibility** - Erişilebilir tasarım

## 🎨 Özelleştirme

### Ses Ayarları
- Patlama sesi açma/kapama
- Ses seviyesi ayarı

### Mobil Kontroller
- Tap gecikmesi ayarı (50-300ms)
- Uzun basma süresi (200ms)
- Haptic feedback (iPhone)

### Görsel Ayarlar
- Klasik Windows 95 tarzı arayüz
- Animasyonlu patlama efektleri
- Responsive hücre boyutları

## 🐛 Sorun Giderme

### PWA Sorunları
**"Ana ekrana ekle" görünmüyor?**
- HTTPS kullanılıyor olmalı (localhost hariç)
- manifest.json ve service-worker.js erişilebilir olmalı

**Offline çalışmıyor?**
- Sayfayı en az bir kez online yükleyin
- Service Worker'ın kayıtlı olduğunu kontrol edin (DevTools > Application)

**Güncellemeler görünmüyor?**
- Tarayıcı cache'ini temizleyin
- Service Worker'ı unregister edip tekrar register edin

### Oyun Sorunları
**Mobilde çift tık çalışmıyor?**
- Tap gecikmesi ayarını artırın (Settings > Mobil Kontroller)
- Uzun basma süresini azaltın

**Ses çalmıyor?**
- Tarayıcı ses ayarlarını kontrol edin
- Ses dosyasının yüklendiğinden emin olun

## 📝 Lisans

Bu proje açık kaynak kodludur ve eğitim amaçlı geliştirilmiştir.

## 👨‍💻 Geliştirici

**Abdülkerim DÜLGER**
- LinkedIn: [abdlkrmdlgr](https://linkedin.com/in/abdulkerimdulger)
- Website: [girisim.dev](https://girisim.dev)

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Commit yapın (`git commit -m 'Add amazing feature'`)
4. Push yapın (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## 📈 Gelecek Planları

- [ ] Multiplayer modu
- [ ] Farklı temalar
- [ ] Daha fazla istatistik
- [ ] Sosyal paylaşım
- [ ] Başarı sistemi
- [ ] Günlük görevler

---

**Not:** Bu oyun tamamen offline çalışır ve kişisel verilerinizi toplamaz. Tüm istatistikler cihazınızda saklanır.
