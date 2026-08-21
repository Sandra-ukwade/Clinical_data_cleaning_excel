# Clinical Data Cleaning & Executive Analytics Dashboard

## Project Overview
I took a raw, highly corrupted clinical dataset and built a bulletproof data cleaning pipeline followed by an interactive Executive Dashboard in Microsoft Excel. This project demonstrates my ability to enforce data integrity, apply international clinical standards (GCP), and translate clean data into actionable healthcare insights.

## Clinical Validation & Data Cleaning Log
Using my healthcare domain knowledge, I performed critical validation checks that a standard data analyst might easily overlook:

* **Physiological Boundaries (Outlier Validation):** Identified and purged impossible metrics (Cholesterol of `9999` and Age of `999`), recognizing them as database sentinel values for missing entries. Left cells truly blank (`Null`) to protect statistical averages.
* **Good Clinical Practice (GCP) Compliance:** Flagged incomplete blood pressure records (e.g., `120/` missing the diastolic metric). Aligned with GCP data integrity rules, I left these blank instead of fabricating data with placeholder zeros.
* **Anatomical Delimiter Split:** Standardized mixed data entry symbols (converting hyphens `120-80` to slashes `120/80`) and parsed composite strings into independent `Systolic_BP` and `Diastolic_BP` variables. Removed post-split text fragments (`N` and `A`).
* **Primary Key & Row Integrity:** Checked table consistency, permanently removing **11 exact duplicate rows** and purging an orphaned "ghost row" at index 25 that contained zero clinical metrics.

## Key Insights Uncovered
1. **Metabolic Risk Cohort:** Average cholesterol levels peak aggressively within the 68–77 age group.
2. **Cardiovascular Discrepancy:** A clear split in blood pressure patterns emerged between genders—Female patients presented higher average Systolic metrics, while Male patients exhibited higher Diastolic pressures.

## Tools & Features Demonstrated
* Data Cleaning (TRIM, Text-to-Columns, Find & Replace, Formatting Normalization)
* Descriptive Aggregation (Pivot Tables, Field Grouping, Custom Labels)
* Visual Dashboarding (Dynamic Slicers, Linked Pivot Charts, Conditional Formatting Alerts)
