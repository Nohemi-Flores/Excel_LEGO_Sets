# Excel_LEGO_Sets

**The data used for this dashboard can be found at: https://mavenanalytics.io/data-playground/lego-sets
Also, I created a SQL project with this dataset as well! [Check it out](https://github.com/Nohemi-Flores/SQL_LEGO_Sets_Project)**

The Excel dashboard involves users by providing a price slicer and a decades slicer. The bar charts display the set name, set id, US retail price and piece count. There are some cases where more or less than 5 sets appear based on the options selected. Filtering the data to only include rows with every cell filled would reduce the ability to do the analysis shown through the dashboard.


## Dashboard Intro

**These skills made the dashboard possible:**

  **1. Charts:** bar charts
 
 **2. Formulas & Functions:** FLOOR(), 
                              
                              Table.AddColumn(#"Sorted rows", "price", 
                              each if[US_retailPrice] = null then "No price available"
                              else if[US_retailPrice] <25 then "Under $25"
                              else if[US_retailPrice] <50 then "$25-$49.99"
                              else if[US_retailPrice] <100 then "$50-$99.99"
                              else if[US_retailPrice] <200 then "$100-$199.99"
                              else if[US_retailPrice] <300 then "$200-$299.99"
                              else if[US_retailPrice]<400 then "$300-$399.99"
                              else if[US_retailPrice] <500 then "$400-$499.99"
                              else "$500+")
    
  **3. Power Query:** Exctract, Transform, Load

  **4. PivotTables**

---

**This analysis set out to answer 2 questions. The questions covered pieces counts and decades:**

**1. What are the top five LEGO sets each decade? And what are the US retail prices of these sets?**

  
