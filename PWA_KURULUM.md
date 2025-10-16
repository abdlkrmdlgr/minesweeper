# 📱 PWA Kurulum Rehberi - Minesweeper

## Telefonunuza Uygulama Olarak Yükleme

### 📱 Android (Chrome)
1. Chrome tarayıcıda `minesweeper.html` dosyasını açın
2. Sağ üst köşedeki ⋮ (üç nokta) menüsüne tıklayın
3. **"Ana ekrana ekle"** veya **"Yükle"** seçeneğini seçin
4. Uygulama adını onaylayın
5. ✅ Ana ekranınızda artık uygulama var!

### 🍎 iOS (Safari)
1. Safari'de `minesweeper.html` dosyasını açın
2. Alt kısımda Paylaş butonuna (📤) tıklayın
3. Aşağı kaydırın ve **"Ana Ekrana Ekle"** seçeneğini bulun
4. **"Ekle"** butonuna tıklayın
5. ✅ Ana ekranınızda artık uygulama var!

### 💻 Masaüstü (Chrome/Edge)
1. Tarayıcıda `minesweeper.html` dosyasını açın
2. Adres çubuğunun sağında görünen yükleme ikonuna (⊕) tıklayın
3. **"Yükle"** butonuna tıklayın
4. ✅ Uygulama artık masaüstünüzde!

## 🌐 Web Sunucusunda Yayınlama

PWA'ların tam olarak çalışması için HTTPS gereklidir. İşte bazı ücretsiz seçenekler:

### Hızlı Test (Localhost)
```bash
# Python 3
python3 -m http.server 8000

# Node.js (npx ile)
npx serve .

# Sonra tarayıcıda: http://localhost:8000/minesweeper.html
```

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

## ✨ PWA Özellikleri

✅ **Offline çalışır** - İnternet olmadan oynanabilir  
✅ **Ana ekrana eklenebilir** - Gerçek uygulama gibi  
✅ **Hızlı yüklenir** - Cache sayesinde anında açılır  
✅ **Tam ekran** - Tarayıcı çubuğu olmadan  
✅ **Mobil uyumlu** - Touch kontroller  

## 🔧 Sorun Giderme

**"Ana ekrana ekle" görünmüyor?**
- HTTPS kullanılıyor olmalı (localhost hariç)
- manifest.json ve service-worker.js erişilebilir olmalı

**Offline çalışmıyor?**
- Sayfayı en az bir kez online yükleyin
- Service Worker'ın kayıtlı olduğunu kontrol edin (DevTools > Application)

**Güncellemeler görünmüyor?**
- Tarayıcı cache'ini temizleyin
- Service Worker'ı unregister edip tekrar register edin

## 📝 Notlar

- İlk ziyarette internet gerekir (cache için)
- Sonraki kullanımlarda tamamen offline çalışır
- localStorage ile oyun istatistikleri cihazda saklanır

