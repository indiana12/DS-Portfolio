# DS-Portfolio
Creating an End to End Data Science Portfolio

#Housing Project - DS 1
# Optimize my datascience portal more in detail

**Housing Prices Prediction**

import matplotlib.pyplot as plt
import seaborn as sns

# Set up the matplotlib figure

f, axes = plt.subplots(2, 2, figsize=(15, 15))

# Plot a histogram for Total_Area

sns.histplot(data=data, x="Total_Area", kde=True, color="skyblue", ax=axes[0, 0])

# Plot a histogram for Price_per_SQFT

sns.histplot(data=data, x="Price_per_SQFT", kde=True, color="olive", ax=axes[0, 1])

# Plot a histogram for Baths

sns.histplot(data=data, x="Baths", kde=True, color="gold", ax=axes[1, 0])

# Plot a barplot for Balcony

sns.countplot(x='Balcony', data=data, ax=axes[1, 1])

plt.tight_layout()

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fc2023e9-c4f9-4d5e-967e-d33b7c92e754/Untitled.png)

1. **`Total_Area`**: Most of the properties have an area in the range of 0 to approximately 5000 square feet. There are some properties with higher area values, but these are outliers.
2. **`Price_per_SQFT`**: Most of the properties have a price per square foot in the range of 0 to approximately 200,000. However, there is a long tail in the distribution which indicates the presence of properties with very high price per square foot values.
3. **`Baths`**: Most of the properties have between 1 to 4 bathrooms, with a majority having either 2 or 3 bathrooms.
4. **`Balcony`**: More properties have balconies compared to those that do not.

Before we proceed with machine learning models, we need to preprocess our data. We have to convert the **`Price`** from string to numerical format and encode the **`Balcony`** variable to numerical format as well. We will also drop the columns that won't be used in our modeling (**`Name`**, **`Property Title`**, **`Location`**, **`Description`**). Our target variable for the models will be **`Price`**.

Certainly, here are ten key insights we can derive from the dataset:

1. **Property Distribution**: The dataset contains 14,528 real estate properties across various locations.
2. **Price Range**: The property prices vary greatly, ranging from a few lakhs to several crores. Some properties are extremely expensive per square foot, suggesting that they may be located in prime areas.
3. **Area Range**: The total area of the properties also varies significantly, with some properties being as small as 70 square feet and others as large as 35,000 square feet. This could indicate a mix of different types of properties, like apartments, villas, and commercial properties.
4. **Bathroom Count**: Most properties have between 1 to 4 bathrooms, with a majority having either 2 or 3 bathrooms.
5. **Balcony Availability**: More properties have balconies compared to those that do not.
6. **Price per Square Foot**: The price per square foot varies widely, indicating a wide range of property values. Some properties have a high price per square foot, which could indicate a prime location or high-end amenities.
7. **No Missing Data**: There are no missing values in the dataset, which is quite rare in real-world datasets. This suggests that the data has been well maintained and curated.
8. **Outliers**: There are some properties with exceptionally high total area and price per square foot. These properties are likely to be luxury properties or located in prime locations.
9. **Uniform Data**: Most of the data is consistently formatted, which makes it easier to analyze and draw insights from. The data also seems to be relatively clean, with few errors or inconsistencies.
10. **Description Insights**: The 'Description' field contains valuable information about each property. This text data could be further analyzed using natural language processing techniques to extract additional insights about the properties.

It's important to note that these insights are derived from a preliminary analysis of the dataset. For a more detailed understanding, a deeper analysis would be needed, possibly including feature engineering and more sophisticated statistical analysis.
