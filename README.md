# Transit Warehouse & Delivery Zone Analysis

This repository contains the analysis of two distinct datasets: one related to transit warehouse employee performance and another concerning delivery zone efficiency. The goal is to derive actionable insights for optimizing operations and resource allocation.

---

## Project Overview

### Part 1: Transit Warehouse Performance Analysis

An analysis of employee and warehouse performance metrics at transit warehouses. The study focuses on identifying high and low-performing warehouses and employees, understanding productivity drivers, and providing data-driven recommendations for improvement.

**Main Focus Areas:**
*   Evaluating warehouse efficiency using metrics like scans/hour and packages/hour.
*   Assessing individual employee productivity (scans/hour).
*   Identifying patterns and segmenting warehouses and employees based on performance.
*   Recommending strategies for performance improvement.

---

### Part 2: Delivery Zone Efficiency Analysis

An analysis of delivery performance across different postal zones. The objective is to evaluate zone efficiency based on multiple key metrics and recommend the best zone for potential expansion or focus.

**Main Focus Areas:**
*   Calculating key delivery metrics (delivery rate, revenue, average order value) per postal zone.
*   Determining a composite score for each zone based on weighted business priorities.
*   Identifying the top-performing delivery zones.
*   Providing a data-driven recommendation for strategic focus.

---

## Key Results & Business Recommendations

### Transit Warehouses

*   **Clustering:** Warehouses were clustered into three distinct groups based on performance metrics:
    *   **Cluster 0 ("Standard Mid-Performers"):** Average performance with efficient processes (60% of warehouses).
    *   **Cluster 1 ("Small Low Performers"):** Low productivity and high handling complexity (20% of warehouses). Requires attention.
    *   **Cluster 2 ("Compact High Performers"):** High efficiency with fewer staff (20% of warehouses). Best practices to be studied.
*   **Employee Performance:** Significant variation in employee productivity was observed, allowing for clear segmentation (Low, Average, High, Expert).
*   **Recommendations:**
    *   Investigate and replicate best practices from Cluster 2 (e.g., Samara, Vladikavkaz) in Cluster 1 (e.g., Chelyabinsk, Syktyvkar).
    *   Optimize complex handling processes (reduce scans/pack) in low-performing warehouses.
    *   Develop differentiated KPIs tailored to each warehouse cluster's characteristics.

### Delivery Zones

*   **Zone Ranking:** Postal zones were ranked using a composite score that weights delivered orders, delivery rate, total revenue, average order value, and order growth rate.
*   **Top Performer:** Zone **111115** was identified as the top performer based on the comprehensive analysis, showing high volume, good delivery rate, significant revenue, and positive order growth.
*   **Recommendation:**
    *   Prioritize zone **111115** for continued investment and focus due to its strong overall performance and growth potential.

---

## Methodology

1.  **Data Loading & Cleaning:** Data was loaded from Excel files (`Транзитные склады.xlsx`, `зоны доставки.xlsx`). Basic information and descriptive statistics were reviewed. Data quality issues (e.g., incorrect shift data) were identified and handled (analysis focused on hours worked).
2.  **Feature Engineering:** Relevant performance metrics were calculated for both employees and warehouses (e.g., Scans/Hour, Packages/Hour, Scans/Pack).
3.  **Aggregation:** Data was aggregated appropriately, especially summing scans and hours for employees working across multiple warehouses.
4.  **Analysis & Visualization:**
    *   **Warehouses:** Comparative bar charts for various metrics. K-Means clustering (k=3) was applied to warehouse metrics (normalized using StandardScaler) to identify performance groups. Principal Component Analysis (PCA) was used for 2D visualization of clusters. Evaluation metrics (Elbow, Silhouette, Calinski-Harabasz, Davies-Bouldin) supported the choice of k=3.
    *   **Employees:** Histograms, boxplots, and bar charts were used to analyze the distribution and identify top performers. Employees were segmented based on productivity scores.
    *   **Delivery Zones:** Metrics were aggregated per postcode. A weighted composite score was calculated to rank zones. Radar charts were used for multi-metric comparison of top zones. Growth rate was calculated by comparing order volumes in the first and second halves of the observation period.
5.  **Insight Generation:** Findings from visualizations and statistical analysis were interpreted to form conclusions and business recommendations.

---

## Tools Used

*   **Programming Language:** Python
*   **Libraries:** pandas, numpy, scikit-learn, scipy, plotly, matplotlib, seaborn
*   **Techniques:** Data Analysis, Data Visualization, Clustering (K-Means), Dimensionality Reduction (PCA), Feature Engineering, Statistical Testing (implicitly via analysis)
*   **Statistical Methods:** Z-score standardization, Ranking, Composite Scoring

---
