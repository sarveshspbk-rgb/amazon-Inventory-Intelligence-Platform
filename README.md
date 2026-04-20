# Amazon Inventory Intelligence Platform

> **Disclaimer:** This is an independent portfolio project built for educational purposes. It is not affiliated with, endorsed by, or connected to Amazon in any way. All data shown is illustrative mock data.

---

## What is this?

This is a single-page web dashboard I built to demonstrate how a large e-commerce company like Amazon might approach the problem of smarter inventory management. The idea is simple: instead of just tracking stock levels, what if the system could also factor in the weather outside, upcoming cultural festivals, regional demographics, and real-time logistics disruptions — and then automatically tell you what to reorder, when, and how much?

The platform is entirely frontend — one HTML file, no backend, no database. All the data is illustrative, but the logic and UI are designed to mirror how a real operations dashboard might actually work.

---

## What's inside

The dashboard is split into five sections, each focusing on a different layer of the inventory problem:

### Morning Briefing (Overview)
The first thing you see when you open the platform. It shows five key metrics at a glance — total SKUs being monitored, how many are at risk of running out, how many are overstocked, the current forecast accuracy, and how many units need to be reordered today. Below that, there's a bar chart ranking the top 10 products by stockout risk this week, a demand vs. supply trend line for the last 30 days, and a live alerts feed that surfaces things like incoming weather events, approaching festivals, and shipment delays.

### Contextual Demand Signals
This is the section that makes the platform feel different from a standard inventory tool. It pulls together three types of external signals:

- **Weather Intelligence** — Shows a 7-day forecast for each fulfilment centre (Mumbai, Dublin, Berlin) and maps the weather to likely product demand shifts. For example, heavy rain in Mumbai pushes up demand for umbrellas and rainwear, while cold snaps in Berlin drive space heater sales.
- **Cultural Calendar** — Tracks major shopping events across the regions served (Diwali in India, Black Friday in Germany, Christmas in Ireland, Prime Day) and shows which product categories are expected to see the biggest lifts.
- **Regional Demographics** — Visualises the age breakdown of each territory's customer base, with a hypothesis about what that means for product mix.

### Inventory Planner
A filterable table of SKUs showing current stock levels, reorder points, recommended order quantities, and lead times. You can filter by critical items only, overstock only, or view everything at once. At the bottom sits the **What-If Scenario Simulator** — the standout feature. You pick a contextual event (Diwali, Black Friday, a severe storm, St. Patrick's Day) and dial in an expected demand lift percentage, and the simulator recalculates how many additional units you'd need to order across the affected SKUs, in real time.

### FC Network View (Warehouse)
A bird's-eye view of the three fulfilment centres — BOM1 in Mumbai, DUB2 in Dublin, and BER3 in Berlin. Each node shows its current capacity utilisation as a circular gauge, total stock value, number of critical SKUs, and the dominant product category. At the bottom, there's a transfer recommendation that flags when it makes sense to move surplus stock between nodes to ease pressure at high-capacity locations.

### Analytics & Reports
Charts and breakdowns for deeper analysis — inventory distribution by category, a 90-day stockout event timeline, and a regional performance comparison. There's also a mock export button for reporting.

---

## How it shows business impact

Every screen in this dashboard is designed around a real operational question that costs money if answered badly:

| Problem | What this platform addresses |
|---|---|
| Stockouts during peak demand | The risk chart and simulator give advance warning so reorders happen before shelves go empty |
| Overstocking slow-moving inventory | Overstock flags and warehouse capacity gauges identify where capital is tied up unnecessarily |
| Ignoring external demand drivers | Weather and cultural calendar signals let planners get ahead of demand surges, not react to them |
| Reacting too late to logistics delays | The alerts feed surfaces shipment disruptions in time to act on them |
| Poor cross-network stock distribution | The transfer recommendation logic identifies imbalances between fulfilment centres |

In a real-world context, getting even one of these right — say, avoiding a single major stockout during Diwali or Black Friday — could protect significant revenue. The platform is designed to make that kind of proactive decision-making the default, not the exception.

---

## Tech stack

- Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools
- [Chart.js](https://www.chartjs.org/) for all visualisations
- Google Fonts (Inter) for typography
- Fully responsive — works on desktop and tablet

---

## Running it

No installation required. Just open `index.html` in any modern browser and it works.

---

## About

Built by **Sarvesh Babu** as a portfolio project during the MSc in Data Analytics at Dublin City University. The goal was to demonstrate product thinking, UI design, and data storytelling — specifically how operational data and external signals can be combined to drive better business decisions in supply chain and inventory management.
