# Vendor Report for Aspire (Power BI) — MIS446 Data Visualization

An interactive **Power BI vendor evaluation dashboard** built for Aspire’s sourcing/procurement workflow. The report helps leadership and the Sourcing team make **fast, data-informed sourcing decisions** aligned with service strategy and risk management. :contentReference[oaicite:0]{index=0}

## Problem
Aspire needs a clear, consistent way to **compare vendors across multiple criteria** (quality, capacity, reputation, support, proximity), while also filtering by **Tier / Material / Location** to create shortlists quickly and reduce sourcing risk. :contentReference[oaicite:1]{index=1}

## Objectives
- Build a visual, interactive tool to support **vendor evaluation + shortlisting**
- Provide a high-level supplier portfolio overview (KPIs + distribution)
- Enable deep comparisons by criteria and vendor ranking
- Add a simulation page to test different sourcing strategies by adjusting weights :contentReference[oaicite:2]{index=2}

## End Users
- **Sourcing / Procurement team**: daily search, compare, shortlist vendors  
- **Management**: high-level view of supplier portfolio and risks  
- **QA / Finance / Compliance**: performance reviews and partner selection discussions :contentReference[oaicite:3]{index=3}

## Dashboard Logic (How it Works)
### KPIs & Filters
- Total suppliers, distribution by **Tier / Location / Component**
- Average scores by **Quality, Capacity, Reputation, Support, Proximity**
- Top vendors by **overall weighted score** :contentReference[oaicite:4]{index=4}

### Ranking Logic
**Overall Vendor Score = weighted sum of evaluation criteria**  
Vendors are sorted descending by total score, with filters applied (Tier, Component, Location). :contentReference[oaicite:5]{index=5}

## Report Pages
### Page 1 — Supplier Overview & Location
Executive snapshot for situational awareness:
- KPI cards (e.g., total suppliers, average score)
- Supplier distribution charts (Tier, company size)
- Map view for geographic distribution
- Material/component breakdown for deeper review :contentReference[oaicite:6]{index=6}

### Page 2 — Vendor Comparison & Shortlisting
Detailed evaluation and ranking:
- Radar chart for multi-criteria comparison
- KPI cards by criteria (Quality, Capacity, Support, Reputation)
- Ranking tables: top performers by quality and total score
- Slicers for **Company / Tier / Material components** :contentReference[oaicite:7]{index=7}

### Page 3 — Simulation / Risk (Strategic Sourcing)
Decision-making + strategy testing:
- Weight controls for **Quality, Reputation, Capacity, Support**
- Scatter plot updates in real time to show recommended vendor group
- Gauges/KPIs + recommendation panel for final suggested strategic partner :contentReference[oaicite:8]{index=8}

## Data Preparation & Modeling (Power Query + Model)
- Load from CSV and promote headers
- Clean and standardize values (e.g., Tier formatting)
- Split address → derive Province
- Create derived columns (e.g., company size category, total score)
- Create a helper table for radar categories
- Data model relationships: `List Tier` → `Initial Vendor List` / `Evaluation` (1-to-many) :contentReference[oaicite:9]{index=9}

## DAX Highlights (Examples)
- `Total Suppliers` = `DISTINCTCOUNT()`
- `Total Tier 1 Suppliers` = `CALCULATE()`
- Dynamic weighted scoring using weight parameters (Quality/Capacity/Reputation/Support)
- Top supplier ranking using `TOPN()` :contentReference[oaicite:10]{index=10}

## Key Features
- Vendor shortlisting by **Component/Material, Tier (1–4), Location**
- Multi-criteria comparison + ranking (weighted score)
- Drill-through / tooltips for vendor detail
- Strategy simulator to adjust weights and see best-fit partners instantly :contentReference[oaicite:11]{index=11}

## Repository Structure
- `Project Aspire - MIS 446.pbix` — Power BI report file
- `Aspire Presentation - Mis 446.pdf` — project presentation & documentation
- `README.md` — project overview (this file)

## How to Use
1. Open `Project Aspire - MIS 446.pbix` in **Power BI Desktop**
2. Use slicers to filter by **Tier / Material / Region / Company**
3. Review:
   - Page 1 for overview
   - Page 2 for comparison & shortlist
   - Page 3 to simulate strategy weights and select strategic partners :contentReference[oaicite:12]{index=12}

## Team (EIU — MIS446)
- Huynh Thuy Bao Tram  
- Nguyen Ngoc Minh Thu  
- Nguyen Thi Hoai Thuong  
- Nguyen Quang Truong :contentReference[oaicite:13]{index=13}
