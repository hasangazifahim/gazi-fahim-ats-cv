# Implementation Plan: ATS-Friendly CV for Gazi Fahim Hasan

Create a modern, ATS-compliant, high-conversion Curriculum Vitae (CV) for **Gazi Fahim Hasan** using data, metrics, case studies, and executive portrait photography extracted from his portfolio.

## User Review Required

> [!IMPORTANT]
> **ATS Compatibility & Image Handling**:
> True ATS systems (Workday, Greenhouse, Lever, Taleo) parse resumes primarily as plain text streams. Having graphics in non-standard placements can confuse older ATS scanners.
> To give you the best of both worlds, we will design:
> 1. **Modern Executive Format (with Portrait)**: Includes your professional grayscale headshot in the header, formatted cleanly so text streams parse top-to-bottom without column interleaving.
> 2. **Strict ATS Text-Only Toggle**: In the interactive viewer, you can toggle off the photo with one click for zero-risk submissions to strict ATS portals.
> 3. **Compiled PDF & Plain-Text Export**: Pre-compiled PDF ready to submit, plus an ATS plain-text copy feature.

## Proposed Changes

### CV Application & PDF Build (`/Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project`)

#### [NEW] [index.html](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/index.html)
- Clean, semantic HTML5 structure with standard ATS headings:
  - `Header`: Gazi Fahim Hasan, SEO Executive & Technical SEO Specialist, verified contact details (email, phone, location, portfolio, GitHub, LinkedIn placeholder).
  - `Professional Summary`: Synthesizes CSE computational background with demonstrable SEO results (+340% traffic, 1.5K+ top keywords, 770% ROI).
  - `Core Competencies`: Categorized keyword matrix (Technical SEO, On-Page & Semantic SEO, Off-Page & Authority, Analytics & Auditing, Web Technologies).
  - `Work Experience`: Action-verb, metric-driven CAR/STAR bullet points for Scaleup Ads Agency, Freelance SEO Consulting, and United Interpreters.
  - `Key SEO Achievements & Case Studies`: Quantifiable highlights (E-commerce +340%, SaaS 98/100 Lighthouse & +210% signups, Local Map Pack #1 in 8 regions).
  - `Education`: B.Sc. in Computer Science & Engineering from Sonargaon University.
  - `Academic & Professional References`: Contact details for CSE Department Head & Coordinator.
- Control Toolbar:
  - "Download PDF" / "Print CV" (triggers `@media print` dialog or serves pre-rendered PDF)
  - "Toggle Photo" (switch between Executive format with headshot and Pure Text ATS format)
  - "Copy Plain Text (ATS)" (copies clean formatted markdown/text directly to clipboard for online job applications)

#### [NEW] [styles.css](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/styles.css)
- Strict ATS typographic principles:
  - System font fallbacks (Inter, Arial, Helvetica, sans-serif) ensuring standard rendering across all ATS PDF converters.
  - Linear layout that reads sequentially from top to bottom, avoiding complex nested float tables that break parsers.
  - `@media print` styling: Exact A4 / US-Letter dimensions, page breaks avoided inside experience items, print-safe margins, clean contrast.

#### [NEW] [assets/images/gazi-portrait.png](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/assets/images/gazi-portrait.png)
- High-resolution studio portrait copied from the portfolio assets.

#### [NEW] [generate_pdf.js](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/generate_pdf.js)
- Automated script using Google Chrome headless print-to-pdf to generate:
  - `Gazi_Fahim_Hasan_ATS_CV.pdf`
  - `Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf`

---

### Portfolio Integration (`/Users/GaziFahim/.gemini/antigravity-ide/scratch/portfolio`)

#### [MODIFY] [frontend/assets/Gazi-Fahim-Resume.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/portfolio/frontend/assets/Gazi-Fahim-Resume.pdf)
- Replace or provide the updated ATS-friendly PDF so the portfolio's "Download CV" buttons immediately download the high-converting, metric-rich ATS resume.

## Verification Plan

### Automated Tests
1. **Headless Chrome PDF Compilation**:
   - Run `generate_pdf.js` to compile the PDF.
2. **ATS Text Parseability Test**:
   - Run a Python `pypdf` test script that extracts text from the newly generated PDF and verifies:
     - All section headings ("SUMMARY", "EXPERIENCE", "EDUCATION", "SKILLS", "REFERENCES") are parsed correctly without scrambled words or strange spacing.
     - Contact details and key statistics (+340%, 1,500+, 770%) are cleanly extracted in linear order.
3. **Visual Inspection**:
   - Use browser subagent to review the rendered CV in desktop and print preview modes, verifying margins, typography, and layout balance.
