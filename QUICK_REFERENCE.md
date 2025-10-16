# Bilingual Website Quick Reference

## How to Use the Language Switcher

### For Visitors
- Look for the flag icons in the **top right corner** of the page
- Click the flag to switch to that language:
  - 🇩🇪 German (Deutsch)
  - 🇬🇧 English
- The current language flag is shown but not clickable

## Page URLs

### German Pages (Default)
```
https://marcelrgberger.github.io/           → Startseite
https://marcelrgberger.github.io/impressum/ → Impressum
https://marcelrgberger.github.io/datenschutz/ → Datenschutzerklärung
```

### English Pages
```
https://marcelrgberger.github.io/en/           → Home
https://marcelrgberger.github.io/en/impressum/ → Imprint
https://marcelrgberger.github.io/en/datenschutz/ → Privacy Policy
```

## For Content Editors

### How to Edit Existing Content

#### German Content
Edit these files:
- `index.md` (main page)
- `impressum/index.md` (imprint)
- `datenschutz/index.md` (privacy)

#### English Content
Edit these files:
- `en/index.md` (main page)
- `en/impressum/index.md` (imprint)
- `en/datenschutz/index.md` (privacy)

### How to Add a New Page

1. **Create German Version**
   ```markdown
   ---
   layout: default
   title: "Your Title"
   permalink: /your-page/
   lang: de
   ---
   
   Your German content here...
   ```

2. **Create English Version**
   ```markdown
   ---
   layout: default
   title: "Your Title"
   permalink: /en/your-page/
   lang: en
   ---
   
   Your English content here...
   ```

3. **Save Files**
   - German: `your-page/index.md`
   - English: `en/your-page/index.md`

4. The language switcher will automatically work!

## Customization

### Change Flag Icons
Replace these files with your own flag designs:
- `images/flag-de.svg` (German flag)
- `images/flag-en.svg` (English flag)

### Adjust Flag Size
Edit `assets/css/language-switcher.css`:
```css
.flag-icon {
  width: 32px;   /* Change this */
  height: 24px;  /* Change this */
}
```

### Change Position
Edit `assets/css/language-switcher.css`:
```css
.language-switcher {
  top: 20px;    /* Distance from top */
  right: 20px;  /* Distance from right */
}
```

## Troubleshooting

### Language switcher not showing
- Check that `_layouts/default.html` includes the language-switcher
- Verify `assets/css/language-switcher.css` is loaded
- Check browser console for errors

### Wrong language on page
- Verify front matter has correct `lang: de` or `lang: en`
- Check `permalink` matches the URL structure

### Broken links after language switch
- Ensure both German and English versions exist at matching paths
- Example: `/contact/` must have `/en/contact/` equivalent

## Need Help?

Refer to detailed documentation:
- `LANGUAGE_IMPLEMENTATION.md` - Technical details
- `IMPLEMENTATION_SUMMARY.md` - Complete overview

Or check the implementation files:
- `_layouts/default.html` - Main layout
- `_includes/language-switcher.html` - Switcher logic
- `_config.yml` - Site configuration
