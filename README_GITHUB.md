# 📱 OEG Referral Pages

Professional, auto-detecting landing pages for influencer marketing campaigns. Automatically redirects users to the correct app store (iOS or Android) with full UTM tracking.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-production-success.svg)]()

## 🌟 Features

- ✅ **Auto Device Detection** - Detects iOS, Android, Mac, and redirects accordingly
- ✅ **Beautiful Design** - Professional gradient design with OEG branding
- ✅ **Automatic Redirect** - Smart redirect after logo loads (3.5 seconds)
- ✅ **UTM Tracking** - Full campaign attribution for analytics
- ✅ **Mobile Responsive** - Perfect on all screen sizes
- ✅ **No Dependencies** - Pure HTML/CSS/JavaScript
- ✅ **Fast Loading** - Optimized with image preloading
- ✅ **Easy Setup** - Create new influencer pages in 2 minutes

## 🎯 Live Demo

**Raphael's Campaign:**
- Landing Page: [View Demo](https://your-domain.com/raphael/)
- Tracks clicks, installs, and conversions

## 📦 What's Included

```
referral-pages/
├── raphael/              # Example influencer page
│   ├── index.html
│   └── logo.png
├── template/             # Template for new influencers
│   ├── index.html
│   └── logo.png
├── index.html            # Dashboard to manage all campaigns
├── logo.png              # OEG logo
├── README.md             # Full documentation
├── SETUP_NEW_INFLUENCER.md  # Quick setup guide
└── .gitignore
```

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/oeg-referral-pages.git
cd oeg-referral-pages
```

### 2. Create New Influencer Page

```bash
# Copy the template
cp -r template john

# Edit the configuration
# Open john/index.html and change line ~293:
const INFLUENCER_NAME = "John"; // Change this!
```

### 3. Deploy

Upload to any web hosting:
- **Netlify**: Drag & drop folder
- **Vercel**: `vercel deploy`
- **GitHub Pages**: Push to repo and enable Pages
- **Firebase**: `firebase deploy`

### 4. Create Short URL

Use [Bitly](https://bitly.com) to create short links:
```
Long:  https://yoursite.com/john/
Short: bit.ly/oeg-john
```

## 📊 Tracking & Analytics

Each referral page tracks users through:

### UTM Parameters (Android)
```
utm_source=InfluencerName
utm_medium=referral
utm_campaign=InfluencerName
```

### Campaign Parameters (iOS)
```
ct=InfluencerName
pt=127265717
```

### View Data In:
1. **Firebase Analytics** - Real-time installs & events
2. **Google Play Console** - Android attribution
3. **App Store Connect** - iOS attribution  
4. **Bitly Analytics** - Click tracking

## 🎨 Customization

### Change Colors

Edit the CSS gradient in any `index.html`:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Redirect Delay

Edit the JavaScript timeout:

```javascript
redirectTimer = setTimeout(() => {
    window.location.href = targetUrl;
}, 3500); // Change this number (milliseconds)
```

### Use Different Logo

Replace `logo.png` in each folder with your logo (120x120px recommended)

## 📖 Full Documentation

- **[Complete Setup Guide](SETUP_NEW_INFLUENCER.md)** - Step-by-step instructions
- **[Main README](README.md)** - Detailed documentation with all features

## 🌐 Deployment Options

### Option 1: Netlify (Easiest)
1. Go to [netlify.com](https://netlify.com)
2. Drag & drop `referral-pages` folder
3. Get instant URL: `https://oeg-referrals.netlify.app`

### Option 2: GitHub Pages (Free)
1. Push this repo to GitHub
2. Settings → Pages → Enable
3. URL: `https://username.github.io/oeg-referral-pages`

### Option 3: Vercel
```bash
npm i -g vercel
vercel
```

### Option 4: Firebase Hosting
```bash
firebase init hosting
firebase deploy
```

## 📱 App Links

**Android (Google Play):**
```
https://play.google.com/store/apps/details?id=our.easy.game
```

**iOS (App Store):**
```
https://apps.apple.com/app/id6444192194
```

## 🎯 Use Cases

- **Influencer Marketing** - Track each influencer's performance
- **Affiliate Programs** - Attribute signups to affiliates
- **Social Campaigns** - Different links for Instagram, TikTok, etc.
- **Email Marketing** - Track which email campaigns convert
- **QR Codes** - Offline marketing with trackable links

## 📈 Performance

- **Page Size**: 8-12KB (tiny!)
- **Load Time**: < 100ms
- **Mobile Optimized**: Works on 2G networks
- **SEO Friendly**: Proper meta tags included

## 🔧 Tech Stack

- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Styling**: CSS Grid, Flexbox, CSS Animations
- **Detection**: User-Agent based device detection
- **Icons**: Inline SVG (App Store, Play Store logos)
- **Optimization**: Image preloading, smart redirect logic

## 📋 Browser Support

- ✅ Chrome/Edge (Latest)
- ✅ Safari (iOS 12+)
- ✅ Firefox (Latest)
- ✅ Samsung Internet
- ✅ Opera

## 🤝 Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 📄 License

MIT License - feel free to use for your own projects!

## 🙏 Credits

Created for **OEG - Smart Tutor Finder**

## 📞 Support

Questions? Check:
- [Setup Guide](SETUP_NEW_INFLUENCER.md)
- [Full README](README.md)
- [Open an Issue](https://github.com/YOUR_USERNAME/oeg-referral-pages/issues)

---

**⭐ Star this repo if you find it useful!**

Made with ❤️ for influencer marketing

