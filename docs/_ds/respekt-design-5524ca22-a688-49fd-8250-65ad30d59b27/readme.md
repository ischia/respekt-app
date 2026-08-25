# Respekt Design System

Design system for **Respekt** (www.respekt.cz) — a Czech weekly news magazine and digital publisher. The brand spans a print magazine, the responsive website, a mobile reading app, and an audio/podcast app ("poslech"). The system codifies Respekt's quiet, confident editorial voice: clean white pages, a single signature red, warm pastel section washes, generous serif reading type, and a calm set of thin line icons.

Tagline: **"Odvaha nejen číst"** (Courage, not just to read).

## Sources
- **Figma:** "Respekt – UI design.fig" (mounted virtual file). Pages: `UI---Desktop`, `UI---Mobile`, `UI---Aplikace` (audio app), `Informa-n-servis` (Respekt Rychle / fast news), `Components` (styleguide & widget library), `Inspo`. Component library lives under `/Components/components`.
- **Fonts (provided):** Adelle & Adelle Sans OTF families (TypeTogether) + spec PDFs (`uploads/DS_Adelle.pdf`, `uploads/DS_Adelle-Sans.pdf`).
- **Logos (provided):** `uploads/respekt black logo.ai`, `uploads/rs-logo-podcast.png`. The RESPEKT wordmark was extracted as a recolorable SVG (`assets/logos/respekt-wordmark.svg`).
- Brief note from the team: *"Používáme barevnou paletu, oblé hrany, pracujeme se symboly (audio, záložky, komentáře, newslettery, podcasty). Chceme být profesionální, neblázníme, ale chceme být hraví, zajímaví, překvapiví."* — a colourful palette, rounded corners, symbol-driven UI; professional but playful, interesting, surprising.

---

## CONTENT FUNDAMENTALS

**Language.** All product copy is **Czech**. Diacritics everywhere (á, č, ď, ě, í, ř, š, ů, ž) — fonts and components must render them cleanly.

**Voice & tone.** Serious, intelligent, and quietly witty. Respekt writes like a thoughtful weekly: declarative headlines, often with a provocative or ironic edge ("Pečínka ze psa a další hity. Jak Donald Trump v debatě promarnil příležitost"). Commentary headlines pose questions ("Co na to Green Deal?", "Máme chtít, aby byl Babiš vyloučen?"). Not clickbait, not stuffy.

**Person.** Editorial copy is third person / impersonal. UI copy addresses the reader directly but politely, usually via imperative or infinitive: "Odebírejte denní novinky", "Zobrazit všechny články", "Poslechnout", "Přihlásit se k odběru". Account actions are plainly labelled: "Můj účet", "Uložené články".

**Casing.** Sentence case for headlines and buttons (Czech orthography — only the first word and proper nouns are capitalised). Category eyebrows are the one place uppercase appears ("KOMENTÁŘ", "PODCAST"), set small with letter-spacing. Never ALL-CAPS a headline.

**Numerals & dates.** Czech formatting: dates as "1. 11. 2024", durations as "12 min", "14:56", counts in parentheses ("Všechny články (160)"). A middot **bodka** (·) separates meta items (author · date · read time).

**Categories / kickers.** Pieces are typed by a short coloured eyebrow: Komentář, Rozhovor, Reportáž, Analýza, Podcast, Audio, Newsletter, Věda, Kultura.

**Emoji.** None. Respekt never uses emoji in product UI. Meaning is carried by colour, line icons, and typography.

**Vibe.** Professional and grown-up, but with small playful moments — the astronaut doodle peeking over the navbar, pastel section blocks, a surprising photo crop. "Neblázníme" — we don't go wild — but we're never grey or boring.

---

## VISUAL FOUNDATIONS

**Colour.** A near-monochrome editorial base — **ink `#181D27` on paper white** — punctuated by a single signature **Respekt red `#CE0B24`** (logo, links, primary buttons, progress, the active state). A muted **gold `#BEA140`** marks the account/premium track ("Můj účet"). Section blocks are washed in soft **pastel tints at ~20% opacity** over white — salmon (`--rs-wash-salmon`) and amber (`--rs-wash-amber`) are the workhorses. Category colours add quiet meaning: audio = purple `#9747FF`, podcast = green, commentary = terracotta, links/info = blue. A separate **pastel data palette** (navy → cobalt → teal → pink) is reserved for maps, charts and infographics in the "Informační servis" product.

**Type.** Two superfamilies. **Adelle Sans** carries all UI, navigation, buttons and most headlines — bold/extrabold at large sizes, with a slightly condensed, news-front feel. **Adelle** (the serif) carries reading: article body, leads/perex, and — notably — the **app's headlines** (the audio app sets titles in serif, the web sets them in sans). Headlines run 20–56px bold/extrabold with tight tracking; body is 18px serif at 1.6 line-height; perex 21px serif; meta 12–14px sans. Czech reads long, so `text-wrap: balance` on headlines and generous line-height keep it comfortable.

**Spacing & layout.** 8px grid. Desktop content sits in an **1180px column** inside a 1440 frame (130px side gutters); mobile is 375/390 with 16px gutters. Card grids are mostly **3-up with a 12px gap**. The navbar is two rows (88px brand row + ~56–64px section rail) and sticky.

**Corners.** Soft and consistent — **cards, widgets and images use 6px** radius (the signature value); buttons & inputs are nearly square at **2–4px**; play/bookmark controls and avatars are **fully round (pills)**. Nothing is sharp-cornered.

**Cards.** The standard article card sits on a flat **`#ECEFF2` surface fill** (not white, not floating) with a 6px radius; image on top (corners 6/6/4/4), play + bookmark controls bottom-right of the image, then a coloured eyebrow, a sans-bold headline, a serif perex, and a faint author/date meta row. Featured "big article" cards are wide and dark: a photo with a left-to-right darkening gradient and white text on the right.

**Backgrounds & imagery.** Pages are predominantly **white**, broken by full-width pastel-wash section bands. Photography is documentary/editorial — real reportage photos, natural colour (neither heavily warm nor cool, not duotoned). Big articles overlay text on photos via a subtle dark gradient (a "protection gradient", not a solid scrim). Magazine covers appear as objects (issue widget). Occasional hand-drawn illustration (caricatures, the astronaut doodle) adds the playful note.

**Elevation & shadows.** Restrained. Most cards have **no shadow** — they're defined by their surface fill against white. Shadows appear only where something genuinely floats: the **docked audio player** (a pill with a soft `0 8px 28px rgba(0,0,0,.16)` shadow) and modals. No neumorphism, no glow.

**Borders & dividers.** Hairlines in `#E0E4E9` separate nav rows, author-list items, article meta, and footer columns. The red 3px left-rule marks pull quotes.

**Motion.** Subtle and functional. Hover lifts a card ~2px and/or darkens a button (`brightness(0.92)`); press scales a round control to ~0.92. Transitions are 120–320ms on a standard ease. No bouncing, no parallax, no decorative looping animation on content. Reduced-motion safe.

**Transparency & blur.** Used sparingly: pastel washes are flat tints (not blurred); the only frosted surface is the occasional "light" control sitting on a photo (`rgba(255,255,255,0.9)`).

---

## ICONOGRAPHY

Respekt's UI iconography is a **thin, rounded line set** — single-weight strokes (~1.8px), round caps and joins, drawn on a 24px grid. Icons are quiet and utilitarian: bookmark (záložka), play / pause, ±15s, skip, headphones & mic (audio/podcast), mail (newsletter), speech bubble (komentáře), share, search (lupa), menu, chevrons, gift, user/account, download, calendar, basket, sleep (moon), lock/unlock. A few **two-tone "color" category glyphs** (podcast, opinion, newsletter) add a dab of colour where a category needs emphasis.

There is **no emoji and essentially no use of unicode glyphs as icons**; the one recurring text-as-symbol is the **bodka** (·) middot separator between meta items, provided as the `.rs-bodka` helper / `<Bodka>`-style dot.

**Implementation in this system.** The original Figma icons are individual vector symbols. They are reimplemented here as a single React **`Icon`** component (`components/core/Icon.jsx`) holding clean inline SVG paths at the matching weight and radius. The path geometry follows the open-source **Lucide** set (ISC license), which is a close visual match to Respekt's house line icons. **⚠️ Substitution flag:** these are *close matches*, not the exact Figma vectors — if pixel-exact parity with the original symbols is required, export the source SVGs from Figma and drop them into `Icon.jsx`. The RESPEKT wordmark and podcast logo are the real brand assets (`assets/logos/`).

---

## INDEX

**Foundations**
- `styles.css` — global entry point (import this one file). `@import`s everything below.
- `tokens/fonts.css` — `@font-face` for Adelle & Adelle Sans.
- `tokens/colors.css` — palette + semantic aliases.
- `tokens/typography.css` — families, weights, type scale.
- `tokens/spacing.css` — 8px spacing, radius, shadow, layout, motion.
- `tokens/base.css` — element defaults + helpers (`.rs-eyebrow`, `.rs-meta`, `.rs-bodka`).
- `guidelines/cards/` — specimen cards rendered in the Design System tab (Colors, Type, Spacing, Brand).

**Components** (`components/`, namespace `window.RespektDesignSystem_5524ca`)
- core: `Icon`, `Tag`, `Badge`, `Avatar`
- forms: `Button`, `IconButton`, `Input`, `Switch`
- content: `ArticleCard`, `FeatureCard`, `AuthorCard`
- media: `AudioPlayer`

**UI kits** (`ui_kits/`)
- `web/` — Respekt.cz desktop (homepage + article, docked audio player).
- `mobile/` — Respekt.cz mobile homepage feed (phone frame).
- `app/` — Respekt audio app "Now Playing" screen (phone frame).

**Brand assets** (`assets/`)
- `logos/respekt-wordmark.svg` (recolorable), `logos/respekt-podcast-logo.png`
- `fonts/` — Adelle & Adelle Sans OTF.
- `img/` — sample editorial photography for kits & cards.

**Newsletter** (`newsletter/`)
- `email/*.twig` — production Twig templates for the CMS (layout, Dnešní Respekt, Nejčtenější, Článek, patička, app-badge strip; HTML + TXT versions).
- `Newslettery - náhled.html` — static preview of all three templates (desktop/mobile, light/dark).
- `Newsletter - Dnešní Respekt.html` + `variant-pastel2.jsx` — the approved design canvas (final D4 iteration).

**Other**
- `SKILL.md` — Agent Skill manifest for use in Claude Code.
- `uploads/` — raw source materials (original OTF families incl. weights not shipped, font spec PDFs, logos, reference screenshots). Not part of the compiled design system; keep for provenance.

---

## CAVEATS
- **Display/masthead font "Despekt"** appears in the source as a custom Respekt display face but was **not provided** — it is not included. Adelle Sans Extrabold stands in for large display headlines.
- **Adelle Semibold (serif)** may render at the wrong weight on some systems; the core reading weights (Regular/Bold/Italic) are present.
- **Icons are Lucide-based substitutes** matched to Respekt's line style (see ICONOGRAPHY) — not the exact Figma vectors.
- The `Roboto` seen throughout the Figma is placeholder/system text; the real brand faces are **Adelle / Adelle Sans**.

## Components

Komponenty jsou materializované 1:1 z Figmy „Respekt – UI design“. Jména jsou PascalCase verze figmových názvů (např. „1440 / navbar“ → `Navbar1440`, „375 / widget / article“ → `WidgetArticle375`, „Forms / button primary“ → `FormsButtonPrimary`, „ico / play“ → ikona `IcoPlay` / icon-set `components/core/icons`). Obsah figmových stránek Trash a Inspo (staré HP varianty, „clanek / stredni“, „clanek / tema“, starý „Navbar“, generický Relume kit Button/Header/Checkbox) je záměrně vynechán — jsou to zavržené pracovní verze, ne součást designu.

### Pokrytí Figma kitu — záměrné odchylky

- Figma počítá 216 „rodin“, protože stejná komponenta je definovaná na více stránkách (např. „1440 / navbar“ ×3, „Forms / button primary“ ×4, „Action / bookmark“ ×3). Každou rodinu stavíme jen jednou — duplicitní definice napříč stránkami nejsou samostatné komponenty.
- Rodiny žijící jen na stránkách Trash/Inspo jsou záměrně vynechané: `clanek / stredni`, `clanek / tema`, `clanek / small`, `clanek/ver4`, `Navbar (Loggedin)`, `Button (30 variant, Relume)`, `Checkbox (Selected/Numbered)`, `input fields`, `Header (Style)`, `player`/`player - dvouradkovy` (staré), `bookmark interakt`, `bookmark`, `Icon / Menu`, `Duh=…` varianty.
- Jména jako `WidgetArticleInfobox1440`, `WidgetArticleNote1440`, `Prispevek3`, `PodcastMini`, `TabBar`, `Vydani`, `StatusBarTime`, `Digitalni*`, `HPZprava`, `VypisZprava*`, `ISSouvisejCLNek`, `Badge*`, `Ico*` jsou PascalCase přepisy figmových názvů se speciálními znaky („1440 / widget / article / infobox“, „3 prispevek“, „podcast - mini“, „_StatusBar-time“, „IS - související článek“…) — záměrné, nejde o nové komponenty mimo kit.

### Core (akce, metadata, glyfy, spinner) — `components/core/`

`ActionBookmark`, `ActionBookmarkBig`, `ActionGallery`, `ActionPlay`, `ActionPlayBig`, `ActionPlayDark`, `AngleDownSolid`, `ArticleMetadata`, `ArticleProgressFullAnimate`, `ArticleStatus`, `AssetsYoutubeIconsYoutube`, `Bodka`, `ButtonDalsiMoznostiKlikaci`, `EllipsisHSolid`, `EllipsisVSolid`, `ExternalLinkAltSolid`, `GiftSolid`, `IcoBookmark`, `IcoColorOppinion`, `IcoEye`, `IcoGallery`, `IcoPause`, `IcoPlay`, `InteraktIkonaAudioClanek`, `LockSolid`, `NewsletterType`, `Payment`, `PrehratVListeInterakt`, `SpinnerGradient`, `Tag`, `TimesSolid`, `Voice`, `Youtube`

### Icons (jeden icon-set, <Icon name="…"/>) — `components/core/icons/`

`Icon`

### Forms (tlačítka, inputy, přepínače) — `components/forms/`

`FormsArticleLink`, `FormsButtonPrimary`, `FormsButtonSecondary`, `FormsButtonTercial`, `FormsCheckbox`, `FormsDropdown`, `FormsIconButtonPrimary`, `FormsIconButtonSecondary`, `FormsInput`, `FormsInputPriceIcon`, `FormsLabelBig`, `FormsLabelSmall`, `FormsNavbarLink`, `FormsRadio`, `FormsSubscriptionForms`, `FormsSwitch`, `FormsSwitchV2`, `FormsToggle`, `IcoCalendar`, `IcoChevronDown`, `IcoChevronLeft`, `IcoGift`, `IcoInfoText`, `IcoLogin`, `IcoShare`, `InputTextSmall`, `OptionSmall`

### Desktop 1440 (navbar, footer, widgety) — `components/desktop/`

`Advertisement1440`, `Apple`, `BadgeAppStore`, `BadgeApplePodcasts`, `BadgeEPub`, `BadgeGooglePodcasts`, `BadgePlayStore`, `BadgeSpotify`, `BadgeYoutube`, `Component1`, `Footer1440`, `FooterSubscription1440`, `Google`, `Ico15Dopredu`, `Ico15Dozadu`, `IcoBasket`, `IcoClose`, `IcoColorPodcast`, `IcoLupa`, `IcoMail`, `IcoMenu`, `IcoOdebiratAutora`, `LOGO`, `Navbar1440`, `NavbarSecondary1440`, `Spotify2`, `WidgetArticle1440`, `WidgetArticleHeroOpinion1440`, `WidgetArticleHeroPodcast1440`, `WidgetArticleHover1440`, `WidgetArticlePr1440`, `WidgetArticleTextMain1440`, `WidgetAuthor1440`, `WidgetBestseller1440`, `WidgetBigArticle1440`, `WidgetNewIssue1440`, `WidgetNewsletter1440`, `WidgetPlayer1440`, `WidgetPodcast1440`, `WidgetReisenauer1440`, `WidgetSerie1440`, `WidgetStore1440`

### Article content (widgety v článku, výpisy zpráv) — `components/content/`

`Clanek`, `ClanekBlockStripSmall`, `FormsButtonTercial4`, `HPZprava`, `HPZpravaMobil`, `ISSouvisejCLNek`, `IcoZalozka`, `Prispevek3`, `VypisZprava`, `VypisZpravaRozbaleni`, `WidgetArticleInfobox1440`, `WidgetArticleNewsletter1440`, `WidgetArticleNote1440`, `WidgetArticlePicture1440`, `WidgetArticlePictureMiddle1440`, `WidgetArticlePictureSmall1440`, `WidgetArticlePodcasts1440`, `WidgetArticleYouTubePlayer1440`, `WidgetFormsNewsletterType1440`

### Mobile 375 — `components/mobile/`

`Footer375`, `FooterSubscription375`, `IcoAccount`, `IcoLogout`, `Navbar375`, `Store375`, `Widget375`, `WidgetArticle375`, `WidgetArticleHero375`, `WidgetArticleHeroOpinion375`, `WidgetArticleHeroPodcast375`, `WidgetAuthor375`, `WidgetBigArticle375`, `WidgetFormsNewsletterType375`, `WidgetIPhone13375`, `WidgetNewIssue375`, `WidgetNewsletter375`, `WidgetPodcast375`, `WidgetPodcasts375`, `WidgetReisenauer375`, `WidgetSerie375`

### App & media (player, tab bar, badges) — `components/media/`

`AD`, `ApplePayMark`, `BadgeAmazonAppstore`, `CheckSolid`, `IcoArchive`, `IcoR`, `MiniPlayer`, `MiniPlayer2`, `PodcastMini`, `StatusBarTime`, `TabBar`, `Vydani`

### Store & předplatné — `components/store/`

`AppleComputers`, `Digitalni`, `DigitalniKlub`, `DigitalniTistene`, `DigitalniTisteneKlub`, `GooglePayButtonGooglePay`, `IPhone`
