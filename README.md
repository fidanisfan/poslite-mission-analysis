# POS Lite Funnel Analysis – Home Task

## 1. KPI Definitions
- Number of Orders
- CPA (Cost Per Acquisiton)
- CR % (Conversion Rate)
- Funnel Drop Off Rate %

A drop in Cost per Lead signals improved efficiency in acquiring leads. However, a longer Sales Cycle Duration can be a warning sign, as it means deals are closing more slowly. This pattern often points to lower-quality leads that need extra nurturing. It’s only a positive outcome if conversion rates and revenue per deal stay strong; otherwise, gains at the top of the funnel may be slowing overall sales momentum.
  
## 2. Data Structure

I structured the project by separating technical cleaning from analytics outputs. The raw Excel data is assumed to be ingested as source tables, then transformed in a staging layer where I standardized data types, cleaned campaign IDs and names, and ensured data quality without applying business logic. On top of this, I built mart tables aggregated at a daily campaign level for both web and leads funnels, including key KPIs, so the data is directly ready for dashboarding and analysis.

## 3. Data Quality Findings

Yes. I found several data quality issues that require cleaning before analysis. Campaign IDs were inconsistently formatted (e.g. numeric values with a .0 suffix), and campaign names contained extra spaces and casing inconsistencies, which caused duplicate groupings. In the staging layer, I normalized data types and column formats to create a reliable foundation for modeling. Other notable issues were many Null values in Campaign ID column and one record which had 10000 Items ordered with 0 Orders which seems to be a wrong data entry. I also observed missing values and zero denominators in funnel metrics, which could lead to misleading KPIs if not handled carefully. These issues were addressed in the staging layer to ensure reliable aggregation and reporting.

The marketing team could benefit from focusing more on lead quality rather than just lead volume. Optimizing campaigns based on downstream metrics like cost per deal and conversion to deals, and working more closely with sales on lead quality definitions, would likely improve overall performance. At the same time, they should avoid scaling channels that generate cheap leads but result in long sales cycles or low deal conversion, as this can hurt revenue efficiency.

## 4. Dashboard Proposal

<img width="784" height="598" alt="Screenshot 2026-02-03 at 07 15 08" src="https://github.com/user-attachments/assets/0964291a-072f-45a5-a171-1a542ca03066" />


## 5. AI Tooling Reflection
