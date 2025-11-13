
# 🧾 Findings & Insights

## 1️⃣ Overview

Using **association rule mining** (FP-Growth algorithm with a minimum support of 0.02), we discovered several strong relationships among products in the **Online Retail dataset**.  
The results reveal that customers tend to purchase **multiple variants of similar collectible items** together — particularly within the *Regency Teacup* collection.

---

## 2️⃣ Top Association Rules

| No. | Rule | Support | Confidence | Lift | Interpretation |
|-----|------|----------|-------------|------|----------------|
| 1 | (Green Regency Teacup, Roses Regency Teacup) → (Pink Regency Teacup) | 0.021 | 0.72 | 24.03 | Customers buying Green & Roses variants are 72% likely to also buy the Pink one. Indicates strong multi-color purchasing. |
| 2 | (Pink Regency Teacup) → (Green Regency & Roses Regency Teacups) | 0.021 | 0.70 | 24.03 | Buyers of Pink Regency often purchase the other two variants, showing collector behavior. |
| 3 | (Green Regency Teacup) → (Pink Regency & Roses Regency Teacups) | 0.021 | 0.56 | 23.99 | Green Regency serves as a gateway product; its buyers tend to expand into the full Regency set. |
| 4 | (Pink Regency & Roses Regency Teacups) → (Green Regency Teacup) | 0.021 | 0.89 | 23.99 | Nearly 9 in 10 customers who buy Pink and Roses also purchase Green Regency — strongest directional rule. |
| 5 | (Pink Regency Teacup) → (Green Regency Teacup) | 0.025 | 0.83 | 22.19 | Pink and Green variants are commonly bought together; strong pairwise relationship. |

---

## 3️⃣ Insights & Interpretation

### 💡 Key Observations
- All top rules have **Lift values > 20**, signifying **non-random, extremely strong associations**.  
- The **Regency Teacup series** behaves like a **collectible category**: customers rarely buy one color variant alone.  
- Confidence values between **0.70 and 0.89** indicate that these relationships are highly predictive of customer behavior.

---

## 4️⃣ Business & Operational Implications

| Area | Recommendation | Rationale |
|-------|----------------|------------|
| 🛒 **Bundling & Promotions** | Create “Regency Teacup Trio” bundles (Green + Pink + Roses). | Customers prefer completing the set — bundling drives volume and satisfaction. |
| 🤖 **Recommendation Systems** | Recommend other color variants when one is viewed or added to cart. | Leverages cross-product lift to increase average order value. |
| 🏬 **Visual Merchandising** | Group Regency teacups together on shelves or online product pages. | Visual proximity encourages collection-based purchases. |
| 📦 **Inventory Management** | Align stock levels across Regency color variants. | Prevents sales loss caused by one variant being out of stock. |

---

## 5️⃣ Visual Example (Insert Screenshot)
> 🖼️ *Placeholder: “Top 10 Frequent Itemsets by Support” bar chart*  
> 🖼️ *Placeholder: “Support vs Confidence” scatter plot of generated rules*

---

## 6️⃣ Summary
The analysis reveals that **association rule mining** can uncover deep customer behavior insights in retail data.  
For the Regency Teacup products, **cross-selling and bundling strategies** are strongly supported by data, and these findings can guide **personalized marketing, shelf organization, and stock planning**.
