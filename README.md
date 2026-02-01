# Quran Reader with Commentary System

## Files Needed

Your project folder should contain these files:

```
quran-reader/
├── index.html              ← Main website file
├── quran-data.json        ← Complete Quran text (download separately)
└── commentary.json        ← Your commentary/notes (provided)
```

---

## Quick Setup Guide

### Step 1: Get the Quran Data
Download the Quran JSON file from:
```
https://api.alquran.cloud/v1/quran/quran-uthmani
```
Save it as `quran-data.json` in your project folder.

### Step 2: Upload to GitHub
1. Create a new GitHub repository
2. Upload all 3 files:
   - `index.html`
   - `quran-data.json` 
   - `commentary.json`

### Step 3: Deploy to Vercel
1. Go to vercel.com and sign in with GitHub
2. Click "New Project"
3. Import your repository
4. Click "Deploy"
5. Done! Your site is live

---

## Features

### 💡 Commentary System (Teacher Notes)
- **Light blue background** for ayahs with commentary
- **Lightbulb icon (💡)** to indicate commentary
- **Beautiful gradient popup** to display commentary
- Everyone sees these notes

### ⭐ Personal Notes System
- **Gold star (★)** for personal notes
- **Yellow highlight** on double-click
- **Private notes** saved in browser
- Only you see these

### 🔍 Search & Navigation
- Search surahs in sidebar
- Click any surah to jump to it
- Smooth scrolling

---

## How to Add Commentary

### Format: `commentary.json`

The format is simple JSON:
```json
{
  "SURAH-AYAH": "Your commentary text in Arabic or English",
  "1-1": "تفسير الآية الأولى...",
  "2-255": "شرح آية الكرسي..."
}
```

### Key Format Rules:
- **Key**: `"SURAH_NUMBER-AYAH_NUMBER"`
- **Value**: Your commentary text
- Use quotes around both key and value
- Separate entries with commas
- Arabic or English text works

### Examples:

```json
{
  "1-1": "البسملة - بسم الله الرحمن الرحيم",
  "1-2": "الحمد لله رب العالمين - الثناء على الله",
  "2-255": "آية الكرسي - أعظم آية في القرآن",
  "36-1": "يس - من الحروف المقطعة",
  "67-1": "تبارك الذي بيده الملك - سورة الملك"
}
```

### Adding Your Notes:

1. **Option A: Edit commentary.json directly**
   - Open `commentary.json` in a text editor
   - Add your entries following the format above
   - Save the file
   - Push to GitHub (Vercel auto-deploys)

2. **Option B: Use JSON formatter**
   - Go to jsonformatter.org
   - Paste your JSON
   - Add new entries
   - Validate to check for errors
   - Copy and save

---

## How to Add Additional Notes Files

You mentioned you'll have more notes in different JSON files. Here's how to integrate them:

### Method 1: Merge JSON Files
Combine all your JSON files into one `commentary.json`:

```json
{
  "1-1": "Note from file 1",
  "1-2": "Note from file 2",
  "2-1": "Note from file 3"
}
```

### Method 2: Load Multiple Files (Requires code update)
If you want separate files like:
- `tafsir.json`
- `linguistic-notes.json`
- `historical-context.json`

Let me know and I'll update the code to load multiple commentary sources.

---

## Usage Instructions

### For Visitors:
1. **View Commentary**: Click the 💡 lightbulb icon
2. **Add Personal Notes**: Right-click any verse
3. **Highlight Text**: Double-click any verse
4. **Navigate**: Click surahs in left sidebar or use search

### For You (Admin):
1. Edit `commentary.json` to add/update commentary
2. Push changes to GitHub
3. Vercel automatically redeploys (30 seconds)
4. Changes are live!

---

## Visual Indicators

| Icon | Meaning | Who Sees It |
|------|---------|-------------|
| 💡 Light blue background | Has commentary | Everyone |
| ⭐ Gold star | Has personal note | Only you |
| 🟡 Yellow highlight | Highlighted by user | Only you |

---

## Common Questions

**Q: Can I have both commentary and personal notes on the same ayah?**
A: Yes! Both icons will appear - lightbulb AND star.

**Q: How do I remove commentary?**
A: Delete the entry from `commentary.json` and push to GitHub.

**Q: Can I use English in commentary?**
A: Yes! The system supports both Arabic and English (or any language).

**Q: What if I have thousands of commentary entries?**
A: No problem! The JSON file can handle it. Just keep it well-formatted.

**Q: How do I share my commentary with others?**
A: Just share your website URL - everyone who visits will see your commentary.

---

## File Size Considerations

- `quran-data.json`: ~4.7 MB (one-time download)
- `commentary.json`: Depends on how much you write
  - 100 notes ≈ 50 KB
  - 1000 notes ≈ 500 KB
- Both are perfectly fine for web hosting

---

## Next Steps

1. ✅ Upload files to GitHub
2. ✅ Deploy to Vercel  
3. ✅ Test the website
4. 📝 **Send me your additional notes** - I'll help you format and integrate them
5. 🎨 Optional: Customize colors, fonts, styling

---

## Need Help?

When you're ready to add your additional commentary files, just share them with me and I'll:
1. Format them correctly
2. Merge them into `commentary.json` OR
3. Update the code to load multiple files

Let me know what format your notes are in:
- Plain text?
- Excel/CSV?
- Word document?
- Another JSON?
- Database?

I'll help you convert them to the right format!
