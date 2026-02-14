# Uncovering the Reality of the Nigerian Real Estate Market

## The Problem
I started with a raw dataset of over 49,000 Nigerian real estate listings. At first glance, the data was incredibly messy. Prices were listed in a mix of Naira and Dollars, numerical columns contained text strings, and severe outliers (like a house listed for 24 Trillion Naira) completely broke standard statistical models. 

## What I Did (Data Engineering & Cleaning)
* **Currency Normalization:** Wrote a script to detect Dollar listings and convert them to Naira using standard exchange rates.
* **String Manipulation:** The `Location` column was unstructured. I engineered a new `State` feature by splitting strings and extracting the root state, revealing that out of 49k listings, over 38,000 were strictly in Lagos. 
* **Outlier Removal:** Used percentile filtering to remove extreme billion-naira outliers, allowing the true distribution of the market to show.
* **Imputation:** Built logic to fill missing Bathroom and Toilet data based on the corresponding Bedroom counts.

## Key Insights
* **Bedrooms Don't Dictate Price (Location Does):** Initially, the correlation between Bedrooms and Price was 0.01 (ruined by outliers). After cleaning, it rose to 0.44. However, a 2-bedroom in Banana Island still vastly outprices a 5-bedroom in Ajah.
* **The En-Suite Standard:** There is a massive 0.84 correlation between Bedrooms and Bathrooms, proving the modern Nigerian standard that almost every bedroom is built en-suite.
