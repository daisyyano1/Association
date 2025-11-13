The main goal of this project was to explore Association Rule Mining, a core data mining technique used to uncover hidden relationships between items in large transactional datasets.

Through this project, we aimed to:

Understand customer purchasing behavior through association analysis.

Identify products that are frequently bought together.

Generate actionable business insights that can improve marketing, inventory, and product placement decisions.

📂 Dataset Description

Dataset Name: Online Retail II Dataset
Source: UCI Machine Learning Repository

🧹 Part 1: Data Preparation

The dataset initially contained duplicate records, missing customer IDs, and irrelevant entries such as canceled orders.

The data cleaning process involved:

Removing missing values and duplicate rows.

Filtering out records with negative quantities or canceled invoices.

Grouping transactions by InvoiceNo and CustomerID.

Converting the dataset into a basket format suitable for association rule mining — where each transaction represented a list of items purchased together.

This structured data was then ready for frequent pattern mining.
📈 Part 2: Frequent Itemset Mining

The Apriori algorithm was applied to identify frequent itemsets — combinations of items frequently purchased together.

Two minimum support thresholds were tested:

0.02 (2%) – Captured broader relationships but included some weak item pairs.

0.05 (5%) – Focused on stronger and more relevant itemsets.

The top 10 most frequent itemsets revealed strong co-purchase relationships between specific product groups, such as decorative teacups and saucers, indicating consistent buying patterns.

A visualization (bar chart) was used to show these top frequent itemsets by support.
Part 3: Association Rule Generation

Using the frequent itemsets, association rules were generated and evaluated using support, confidence, and lift metrics.

Key definitions:

Support measures how frequently items appear together in all transactions.

Confidence measures the likelihood of buying the consequent item given that the antecedent item was purchased.

Lift measures how much more often the antecedent and consequent occur together than expected if they were independent.

💡 Example Rules and Interpretation

If a customer buys a “green regency teacup and saucer” and “roses regency teacup and saucer”, they are likely to buy a “pink regency teacup and saucer”.

Support: 2.1%

Confidence: 72.1%

Lift: 24.03

Interpretation: There is a very strong co-purchase tendency among customers who buy this set of teacups.

Customers who purchase a “pink regency teacup and saucer” are also likely to buy “green regency teacup and saucer”.

Support: 2.4%

Confidence: 82.7%

Lift: 22.19

Interpretation: Customers show a strong preference for buying complementary colors or full collections of similar items.

Buying a “green regency teacup and saucer” increases the likelihood of buying a “roses regency teacup and saucer”.

Confidence: 56.4%

Lift: 23.99

Interpretation: Decorative tableware items tend to be purchased as matching sets, showing cross-selling potential.

These rules highlight product affinity patterns that can inform marketing campaigns, promotional bundles, or store layout planning.

📊 Part 4: Insights & Business Value

From the analysis, several key business insights emerged:

Customers often buy items in coordinated sets, especially within the same design theme.

Bundling similar or complementary products could increase average transaction value.

Products with high lift values should be placed near each other in both physical and online stores.

These patterns can guide personalized recommendations and targeted marketing campaigns.

🧰 Libraries Used

pandas – For data cleaning and manipulation

mlxtend.frequent_patterns – For Apriori and association rule generation

matplotlib / seaborn – For data visualization

numpy – For numerical processing

🪞 Conclusion

This project successfully demonstrated the use of Association Rule Mining to extract meaningful patterns from transactional data.
Through frequent itemset discovery and rule analysis, we uncovered strong product relationships that can improve retail operations, marketing strategies, and customer experience.
