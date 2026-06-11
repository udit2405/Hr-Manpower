# Hr-Manpower — photo of the manpower form → filled Excel

Live page: **https://udit2405.github.io/Hr-Manpower/**

Upload a photo of the handwritten Daily Manpower Report, and the AI reads it and
fills your Excel template — values land in the right cells, totals calculate
themselves, and any row whose numbers don't add up to its Total is flagged red
for a quick check before download.

## Zero-setup option: ChatGPT mode

No key, no new account. On the page: click **Copy instructions** → open
chatgpt.com → attach the form photo, paste, send → copy ChatGPT's whole
reply → paste it back on the page → review → download the filled Excel.
Works with any normal (even free) ChatGPT account.

## One-time setup for one-click mode (you, ~3 minutes)

1. **Get a free AI key** — go to https://aistudio.google.com/apikey (sign in
   with your normal Google account), click *Create API key*, copy it (starts
   with `AIza`). Free, no credit card.
2. **Add your blank Excel template to this repo** — on the repo page click
   *Add file → Upload files*, upload your blank report file named exactly
   `template.xlsx`. The page then loads it automatically so nobody has to
   upload the Excel again.
3. *(Optional, recommended)* In Google Cloud → Credentials, restrict the key
   to website `udit2405.github.io/*` so it works only on this page.

## Sharing with your boss (zero setup for him)

Send him this link **once**:

```
https://udit2405.github.io/Hr-Manpower/#k=PASTE_YOUR_KEY_HERE
```

Opening it saves the key into his browser automatically. From then on the
plain link works: open page → upload photo → Extract → glance at any red
rows → Generate Excel → Download. No sign-ups, no keys, nothing to type.

(Alternative: paste the key into the `BUILTIN_KEY` line near the top of the
script in `index.html` — then even the first link is the plain one.)

There is no sign-in and no popup anywhere — once the link is opened once,
the page is permanently connected on that browser.

## Accuracy

Uses Gemini 2.5 Pro for reading. Every row is cross-checked against its Total
column; mismatches show red on the review screen so mistakes can't slip into
the Excel unnoticed. For best results photograph the form straight-on in good
light.
