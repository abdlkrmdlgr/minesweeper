# 💣 Minesweeper - Classic Mine Sweeper Game

A modern Progressive Web App (PWA) implementation of the classic Minesweeper game, built with web technologies. Works perfectly on both desktop and mobile devices.

## ✨ Features

### 🎮 Game Features
- **Classic Minesweeper experience** - All original game rules
- **3 difficulty levels** - Easy (10%), Medium (15%), Hard (25%)
- **Custom dimensions** - Customizable from 5x5 to 30x30
- **Advanced statistics** - 3BV, efficiency, experience points
- **Estimated time** - Pre-calculated time estimation
- **Explosion effects** - Visual and audio effects
- **Haptic feedback** - Vibration support on compatible devices

### 📱 PWA Features
- **Works offline** - Play without internet connection
- **Installable** - Add to home screen like a real app
- **Fast loading** - Instant opening thanks to caching
- **Full screen** - No browser bars
- **Mobile optimized** - Touch controls

### 🎯 Controls
- **Single Click/Tap:** Reveal cell
- **Double Click/Tap:** Closed cell → Flag/unflag | Open cell → Reveal surroundings
- **Right Click:** Flag/unflag (PC)
- **Long Press (0.2s):** Flag/unflag (Mobile)
- **Adjustable tap delay** - Optimized for mobile experience

## 🚀 Installation and Setup

### Local Development
```bash
# Clone the project
git clone <repository-url>
cd minesweeper

# Start a simple HTTP server
# Python 3
python3 -m http.server 8000

# Node.js (with npx)
npx serve .

# Open in browser: http://localhost:8000/minesweeper.html
```

### Install as PWA

#### 📱 Android (Chrome)
1. Open `minesweeper.html` in Chrome browser
2. Tap the ⋮ (three dots) menu in the top right
3. Select **"Add to Home screen"** or **"Install"**
4. Confirm the app name
5. ✅ App is now on your home screen!

#### 🍎 iOS (Safari)
1. Open `minesweeper.html` in Safari
2. Tap the Share button (📤) at the bottom
3. Scroll down and find **"Add to Home Screen"**
4. Tap **"Add"**
5. ✅ App is now on your home screen!

#### 💻 Desktop (Chrome/Edge)
1. Open `minesweeper.html` in browser
2. Click the install icon (⊕) in the address bar
3. Click **"Install"**
4. ✅ App is now on your desktop!

## 🌐 Deploy to Web Server

PWAs require HTTPS to work properly. Here are some free options:

### Free Hosting Options

1. **GitHub Pages** (Recommended)
   - Upload repo to GitHub
   - Settings > Pages > Deploy from main branch
   - Automatic HTTPS

2. **Netlify**
   - Drag and drop folder to Netlify
   - Automatic HTTPS

3. **Vercel**
   - Deploy with `vercel` command
   - Automatic HTTPS

4. **Cloudflare Pages**
   - Auto-deploy from GitHub
   - Free and fast

## 🎮 How to Play

### Basic Rules
- **Goal:** Win by flagging all mines or revealing all safe cells
- **Numbers:** Show the count of adjacent mines
- **Hint:** Your first click will never be a mine

### Controls
- **Single Click/Tap:** Reveal cell
- **Double Click/Tap:** 
  - Closed cell → Flag/unflag
  - Open cell → Reveal surroundings (Chord operation)
- **Right Click:** Flag/unflag (PC)
- **Long Press (0.2s):** Flag/unflag (Mobile)

### Difficulty Levels
- **Easy:** 10x10, 10 mines (10%)
- **Medium:** 10x10, 15 mines (15%)
- **Hard:** 10x10, 25 mines (25%)
- **Custom:** Customizable from 5x5 to 30x30

## 📊 Statistics and Analysis

### Basic Statistics
- Games played
- Games won
- Games lost
- Win rate
- Best time

### Advanced Statistics (3BV System)
- **3BV (Board Benchmark Value):** Minimum clicks required to solve the board
- **3BV/s:** 3BV per second (speed indicator)
- **Efficiency:** 3BV / Total Left Clicks ratio
- **Experience:** Stars earned based on performance
- **Estimated time:** Pre-calculated time estimation

## 🔧 Technical Details

### Technologies Used
- **HTML5** - Semantic markup
- **CSS3** - Modern styling, animations, responsive design
- **Vanilla JavaScript** - Framework-free, performant
- **PWA** - Service Worker, Web App Manifest
- **LocalStorage** - Offline data persistence

### File Structure
```
minesweeper/
├── minesweeper.html      # Main game file
├── manifest.json         # PWA manifest
├── service-worker.js     # Service Worker (PWA)
├── explosion.mp3         # Explosion sound effect
└── README.md            # This file
```

### Features
- **Responsive Design** - Mobile and desktop compatible
- **Touch Optimized** - Mobile touch controls
- **Offline First** - Works without internet
- **Performance** - Fast loading and execution
- **Accessibility** - Accessible design

## 🎨 Customization

### Audio Settings
- Toggle explosion sound on/off
- Sound volume adjustment

### Mobile Controls
- Tap delay setting (50-300ms)
- Long press duration (200ms)
- Haptic feedback (iPhone)

### Visual Settings
- Classic Windows 95 style interface
- Animated explosion effects
- Responsive cell sizes

## 🐛 Troubleshooting

### PWA Issues
**"Add to Home Screen" not showing?**
- Must use HTTPS (except localhost)
- manifest.json and service-worker.js must be accessible

**Not working offline?**
- Load the page online at least once
- Check Service Worker is registered (DevTools > Application)

**Updates not showing?**
- Clear browser cache
- Unregister and re-register Service Worker

### Game Issues
**Double tap not working on mobile?**
- Increase tap delay setting (Settings > Mobile Controls)
- Reduce long press duration

**Sound not playing?**
- Check browser audio settings
- Ensure sound file is loaded

## 📝 License

This project is open source and developed for educational purposes.

## 👨‍💻 Developer

**Abdülkerim DÜLGER**
- LinkedIn: [abdlkrmdlgr](https://linkedin.com/in/abdulkerimdulger)
- Website: [girisim.dev](https://girisim.dev)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📈 Future Plans

- [ ] Multiplayer mode
- [ ] Different themes
- [ ] More statistics
- [ ] Social sharing
- [ ] Achievement system
- [ ] Daily challenges

---

**Note:** This game works completely offline and does not collect personal data. All statistics are stored locally on your device.
