# Cryptocurrency Market Data Clustering

This project focuses on clustering cryptocurrency market data using K-Means clustering and Principal Component Analysis (PCA) for dimensionality reduction. By analyzing price changes over various periods, this script groups cryptocurrencies based on similar behavior, offering insights into market trends and relationships among different coins.

## Dataset

The data consists of cryptocurrency price changes over various time frames (24 hours, 7 days, 14 days, etc.). Each row represents a cryptocurrency with the following features:

- `price_change_percentage_24h`
- `price_change_percentage_7d`
- `price_change_percentage_14d`
- `price_change_percentage_30d`
- `price_change_percentage_60d`
- `price_change_percentage_200d`
- `price_change_percentage_1y`

Data is loaded from `crypto_market_data.csv`.

## Dependencies

This project uses the following libraries:

- **pandas**: For data manipulation and analysis.
- **hvplot.pandas**: For creating visualizations.
- **sklearn**: For K-Means clustering, PCA, and data standardization.

## Key Steps

1. **Data Loading and Preprocessing**  
   Load the CSV data, normalize it using `StandardScaler`, and prepare it for clustering.

2. **K-Means Clustering**  
   - Identify the optimal number of clusters (`k`) by calculating inertia values and plotting the Elbow curve.
   - Select the best `k` value (4 in this case) and perform clustering on the normalized data.
   
3. **Visualization**  
   - Plot the clustering results to visualize the relationships between cryptocurrencies based on recent price changes.
   
4. **Dimensionality Reduction with PCA**  
   - Apply PCA to reduce the data to three principal components, optimizing the clustering results.
   
5. **Cluster Visualization with PCA Data**  
   - Generate a scatter plot based on two selected features, colored by cluster labels for easier interpretation.

## Usage

1. Ensure all dependencies are installed.
2. Execute the script to load and preprocess the data.
3. View the plots for insights into the clustering and PCA analysis.

## Conclusion

The project groups cryptocurrencies based on similar price change patterns, providing a foundational approach for analyzing market segments in crypto trading. The clustering and PCA techniques offer data-driven insights to explore potential correlations among cryptocurrencies in a dynamic market environment. 

