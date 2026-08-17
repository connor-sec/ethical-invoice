# Ethical Invoice

A fully local, privacy-respecting invoice generator designed for **authorized red teaming and social engineering engagements**. Runs entirely in your browser — no network, no dependencies, nothing leaves the page.

Maintained by [@connor-sec](https://github.com/connor-sec).

<p align="center">
    <img src="Ethical_Invoice_logo.png" alt="Ethical Invoice" width="400">
</p>

> **Download:** the latest single-file build is available from the **Packages** tab (or the [Releases](https://github.com/connor-sec/ethical-invoice/releases) page) — one `.html` file, ready to open.

## Usage

Open `Ethical_Invoice.html` in any modern browser (Chrome, Firefox, Edge, Safari). That’s it — no install, no server, no internet required.

## ⚠️ Authorized use only — for security research and authorized testing

**Authorized use.** This tool is intended exclusively for legitimate security testing, red team exercises, penetration testing, purple team activities, and security awareness programs conducted under proper written authorization. Use it only within an expressly authorized and documented testing scope.

**Illegal use is prohibited.** Creating or distributing invoices for fraud, unauthorized access, phishing without consent, or any other illegal activity is strictly forbidden and may violate applicable laws. Authorization must come from the target organization (or from ownership / explicit permission to test).

**No data collection.** The tool runs entirely in your browser. It does not transmit, store, or process any invoice data outside of your local machine (optional `localStorage` drafts stay on your device only).

**Warranty.** Provided “as is”, without warranty of any kind. This is not legal advice. The authors accept no liability for misuse.

## Why this exists

Realistic invoices are one of the most effective and commonly used pretexts in social engineering and physical security assessments. Public online invoice generators are convenient but require sending data to third-party servers and often leave traces.

This project exists to give red teamers and security professionals a clean, fully offline alternative: a single HTML file you can keep on a laptop or USB drive, open anywhere (internet or not), and use to produce professional multi-page invoices for authorized engagements — especially those involving multiple service locations or sites.

Nothing is ever uploaded. Everything stays under your control.

## Features

- **100% client-side** — No backend, no accounts, no telemetry. Your data never leaves the browser.
- **Multi-address support** — Add up to **10 service locations / offices**. Printing automatically generates one invoice page per address (with sequential invoice numbers when multiple addresses are present).
- **Professional layout** — Clean, modern invoice design suitable for real engagements.
- **Logo upload** — Add a company logo that appears on the printed pages.
- **Flexible line items** — Quantity, rate, and amount fields (editing the amount automatically adjusts the rate).
- **Tax & discount** — Percentage tax rate + flat discount support.
- **Multi-currency** — Select from common currencies.
- **Signature block** — Point-of-contact name, title, authorizing party, date, and a customizable cursive-style signature (font + size).
- **Notes / payment instructions** — Free-text area for additional context or terms.
- **Local drafts** — Save and reload drafts using browser `localStorage`.
- **Print to PDF** — Native browser print dialog produces a multi-page PDF.

## How to Print / Generate PDF

1. Fill out the invoice (company details, line items, service addresses, signature, etc.).
2. Click the **Print / Download PDF** button.
3. In the browser print dialog:
   - Destination → **Save as PDF** (or “Microsoft Print to PDF”)
   - Layout → **Portrait**
   - Margins → **None** or **Minimum**
   - Background graphics → **Enabled** (so colors and the logo appear correctly)
4. Save the file.

**Tip:** When multiple service addresses are added, each address becomes its own page with a sequential invoice number.

## Multi-Address Behavior

- **0 addresses** → one invoice page is generated.
- **1–10 addresses** → one invoice page is generated **per address**.
- Invoice numbers can auto-increment across pages when multiple addresses are present.
- Each page clearly shows the corresponding **Service Address / Location**.

This is especially useful for multi-site or multi-campus engagements.

## Privacy & Technical Details

| Aspect                  | Detail                                      |
|-------------------------|---------------------------------------------|
| Stack                   | Single HTML file (HTML + CSS + Vanilla JS)  |
| Network                 | None — works fully offline                  |
| Dependencies            | Zero                                        |
| Storage                 | Optional browser `localStorage` only        |
| Max service addresses   | 10                                          |
| Browser support         | Modern evergreen browsers                   |

- No analytics  
- No external fonts or scripts (except system fonts)  
- Logo images and all invoice data remain in memory / localStorage on your machine  

## License

This project is released under the [MIT License](LICENSE).
