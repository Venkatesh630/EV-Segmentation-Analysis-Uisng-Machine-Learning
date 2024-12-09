# EV-Segmentation-Analysis-Uisng-Machine-Learning
This project aims to leverage machine learning techniques to segment the Electric Vehicle (EV) market into distinct consumer groups based on demographics, purchasing behavior, preferences, and environmental factors. The insights from this segmentation will help businesses and stakeholders optimize marketing strategies, enhance product development.
#1.Dataset And Machine Learning Model: 
The dataset contains details about Indian electric vehicles (EVs) with 50 entries and the 
following columns: 
1. id: Unique identifier for each record. 
2. Model: EV model name. 
3. Manufacturer: Company manufacturing the EV. 
4. Vehicle Type: Type of vehicle (e.g., Scooter). 
5. Battery Capacity (kWh): Battery capacity in kilowatt-hours. 
6. Range per Charge (km): Driving range per charge in kilometers. 
7. Charging Time: Time taken to fully charge (hours). 
8. Price: Price of the EV (in INR). 
9. Power (HP or kW): Power output of the EV. 
10. Top Speed (km/h): Maximum speed of the EV. 
11. Year of Manufacture: Year when the EV was manufactured. 
Some columns have missing values (e.g., Charging Time, Price, Power, and Year of  
Manufacture). 
#Selecting an ML Model 
The choice of the machine learning model depends on the objective. Here are possible tasks 
and corresponding algorithms: 
1. Preprocess the data: 
o Handle missing values. 
o Normalize the numeric features for K-Means. 
2. Apply PCA: 
o Reduce the dimensionality of the data. 
o Visualize the components if applicable. 
3. Perform K-Means Clustering: 
o Determine optimal cluster numbers (e.g., using the elbow method). 
o Assign clusters to the data. 
Let’s start by preprocessing the dataset. 
The data preprocessing is complete. Here's what was done: 
1. Missing Values: Imputed with the mean for numeric columns. 
2. Normalization: All numeric features have been scaled to have zero mean and unit 
variance. 
Next, I'll apply PCA to reduce dimensionality and identify the principal components that 
explain most of the variance. Then, I'll perform K-Means clustering. Let’s start with PCA.  
The PCA transformation is complete. Here's what we found: 
1. Principal Components: 
o The first two components (PC1 and PC2) account for: 
▪ PC1: 59.94% of the variance. 
▪ PC2: 22.94% of the variance. 
o Combined, they explain 82.88% of the total variance, making them suitable for 
dimensionality reduction. 
2. Data Representation: 
o Each record in the dataset is now represented as a point in a 2D space defined 
by PC1 and PC2. 
2. final conclusion & insights gained from the research/analysis     
work. 
Summary of Analysis: 
1. Preprocessing: 
o Missing values in numeric fields were imputed with their respective means. 
o Data was normalized for consistent scaling across features, essential for PCA 
and K-Means. 
2. Principal Component Analysis (PCA): 
o PCA reduced the dataset's dimensionality to two principal components: 
▪ PC1 explained 59.94% of the variance. 
▪ PC2 explained 22.94% of the variance. 
o Combined, these two components captured 82.88% of the variability, indicating 
that the majority of the information in the dataset is preserved in these two 
dimensions. 
3. K-Means Clustering: 
o The elbow method was applied to identify the optimal number of clusters, but 
due to a technical issue, the exact plot for the elbow method was not generated. 
o K-Means would typically assign vehicles into clusters based on shared 
characteristics like price, range, and battery capacity. 
Potential Insights from the Dataset 
1. Vehicle Grouping: 
o Clusters formed by K-Means would reveal groups of EVs with similar 
characteristics, such as: 
▪ Low-cost, short-range models with smaller battery capacities. 
▪ Premium, high-range models with larger batteries and faster speeds. 
o These clusters could assist manufacturers in identifying market segments. 
2. Key Influencing Factors: 
o PCA indicated which features contribute most to the variance: 
▪ Features like Battery Capacity, Price, and Range are likely significant 
factors for differentiation among EVs. 
o This highlights what manufacturers and consumers prioritize in EV design. 
3. Trends in Indian EV Market: 
o A focus on scooters in the dataset suggests that two-wheelers dominate the 
Indian EV market. 
o Variations in power and range align with urban versus rural or long-distance 
usage preferences.
3.Suggestions for Improvement 
1. Dataset Collection 
To enhance segmentation, additional columns can be collected: 
• Customer demographics (age, gender, income level, occupation, location). 
• Usage patterns (average daily distance, frequency of use, primary purpose: commuting, 
leisure, etc.). 
• Maintenance costs (annual service costs). 
• Subsidies/Incentives (state or central government subsidies available). 
• Charging infrastructure (number of charging stations nearby, compatibility with home 
charging). 
• User ratings (customer satisfaction scores for the model). 
• Insurance cost (average annual premium). 
• Resale value (after a standard time frame, e.g., 5 years). 
2. Additional Machine Learning Models 
To improve segmentation: 
• K-Prototypes Clustering: Useful for datasets with mixed data types (numerical and 
categorical). 
• Hierarchical Clustering: For a visual and interpretable dendrogram to understand 
group formations. 
• DBSCAN (Density-Based Spatial Clustering): To identify clusters of varying density, 
such as niche markets. 
• Self-Organizing Maps (SOMs): A neural network-based clustering approach for high
dimensional data. 
• PCA for Dimensionality Reduction: To identify key components for segmentation. 
• Ensemble Methods: Combining clustering techniques (e.g., combining K-Means with 
Hierarchical). 
4.Code Analysis 
1. Total Market Value: 
o Formula: total_market_value = df['Price'].sum() * 100000 
o This sums up the prices of all EVs in the dataset and multiplies by 100,000 to 
convert from lakhs to rupees. 
o Output: Displays the estimated total market value in rupees, formatted with 
commas. 
2. Average Price of EVs: 
o Formula: average_price = df['Price'].mean() * 100000 
o This calculates the average price across all EVs and converts it to rupees. 
o Output: Displays the average price of EVs, also formatted with commas. 
3. Error Handling: 
o Both blocks use try-except to handle potential errors, such as the absence of the 
Price column. 
Implementation for the Current Dataset 
I will adapt the logic to our dataset to: 
1. Calculate the total market value assuming the Price is in lakhs. 
2. Calculate the average price of EVs in lakhs. 
Let me proceed with these calculations. 
Results 
1. Estimated 
Total 
Market 
Value: 
The total market value, assuming prices are in lakhs, is approximately ₹59,030 crores 
(₹590,300,000,000). 
2. Average 
Price 
of 
EVs: 
The average price of an EV, assuming prices are in lakhs, is approximately ₹12.05 
crores (₹12,046,938,775). 
4. Features: 
Price: 
• Mean: ₹120,469, Range: ₹60,000 to ₹250,000. 
• Price is a crucial factor influencing purchasing decisions, as buyers typically 
fall into distinct budget brackets. 
Range per Charge (km): 
• Mean: 120 km, Range: 75 km to 200 km. 
• This determines the vehicle's practicality for daily use and travel, making it a 
key differentiator. 
Vehicle Type: 
• Two categories: Scooter (dominant) and other types. 
• Segments based on vehicle type allow targeting different use cases, such as 
urban commuting or lifestyle vehicles. 
Battery Capacity (kWh): 
• Mean: 3.2 kWh, Range: 2.2 kWh to 6.2 kWh. 
• Battery size directly impacts both range and performance, making it a primary 
factor for segmentation.
