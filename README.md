# Carnatic Swara Ear Trainer - PWA

A Progressive Web App for training your ear to recognize Carnatic music swaras.

## 📱 Features

- **3 Difficulty Levels:** Single swara, 2-note sequences, 3-note sequences
- **Custom Swara Selection:** Choose which swaras to practice
- **Volume Control:** Adjust playback volume
- **Score Tracking:** Track your progress with detailed statistics
- **Offline Support:** Works without internet after first visit
- **Installable:** Add to home screen on iOS and Android
- **Mobile Optimized:** Perfect touch interactions and responsive design

## 🚀 Installation Options

### Option 1: Deploy to GitHub Pages (Recommended)

1. **Create a new GitHub repository** (or use existing one)

2. **Upload all files** from this folder to your repository:
   - index.html
   - manifest.json
   - service-worker.js
   - icon-*.png (all icon files)

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Source", select "main" branch
   - Click Save
   - Your app will be available at: `https://[username].github.io/[repo-name]/`

4. **Test the PWA:**
   - Visit the URL on your phone
   - You should see an "Install" prompt
   - Click "Add to Home Screen"

### Option 2: Deploy to Hugging Face Spaces (Static Site)

1. **Create a new Space:**
   - Go to https://huggingface.co/spaces
   - Click "Create new Space"
   - Choose "Static" as the Space SDK
   - Name it (e.g., "swara-trainer")

2. **Upload files:**
   - Upload all files from this folder
   - The app will be available at: `https://[username]-swara-trainer.hf.space`

3. **Configure for PWA:**
   - Make sure all icon files are uploaded
   - Test the manifest.json is accessible

### Option 3: Deploy to Netlify/Vercel

1. **Netlify:**
   - Drag and drop the folder to https://app.netlify.com/drop
   - Your app is instantly live!

2. **Vercel:**
   - Install Vercel CLI: `npm i -g vercel`
   - Run: `vercel` in this folder
   - Follow the prompts

## 📲 Adding to Home Screen

### iOS (iPhone/iPad):
1. Open the app in Safari
2. Tap the Share button (square with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add"
5. The app icon appears on your home screen!

### Android:
1. Open the app in Chrome
2. Tap the three dots menu (⋮)
3. Tap "Add to Home Screen" or "Install app"
4. Tap "Add"
5. The app icon appears on your home screen!

## 🎨 Customizing Icons

The default icons are simple musical note designs. To create custom icons:

1. **Use a design tool:**
   - Figma: https://www.figma.com
   - Canva: https://www.canva.com
   - Adobe Illustrator

2. **Create icons in these sizes:**
   - 72x72, 96x96, 128x128, 144x144, 152x152, 192x192, 384x384, 512x512

3. **Design tips:**
   - Use a simple, recognizable design
   - Bright colors work well (current: orange/red)
   - Make sure it's visible at small sizes
   - Consider adding your app name or logo

4. **Replace the files:**
   - Save as PNG format
   - Name them: icon-72.png, icon-96.png, etc.
   - Replace the existing icon files

5. **Optional: Add maskable icons** for Android
   - These adapt to different device shapes
   - Use https://maskable.app to create them

## 🔧 Customization

### Change App Name:
Edit `manifest.json`:
```json
"name": "Your App Name",
"short_name": "Short Name"
```

### Change Colors:
Edit `manifest.json`:
```json
"theme_color": "#ea580c",
"background_color": "#ffffff"
```

And in `index.html`, update the Tailwind classes for different colors.

### Add More Swaras:
Edit the `SWARAS` array in `index.html`:
```javascript
const SWARAS = [
  { name: 'Sa', fullName: 'Shadja', ratio: 1, frequency: 261.63 },
  // Add more swaras here...
];
```

## 🌐 Adding Download Link to Your Website

Add this HTML to your website:

```html
<a href="https://your-app-url.com" class="download-button">
  📱 Download Swara Trainer App
</a>
```

Or create a QR code:
1. Go to https://www.qr-code-generator.com
2. Enter your app URL
3. Download the QR code
4. Add it to your website: "Scan to install app"

## 📊 Testing Your PWA

Use these tools to test your PWA:

1. **Lighthouse** (in Chrome DevTools):
   - Open DevTools (F12)
   - Go to "Lighthouse" tab
   - Check "Progressive Web App"
   - Click "Generate report"

2. **PWA Builder:**
   - Visit https://www.pwabuilder.com
   - Enter your URL
   - Get a detailed report

## 🔄 Updates

When you update your app:

1. **Change the cache version** in `service-worker.js`:
   ```javascript
   const CACHE_NAME = 'swara-trainer-v2'; // Increment version
   ```

2. **Push changes** to your hosting platform

3. **Users will auto-update** the next time they open the app

## 📁 File Structure

```
swara-ear-trainer-pwa/
├── index.html              # Main app file
├── manifest.json           # PWA configuration
├── service-worker.js       # Offline functionality
├── generate_icons.py       # Icon generator script
├── icon-72.png            # App icons (various sizes)
├── icon-96.png
├── icon-128.png
├── icon-144.png
├── icon-152.png
├── icon-192.png
├── icon-384.png
├── icon-512.png
└── README.md              # This file
```

## 🐛 Troubleshooting

**Problem: App doesn't install**
- Make sure you're using HTTPS (GitHub Pages provides this)
- Check that manifest.json is accessible
- Ensure all icon files exist

**Problem: Audio doesn't play on iOS**
- iOS requires user interaction before playing audio
- The app handles this automatically on first tap

**Problem: Offline mode not working**
- Check if service worker registered successfully
- Look in browser console for errors
- Clear cache and reload

**Problem: Icons not showing**
- Verify all icon files are uploaded
- Check file names match manifest.json
- Use browser DevTools to see which files are missing

## 💡 Future Enhancements (Optional)

Want to add more features? Here are some ideas:

- **Leaderboards:** Track high scores
- **Different Ragas:** Practice different scale patterns
- **Tanpura Drone:** Background drone sound
- **Progress Tracking:** Save progress over time
- **Social Sharing:** Share scores with friends
- **Ads:** Add Google AdSense for monetization

## 📝 License

Free to use and modify for personal or commercial projects.

## 🙏 Credits

Built for Carnatic music learners worldwide.

---

**Questions or need help?** 
- Check the troubleshooting section above
- Test using Chrome DevTools
- Use Lighthouse to identify issues

**Ready to deploy?** Choose one of the deployment options above and your app will be live in minutes! 🎉
