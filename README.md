# ME204 Final Project: Growth Strategies Across Technology, Pharma, and Energy

| GitHub username | LSE ID      |
| ---------------- | ----------- |
| `silyzch`         | `250088575` |

## Overview

This project investigates how companies in the Technology, Healthcare, and Energy sectors fund and sustain growth. Using financial statement data collected from the SEC EDGAR Company Facts API, it compares companies' investment in R&D, profitability, and cash generation to understand how growth strategies differ across industries.

The project answers the following question:

**How do Technology, Healthcare, and Energy companies differ in their strategies for supporting future growth, based on their investment in R&D, profitability, and free cash flow generation?**

Nine companies are covered, three per sector:

- **Technology:** Microsoft, Nvidia, Apple
- **Healthcare:** Pfizer, Johnson & Johnson, Stryker
- **Energy:** ExxonMobil, Chevron, Duke Energy

## Data sources

**Main source:** [SEC EDGAR Company Facts API](https://www.sec.gov/edgar/sec-api-documentation) — a public API providing structured XBRL financial data (revenue, R&D, capex, cash flow, etc.) reported by every US-listed company. No API key is required, but SEC requests require a `User-Agent` header identifying the requester (name and email).

No supplementary static datasets were used; all financial data comes directly from the API.

To ensure comparability across sectors, the analysis was restricted to the 2018–2024 period, where all nine companies had available SEC XBRL data for the selected financial concepts.

## How to reproduce

1. Clone the repository and `cd` into it.
2. Create a virtual environment and install dependencies:
```bash
   python -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   pip install -r requirements.txt
```
3. Copy `.env.example` to `.env` and fill in your own contact details (no SEC API key is required — this is only used to build the request header SEC asks for):