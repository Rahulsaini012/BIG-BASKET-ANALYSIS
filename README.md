## 📊 Big Basket Products Analysis


<!-- Replace with an actual image link if needed -->


Welcome to the Big Basket Products Analysis project! This project aims to explore, analyze, and visualize a dataset of products from Big Basket, uncovering key insights such as product distribution, pricing, discounts, and ratings.


## 🌟 Features

Data Cleaning & Preparation: Handle missing values, compute discounts, and preprocess data.

Statistical Analysis: Descriptive statistics, correlations, and data distributions.

Visualizations: Interactive plots for better insights into product categories, brands, prices, and ratings.

Top & Least Sold Products: Analyze best and least-selling products to understand trends.

## 📁 Dataset Overview

Index	Product	Category	Sub Category	Brand	Sale Price	Market Price	Type	Rating	Description

1	Garlic Oil	Beauty & Hygiene	Hair Care	Sri Sri Ayurveda	220.00	220.00	Hair Oil & Serum	4.1	Contains Garlic Oil...

...	...	...	...	...	...	...	...	...	...

Dataset Size: 27,555 rows × 10 columns

Format: CSV file (BigBasket Products.csv)


📊 Analysis and Visualizations
                                
                                
                                1. Data Overview
                                
                                First 12 Rows of the Dataset:
                                
                                python
                                
                                data.head(12)
                                
                                Summary Statistics:
                                
                                python
                                
                                
                                data.describe()

                                2. Missing Value Handling
                                
                                Fill missing values using mean or mode. Example:
                                
                                python
                                
                                
                                data['sale_price'] = data['sale_price'].fillna(data['sale_price'].mean())

                                3. Data Visualizations
                                
                                Sale Price Distribution:
                                
                                python
                                
                                import seaborn as sb
                                
                                import matplotlib.pyplot as plt
                                
                                sb.histplot(data['sale_price'], bins=30, kde=True, color='skyblue')
                                
                                plt.title("Distribution of Sale Prices")
                                
                                plt.show()
                                
                                Top 10 Brands by Count:
                                
                                
                                python
                                
                                
                                top_brands = data['brand'].value_counts().head(10)
                                
                                sb.countplot(x='brand', data=data[data['brand'].isin(top_brands)], order=top_brands)

                                4. Discount Calculation
                                
                                Compute discounts on products:
                                
                                python
                                
                                
                                data['discount'] = ((data['market_price'] - data['sale_price']) / data['market_price']) * 100

                                5. Correlation Heatmap:
                                
                                python
                                
                                
                                
                                sb.heatmap(data.corr(), cmap='rainbow', annot=True)

## 📈 Insights

Top-Selling Products: Turmeric Powder, Extra Virgin Olive Oil, etc.

Significant Discounts: Products with up to 52% discounts.

High-Rated Products: Majority products have an average rating of 4+ stars.

## 🛠️ Technologies Used

Python: Data manipulation and analysis.

Pandas: For data handling.

Matplotlib & Seaborn: For visualizations.

Scikit-learn: Data preprocessing.

## 📝 Future Scope

Add predictive models to analyze future trends.

Build dashboards for interactive reporting.

## 🤝 Contribution

Feel free to open issues or submit pull requests to contribute to this project. For major changes, please open an issue first to discuss your ideas.

##📄 License

This project is licensed under the MIT License. See the LICENSE file for more details.

## 🌐 Connect

Email: pb65rahulsaini@gmail.com

LinkedIn: https://www.linkedin.com/in/rahul-saini-2b4b33337/
