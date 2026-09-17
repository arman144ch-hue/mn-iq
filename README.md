# Mn-IQ — AI-Driven Manganese Intelligence & Production Risk Platform

Smart India Hackathon 2026 · Problem statement **SIH26009** · Theme: Space Technology · Category: Software

**Observe → Verify → Prioritise.** Mn-IQ observes manganese mine surface activity from space, compares it with available reported production, and ranks areas for further exploration. It is a decision-support prototype: it flags and explains, and a person decides.

## Live demo
Open the website: `https://<your-github-username>.github.io/<repo-name>/`

## Current status (honest)
| Part | Status |
|---|---|
| Website, go / no-go check, comparison logic, grade scenario | Working |
| Demo mode data (fictional mine) | SIMULATED |
| Tests A–F (reported vs observed, blind deposit, baseline, monsoon, grade, uncertainty) | NOT RUN yet |
| Real mine results | Not loaded yet |
| Operator data, live Earth Engine queries | ROADMAP |

No result shown on the site is a real measurement until a results file from the pipeline is loaded and the Validation centre says so.

## How it works
1. Pipeline notebooks (Google Colab / Google Earth Engine) process public data: Sentinel-1, Sentinel-2, ASTER/Landsat, DEM, GSI Bhukosh, IMD, IBM, company annual reports.
2. They export one file, `mniq_results.json` (format shown on the site's Data page).
3. The website loads that file and shows monitoring, comparison, exploration priority and validation results.

## Repository layout (planned)
```
index.html          the website (single file, runs offline)
data/               mniq_results.json exported by the pipeline (added when results exist)
notebooks/          Earth Engine / Colab scripts (added as they are written)
```

## Limits
- Satellites observe surface activity, not underground manganese.
- Exploration outputs are ranked surface targets, not certified reserves; drilling is required.
- Public production data may be annual or not mine-level.
- Divergence between observed and reported figures is a review signal, not proof of incorrect reporting.
- Grade and equipment data are simulated.

## Team
Ekta Goyal (lead) · Kratika Sharma · Kiran Lalchandani · Astik Khandelwal · Vipul Sharma · Arman Meena
