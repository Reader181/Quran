# Simple Quran Reader - Arabic & English

A clean, minimal Quran reader displaying Arabic text with English translations.

## Files

```
quran-reader/
├── quran-simple.html       ← Main website file
└── quran-english.json      ← Complete Quran with translations
```

## Features

✅ **Arabic Text** - Beautiful Quranic Arabic in Scheherazade font  
✅ **English Translation** - Clear English translation under each verse  
✅ **All 114 Surahs** - Complete Quran  
✅ **Search** - Search for any Surah by name  
✅ **Clean Design** - No distractions, just the Quran  
✅ **Responsive** - Works on desktop and mobile  
✅ **Offline** - Works without internet after initial load  

## What's Removed

❌ No commentary system  
❌ No personal notes  
❌ No highlighting  
❌ No complex features  

## Setup

### Option 1: Local Use
1. Keep both files in the same folder
2. Open `quran-simple.html` in your browser
3. Done!

### Option 2: Deploy Online (GitHub + Vercel)

1. **Upload to GitHub:**
   - Create a new repository
   - Upload `quran-simple.html` and `quran-english.json`
   - Rename `quran-simple.html` to `index.html`

2. **Deploy to Vercel:**
   - Go to vercel.com
   - Import your repository
   - Click Deploy
   - Your site is live!

## File Structure

### quran-english.json

```json
[
  {
    "id": 1,
    "name": "الفاتحة",
    "transliteration": "Al-Fatihah",
    "translation": "The Opener",
    "type": "meccan",
    "total_verses": 7,
    "verses": [
      {
        "id": 1,
        "text": "بِسۡمِ ٱللَّهِ ٱلرَّحۡمَٰنِ ٱلرَّحِيمِ",
        "translation": "In the name of Allah, the Entirely Merciful, the Especially Merciful"
      }
    ]
  }
]
```

## Usage

- Click any Surah in the sidebar to view it
- Search for Surahs using the search box
- Scroll to read verses with translations
- That's it! Simple and clean.

## Customization

Want to customize the colors or fonts? Edit the CSS in `quran-simple.html`:

```css
:root {
    --bg-primary: #f8f6f1;        /* Background color */
    --accent-emerald: #3d6b5a;     /* Primary color */
    --accent-gold: #d4af37;        /* Accent color */
}
```

## File Sizes

- `quran-simple.html`: ~12 KB
- `quran-english.json`: ~1.8 MB
- Total: ~1.81 MB

Both files are optimized and load quickly!

## Browser Support

Works on all modern browsers:
- Chrome ✅
- Firefox ✅
- Safari ✅
- Edge ✅
- Mobile browsers ✅

## Credits

- Quran text and translation from Sahih International
- Fonts: Google Fonts (Amiri, Scheherazade New, Cairo)
- Design: Clean and minimal for focused reading

---

Enjoy reading the Quran! 📖
