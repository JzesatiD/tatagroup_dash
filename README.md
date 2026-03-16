# Tata Insights and Quants (Tata Group) - Project Overview
<c>**Retail Strategy & Insights**<c/>
![Dashboard](https://github.com/JzesatiD/tatagroup_dash/blob/main/assets/dashboard.png?raw=true)

**Overview** The primary objective of this project was to transform over 500,000 raw transactional records into actionable business intelligence for the CEO and CMO of a global retail store. By performing rigorous data cleaning and multidimensional analysis, the project identifies seasonal revenue trends, high-value customer segments, and geographic expansion opportunities to drive strategic fiscal planning.

**Background & Motivation** The Tata Group requested a comprehensive "health check" of their retail operations to prepare for future forecasting. The organization faced challenges with data integrity—specifically regarding negative quantities and pricing errors—which threatened to skew revenue reporting and international expansion plans.

The motivation was to move beyond "vanity metrics" and provide the executive team with a "Cleaned Data" model. This model identifies exactly where demand is surging and which international markets represent the highest ROI for an expansion strategy, ensuring that marketing and operational spend are backed by verified data.

---

## Dataset Structure

The analysis was performed on a transactional dataset containing approximately 542,000 records including fields for Quantity, Unit Price, CustomerID, Country, and Invoice Date. Through a non-destructive Power Query transformation, the dataset was refined to ~379,000 high-fidelity records, ensuring that only valid, non-duplicated commercial transactions were included in the final model.

**Data Cleaning Logic:**
* **Quantity Filter:** Isolated and removed "returns" (negative quantities) by enforcing a minimum of 1 unit.
* **Price Filter:** Enforced a $0 floor on unit prices to eliminate input errors.
* **Deduplication:** Utilized a count-based rule in Power Query to filter out duplicate records without destroying the primary query integrity.

---

## Executive Summary

### Overview of Findings
The analysis uncovered a massive seasonal surge in the latter half of 2011, identifying a 76.5% revenue rally starting in August. Key Performance Indicators (KPIs) focused on Monthly Revenue, International Demand Ranking, and Customer Value Concentration. By filtering out domestic (UK) outliers, the model identified the Netherlands and Ireland as the primary engines for international growth, providing a clear roadmap for geographic expansion.

![Dashboard](https://github.com/JzesatiD/tatagroup_dash/blob/main/assets/dashboard.png?raw=true)

### Insights Deep Dive

#### Metric A: Revenue Seasonality & Trends
- **$640,000 Revenue Anchor**: In August 2011, the store hit a revenue baseline of $640k, which served as the launchpad for a significant Q4 rally.
- **76.5% Seasonal Increase**: Analysis identified a massive three-month rally where revenues surged by over 76%, peaking at the end of the year.
- **Holiday Demand Narrative**: Historical data suggests this surge is highly correlated with holiday shopping cycles, indicating that marketing spend should be front-loaded in Q3 to capture this momentum.
