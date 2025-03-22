# Wholesale-Customer-Data-Analysis
Wholesale Customers Data Analysis<br>
Exploratory Data Analysis and Customer Segmentation<br>
This project analyzes the "Wholesale customers data.csv" dataset using a Google Colab notebook to explore customer behavior and perform segmentation. Here's a breakdown of the steps involved:<br>

1. Import necessary libraries:<br> The notebook imports essential libraries including pandas, numpy, seaborn, matplotlib.pyplot, and components from sklearn (like train_test_split, StandardScaler, KNeighborsClassifier, and metrics functions).

2. Load the dataset:<br> The code loads the "Wholesale customers data.csv" from Google Drive using pd.read_csv.

3. Data Cleaning and Preprocessing:<bbr>

Handling missing values: The notebook checks for missing values using df.info(). It confirms that there are no missing values in the dataset.<br>

Dropping irrelevant columns: The code drops 'Channel' and 'Region' columns using df.drop(), considering them less relevant for the analysis.<br>

Duplicate Removal: The notebook identifies and removes duplicate rows using df.duplicated().sum().<br>

Outlier Detection and Removal: Outliers are detected and removed using the Z-score method from scipy.stats. Numerical features are analyzed, and outliers exceeding a threshold are removed to create a new dataframe df_no_outliers.<br>

4. Data Visualization and Exploration:

Correlation heatmap: A correlation heatmap is generated using sns.heatmap to visualize relationships between numerical features.<br>

Descriptive statistics: The describe().transpose() function is used to provide summary statistics of the dataset for initial exploration.<br>

Boxplots: Boxplots are created using sns.boxplot to visualize the distribution of features and identify potential outliers visually.<br>
Pairplots: sns.pairplot is used to create scatterplots for all feature combinations, aiding in understanding feature relationships.<br>

5. Customer Segmentation:<br>

KMeans Clustering: KMeans clustering is applied to segment customers based on 'Fresh' and 'Milk' features. The results are visualized using a scatterplot.<br>

Predictive Modeling: A KNeighborsClassifier is trained to predict customer clusters based on the features. The model's accuracy and performance are evaluated using metrics like accuracy score, classification report, and confusion matrix.<br>

Feel free to download the code and data.
