# Thread Consumption Planner

A single-page web app for planning **sewing thread consumption** per garment and per order.
It runs entirely in the browser – no server, no build step.

## Features
- **Garment & Fabric** – buyer, job/style, order quantity, sizes, fabric weight (Light / Medium / Heavy), garment photo and company logo.
- **Threads** – up to 8 thread/colour lines with cone length, price and remarks.
- **Operations** – stitch type, SPI, rows and length per operation; a separate thread for every needle, bobbin, looper and cover.
- **Result** – metres per piece, cones for the order, cost per piece and order value, with bar breakdowns.
- **Summary Report** – the thread consumption report layout (Print or Export PDF).
- **Calculation & Ratios** – editable wastage rules (qty above 5,000 pcs = 5 %, otherwise 8 %), size adjustment, thread factor by SPI and thread split per stitch.
- **Export** – PDF report, and a styled Excel workbook with live formulas.
- Entries are saved automatically in the browser (`localStorage`).

## Run locally
Open `index.html` in a browser (needs internet once, for the PDF / Excel libraries from cdnjs).

## Publish with GitHub Pages
1. Create a repository and push these files to the `main` branch.
2. Repository **Settings → Pages → Build and deployment**.
3. Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)**, then Save.
4. After a minute the app is live at `https://<your-user>.github.io/<repo-name>/`.

```bash
git init
git add .
git commit -m "Thread Consumption Planner"
git branch -M main
git remote add origin https://github.com/<your-user>/<repo-name>.git
git push -u origin main
```

## Files
| Path | Purpose |
|---|---|
| `index.html` | The whole app (HTML, CSS, JavaScript, data tables, default images) |
| `excel/Sewing_Thread_Consumption_Master.xlsx` | Excel master workbook (Light / Medium / Heavy calculator in one file) |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Libraries (loaded from cdnjs)
jsPDF 2.5.1, jsPDF-AutoTable 3.8.2, ExcelJS 4.4.0, SheetJS 0.18.5 (fallback export).

## Before making the repository public
- Thread factors and splits come from the A&E ANECALC calculators (Light / Medium / Heavy weight files). Confirm you may publish them.
- `index.html` embeds a sample company logo, garment photo and report text from a customer report. Replace or remove them (Garment & Fabric tab, or edit the defaults) if they are confidential.
- A private repository keeps everything internal (GitHub Pages on private repos needs a paid plan).
