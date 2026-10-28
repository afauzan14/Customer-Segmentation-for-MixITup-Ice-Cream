# 🍦 Customer Segmentation for MixITup Ice Cream using K-Prototypes Clustering
### Unsupervised Machine Learning on Mixed Data Types (Numerical & Categorical) for Data-Driven F&B Marketing Strategies

[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter&logoColor=white)](Kelompok_C_Study_Case_02.ipynb)
[![Dataset](https://img.shields.io/badge/Dataset-MixITup%20Transactions-green)](Case-Study-02-MixITup.csv)
[![Algorithm](https://img.shields.io/badge/Algorithm-K--Prototypes-red)]()
[![Domain](https://img.shields.io/badge/Domain-F%26B%20Retail%20Analytics-purple)]()

---

## 📌 Project Overview & Business Understanding

**MixITup** is a rapidly scaling Food & Beverage (F&B) startup specializing in artisanal ice cream, boba drinks, and specialty desserts. Currently operating across high-density urban hubs in **Jakarta, Depok, and Tangerang**, the brand experiences substantial foot traffic across both dine-in and online delivery channels.

Following a successful **Series B funding round of Rp 33 Billion**, MixITup is preparing for multi-city retail expansion and large-scale marketing blitzes. To ensure optimal return on marketing spend (ROAS) and prevent customer churn, executive leadership requires an empirical, data-driven customer segmentation framework to identify behavioral patterns, purchasing habits, and regional flavor preferences.

This project implements **K-Prototypes Clustering**, an advanced unsupervised machine learning algorithm designed to natively partition **mixed data types (numerical and categorical attributes simultaneously)** without arbitrary feature transformations.

---

## 🎯 Analytical Objectives

1. **Uncover Demographic & Transactional Behaviors:** Analyze multidimensional customer profiles, income distributions, and spending tendencies across retail locations.
2. **Build Meaningful Customer Personas:** Derive statistically robust and business-actionable customer tiers.
3. **Formulate Tailored Marketing Strategies:** Design targeted promotions, operational workflows, and loyalty retention programs customized for each specific cluster.

---

## 🔬 K-Prototypes Modeling & Optimal Cluster Selection

Standard clustering algorithms (e.g., K-Means or K-Modes) are inherently constrained to either purely continuous or purely discrete variables. **K-Prototypes** integrates *Euclidean distance* for numerical dimensions (`age`, `income`, `spending_score`) with a *simple matching dissimilarity metric* weighted by $\gamma$ for categorical dimensions (`gender`, `marital_status`, `city`, `promo_usage`, `day_of_purchase`, `flavor_preference`).

### Optimal Cluster Evaluation ($k$ Selection)
* Evaluated cost function variations across cluster sizes $k \in [1, 9]$ using the **Elbow Method**.
* A distinct inflection point (*elbow knee*) emerged at **$k = 4$**.
* Selected **$k = 4$** as the optimal configuration, achieving maximum intra-cluster cohesion and clear separation across customer spending tiers.

---

## 🏆 Customer Cluster Profiles (Personas)

| Customer Tier | Cluster ID | Dominant Region | Financial & Spending Profile | Purchasing Pattern | Preferred Flavor |
| :--- | :---: | :---: | :--- | :--- | :---: |
| **Bronze** 🥉 | Cluster 0 | **Tangerang** | Lower-to-middle income, lower spending score. Highly price-sensitive. | Highly responsive to promotions; peak buying day: **Monday**. | Chocolate |
| **Silver** 🥈 | Cluster 2 | **Jakarta** | Upper-middle income, moderate spending score. Rarely utilizes discounts. | Weekend-centric transactions; peak buying day: **Saturday**. | Blueberry |
| **Gold** 🥇 | Cluster 1 | **Jakarta** | High income, high spending score. High-frequency premium buyers. | Low promo sensitivity; peak buying day: **Monday**. | Vanilla |
| **Platinum** 💎 | Cluster 3 | **Depok** | Moderate-to-high income, highest spending score. Core brand champions. | Organic buyers; peak buying day: **Monday**. | Vanilla |

---

## 💡 Actionable Business & Marketing Strategies

### 🥉 1. Bronze Tier (Tangerang — Price Sensitive & Deal Seekers)
* **Off-Peak Value Bundles:** Launch *"Sweet Monday"* bundled promotions combining Chocolate ice cream with secondary items to stimulate foot traffic early in the week.
* **Tiered Stamp Loyalty Program:** Implement a digital loyalty stamp card rewarding repeat purchases, encouraging progression toward higher spending tiers.

### 🥈 2. Silver Tier (Jakarta — Weekend Socializers)
* **Weekend Operational Optimization:** Extend dine-in store hours and optimize seating layouts on Saturdays to capture social groups and leisure diners.
* **Geo-Targeted Digital Campaigns:** Focus programmatic social media advertisements around commercial office districts, universities, and lifestyle centers in Jakarta.

### 🥇 3. Gold Tier (Jakarta — Premium High-Spenders)
* **Exclusive Flavor Innovations:** Introduce limited-time artisanal offerings (e.g., premium seasonal blends, gourmet toppings) to satisfy desire for exclusivity.
* **Barista Workforce Allocation:** Optimize staff scheduling and fast-service lines on Mondays to ensure seamless service for high-value routine customers.

### 💎 4. Platinum Tier (Depok — Top Brand Champions)
* **VIP Priority Access:** Establish an exclusive VIP fast-track queue for loyal regulars, minimizing wait times during peak rush hours.
* **Surprise & Delight Rewards:** Deliver personalized loyalty tokens, complimentary birthday treats, and secret menu invitations without relying on generic discount coupons.
