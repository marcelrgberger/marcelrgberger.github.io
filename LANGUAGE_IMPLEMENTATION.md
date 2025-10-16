# Bilingual Website Implementation

This website now supports both German (DE) and English (EN) languages.

## Features

- **Language Switcher**: Located in the top right corner of every page with flag icons
- **German Content**: Root paths (/, /impressum/, /datenschutz/)
- **English Content**: /en/ paths (/en/, /en/impressum/, /en/datenschutz/)
- **Automatic Language Detection**: Each page has a `lang` attribute in the front matter
- **Metadata Support**: Language-specific metadata in _config.yml

## File Structure

```
/
├── index.md (German homepage)
├── impressum/index.md (German imprint)
├── datenschutz/index.md (German privacy policy)
├── en/
│   ├── index.md (English homepage)
│   ├── impressum/index.md (English imprint)
│   └── datenschutz/index.md (English privacy policy)
├── _layouts/
│   └── default.html (Custom layout with language switcher)
├── _includes/
│   ├── language-switcher.html (Language switcher component)
│   └── head-custom.html (Custom head content)
├── assets/css/
│   └── language-switcher.css (Language switcher styles)
└── images/
    ├── flag-de.svg (German flag icon)
    └── flag-en.svg (English/UK flag icon)
```

## How it Works

1. Each page has a `lang: de` or `lang: en` attribute in its front matter
2. The layout uses this attribute to set the HTML lang attribute
3. The language switcher checks the current page's lang attribute and URL
4. Links automatically toggle between German (/) and English (/en/) versions
5. The site title links to the appropriate language homepage

## Adding New Pages

To add a new page in both languages:

1. Create the German version in the root or appropriate directory
2. Create the English version in the /en/ directory with the same path structure
3. Add `lang: de` to German pages and `lang: en` to English pages in front matter
4. The language switcher will automatically work for the new pages

## Customization

- Edit `_config.yml` to change site metadata for each language
- Modify `_includes/language-switcher.html` to change switcher behavior
- Update `assets/css/language-switcher.css` to adjust styles
- Replace flag SVGs in `/images/` for different icons
