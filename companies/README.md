# Geo Companies

A curated CSV dataset of geospatial, GIS, remote sensing, drone, LiDAR, and satellite-data-related companies.

The repository currently contains one main dataset:

- [geo-companies.csv](/Users/a.rezaie/claude/geo-companies/geo-companies.csv)

As of April 17, 2026, the CSV contains `6,573` data rows.

## What This Is

This repository is intended as a starting point for:

- market research
- competitive landscape analysis
- lead generation
- partnership scouting
- ecosystem mapping

The dataset is geospatial-focused, but it is not a perfect ground-truth registry. Some rows are richly populated, while others are sparse and still need manual verification.

## File Format

- Encoding: `UTF-8`
- Delimiter: comma
- Header row: yes

## Schema

`geo-companies.csv` contains these columns:

- `name`
- `website`
- `country`
- `city`
- `industry_category`
- `short_description`
- `products_services`
- `uses_gis`
- `uses_remote_sensing`
- `uses_drones`
- `uses_lidar`
- `uses_satellite_data`
- `source_links`
- `linkedin_url`
- `followers`
- `estimated_revenue`

## Column Notes

- `name`: company or organization name
- `website`: primary website when available
- `country`, `city`: basic location fields
- `industry_category`: rough classification such as GIS partner, remote sensing, surveying, drone ecosystem, and related buckets
- `short_description`: short summary of the company or product focus
- `products_services`: product, service, or capability notes
- `uses_gis`, `uses_remote_sensing`, `uses_drones`, `uses_lidar`, `uses_satellite_data`: simple `yes`/blank capability flags
- `source_links`: source URLs used for the row
- `linkedin_url`, `followers`: optional LinkedIn signal fields
- `estimated_revenue`: optional commercial signal field

## Caveats

- Missing values are expected.
- Some rows are stronger than others in source quality.
- Company names and websites may change over time.
- A few rows may represent organizations, programs, research groups, or products closely tied to the geospatial ecosystem rather than pure private companies.
- This dataset should be reviewed before high-stakes commercial use.

## Suggested Market Research Fields

If you want to extend this dataset for deeper market research, add fields like:

- founded year
- headquarters
- target customer type
- product category
- pricing model
- deployment model
- industry verticals
- notable customers
- competitors
- funding
- employee count
- recent news

## Target Enrichment Spec

The intended end state for this repository is not just a company list. The target output is a market-research-ready CSV enriched from primary and trusted secondary sources.

### Brooksie AI Context

Brooksie is an AI-native geospatial platform that:

- turns natural language into geospatial analysis
- helps users clarify vague problems before execution
- integrates multiple data sources such as satellite, GIS, APIs, and private data
- executes workflows and returns maps, insights, and reports

In short:

- Brooksie = geo research assistant + execution platform

### Enrichment Goal

For each company in the CSV:

- visit the company website
- supplement with trusted sources such as Crunchbase, LinkedIn, G2, Product Hunt, and press releases
- preserve the original row
- add structured company, product, commercial, traction, and Brooksie-strategic fields

### Required Fields

#### Core

- `hq_country`
- `hq_city`
- `founded_year`
- `status`

#### Product

- `main_product_or_service`
- `product_category`
- `short_description`
- `core_use_cases`
- `industry_verticals`
- `delivery_model`

#### Customer

- `target_customer_type`
- `target_roles`
- `regions_served`
- `notable_customers`

#### Commercial

- `pricing_model`
- `pricing_public`
- `entry_price_or_plan`
- `revenue_model`

#### Market Position

- `key_differentiators`
- `main_competitors`
- `partnerships`
- `channel`
- `go_to_market_notes`

#### Traction / Signal

- `employee_count`
- `linkedin_followers`
- `funding`
- `estimated_revenue_or_proxy`
- `web_traffic_proxy`
- `recent_news_or_launches`
- `source_links`
- `last_verified_date`

#### Geospatial-Specific Flags

- `uses_gis`
- `uses_remote_sensing`
- `uses_drones`
- `uses_lidar`
- `uses_satellite_data`
- `data_sources`
- `tech_stack_or_platform_notes`

#### Brooksie Strategic Fields

- `competitive_with_brooksie`
- `potential_customer_of_brooksie`
- `brooksie_as_customer_of_them`

### Rules

- Prefer primary sources whenever possible.
- Include source URLs for all non-trivial claims.
- If data is unknown, write `unknown`.
- Use ISO country names.
- Use `YYYY` format for `founded_year`.
- Keep `short_description` to 25 words or fewer.
- Stamp `last_verified_date` with the date the row was checked.
- Flag acquired, merged, and defunct companies clearly in `status`.

### Minimum Viable Enrichment

If full enrichment is not possible, the minimum acceptable set is:

- `company_name`
- `website`
- `hq_country`
- `main_product_or_service`
- `product_category`
- `short_description`
- `core_use_cases`
- `industry_verticals`
- `target_customer_type`
- `pricing_model`
- `main_competitors`
- `source_links`
- `competitive_with_brooksie`
- `potential_customer_of_brooksie`
- `brooksie_as_customer_of_them`

### Deliverable

The desired final deliverable is:

- one UTF-8 CSV with a header row
- original rows preserved
- all new enrichment fields added

### Required Summary Output

At the end of enrichment work, report:

- total rows
- fully enriched rows
- rows with missing data
- companies that appear shut down or unreachable
## Usage

Example with Python:

```python
import csv

with open("geo-companies.csv", newline="", encoding="utf-8") as f:
    rows = list(csv.DictReader(f))

print(len(rows))
print(rows[0]["name"], rows[0]["website"])
```

## Contributing

Useful improvements include:

- filling missing websites
- adding better source links
- correcting company names
- expanding product and market fields
- removing duplicates
- validating questionable rows

When updating rows, prefer adding a source URL so the data stays auditable.
