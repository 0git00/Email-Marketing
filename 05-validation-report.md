# Validation Report

Only checks that were actually run are listed.

## Performed
| Check | Tool/method | Result |
|---|---|---|
| Old URL fully replaced | text search | 0 leftover `MuhammadHarisAfzal`; 13 `Emil-Marketing` URLs |
| Canonical and og:url | regex extract | both `https://0git00.github.io/Emil-Marketing/` |
| JSON-LD (2 blocks) | JSON parse | valid JSON |
| sitemap.xml | xmllint | well-formed XML |
| site.webmanifest | JSON parse | valid JSON |
| Duplicate IDs | script | none |
| In-page anchors (#about, #contact...) | script | all resolve |
| Files referenced by index.html exist (manifest, sitemap, og-image, profile, apple-touch-icon) | file check | all present |
| Image alt attributes | script | 13/13 present |
| JavaScript syntax (4 inline blocks) | `node --check` | OK |
| CSS brace balance | script | 515 open / 515 close |
| og-image size and look | opened and inspected | 1200x630, text no longer overlaps the photo |

## Not performed (no network or no tool)
- W3C HTML/CSS validator and Google Rich Results Test (need internet).
- Live link check of social URLs and the deployed site.
- Lighthouse/PageSpeed and real-device mobile rendering.
- Contact form submission (FormSubmit needs a live test).
- Schema semantic validation beyond JSON syntax.

After deploying, run: PageSpeed Insights, Schema Markup Validator (validator.schema.org), Rich Results Test, and open the site on your phone.
