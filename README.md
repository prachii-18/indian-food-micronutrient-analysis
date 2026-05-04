# 🧠 Brain-Health Micronutrient Analysis of Indian Foods

This project explores whether Indian food items can be grouped based on the density of micronutrients associated with brain health. Using the Indian Nutrient Databank (INDB), foods were analyzed based on neuro-supportive micronutrients involved in neurotransmitter production, nerve function, and brain protection.

The study focused on Vitamin B-complex (B1–B9), Vitamin C, and minerals including iron, magnesium, selenium, manganese, copper, and zinc.

---

## Methodology

Nutrient values were cleaned, standardized, and converted to a common per-100g basis. Serving units were mapped to gram equivalents, missing values were removed, and outliers were filtered using an IQR-based method.

The processed data was log-transformed, scaled, and analyzed using K-means clustering. The elbow method indicated **3 optimal clusters**. Principal Component Analysis (PCA) was used for visualization.

To study nutrient relationships within clusters, nutrient values were binarized using the 75th percentile threshold and association pattern mining was performed using the FP-Growth algorithm.

---

## Dataset Summary

| Description | Count |
|---|---|
| Total foods originally | 1,014 |
| Foods after cleaning | 863 |
| Foods removed during preprocessing | 151 |

---

## Key Results

Three distinct micronutrient-based food clusters were identified.

### Cluster Distribution

| Cluster | Number of Foods |
|---|---|
| Cluster 0 | 321 |
| Cluster 1 | 171 |
| Cluster 2 | 371 |

### Cluster Characteristics

- **Cluster 0:** relatively lower micronutrient density
- **Cluster 1:** highest micronutrient density and strongest nutrient co-occurrence patterns
- **Cluster 2:** moderate micronutrient density

Across all clusters, **magnesium, vitamin C, and iron** emerged as the most prominent nutrients.


### Association Mining Highlights
- **Cluster 0:** no meaningful association rules identified
- **Cluster 1:** strong co-occurrence of copper, iron, and zinc
- **Cluster 2:** notable associations between Vitamin B1 and B3, and between Vitamin C and B9

These patterns are broadly consistent with known nutritional relationships in legumes, cereals, vegetables, fruits, and animal-based foods.

---

## Key Takeaway

The analysis shows that Indian foods can be meaningfully grouped based on micronutrient composition relevant to brain health. This provides a useful data-driven framework for nutritional research and dietary pattern analysis.

---

## Tools Used

Python · pandas · NumPy · scikit-learn · matplotlib · seaborn · mlxtend · openpyxl · Google Colab

---

## Repository Note

This repository summarizes a research internship project. The original code and dataset are not publicly shared at this stage due to ongoing academic use.
