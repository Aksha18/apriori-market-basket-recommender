# 🛒 Apriori-Based Market Basket Recommender System

This project implements **Market Basket Analysis** using the **Apriori algorithm** and **FP-Growth** to find associations between products and recommend items that are frequently bought together. It uses real-world e-commerce transaction data to demonstrate product affinity patterns.

---

## 📌 Objective

The goal is to:
- Discover frequent itemsets and associations using Apriori and FP-Growth.
- Analyze **support**, **confidence**, and **lift** for generating association rules.
- Build a **simple recommender** system based on these rules.
- Visualize top product associations.

---

## 🧾 Dataset

We use the [Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail) from the UCI Machine Learning Repository. It contains transactional data of a UK-based online store from 2010 to 2011.

Each row in the dataset represents a product purchased in a particular invoice. Products purchased together have the same **InvoiceNo**.

---

## 💡 Techniques Used

- **Apriori Algorithm** – to extract frequent itemsets.
- **FP-Growth Algorithm** – for memory-efficient pattern mining.
- **Association Rule Mining** – to derive rules using support, confidence, and lift.
- **Market Basket Analysis** – to find patterns in customer buying behavior.

---

## 🔢 Key Metrics

| Metric     | Description |
|------------|-------------|
| **Support** | Frequency of itemset in all transactions. |
| **Confidence** | Likelihood of seeing B in a transaction if A is present. |
| **Lift** | Strength of association. A lift > 1 indicates a positive association. |

---

## 📈 Visualizations

- Top 10 product associations by **lift**.
- Bar charts showing high-confidence item combinations.

---

## 🧠 Recommender Function

The recommender suggests products based on an input product by checking the learned association rules.

```python
recommend("HAND WARMER UNION JACK", rules_df)
