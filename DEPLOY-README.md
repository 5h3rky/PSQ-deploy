# Pavilion Square KL — Deploy Notes

## Before you upload

Search the whole folder for `REPLACE_ME` and fill in every hit. Nothing should
ship with a placeholder still in it.

| Token | What to put in |
|---|---|
| `REPLACE_ME_EMAIL` | A domain email, e.g. `kristy@zeonproperties.my`. **Do not ship a Gmail address.** |
| `REPLACE_ME_SSM` | Zeon Properties SSM company registration number |
| `REPLACE_ME_ENUMBER` | BOVAEP agency licence, e.g. `E (3) 1234` |
| `REPLACE_ME_DEVLICENCE` | Developer's licence number (from the developer) |
| `REPLACE_ME_APDL` | Advertising permit number (from the developer) |
| `REPLACE_ME_PERMIT_VALIDITY` | Permit validity dates |
| `REPLACE_ME_DOMAIN` | Final live domain, e.g. `https://zeonproperties.my` |
| `REPLACE_ME_DATE` | Date the privacy policy goes live |
| `REPLACE_ME_ANALYTICS_PARAGRAPH` | Describe any GA4 / Meta Pixel / Google Ads tag you install. If none, write: "We do not run any additional analytics or advertising tracking on this site." |
| `REPLACE_ME_RETENTION_PERIOD` | e.g. `24 months` |
| `REPLACE_ME_BM_NOTICE` | Either a BM translation, or: "Salinan Bahasa Malaysia boleh diperolehi dengan menghubungi kami di [email]." |

Also update the `canonical`, `og:url` and `og:image` URLs in `index.html` to the
final domain.

## Do NOT upload

- `.git/` — exposes full source history at `yourdomain.com/.git/`
- `Pavilion Square Training.pdf` — internal sales material, would be public
- `PQS Image/` — unreferenced WhatsApp screenshots
- `__MACOSX/`, `.DS_Store`

This folder already excludes them. Upload the contents of this folder only.

## After you upload (Hostinger)

1. Force HTTPS and confirm the SSL certificate is issued.
2. Set the www / non-www redirect and make sure `canonical` matches whichever
   you pick.
3. Open `yourdomain.com/.git/config` in a browser. You should get a 404. If you
   get a file, delete the directory from the server immediately.
4. Open `yourdomain.com/privacy.html` and check every link works.
5. Submit a test enquiry and confirm the email arrives with the consent
   timestamp included.

## Still needs a human decision

- **Domain.** `pavilionsquarekl-property.my` is still built from the developer's
  brand. `zeonproperties.my/pavilion-square` removes the impersonation signal
  entirely. Whatever you choose, register it to the same legal entity as the
  verified Google Ads account — a WHOIS mismatch fails advertiser verification
  on its own.
- **Written authorisation.** Get the developer's letter appointing Zeon as
  marketing agent, and written permission to use the renders and the Pavilion
  Square logo. Keep it on file — it is your evidence in a suspension appeal.
- **Press section.** The fabricated NST / The Star / The Edge cards have been
  removed and replaced with unattributed neighbourhood context. A template for
  reinstating real, linked articles is in an HTML comment at the bottom of
  `index.html`.
- **Ad copy.** Check no headline says "Official Site", "Developer Direct" or
  quotes a price the landing page does not display.
