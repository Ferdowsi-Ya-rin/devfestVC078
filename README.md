# Tender Package Builder (AI DevFest Vibe Coding)

- Name / Registration no.: Qazi Ferdowsi Jahan Yarin
- Live link (HTTPS): https://ferdowsiyarin.vercel.app/
- Run: static site, no build. Open `index.html` or deploy the folder to Vercel (Framework: Other, no build command).
- Main features: load requirements.json, upload PDFs (non-PDF and damaged/encrypted files rejected), match/unmatch, expiry dates, live statuses, duplicate detection by SHA-256, Bangla/English switch, combined PDF with English cover page and `<tender_id> | Page X of Y` footer in an added bottom margin (never covers content), download as `<tender_id>_Package.pdf`.
- Bonus: safe handling of bad files.
- Known problems: Bangla text is not drawn on the PDF cover (cover is English); pages with a /Rotate flag may not embed rotated.
- AI tools used: Claude
- Most useful prompt:
the first one is the problem statement for the vibe coding i'm participating
the other two are the files i already pushed on the github
but the html file doesn't do after the validation is checked, i need it to do the next step, the pdf generator, which is explained detailly on the statement, what should be on the output
following is the roadmap I created
try making the next steps work on the same file as index.html, which i'll refresh on the repo


              REQUIREMENTS.JSON
                    │
                    ▼
          ┌──────────────────┐
          │ Tender Information│
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ Required Docs    │
          │ ordered 1...N    │
          └────────┬─────────┘
                   │
                   │ MATCH
                   ▼
          ┌──────────────────┐
          │ Uploaded PDFs    │
          │ + page counts    │
          │ + duplicates     │
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ Validation       │
          │                  │
          │ Missing          │
          │ Expiry needed    │
          │ Expired          │
          │ Not provided     │
          │ OK               │
          └────────┬─────────┘
                   │
             no blocking issues
                   │
                   ▼
          ┌──────────────────┐
          │ PDF GENERATOR    │
          │                  │
          │ Cover            │
          │ + Documents      │
          │ + Footer         │
          │ + Page X of Y    │
          └────────┬─────────┘
                   │
                   ▼
       T-2026-0417_Package.pdf
