# python-ai-modeling
Overview
Our team implemented a content-based recommendation system to suggest the most optimal commercial districts. The project utilizes two distinct methods, combining cosine similarity, category scores, and advanced techniques like frequent itemsets and association rules to improve recommendation accuracy.

Methodology
1. Initial System
In the first approach, we vectorized both user input and the dataset and applied a content-based recommendation algorithm.

Cosine Similarity: Used to measure the similarity between user input and the dataset.
Category Score: Districts with the lowest category ratios were assigned higher scores.
Final Recommendation Score: A weighted combination of cosine similarity and category scores was used to generate the final score.
📊 Results: The chart on the right illustrates the recommendations produced by this system.

Limitation:
The initial system assumed that districts with low category ratios had higher chances of business success, which was not always accurate.

2. Refined System: Leveraging Association Rules
To address the limitations of the initial system, we integrated frequent itemsets and association rules into the recommendation process.

Steps
Transaction Generation

Each district was treated as a single "transaction," where a basket of items represented the category distribution within the district.
Frequent Itemset Extraction

Itemsets with a minimum support threshold of 0.2 were extracted to identify frequent itemsets.
Association Rule Generation

Using the frequent itemsets, we applied a minimum confidence threshold of 0.5 to extract association rules.
Among the extracted rules, only the rule with the highest confidence was retained for each category.
Category Score Adjustment

Association rule confidence values were used as weights when calculating category scores, ensuring more accurate recommendations.
📊 Results: The refined system's chart highlights clear differences from the initial system, providing improved recommendations for optimal commercial districts.

Final Report Generation
Once an optimal commercial district is determined, the system generates an analytical report containing:

Key district information
Visualized statistics (charts and graphs)
Insights to support informed decision-making
The analytical report allows users to gain a comprehensive understanding of the recommended district.

Results
The refined system combines content-based recommendations with association rule confidence weights, resulting in better accuracy and more reliable suggestions for users.

Conclusion
By addressing the limitations of the initial system and incorporating frequent itemsets and association rules, our refined approach offers users optimal commercial district choices. The addition of detailed analytical reports further enhances the decision-making process, ensuring business success.


Python (Pandas, NumPy, Scikit-learn)
Association Rule Mining (Apriori Algorithm)
Data Visualization Tools (Matplotlib, Seaborn)
