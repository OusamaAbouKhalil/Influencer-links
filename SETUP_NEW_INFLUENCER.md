# 🚀 Quick Setup Guide - New Influencer Page

Follow these steps to create a referral page for a new influencer.

---

## Method 1: Copy & Edit (Easiest - 2 minutes)

### Step 1: Copy the Template Folder
```bash
# Windows PowerShell
Copy-Item -Recurse referral-pages\template referral-pages\NEW_INFLUENCER_NAME

# Mac/Linux
cp -r referral-pages/template referral-pages/NEW_INFLUENCER_NAME
```

**Note:** The OEG logo (`logo.png`) is already included in the template and will be copied automatically!

### Step 2: Edit the Configuration
Open `referral-pages/NEW_INFLUENCER_NAME/index.html`

Find this section at the top of the `<script>` tag:

```javascript
// 🔧 CONFIGURATION - EDIT THIS SECTION
const INFLUENCER_NAME = "INFLUENCER_NAME"; // Change this!
const PROVIDER_TOKEN = "127265717";         // Your iOS Provider Token
const IOS_APP_ID = "6444192194";            // Your iOS App Store ID
const ANDROID_PACKAGE = "our.easy.game";     // Your Android package name
```

**Change only the first line:**
```javascript
const INFLUENCER_NAME = "Sarah"; // Replace with actual name
```

**Save the file!**

### Step 3: Test Locally
Open the file in your browser:
```
file:///path/to/referral-pages/NEW_INFLUENCER_NAME/index.html
```

You should see:
- "Referred by Sarah" badge
- Auto-redirect after 2 seconds
- Correct app store buttons

### Step 4: Deploy
Upload the folder to your web hosting or use one of these free options:

**Option A: Netlify (Drag & Drop)**
1. Go to https://netlify.com
2. Drag the `NEW_INFLUENCER_NAME` folder
3. Get URL: `https://yoursite.netlify.app/`

**Option B: GitHub Pages**
1. Push to GitHub repository
2. Enable GitHub Pages in Settings
3. URL: `https://username.github.io/oeg-referrals/NEW_INFLUENCER_NAME/`

**Option C: Firebase Hosting**
```bash
cd referral-pages/NEW_INFLUENCER_NAME
firebase init hosting
firebase deploy
```

### Step 5: Create Short URL
1. Go to https://bitly.com
2. Paste your deployed URL
3. Create custom short link: `bit.ly/oeg-sarah`
4. Give this to your influencer!

---

## Method 2: One-Line Command (Advanced)

Create a new influencer page with one command:

### Windows PowerShell:
```powershell
$influencer = "Sarah"
Copy-Item -Recurse referral-pages\template "referral-pages\$influencer"
(Get-Content "referral-pages\$influencer\index.html") -replace 'INFLUENCER_NAME', $influencer | Set-Content "referral-pages\$influencer\index.html"
```

### Mac/Linux/Git Bash:
```bash
INFLUENCER="Sarah"
cp -r referral-pages/template "referral-pages/$INFLUENCER"
sed -i "s/INFLUENCER_NAME/$INFLUENCER/g" "referral-pages/$INFLUENCER/index.html"
```

Then just deploy!

---

## 📋 Example: Creating Page for "Mike"

### Step by Step:

1. **Copy template:**
   ```bash
   cp -r referral-pages/template referral-pages/mike
   ```

2. **Edit `referral-pages/mike/index.html`:**
   ```javascript
   const INFLUENCER_NAME = "Mike"; // Changed!
   ```

3. **Test locally:**
   - Open: `referral-pages/mike/index.html`
   - Should show: "Referred by Mike"
   - URLs should contain: `ct=Mike` (iOS) and `utm_source=Mike` (Android)

4. **Deploy to web hosting**

5. **Create short URL:**
   - Long: `https://yoursite.com/referral-pages/mike/`
   - Short: `bit.ly/oeg-mike`

6. **Give to Mike:**
   ```
   Hey Mike! Your tracking link: bit.ly/oeg-mike
   ```

---

## 🎨 Advanced Customization (Optional)

### Change Colors
Edit these CSS gradients:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Redirect Delay
Edit JavaScript timeout:
```javascript
setTimeout(() => {
    window.location.href = targetUrl;
}, 2000); // Change to 3000 for 3 seconds
```

### Add Custom Message for Specific Influencer
After the referral badge:
```html
<div class="referral-badge">
    🎉 <span id="referrerName">Referred by Mike</span>
</div>
<p style="color: #667eea; font-weight: 600; margin-bottom: 20px;">
    Get 10% off with code MIKE10!
</p>
```

### Add Logo Image
Replace the logo div:
```html
<div class="logo">
    <img src="oeg-logo.png" alt="OEG" style="width: 100%; height: 100%; border-radius: 24px;">
</div>
```

---

## ✅ Quick Checklist

For each new influencer:

- [ ] Copy template folder
- [ ] Rename folder to influencer name
- [ ] Edit `INFLUENCER_NAME` in index.html
- [ ] Test locally (open in browser)
- [ ] Verify "Referred by [NAME]" shows correctly
- [ ] Deploy to web hosting
- [ ] Create Bitly short URL
- [ ] Test on mobile device (iOS & Android)
- [ ] Give short URL to influencer
- [ ] Add to tracking spreadsheet

---

## 📊 Tracking Multiple Influencers

Create a simple spreadsheet:

| Influencer | Short URL | iOS Installs | Android Installs | Total |
|------------|-----------|--------------|------------------|-------|
| Raphael    | bit.ly/oeg-raphael | 45 | 78 | 123 |
| Sarah      | bit.ly/oeg-sarah   | 32 | 54 | 86  |
| Mike       | bit.ly/oeg-mike    | 28 | 41 | 69  |

**Update weekly from:**
- Firebase Analytics (real-time)
- Google Play Console (Android)
- App Store Connect (iOS)

---

## 🔍 Troubleshooting

### Issue: Referral name not showing
**Solution:** Make sure you saved the HTML file after editing

### Issue: Links don't work
**Solution:** Check that INFLUENCER_NAME doesn't have special characters. Use alphanumeric only.

### Issue: Can't track in Firebase
**Solution:** Wait 24-48 hours for data to appear. Check UTM parameters are correct.

### Issue: Page not loading
**Solution:** Check HTML syntax is valid. Use: https://validator.w3.org/

---

## 🎯 Mass Create Multiple Influencers

If you have many influencers, use this script:

### Windows PowerShell:
```powershell
$influencers = @("Sarah", "Mike", "John", "Emma", "David")

foreach ($name in $influencers) {
    Copy-Item -Recurse referral-pages\template "referral-pages\$name"
    (Get-Content "referral-pages\$name\index.html") -replace 'INFLUENCER_NAME', $name | Set-Content "referral-pages\$name\index.html"
    Write-Host "✅ Created page for $name"
}

Write-Host "`n🎉 All pages created! Deploy them now."
```

### Mac/Linux:
```bash
#!/bin/bash
influencers=("Sarah" "Mike" "John" "Emma" "David")

for name in "${influencers[@]}"; do
    cp -r referral-pages/template "referral-pages/$name"
    sed -i "s/INFLUENCER_NAME/$name/g" "referral-pages/$name/index.html"
    echo "✅ Created page for $name"
done

echo "🎉 All pages created! Deploy them now."
```

---

## 📱 QR Code Generation (Bonus)

Create QR codes for offline marketing:

1. Go to: https://qr-code-generator.com
2. Enter your short URL: `bit.ly/oeg-raphael`
3. Download QR code
4. Give to influencer for Instagram stories, flyers, etc.

---

## 🚀 Next Steps

After creating pages for all influencers:

1. ✅ Deploy all pages
2. ✅ Create short URLs for each
3. ✅ Test on multiple devices
4. ✅ Send links to influencers
5. ✅ Monitor Firebase Analytics
6. ✅ Compare performance
7. ✅ Reward top performers

---

**Questions?** Check the main README.md or Firebase Analytics dashboard!

**Happy tracking! 🎉**

