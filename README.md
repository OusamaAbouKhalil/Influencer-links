# OEG Referral Landing Pages

Professional landing pages that auto-detect device type and redirect users to the correct app store (iOS or Android).

## 📁 Structure

```
referral-pages/
├── raphael/
│   └── index.html          # Raphael's referral page
├── template/
│   └── index.html          # Template for new influencers
└── README.md               # This file
```

## 🚀 How to Use

### For Raphael's Campaign

**Landing Page URL:**
```
https://yourwebsite.com/referral-pages/raphael/
```

**What it does:**
1. Auto-detects if user is on iOS or Android
2. Shows branded loading screen
3. Automatically redirects to correct app store after 2 seconds
4. Includes manual download buttons as backup
5. Tracks referral with campaign parameters

**iOS Link:**
```
https://apps.apple.com/app/apple-store/id6444192194?pt=127265717&ct=Raphael&mt=8
```

**Android Link:**
```
https://play.google.com/store/apps/details?id=our.easy.game&referrer=utm_source%3DRaphael%26utm_medium%3Dreferral%26utm_campaign%3DRaphael
```

---

## 🎨 Features

✅ **Auto Device Detection** - Detects iOS, Android, Mac, and other devices  
✅ **Beautiful Design** - Professional gradient design matching OEG branding  
✅ **Automatic Redirect** - Redirects after 2 seconds  
✅ **Manual Fallback** - Backup buttons if auto-redirect fails  
✅ **Mobile Responsive** - Works perfectly on all screen sizes  
✅ **Referral Badge** - Shows who referred the user  
✅ **Feature Highlights** - Displays key app features  
✅ **No Dependencies** - Pure HTML/CSS/JavaScript, no external libraries  
✅ **Fast Loading** - Loads instantly, no delay  

---

## 📊 Tracking

### UTM Parameters (Android)
- **utm_source**: Raphael
- **utm_medium**: referral  
- **utm_campaign**: Raphael

### Campaign Parameters (iOS)
- **ct** (Campaign Token): Raphael
- **pt** (Provider Token): 127265717

### Where to Track:
1. **Firebase Analytics**: Real-time installs and events
2. **Google Play Console**: Android install attribution
3. **App Store Connect**: iOS install attribution
4. **Google Analytics 4**: User behavior

---

## 🔧 Create New Influencer Page

### Method 1: Copy Raphael's Folder
```bash
# Copy the raphael folder
cp -r raphael new-influencer-name

# Edit the HTML file
# Replace "Raphael" with new influencer name in:
# - UTM parameters
# - Campaign parameters  
# - Referral badge text
```

### Method 2: Use Template (Coming next)
```bash
# Copy template folder
cp -r template influencer-name

# Edit index.html
# Update INFLUENCER_NAME variable at top of script
```

---

## 🌐 Deployment Options

### Option 1: Host on Your Website
Upload `referral-pages` folder to your web server:
```
https://yourwebsite.com/referral-pages/raphael/
```

### Option 2: Firebase Hosting (Free)
```bash
cd referral-pages
firebase init hosting
firebase deploy
```
Result: `https://yourapp.web.app/raphael/`

### Option 3: Netlify (Free)
1. Drag and drop `referral-pages` folder to Netlify
2. Get URL: `https://oeg-referrals.netlify.app/raphael/`

### Option 4: GitHub Pages (Free)
1. Push to GitHub repository
2. Enable GitHub Pages
3. URL: `https://yourusername.github.io/oeg-referrals/raphael/`

### Option 5: Vercel (Free)
```bash
npm i -g vercel
cd referral-pages
vercel
```

---

## 📱 Short URL Setup

After deploying, create short URLs with Bitly:

**Long URL:**
```
https://yourwebsite.com/referral-pages/raphael/
```

**Bitly Short URL:**
```
bit.ly/oeg-raphael
```

**Give this to Raphael to share!**

---

## 🎯 Testing

### Test on Different Devices

**Desktop:**
1. Open: `file:///path/to/referral-pages/raphael/index.html`
2. Should redirect to Android (default)

**iPhone/iPad:**
1. Open URL on iOS device
2. Should redirect to App Store

**Android Phone:**
1. Open URL on Android device
2. Should redirect to Google Play Store

### Test with Browser Dev Tools

**Chrome/Edge:**
1. Open page
2. Press F12 → Device Toolbar (Ctrl+Shift+M)
3. Select iPhone or Android device
4. Refresh page
5. Check correct redirect

---

## 🔄 Customization Guide

### Change Colors
Edit the CSS gradient in `index.html`:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Logo
Replace the logo div:
```html
<div class="logo">
    <img src="your-logo.png" alt="OEG Logo">
</div>
```

### Change Redirect Delay
Edit JavaScript timeout (default 2000ms = 2 seconds):
```javascript
setTimeout(() => {
    window.location.href = targetUrl;
}, 2000); // Change this number
```

### Add Google Analytics
Add before closing `</head>` tag:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
  gtag('event', 'referral_page_view', {
    'referrer': 'Raphael'
  });
</script>
```

---

## 📈 Performance

- **Page Size**: ~8KB (tiny!)
- **Load Time**: < 100ms
- **No External Dependencies**: Loads instantly
- **Mobile Optimized**: Works on 2G networks
- **SEO Friendly**: Proper meta tags included

---

## ❓ FAQ

**Q: Can I use custom domain?**  
A: Yes! Deploy to any hosting and use your domain.

**Q: Does this work offline?**  
A: The redirect requires internet, but page loads offline.

**Q: Can I track which influencer performs best?**  
A: Yes! Each influencer has unique UTM parameters tracked in Firebase/Play Console.

**Q: How do I add more influencers?**  
A: Copy the `raphael` folder, rename it, and update the influencer name in the HTML.

**Q: Can I use this with Bitly?**  
A: Yes! Shorten the landing page URL with Bitly for cleaner links.

**Q: Will this work with app deep links?**  
A: This is a web landing page. For app deep links, you need Firebase Dynamic Links or Branch.io.

---

## 🚀 Next Steps

1. ✅ Deploy `referral-pages` to your web hosting
2. ✅ Create short URL with Bitly
3. ✅ Send link to Raphael
4. ✅ Monitor Firebase Analytics for installs
5. ✅ Create more influencer pages using template

---

## 📞 Support

Need help? Check:
- Firebase Analytics: Track installs
- Google Play Console: Android attribution
- App Store Connect: iOS attribution

---

**Created for OEG - Smart Tutor Finder**  
Version 1.0 - November 2025

