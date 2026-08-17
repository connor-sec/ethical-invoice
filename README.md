# Ethical Invoice Generator

A fully local, privacy-respecting invoice generator designed for **authorized red teaming and social engineering engagements**.

> **⚠️ Authorized Use Only**  
> This tool is intended exclusively for legitimate security testing, red team exercises, penetration testing, and security awareness programs conducted under proper written authorization. Unauthorized use for fraud, phishing without consent, or any illegal activity is strictly prohibited and may violate applicable laws.

---

## How to Print / Generate PDF

1. Fill out the invoice (company details, line items, addresses, signature, etc.).
2. Click the **Print / Download PDF** button.
3. In the browser print dialog:
   - Destination → **Save as PDF** (or “Microsoft Print to PDF”)
   - Layout → **Portrait**
   - Margins → **None** or **Minimum** (recommended for clean edges)
   - Background graphics → **Enabled** (so colors and the logo print correctly)
4. Save the multi-page PDF.

**Tip:** When multiple service addresses are added, each address automatically becomes its own page with a sequential invoice number.

---

## Purpose

Realistic invoices are a common and highly effective pretext in social engineering and physical security assessments. This generator helps red teamers and security professionals create professional-looking invoices that can support scenarios such as:

- Pretexting as vendors, service providers, or contractors
- Multi-location / multi-site engagement simulations
- Physical access testing (service invoices for facilities, HVAC, IT, cleaning, etc.)
- Security awareness training and phishing simulations (with proper authorization)
- Tabletop exercises and purple team activities

Everything runs entirely in the browser. **No data is ever sent to a server.**

---

## Features

- **100% Client-Side** — No backend, no accounts, no telemetry. Your data never leaves the browser.
- **Multi-Address Support** — Add up to **10 service locations / offices**. When you print, the tool generates a separate invoice page for each address (with sequential invoice numbers if desired).
- **Professional Layout** — Clean, modern invoice design inspired by popular online generators.
- **Logo Upload** — Add a company logo that appears on the printed invoice.
- **Line Items** — Flexible quantity / rate / amount fields (editing the amount automatically adjusts the rate).
- **Tax & Discount** — Percentage tax rate + flat discount.
- **Multi-Currency** — Select from common currencies.
- **Signature Block** — Point-of-contact name, title, authorizing party, date, and a customizable cursive-style signature (font + size).
- **Notes / Payment Instructions** — Free-text area for terms or additional context.
- **Local Drafts** — Save and load drafts using browser `localStorage`.
- **Print to PDF** — Use the browser’s native print dialog to produce a multi-page PDF (one page per service address).

---

## Quick Start

1. Clone or download this repository.
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
3. Fill in the invoice details.
4. Optionally add service addresses (up to 10).
5. Click **Print / Download PDF** and choose “Save as PDF” in the print dialog.

No installation, no dependencies, no build step.

---

## Multi-Address Printing Behavior

- If you add **no** service addresses → one invoice page is generated.
- If you add **1–10** addresses → one invoice page is generated **per address**.
- Invoice numbers can auto-increment across the pages when multiple addresses are present.
- Each page clearly shows the corresponding **Service Address / Location**.

This is particularly useful for engagements involving multiple sites, campuses, or regional offices.

---

## Ethical & Legal Guidelines

This tool exists to support **defensive** security work. Users must:

1. Have **explicit written authorization** from the target organization (or be operating under an approved red team / purple team scope).
2. Comply with all applicable local, state, and federal laws.
3. Use generated invoices only within the boundaries of the authorized engagement.
4. Never use this tool to commit fraud, unauthorized access, or any other illegal activity.

The authors and contributors accept no liability for misuse.

---

## Technical Details

| Aspect              | Detail                                      |
|---------------------|---------------------------------------------|
| Stack               | Single HTML file (HTML + CSS + Vanilla JS)  |
| Storage             | Browser `localStorage` only (optional)      |
| Network             | None — works fully offline                  |
| Dependencies        | Zero                                        |
| Browser Support     | Modern evergreen browsers                   |
| Max Service Addresses | 10                                        |

---

## Privacy

- No analytics
- No external fonts or scripts (except system fonts)
- No cookies beyond what the browser itself may use
- Logo images and all invoice data stay in memory / localStorage on your machine

---

## License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2026 Connor Haft

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
