# Apoc

A reader for extra-biblical works — texts that fall outside the major Christian and Jewish canons (for example, apocrypha, pseudepigrapha, deuterocanonical books, and related ancient literature).

## License

**Application code** (this repository’s software — UI, tooling, layout, and reader logic) is licensed under the [MIT License](LICENSE). You may use, modify, and distribute it freely under those terms.

**Included texts are not covered by MIT.** Each work brought into the app remains under its own copyright and license (public domain, Creative Commons, permission-granted, etc.). Rights and attribution for a given text are documented in that work’s `works/<slug>/source.json` and must be respected independently of the MIT license on the app itself.

Do not assume that because the app is MIT-licensed, every text in it is free to reuse. Check each work’s metadata before redistributing or adapting its content.

## Development

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000). Use the **Run and Debug** panel (`.vscode/launch.json`) to attach a debugger.

## Source and attribution

Every text in this app must be traceable to a specific, documented source. Attribution is not optional — it is how we stay within copyright and licensing law and give proper credit to translators, editors, and hosting institutions.

### Before adding a work

1. **Confirm you may use the text.** Check the license, copyright status, and any terms of use at the source. Prefer:
   - Public domain texts (and confirm the *translation* is also public domain where applicable)
   - Explicitly licensed editions (e.g. Creative Commons) that permit redistribution and display
2. **Record where you got it.** Do not add a work from memory, an unattributed PDF, or a source you cannot cite.
3. **Prefer primary or reputable hosts.** Examples include university digital libraries, established translation projects, and archives that state rights clearly. Avoid scraped or aggregator sites with unclear provenance.

### Required metadata per work

When a work is added, document it in `works/<slug>/source.json` (or equivalent) with at least:

| Field | Description |
| --- | --- |
| `title` | Full title of the work |
| `author` | Original author, or `"Unknown"` / `"Traditional"` as appropriate |
| `translator` | Translator(s) or editor(s), if applicable |
| `sourceName` | Name of the site, archive, or publication |
| `sourceUrl` | Direct URL where the text was obtained |
| `retrievedAt` | ISO date the text was fetched or verified |
| `license` | Stated license or legal status (e.g. `"Public domain"`, `"CC BY 4.0"`) |
| `licenseUrl` | Link to license terms, when available |
| `notes` | Any conditions, attribution wording required by the licensor, or edition-specific caveats |

The reader UI must surface this attribution to users (e.g. on each work’s title page or in an “About this text” panel).

### In the repository

- Keep a copy of or link to the **exact edition** used (filename, version, or snapshot date).
- Do not strip copyright notices, license headers, or required attribution text from source files.
- If a licensor requires specific wording (e.g. “Translation © …, used under …”), reproduce it verbatim in `source.json` and in the app.

### When in doubt

Do not import the text until rights are clear. Open an issue documenting the proposed source, license, and intended use for review.

## Scope

This project is for reading and study. It does not claim canonical status for any included work. Inclusion of a text is for historical and literary access, not endorsement of its contents or tradition.
