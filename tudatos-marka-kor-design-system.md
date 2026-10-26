# Tudatos Márka Kör — Design System

**Verzió:** v1.3 · 2026
**Weboldal:** tudatosmarkakor.hu
**Tagline:** Tiszta rendszer. Saját hang. Következetes márka. ♥

---

## Tartalom

1. [Márkaidentitás](#1-márkaidentitás)
2. [Színrendszer](#2-színrendszer)
3. [Tipográfia](#3-tipográfia)
4. [Logó rendszer](#4-logó-rendszer)
5. [Spacing és rács](#5-spacing-és-rács)
6. [Komponensek](#6-komponensek)
7. [Grafikai elemek](#7-grafikai-elemek)
8. [Hangulat és márkahang](#8-hangulat-és-márkahang)
9. [Használati szabályok](#9-használati-szabályok)

---

## 1. Márkaidentitás

A Tudatos Márka Kör egy havi tagságos közösség magyar női vállalkozóknak, akik AI-eszközöket szeretnének saját márkájuk hangján, következetesen és emberi érzéssel használni. A vizuális identitás ezt az értéket tükrözi: csendes elegancia, nőies finomság, szakmai magabiztosság.

| Elem | Leírás |
|------|--------|
| Célközönség | Magyar női vállalkozók |
| Ígéret | AI, ami a te márkád hangján szól |
| Hangulat | Csendes magabiztosság, alkotói rend |
| Közeg | Aszinkron, introvertált-barát közösség |
| Formátum | Havi tagság, rugalmas belépés |

---

## 2. Színrendszer

### Alap paletta

| Token | Hex | CSS változó | Felhasználás |
|-------|-----|-------------|--------------|
| Gold | `#C3944D` | `--color-gold` | Akcentszín, CTA, badge, díszítés |
| Gold Light | `#E8B86D` | `--color-gold-light` | Gradiens vég, szöveg highlight |
| Plum | `#5B2C59` | `--color-plum` | Elsődleges márka, fejléc, gomb |
| Lilac | `#9B5990` | `--color-lilac` | Másodlagos szín, ikon, script szöveg |
| Mauve | `#D3A0AA` | `--color-mauve` | Határvonalak, hover, dekoráció |
| Blush Pink | `#D4889A` | `--color-blush-pink` | Logó szív fill elem, kiemelés |
| Blush | `#F6F2F6` | `--color-blush` | Kártya hátterek, badge fill |
| Cream | `#FAF7F5` | `--color-cream` | Oldal alap háttér |
| Dark Plum | `#3A1A3A` | `--color-dark-plum` | Dark section, mélység, hover |
| Text | `#2E1A2E` | `--color-text` | Törzsszöveg |
| Text Muted | `#7A5C7A` | `--color-text-muted` | Másodlagos szöveg, label |

> **Megjegyzés:** A Blush Pink (`#D4889A`) kizárólag a logó szív-fill elemből ered - ez a szín közvetlenül a logóból van kiolvasva, és csak nagyon mértéktartóan, dekoratív szerepben alkalmazható.

### Mood board / marketing-vizuál szerepkiosztás — v2 (2026)

> **Fontos:** ez az alszekció kizárólag az AI-képgeneráláshoz (mood board promptok, marketing vizuálok) használt szerepkiosztást dokumentálja. A 6. fejezetben (Komponensek) leírt élő weboldal-komponensek (gombok, kártyák, gradiensek) továbbra is a fenti Alap paletta szerint működnek - ezt a frissítés nem érinti.

Az 5 fő szín, amit a mood board promptok színswatch-sorként használnak:

| Szerep | Token | Hex |
|--------|-------|-----|
| Elsődleges | Középlila (Lilac) | `#9B5990` |
| Másodlagos | Mauve | `#D3A0AA` |
| Sötét | Mély bíbor (Plum) | `#5B2C59` |
| Világos | Törtfehér (Blush) | `#F6F2F6` |
| Kiemelő | Arany (Gold) | `#C3944D` |

> **Megjegyzés:** ez a felosztás kizárólag az Alap paletta tokenjeit használja. Egy korábbi verzióban Másodlagosként `#CC81AB` szerepelt - ez a szín a képgenerátor által kitalált felirat volt, nem márkaszín, 2026-07-05-én törölve. A Dark Plum (`#3A1A3A`) szándékosan nem része a mood board felosztásnak (a boardok lágyabb összképe miatt), az élő weboldalon változatlanul használatos.

Az 5 kiegészítő árnyalat, amit a mood board promptok a háttér- és fotóstílus-leírásokba építenek:

| Token | Hex | Szerep a mood boardban |
|-------|-----|------------------------|
| Gold Light | `#E8B86D` | finom fólia-akcentus a háttér szélein |
| Blush Pink | `#D4889A` | ritka, emlékezetes színpillanat |
| Cream | `#FAF7F5` | fő háttértónus, papírtextúra |
| Text | `#2E1A2E` | mélytónusú tipográfia a promptban |
| Text Muted | `#7A5C7A` | másodlagos felirat tónusa |

### Gradiens rendszer

```css
/* Hero Dark — sötét szekciókhoz */
background: linear-gradient(135deg, #3A1A3A, #5B2C59);

/* Brand Gradient — logó, ikonok */
background: linear-gradient(135deg, #5B2C59, #9B5990);

/* Soft Blush — kártyák, panel hátterek */
background: linear-gradient(135deg, #F6F2F6, #D3A0AA);

/* Gold Shimmer — arany akcentekhez */
background: linear-gradient(135deg, #C3944D, #E8B86D);
```

### Kontraszt szabályok

- Plum (`#5B2C59`) fehér háttéren: AA megfelelő
- Gold (`#C3944D`) fehér háttéren: kizárólag nagy szöveghez (min. 18px)
- Dark szekciókban fehér szöveg: min. `rgba(255,255,255,0.75)`

---

## 3. Tipográfia

### Betűtípus rendszer — v1.1

#### Display & Heading — Fraunces

```css
font-family: 'Fraunces', Georgia, serif;
```

Optikai tengelyes (optical-size: 9–144) display serif. Lágy, megható személyiség nagy méretben — nem merev, hanem organikus. A Tudatos Márka Kör márkahangjának tükre: tudatos, elegáns, nem hivalkodó.

- Súlyok: **400, 500, 600, 700**
- Italic: idézetek, lead szöveg, érzelmi kiemelés
- Optical size: nagy méretben `opsz: 144`, kisebben `opsz: 36`
- Minimum méret: 18px — kisebb méretben Nunito Sans vehet át

#### Body & UI — Nunito Sans

```css
font-family: 'Nunito Sans', system-ui, sans-serif;
```

Lágyan lekerekített humanista groteszk — barátságos, levegős, könnyen olvasható. A lekerekített végű betűk lágy karaktere harmonizál a Fraunces organikus vonalaival és a márka nőies, meleg hangulatával.

- Súlyok: **300, 400, 500, 600, 700**
- 700: alcímek, erős labelek, uppercase felirat
- 600: gombok, kártya cím (Nunito Sans verzió)
- 500: feature label, chip, badge szöveg
- 400: törzsszöveg, bekezdés, leírás
- 300: nagyon nagy méretű kísérőszövegekhez

#### Script Accent — Caveat

```css
font-family: 'Caveat', cursive;
```

Laza, markeres kézírásos betűtípus. Kizárólag dekorációs szerepben: section eyebrow-ok, kísérőfeliratok, érzelmi tagmondat.

- Súlyok: **400, 500, 600, 700** — ez a legnagyobb előnye a korábbi script betűtípusokhoz képest
- Eyebrow szerepben: 500–600
- Nagy CTA felirat előtt: 700
- Minimum méret: 16px
- Maximum 1-2 sor hosszon
- Soha ne törzsszövegként, soha ne gombban

**Betöltés** — Google Fonts, megbízható CDN:

```html
family=Caveat:wght@400;500;600;700
```

---

### Mini betűrendszer — használati táblázat

| Szerep | Betűtípus | Súly | Megjegyzés |
|--------|-----------|------|------------|
| Logó / márkanév | Fraunces | 600–700 | Csak a logófájlban, ne helyettesítsd |
| Nagy főcímek | Fraunces | 600 | Hero, section heading |
| Alcímek | Nunito Sans | 700 | Kártya cím, feature cím |
| Törzsszöveg | Nunito Sans | 400 | Bekezdés, leírás, hint |
| Gombok | Nunito Sans | 600 | Pill-shape, uppercase-mentes |
| Idézetek | Fraunces Italic | 400–500 | Testimonial, quote callout |
| Apró címkék | Nunito Sans | 700 | Uppercase + 0.12–0.15em letter-spacing |

### Típusskála

| Token | Méret | Felhasználás |
|-------|-------|--------------|
| `--text-xs` | 12px | Label, badge, meta, uppercase eyebrow |
| `--text-sm` | 14px | Kártyaszöveg, hint, input-label |
| `--text-base` | 16px | Törzsszöveg, input, bekezdés |
| `--text-lg` | 18px | Lead, testimonial body |
| `--text-xl` | 22px | Alcím (Grotesk 600) |
| `--text-2xl` | 28px | Section subheading (Fraunces) |
| `--text-3xl` | 36px | Section heading (Fraunces) |
| `--text-4xl` | 48px | Hero cím (Fraunces) |
| `--text-5xl` | 60px | XL display, különleges alkalom |

### Szövegtávolság és sortávolság

```css
/* Törzsszöveg */
line-height: 1.65 - 1.7;

/* Heading (Fraunces) */
line-height: 1.1 - 1.25;

/* Idézet, testimonial */
line-height: 1.5 - 1.6;

/* Uppercase section label */
letter-spacing: 0.12 - 0.15em;

/* Gomb szöveg */
letter-spacing: 0.02 - 0.03em;
```

---

## 4. Logó rendszer

### A logó elemei és szimbolizmusuk

A végleges logó egy összetett, de letisztult kompozíció. Minden elem szándékos.

| Elem | Leírás | Szimbolizmus |
|------|--------|--------------|
| Szív outline (arany) | Körvonalasított szív forma | Közösség, gondoskodás, a "Kör" maga |
| Blush fill (bal szívfél) | Lágy rózsaszín (`#D4889A`) töltés | Nőiesség, személyesség, érzelem |
| Botanikai levélsor | 2 arany levél eltérő méretben | Növekedés, tudatosság, organikusság |
| Tech csomópontok | 3 kis kör a szárvégeken | AI integráció, digitális tudatosság |
| Pecsét keret | Kettős arany kör + pontsor | Zárt közösség, hitelesség, tekintély |
| Körfelirat | "TUDATOS MÁRKA KÖR" | Komplett márkaidentitás, badge verzió |

### Logó fájlok

| Fájl | Tartalom | Felhasználás |
|------|----------|--------------|
| `logo_gk.png` | Ikon + pontozott kör | Elsődleges digitális verzió, header |
| `logo_g.png` | Csak ikon (kör nélkül) | Kisebb méret, favicon, app ikon |
| `logo.png` | Teljes pecsét (plum bg + felirat) | Nyomtatás, partnerek, prémium |

### Logó háttér szabályok

| Háttér | Ajánlott verzió | Megjegyzés |
|--------|----------------|------------|
| Cream / White | `logo_gk.png` | Alapértelmezett |
| Plum | `logo_gk.png` | Hero, banner — a logó aranya megmarad |
| Dark Plum | `logo_gk.png` | Dark section — kontrasztos |
| Blush / Mauve | `logo_g.png` | Kártyán belül, kisebb méretben |

### Méret szabályok

| Méret | Verzió | Kontextus |
|-------|--------|-----------|
| 80px+ | `logo_gk.png` | Header, hero, önálló megjelenés |
| 48px | `logo_gk.png` | Navigáció, sticky bar |
| 32px | `logo_gk.png` | Kis header, lista |
| 24px és alatt | `logo_g.png` | Favicon méret — kör nélküli verzió |

### Tiltott logó használat

- Ne forgasd el
- Ne változtasd meg az arányokat
- Ne alkalmazd alacsony kontrasztú háttéren
- Ne add hozzá drop shadow-t a szimbólumhoz
- Ne cseréld ki a betűtípust a pecsét verziójában
- Ne vágd le a kör keretet

---

## 5. Spacing és rács

### Spacing skála

| Token | Érték | Tipikus felhasználás |
|-------|-------|---------------------|
| `--space-1` | 4px | Ikon-szöveg gap, belső badge padding |
| `--space-2` | 8px | Kis gap, gomb ikon közé |
| `--space-3` | 12px | Input padding, badge, chip padding |
| `--space-4` | 16px | Kártya belső gap, lista item |
| `--space-6` | 24px | Section elem gap, grid gap |
| `--space-8` | 32px | Kártya padding, belső elem spacing |
| `--space-12` | 48px | CTA banner padding, logó anatomy |
| `--space-16` | 64px | Nagy section padding |
| `--space-24` | 96px | Section közti távolság |

### Border Radius

```css
--radius-sm:   6px;    /* Chip, kis belső elem */
--radius-md:   12px;   /* Kártyák, input, swatch */
--radius-lg:   20px;   /* Nagy kártyák, CTA banner */
--radius-full: 9999px; /* Gombok (pill), badge, avatar */
```

### Árnyékok

```css
--shadow-sm: 0 1px 4px rgba(91,44,89,0.08);   /* Swatch, kis kártya */
--shadow-md: 0 4px 16px rgba(91,44,89,0.12);  /* Normál kártya, input sor */
--shadow-lg: 0 8px 32px rgba(91,44,89,0.16);  /* Hover állapot, kiemelés */
```

### Rács

| Grid | Alkalmazás |
|------|------------|
| 2 oszlop | Form layout, szöveg + kép, hangulat táblázat |
| 3 oszlop | Kártyák, feature sor, testimonial |
| 4 oszlop | Ikon feature, statisztika kártyák, szín palette |
| 5 oszlop | Teljes paletta megjelenítés |

Max tartalom szélesség: **1140px**, `margin: 0 auto`.
Oldal padding: `32px` (desktop) / `16px` (mobil).

---

## 6. Komponensek

### Gombok

Minden gomb font-family: **Nunito Sans**, font-weight: **600**, border-radius: **full (pill)**.

#### Elsődleges gomb

```css
background: var(--color-plum);
color: white;
padding: 12px 32px;
border-radius: var(--radius-full);
font-family: 'Nunito Sans', sans-serif;
font-weight: 600;
box-shadow: 0 4px 16px rgba(91,44,89,0.28);
```

Hover: `background: dark-plum`, `translateY(-1px)`, erősebb árnyék.

#### CTA / Gold gomb

```css
background: var(--color-gold);
color: white;
font-weight: 600;
box-shadow: 0 4px 16px rgba(195,148,77,0.32);
```

Fő CTA-khoz: "Csatlakozom a tagsághoz", "Kérem az útmutatót!" stb.

#### Outline, Ghost

- Outline: `border: 2px solid plum` - másodlagos akciókhoz
- Ghost: semleges, navigációs visszalépéshez, dark bg-n fehér szöveg

#### Méretek

| Osztály | Padding | Font |
|---------|---------|------|
| `.btn-sm` | 8px 24px | 14px |
| default | 12px 32px | 16px |
| `.btn-lg` | 16px 48px | 18px |

---

### Badge-ek és Chip-ek

Font: **Nunito Sans 600**, letter-spacing: **0.06–0.08em**, pill shape.

```css
/* badge-plum */
background: var(--color-blush);
color: var(--color-plum);
border: 1px solid var(--color-mauve);
padding: 4px 12px;
```

Variációk: `badge-plum`, `badge-gold`, `badge-lilac`.
Chip-ek: kisebb gap, interaktívabb megjelenés keresési tag-ekhez.

---

### Kártyák

Három alap stílus:

**Standard:** `background: white`, `border-radius: 20px`, `box-shadow: shadow-md`, `padding: 32px`
**Dark:** `background: dark-plum`, fehér szöveg, `rgba(255,255,255,0.7)` body szöveg
**Blush:** `background: blush`, `border: 1px solid mauve`, `shadow-sm`

Hover minden kártyán: `translateY(-2px)`, `shadow-lg`.

Kártya ikon: 44×44px, `radius-md`, blush-mauve gradiens háttér, arany kerettel opcionálisan.

---

### Testimonial kártya

- Bal oldali `3px solid gold` border
- Dekorációs nagy `"` idézőjel: Fraunces, 80px, blush szín
- Idézet szöveg: **Fraunces Italic**, 18px, plum
- Szerző avatar: 36px kör, plum-lilac gradiens, display serif monogram
- Szerző neve: Nunito Sans 700, plum
- Szerepe: Nunito Sans 400, text-muted

---

### Input mezők

Font: **Nunito Sans 400** (érték), **700** (label).

```css
border: 1.5px solid var(--color-mauve);
border-radius: var(--radius-md);
padding: 12px 16px;
```

Focus: `border-color: plum`, `box-shadow: 0 0 0 3px rgba(91,44,89,0.12)`.

Email inline sor: lekerekített pill container, az input és a gomb egybeolvad.

---

### CTA Banner

```css
background: linear-gradient(135deg, dark-plum, plum);
border-radius: var(--radius-lg);
padding: 48px 32px;
text-align: center;
```

Belül: Caveat eyebrow arany → Fraunces heading fehér → Nunito Sans body `rgba(255,255,255,0.75)` → gombok flex centerben.

---

### Quote Callout

```css
background: var(--color-blush);
border: 1px solid var(--color-mauve);
border-radius: var(--radius-lg);
padding: 32px 40px;
text-align: center;
```

Szöveg: **Fraunces Italic**, 22px, plum.

---

### Membership Badge

Körbe foglalt felirat, arany keret, Nunito Sans 700 uppercase. Csak header vagy hero szekciókban.

---

## 7. Grafikai elemek

### Díszítő elemek

| Elem | Szín | Felhasználás |
|------|------|--------------|
| ♥ Gold Heart | `--color-gold` | Divider, bullet pont, section zárás |
| Botanikai levél | `--color-gold` | Háttér dekoráció, fejléc keret |
| Pontmátrix | `--color-mauve` | Absztrakt háttér textúra |
| Divider ornament | `--color-mauve` + gold szöveg | Section elválasztó |

### Divider CSS

```css
/* Ornament divider */
.ornament-divider::before,
.ornament-divider::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--color-mauve);
}

/* Fading gold divider */
background: linear-gradient(to right, transparent, var(--color-mauve), transparent);
```

### Ikon stílus

- Stílus: outline (körvonal), nem tömör
- Méret: 20–24px (UI ikon), 32–44px (feature icon kör belsejében)
- Konténer: `border-radius: md`, `background: blush`, `border: 1px solid mauve`
- Gold verzió: `background: #FBF4E8`, `border: gold`

---

## 8. Hangulat és márkahang

### Vizuális hangulat

Nem túlzsúfolt, nem maximálisan dekoratív. Elegáns, nőies, strukturált. Az egyensúly: levegős elrendezés, egy-két erős vizuális pillanat.

- Virágok, botanikus elemek: dekorációs szerepben, nem strukturálisként
- Arany: mértéktartóan, a legfontosabb CTA és díszítő helyeken
- Szöveg: levegős, bőséges fehér tér
- Animáció: minimális — csak célzott hover és scroll reveal

### Kulcs márkamondatok

Ezeket mindig Fraunces Italic-ban érdemes megjeleníteni, ha kiemelésről van szó:

- *"AI, ami a te márkád hangján szól."*
- *"Tiszta rendszer. Saját hang. Következetes márka."*
- *"Nyugodt keretek. Használható rendszer. Saját hang."*
- *"Tanulj. Automatizálj. Építs márkát. Fejlődj."*
- *"Nem kell tökéletesnek lenned. Elég, ha tisztán, a saját hangodon szól a márkád."*
- *"Egy hely, ahol a márkád nem elvészik az AI-korban, hanem pontosabb lesz."*

### A tiltott stílusok

- Clickbait vagy agresszív értékesítési nyomás
- Több mint 3 egyidejű vizuális kiemelés egy sectionben
- Neon vagy élénk, kontrasztos színek
- Tömör fekete háttér (dark-plum-ot használj helyette)
- Fraunces és Caveat kombinálása egy sorban (mindkettő egyszerre túl sok egyéniség)
- Gold szöveg kis méretben (kontrasztprobléma)

---

## 9. Használati szabályok

### Csináld

- Bőséges fehér tér — levegős, lassú ritmus
- Rövid, scanelhető szövegek
- Pill-shape gombok minden CTA-hoz
- Gold szín az érdeklődést felkeltő akció helyekre
- Dark plum szekciók ritkán, kiemelő hatásuk érdekében
- Képek puha, természetes fénnyel (mosolygó arc, laza háttér)
- Fraunces Italic idézetek és testimonialok szövegeiben

### Ne csináld

- Ne halmozz 3-nál több vizuális kiemelést egy sectionben
- Ne keverj Fraunces-t és Caveat-ot azonos sorban
- Ne alkalmazz gold szöveget 14px alatt
- Ne hagyj kártyát árnyék és border nélkül
- Ne törjük meg a cream / blush oldalháttereket élénk elemekkel
- Ne váltsunk más groteszk betűtípusra (Montserrat v1.0, Schibsted Grotesk v1.1 volt — Nunito Sans a jelenlegi)
- Ne használj kalligrafikus script betűtípust accent szerepben (Great Vibes, Sacramento stb.) — a Caveat a végleges választás

### Hozzáférhetőség

- Minden ikon-only elem kap `aria-label`-t
- Input mezők mindig látható `<label>` elemmel
- Focus ring: `box-shadow: 0 0 0 3px rgba(91,44,89,0.12)` minden interaktív elemen
- `@media (prefers-reduced-motion: reduce)` blokk minden animációt letilt
- Min. 4.5:1 kontraszt arány törzsszöveg és háttér között

---

*Tudatos Márka Kör Design System — v1.3 · 2026*
*Betűtípusok: Fraunces (display) + Nunito Sans (body) + Caveat (accent)*
*Tiszta rendszer. Saját hang. Következetes márka. ♥*
