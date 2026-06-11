RABONA KUWAIT - STATIC AFFILIATE SITE (BILINGUAL EN/AR)
==========================================================

Brand:       Rabona Kuwait
Type:        Static HTML/CSS/JS affiliate site
Languages:   English (root) + Arabic (/ar/)
Theme:       Dark base with Rabona red header + yellow CTAs (per official Rabona brand)
Pages:       9 main EN + 9 main AR + 2 redirect loaders + 1 error page = 21 HTML files

----------------------------------------------------------
1. FILE STRUCTURE
----------------------------------------------------------
/
├── index.html                     EN Home (hero, live odds, sports, live betting, app)
├── 404.html                       Error page (EN, noindex)
├── styles.css                     Full site CSS (Rabona palette, shared EN+AR)
├── script.js                      Mobile nav toggle (shared EN+AR)
├── sitemap.xml                    18 URLs (9 EN + 9 AR with full hreflang)
├── robots.txt                     Sitemap pointer, /play-rabona/ + /ar/play-rabona/ disallowed
├── README.txt                     This file
├── assets/
│   ├── logo.webp                  Rabona wordmark (375x200, on red background)
│   ├── favicon.ico                Rabona favicon
│   └── *.webp                     All shared between EN and AR (paths relative)
│
├── about/index.html               EN: About Rabona Kuwait
├── bonuses/index.html             EN: Bonuses & Promotions
├── contact/index.html             EN: Contact & Support (FAQPage schema)
├── login/index.html               EN: Login guide (+965 country code)
├── mobile-app/index.html          EN: Mobile App page
├── play-rabona/index.html         EN affiliate redirect loader (1.5s)
├── privacy/index.html             EN: Privacy Policy
├── responsible-gaming/index.html  EN: Responsible Gaming
├── terms/index.html               EN: Terms & Conditions
│
└── ar/                            Arabic version (lang="ar" dir="rtl")
    ├── index.html                 AR Home (full RTL mirror)
    ├── about/index.html           AR: من نحن
    ├── bonuses/index.html         AR: العروض
    ├── contact/index.html         AR: التواصل والدعم (FAQPage schema in Arabic)
    ├── login/index.html           AR: تسجيل الدخول
    ├── mobile-app/index.html      AR: تطبيق الجوال
    ├── play-rabona/index.html     AR affiliate redirect loader (1.5s, RTL)
    ├── privacy/index.html         AR: سياسة الخصوصية
    ├── responsible-gaming/index.html  AR: اللعب المسؤول
    └── terms/index.html           AR: الشروط والأحكام

----------------------------------------------------------
2. DOMAIN PLACEHOLDER - REPLACE BEFORE DEPLOY IF DIFFERENT
----------------------------------------------------------
Throughout the HTML and sitemap.xml, the production domain is:

   https://rabona-kuwait.com/

If the real production domain differs, search-and-replace before deploying.

----------------------------------------------------------
3. AFFILIATE REDIRECT - PRODUCTION URL
----------------------------------------------------------
In /play-rabona/index.html and /ar/play-rabona/index.html the redirect
target is the production affiliate link:

   https://www.time4bets504.com/

Both loaders point to this destination via meta-refresh (1.5s) + JS
fallback. No change needed before deploy.

----------------------------------------------------------
4. ASSETS NOTE
----------------------------------------------------------
All image assets sit in /assets/ and are shared between EN and AR.

   logo.webp        - Provided Rabona brand logo (375x200, red bg, white wordmark
                      with yellow accent under "O" - matches official Rabona brand)
   favicon.ico      - Provided Rabona favicon
   hero-*.webp      - Hero football imagery (kept from template; replace if you
                      want Rabona-specific creative)
   live-betting-*   - Live betting visual
   multi-sports-*   - Sports markets visual
   bonus-dinar-*    - Bonus visual (renamed from bonus-naira; image may still
                      reflect generic currency notes - replace before deploy if
                      you want Kuwaiti dinar-specific creative)
   rabona-app-phone-* - Phone mockup (renamed from sportybet-app-phone;
                        the phone screen may still show the previous brand
                        UI - replace this asset with a Rabona-branded screen
                        capture before deploy for full brand consistency)

Path conventions:
   - Root EN pages:        assets/foo.webp        styles.css        script.js
   - Inner EN pages:       ../assets/foo.webp     ../styles.css     ../script.js
   - AR home (/ar/):       ../assets/foo.webp     ../styles.css     ../script.js
   - AR inner pages:       ../../assets/foo.webp  ../../styles.css  ../../script.js

----------------------------------------------------------
5. BRAND TOKENS (in styles.css)
----------------------------------------------------------
   --red:         #d50032   Header bar, primary brand red (matches Rabona logo bg)
   --red-bright:  #ff2e58   Hover lifts
   --red-deep:    #a8002a   Pressed states
   --yellow:      #ffea00   Primary CTA fill (Register, Bet now), accent
   --yellow-bright:#fff540  Primary CTA hover
   --yellow-deep: #d9c800   Primary CTA active
   --yellow-soft: #ffc629   Secondary yellow (HOT badge, soft accents)
   --dark-text:   #0a0a0a   Text color on yellow CTAs (legibility)
   --bg:          #070b14   Page background
   --surface:     #0f1521   Card background
   --text:        #f3f5f9   Body text
   --muted:       #98a4b6   Secondary text

CTA color rationale: primary buttons use yellow gradient with dark text to
match the official Rabona site's "Join us now" yellow button style. Red is
reserved for the header band and accent states.

----------------------------------------------------------
6. SEO NOTES
----------------------------------------------------------
- All pages have unique title, description, keywords (EN in English, AR in Arabic)
- index.html (EN) and ar/index.html include Organization + WebSite schema
- contact/index.html and ar/contact/index.html include FAQPage schema
- canonical set on every page
- hreflang set on every page: en + ar + x-default (pointing to EN)
- og:locale: en_KW on EN, ar_KW on AR (with en_KW as og:locale:alternate on AR)
- 18+ messaging in footer of every page (EN: "18+", AR: "+18")
- /play-rabona/ and /ar/play-rabona/ both noindex,nofollow + disallowed in robots
- Sports + casino entertainment positioning (Rabona is a dual-vertical brand
  unlike a sports-only template; AR home references this explicitly, EN copy
  stays sports-focused in the main funnel)
- Honest legality framing: no claim of in-country license; user responsibility
  to know local rules; operator framed as "within the regulatory frame of the
  markets it serves"

----------------------------------------------------------
7. LOCALIZATION NOTES
----------------------------------------------------------
EN copy targets a Kuwait audience:
  - Brand: Rabona Kuwait / Rabona Kuwait City (alternate name)
  - Country code: +965
  - Currency context: Kuwaiti Dinar (KWD)
  - Local leagues referenced: Kuwaiti Premier League, AFC Asian Cup,
    AFC Champions League
  - Local clubs referenced on homepage: Al Kuwait SC, Al-Arabi, Qadsia SC
  - International coverage retained: EPL, La Liga, UCL, NBA, ATP/WTA

AR copy is a direct localized translation:
  - Brand transliteration: رابونا
  - lang="ar" dir="rtl" on every AR page
  - All UI strings, headings, body copy, FAQ schemas, alt text translated
  - Currency notes: "دنانير كويتية" / "دينار"
  - Country code shown as 965+ (Arabic convention places + after digits in
    body text, though the schema uses the same +965 numeric form)
  - 18+ rendered as +18 in Arabic (RTL convention)

CSS is shared. AR pages rely on the same stylesheet with `dir="rtl"` at the
html element. No CSS modifications were made for AR.

----------------------------------------------------------
8. DEPLOY CHECKLIST
----------------------------------------------------------
[ ] Confirm production domain is rabona-kuwait.com (else search-and-replace
    in sitemap.xml + all HTML)
[ ] Verify logo.webp + favicon.ico render correctly (already embedded)
[ ] Replace rabona-app-phone.webp / -240.webp with a Rabona-branded phone
    mockup if you want full brand consistency in the app section
[ ] Optionally replace bonus-dinar.webp / -280.webp with Kuwaiti dinar
    creative
[ ] Submit sitemap.xml in Search Console
[ ] Verify hreflang setup in Search Console (International Targeting)
[ ] Spot-check responsive layout at 360px, 768px, 1280px
[ ] Spot-check AR pages render RTL correctly
[ ] Verify FAQPage schema validates for both contact pages
[ ] Check that all internal nav links work in both EN and AR
[ ] Confirm /play-rabona/ + /ar/play-rabona/ redirect within ~1.5s to
    https://www.time4bets504.com/ (production affiliate URL — no change needed)


Content update 2026-06-11: global rewrite completed, informational blocks reordered, FAQ/checklist blocks added, metadata updated for Rabona Kuwait branded queries.
