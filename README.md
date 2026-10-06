# Tender Package Builder (AI DevFest Vibe Coding)

- Name / Registration no.: Qazi Ferdowsi Jahan Yarin
- Live link (HTTPS): <your vercel.app URL>
- Run: static site, no build. Open `index.html` or deploy the folder to Vercel (Framework: Other, no build command).
- Main features: load requirements.json, upload PDFs (non-PDF and damaged/encrypted files rejected), match/unmatch, expiry dates, live statuses, duplicate detection by SHA-256, Bangla/English switch, combined PDF with English cover page and `<tender_id> | Page X of Y` footer in an added bottom margin (never covers content), download as `<tender_id>_Package.pdf`.
- Bonus: safe handling of bad files.
- Known problems: Bangla text is not drawn on the PDF cover (cover is English); pages with a /Rotate flag may not embed rotated.
- AI tools used: Claude
- Most useful prompt: <paste yours>
