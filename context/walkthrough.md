# Walkthrough: ATS-Friendly CV for Gazi Fahim Hasan

Created a modern, high-conversion, ATS-optimized Curriculum Vitae (CV) for **Gazi Fahim Hasan**, synthesizing portfolio data, verified performance metrics, technical case studies, and executive portrait photography.

---

## Visual Preview

![Executive Header and Contact Layout](/Users/GaziFahim/.gemini/antigravity-ide/brain/e8e1aeb0-23bd-41d5-9cc8-2f923d28664a/cv_header.png)

![Full CV Document Layout](/Users/GaziFahim/.gemini/antigravity-ide/brain/e8e1aeb0-23bd-41d5-9cc8-2f923d28664a/cv_preview.png)

---

## What Was Created & Configured

### 1. Dedicated CV Project (`cv-project`)
- **Interactive Web Viewer & Print Engine**: [index.html](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/index.html)
  - **Single `<h1>` and Standard ATS Hierarchy**: Uses verified headings (`PROFESSIONAL SUMMARY`, `CORE COMPETENCIES & TECHNICAL SKILLS`, `PROFESSIONAL EXPERIENCE`, `FEATURED SEO CASE STUDIES & IMPACT`, `EDUCATION`, `LANGUAGES`, `ACADEMIC & PROFESSIONAL REFERENCES`).
  - **One-Click Action Toolbar**:
    - **Print / Save PDF**: Direct invocation of print dialog with `@media print` CSS optimization.
    - **Download PDF**: Instant access to compiled PDF.
    - **Hide / Show Photo**: Quickly toggle between Executive Portrait format and Pure-Text ATS format.
    - **Copy ATS Plain Text**: Instant modal with clean, formatted plain text ready to paste into job application portals (Workday, Greenhouse, Lever, Taleo).
- **Typographic & Print Stylesheet**: [styles.css](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/styles.css)
  - ATS-safe system fonts with high contrast charcoal/black palette (`#111827`, `#374151`) and executive navy accents (`#1e3a8a`).
  - Strict print pagination with `page-break-inside: avoid` preventing orphaned job entries or split cards.
  - Linear DOM structure that guarantees top-to-bottom text parsing.

### 2. Compiled Production PDF Files
Two standalone PDF files generated via Google Chrome headless print-to-pdf:
1. **Executive Mode (With Photo)**: [Gazi_Fahim_Hasan_ATS_CV.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/Gazi_Fahim_Hasan_ATS_CV.pdf)
2. **Strict ATS Text-Only Mode**: [Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf)

### 3. Portfolio Asset Synchronization
Updated all resume links and files in your portfolio directory:
- [Gazi-Fahim-Resume.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/portfolio/frontend/assets/Gazi-Fahim-Resume.pdf)
- [Gazi_Fahim_Hasan_CV.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/portfolio/frontend/assets/Gazi_Fahim_Hasan_CV.pdf)
- [Gazi_Fahim_Hasan_ATS_CV.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/portfolio/frontend/assets/Gazi_Fahim_Hasan_ATS_CV.pdf)
- [Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/portfolio/frontend/assets/Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf)

---

## Validation & ATS Verification Results

We verified parseability using Python's `pypdf` parser simulating an automated Applicant Tracking System extraction pipeline:

| Test Item | Verification Criteria | Status |
| :--- | :--- | :--- |
| **Candidate Identity** | `GAZI FAHIM HASAN` | **PASS** |
| **Current Designation** | `SEO Executive & Technical SEO Specialist` | **PASS** |
| **Contact Data** | Location, Phone (`+880 1857571304`), Email, Portfolio, GitHub, LinkedIn | **PASS** |
| **Quantifiable Traffic Metric** | `+340%` average organic traffic lift | **PASS** |
| **Keyword Rankings Metric** | `1,500+` commercial keywords in Google Top 3 | **PASS** |
| **Technical Crawl Metric** | `1,200+` crawl errors fixed | **PASS** |
| **Core Competencies** | Categorized keyword groupings without table formatting | **PASS** |
| **Experience Extraction** | Linear sequential parsing of Scaleup Ads, Freelance, and United Interpreters | **PASS** |
| **Education Parsing** | `B.Sc. in Computer Science & Engineering`, Sonargaon University | **PASS** |
| **References** | Associate Professor & Head + Assistant Professor & Coordinator | **PASS** |
| **Section Headings** | Standard uppercase titles recognized cleanly without letter-spacing artifacts | **PASS** |

---

## Quick Usage Guide

1. **View in Browser**:
   Open [index.html](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/index.html) in Google Chrome or your browser of choice.
2. **Apply to Strict ATS Portals**:
   Click **"Copy ATS Plain Text"** to copy the formatted text directly, or submit [Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/Gazi_Fahim_Hasan_ATS_CV_TextOnly.pdf).
3. **Send to Recruiters / Hiring Managers**:
   Attach [Gazi_Fahim_Hasan_ATS_CV.pdf](file:///Users/GaziFahim/.gemini/antigravity-ide/scratch/cv-project/Gazi_Fahim_Hasan_ATS_CV.pdf) featuring your executive portrait.
