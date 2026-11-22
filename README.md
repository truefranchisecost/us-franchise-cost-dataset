# U.S. Franchise Startup Cost & Disclosures Dataset (2026 Edition)

An open, structured financial disclosures dataset compiled from official Franchise Disclosure Documents (FDDs) registered with state regulatory authorities (including Minnesota, California, and Wisconsin state databases).

Published by **[True Franchise Cost](https://truefranchisecost.com)**.

## Overview

Franchise Disclosure Documents (FDDs) contain critical unit-level economic metrics required under Federal Trade Commission (FTC) franchise regulations. However, these documents are typically published as dense, multi-hundred-page unstructured PDFs.

This dataset aggregates and structures verifiable disclosures across 220+ major U.S. franchise brands into a clean, machine-readable CSV format.

## Dataset Contents

The primary dataset file is `franchise-cost-dataset.csv`.

### Schema & Field Definitions

| Column | Type | Description | FTC FDD Source |
| :--- | :--- | :--- | :--- |
| `brand` | String | Legal commercial trade name of the franchise | Item 1 |
| `category` | String | Industry category (e.g., `food`, `fitness`, `home-services`, `cleaning`, `retail`, `children`, `senior-care`, `automotive`, `business-services`) | Editorial taxonomy |
| `fdd_year` | Integer | Reporting FDD disclosure year | Cover Page |
| `fdd_issue_date` | Date (`YYYY-MM-DD`) | State registration / issuance date of filing | Cover Page |
| `item7_low` | Float / Currency | Minimum estimated initial investment outlay | Item 7 Schedule |
| `item7_high` | Float / Currency | Maximum estimated initial investment outlay | Item 7 Schedule |
| `initial_fee` | Float / Currency | Base initial franchise fee (Item 5) | Item 5 |
| `royalty` | Float (%) | Continuing royalty fee percentage (where fixed) | Item 6 Table |
| `ad_fund` | Float (%) | System-wide national advertising / brand marketing fund | Item 6 Table |
| `item19_disclosed` | Boolean | Whether franchisor provides an Item 19 Financial Performance Representation | Item 19 |
| `units_end_of_year` | Integer | Total open franchised outlets at end of reporting year | Item 20 Table 3 |
| `net_change_3yr` | Integer | 3-year net franchised outlet growth / contraction | Item 20 Table 3 |
| `source_url` | URL | Direct link to official state-filed public PDF document | State Registry |
| `last_verified` | Date | Verification date against state filing record | Audit Record |
| `initial_fee_high` | Float / Currency | Upper bound of initial franchise fee (multi-unit tiers) | Item 5 |
| `verification_status` | String | Audit verification status (`verified`, `review-required`) | TrueFranchiseCost Audit |
| `provisional_publication` | Boolean | Provisional audit flag | Audit Record |

## Data Verification & Methodology

1. **Official State Filings**: All records are sourced directly from regulatory repositories (e.g. Minnesota Commerce Department, California Department of Financial Protection and Innovation).
2. **Item 7 Capital Standards**: Excludes speculative land purchase costs where leasehold alternatives are provided by the franchisor, standardizing on typical initial turnkey cash outlay.
3. **Reproducibility**: Each brand record contains a direct URL (`source_url`) pointing to the verifiable state filing document.

## Interactive Tools & Live Directory

For interactive brand comparisons, line-by-line Item 7 cost breakdowns, and live filtering:
- Explore the interactive explorer at [truefranchisecost.com](https://truefranchisecost.com)
- Line-by-line expense tables: `https://truefranchisecost.com/franchise/<brand-slug>`
- Live dataset download: [https://truefranchisecost.com/data/franchise-cost-dataset](https://truefranchisecost.com/data/franchise-cost-dataset)

## License

This dataset is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to share, adapt, and build upon this material for commercial or academic research, provided appropriate attribution is given to [True Franchise Cost](https://truefranchisecost.com).
