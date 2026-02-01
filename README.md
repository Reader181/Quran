# Quran Reader - Setup Instructions

## How to Get the Quran JSON Data

You have several options to get the complete Quran text in JSON format:

### Option 1: Download from API (Recommended)
Visit this URL in your browser and save the file as `quran-data.json`:
```
https://api.alquran.cloud/v1/quran/ar.alafasy
```

### Option 2: Use Different Arabic Editions
You can choose different Arabic text editions:

- **Uthmani Script**: https://api.alquran.cloud/v1/quran/quran-uthmani
- **Simple Arabic**: https://api.alquran.cloud/v1/quran/ar.alafasy
- **With Tajweed**: https://api.alquran.cloud/v1/quran/ar.muyassar

### Option 3: Multiple Languages/Translations
For translations, you can download:
```
https://api.alquran.cloud/v1/quran/en.asad (English - Asad)
https://api.alquran.cloud/v1/quran/en.sahih (English - Sahih International)
https://api.alquran.cloud/v1/quran/ur.jalandhry (Urdu)
```

## File Structure

The JSON file should have this structure:
```json
{
  "code": 200,
  "status": "OK",
  "data": {
    "surahs": [
      {
        "number": 1,
        "name": "الفاتحة",
        "englishName": "Al-Fatihah",
        "englishNameTranslation": "The Opening",
        "revelationType": "Meccan",
        "numberOfAyahs": 7,
        "ayahs": [
          {
            "number": 1,
            "text": "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",
            "numberInSurah": 1,
            "juz": 1,
            "manzil": 1,
            "page": 1,
            "ruku": 1,
            "hizbQuarter": 1,
            "sajda": false
          },
          ...
        ]
      },
      ...
    ]
  }
}
```

## Setup Steps

1. **Download the HTML file** (`quran-reader-json.html`)

2. **Download the JSON data**:
   - Visit: https://api.alquran.cloud/v1/quran/quran-uthmani
   - Save the page as `quran-data.json`
   - Or use curl/wget:
     ```bash
     curl https://api.alquran.cloud/v1/quran/quran-uthmani -o quran-data.json
     ```

3. **Place files in the same folder**:
   ```
   my-quran-folder/
   ├── quran-reader-json.html
   └── quran-data.json
   ```

4. **Open the HTML file** in your browser

## Features

- ✅ **Offline Reading** - Works without internet once JSON is loaded
- ✅ **Text Highlighting** - Double-click any verse to highlight
- ✅ **Personal Notes** - Right-click to add notes with star markers
- ✅ **Search** - Search for any Surah by name
- ✅ **Responsive Design** - Works on desktop and mobile
- ✅ **Local Storage** - All highlights and notes saved in browser

## Usage

### Highlighting Text
- **Double-click** any verse to highlight it in yellow
- Double-click again to remove highlight

### Adding Notes
- **Right-click** any verse to add a personal note
- A gold star (★) will appear on verses with notes
- Click the star to view/edit the note

### Navigation
- Click any Surah name in the sidebar
- Use the search box to find specific Surahs

## Alternative: Create Your Own JSON

If you want to customize the data structure, you can create a simplified version:

```json
{
  "data": {
    "surahs": [
      {
        "number": 1,
        "name": "الفاتحة",
        "englishName": "Al-Fatihah",
        "revelationType": "Meccan",
        "ayahs": [
          {
            "numberInSurah": 1,
            "text": "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ"
          }
        ]
      }
    ]
  }
}
```

## Notes

- The JSON file is approximately 4-5 MB
- All data is stored locally in your browser
- No data is sent to any server
- Works completely offline after initial setup

## Troubleshooting

**Error: "Failed to load Quran data"**
- Make sure `quran-data.json` is in the same folder as the HTML file
- Check that the JSON file is valid (not corrupted)
- Try downloading the JSON file again

**Highlights/Notes not saving**
- Make sure browser cookies/local storage are enabled
- Data is stored per browser - won't sync across devices

## Credits

- Quran text from: https://alquran.cloud/api
- Fonts: Google Fonts (Amiri, Scheherazade New, Cairo)
