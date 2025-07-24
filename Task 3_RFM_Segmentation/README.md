###  Task 3 – RFM Customer Segmentation Analysis

This project is part of my Elevvo Data Analytics Internship, where I performed **Customer Segmentation** using **RFM (Recency, Frequency, Monetary)** analysis. The objective is to understand customer behavior patterns and group them into actionable segments for targeted marketing.

---

###  Dataset

* **Source**: [Online Retail Dataset - UCI](https://archive.ics.uci.edu/ml/datasets/online+retail)
* **Details**: Contains \~500,000 transactions from a UK-based online retailer between 2010–2011.

---

###  Tools & Technologies Used

| Tool              | Purpose                        |
| ----------------- | ------------------------------ |
| **Python**        | Data manipulation and analysis |
| **Pandas**        | Handling tabular data          |
| **Seaborn**       | Data visualization             |
| **Matplotlib**    | Plot customization             |
| **Jupyter/Colab** | Development environment        |

---

###  Key Steps Performed

1. **Data Loading & Cleaning**

   * Removed missing values and cancelled orders.
   * Ensured correct date/time format and numeric conversion.

2. **RFM Metric Calculation**

   * **Recency**: Days since last purchase
   * **Frequency**: Number of repeat purchases
   * **Monetary**: Total amount spent

3. **Scoring & Segmentation**

   * Scaled RFM metrics from 1 to 4 using quantiles.
   * Created combined RFM scores and assigned customer segments:

     *  **Champions**
     *  **Loyal Customers**
     *  **At Risk**
     *  **Lost**
     *  **New Customers**, etc.

4. **Visual Analysis**

   * Count plots for customer segments
   * Boxplots of Monetary by Segment
   * Heatmaps for R vs F scores
   * Cluster trends via colored distributions

---

###  Visualizations

All visualizations are designed with clean, professional themes and color schemes to enhance readability and storytelling.

| Chart Type              | Purpose                             |
| ----------------------- | ----------------------------------- |
| Barplot (Segment Dist.) | Show distribution of customer types |
| Boxplot (Monetary)      | Understand value by segment         |
| Heatmap (R vs F)        | Visualize relationship scores       |

---

###  Key Insights

* **Champions** are top customers spending the most recently and frequently.
* **At Risk** and **Lost** customers may need re-engagement campaigns.
* **New Customers** and **Potential Loyalists** show promise for nurturing.
* **High Monetary but Low Frequency** might indicate occasional big spenders.

---

###  Files Included

* `rfm_analysis.ipynb` — Code notebook
* `README.md` — Documentation
* `/charts/` — Saved visualizations (optional)

---

###  Future Enhancements

* Apply clustering (K-Means) for deeper segment analysis
* Build an interactive dashboard (e.g., with Plotly or Power BI)
* Integrate marketing strategy suggestions per segment

---

###  Connect

If you're interested in collaborating or have feedback, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/abdur-rahmanml/)!
