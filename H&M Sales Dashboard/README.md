# H&M Sales Dashboard

## Project Background

H&M is a global fast-fashion retailer operating across online and in-store channels, offering a wide range of apparel and accessories across product categories and seasons. The company’s business model relies on high transaction volumes, trend-driven assortments, and efficient product performance monitoring.

The objective of this project is to analyze historical transaction data across multiple years (2018-2020) to understand **sales distribution, product performance, customer behavior, and seasonal preferences**. This analysis focuses on identifying which product types and products contribute most to total purchases and revenue, how purchasing behavior differs across age groups and channels, and how colour and pattern preferences vary by season.

Insights and recommendations are provided on the following key areas:
- **Sales & Revenue Trends**
- **Product & Category Performance**
- **Customer Demographics & Purchase Behavior**
- **Seasonal Colour & Pattern Trends**

The interactive Tableau dashboard can be found [here](https://public.tableau.com/app/profile/anweasha.saha/viz/HMSalesDashboard_17439279279890/Dashboard1).

## Data Structure & Initial Checks

The dataset consists of three primary tables with historical transactional data and supporting metadata.

### Tables Overview

- **articles**: Contains detailed metadata for each article_id available for purchase, including product category, garment type, perceived colour, pattern, and descriptive attributes.

- **customers**: Contains metadata for each customer_id, including age, age group, and club membership status.

- **transactions_train**: Contains transaction-level purchase data (September 2018 - September 2020), including customer_id, article_id, transaction date, price, and sales channel.
Duplicate rows indicate multiple purchases of the same item by the same customer on the same date.

## Executive Summary

### Overview of Findings

Between 2018 and 2020, H&M recorded **31.8M total purchases**, generating approximately **€884.6K in revenue**, with **online purchases accounting for 70.4% of total transactions** and **a high customer repeat rate of 90.35%**. Customers in their **20s and 30s contribute the highest share of purchases**, making this age group a key driver of overall sales activity.

Sales activity shows visible month-to-month fluctuations, while product demand is highly concentrated within a small set of product types. **Trousers, dresses, and sweaters emerge as the highest-impact categories**, together accounting for a disproportionate share of total revenue. Category-level analysis shows **Ladieswear as the dominant contributor to overall purchases**, with **consistent demand for neutral colours and solid patterns across seasons**, alongside clear **seasonal shifts toward lighter colours and striped patterns in warmer months**.

<img width="1190" height="109" alt="Screenshot 2025-12-28 at 7 00 04 PM" src="https://github.com/user-attachments/assets/e687ca90-efdf-4aaa-aa7f-4317087e3d5e" />

## Insights Deep Dive

### Sales & Revenue Trends
-	A **recurring spike in both purchases and revenue is visible during the summer months of 2019 and 2020**, suggesting **increased shopping activity during end-of-season sales** and discount periods.
-	Monthly sales and revenue show clear fluctuations across the 2018–2020 period, indicating strong seasonality rather than steady linear growth. Despite short-term peaks, overall performance remains cyclical, highlighting the importance of aligning inventory planning and promotions with seasonal demand patterns.

<img width="578" height="340" alt="Screenshot 2025-12-28 at 6 57 34 PM" src="https://github.com/user-attachments/assets/5dc17a9d-492b-412f-a643-d886dd0b43e3" />

### Product & Category Performance
- **Ladieswear emerges as the dominant category by purchase volume**, contributing over **20M purchases** and significantly outperforming Menswear, Divided, Sport, and Children. Within Ladieswear, the **Garment Upper Body** subcategory accounts for the largest share of purchases.
- A highly concentrated revenue pattern is visible at the product-type level, where **Trousers, Dresses, and Sweaters together account for 66.79% of total revenue**, as highlighted by the Pareto analysis.
- At the individual product level, a small number of SKUs, such as *Jade HW Skinny Denim TRS* and *Luna Skinny RW*, generate disproportionately higher revenue compared to the rest of the product catalog.

<img width="1040" height="358" alt="Screenshot 2025-12-28 at 7 02 27 PM" src="https://github.com/user-attachments/assets/678f1774-7630-442e-89d3-fb50d236d373" />

### Customer Demographics & Purchase Behavior
- **Online purchases account for the majority of total transactions**, significantly outperforming in-store purchases across most age groups.
- The **20s and 30s** age groups show the highest overall purchase volumes, particularly through online channels, while in-store purchases remain comparatively lower across all demographics.

<img width="580" height="300" alt="Screenshot 2025-12-28 at 6 58 53 PM" src="https://github.com/user-attachments/assets/abd27253-f95a-4278-9b4b-037575209566" />

### Seasonal Colour & Pattern Trends
- **Neutral colours such as black, white, grey, and beige show consistently strong demand across all seasons**, indicating stable, year-round customer preferences.
- **Spring and summer months show increased interest in lighter colours and striped patterns**, suggesting a seasonal shift toward fresher, warmer-weather styles.
- Fall and winter periods exhibit relatively higher demand for darker tones, melange textures, and heavier patterns, while solid patterns remain popular regardless of season.

<img width="680" height="300" alt="Screenshot 2025-12-28 at 6 58 18 PM" src="https://github.com/user-attachments/assets/9876db5c-e407-47bd-b329-025832bb3d05" />

## Recommendations

Based on the insights above, the findings can help inform decisions across marketing, product, and merchandising teams:
- The strong revenue concentration among **Trousers, Dresses, and Sweaters** highlights where inventory planning and assortment decisions can be prioritized for maximum impact.
- The dominance of **Ladieswear and its top-performing subcategories** suggests opportunities for product teams to deepen assortments and for marketing teams to focus category-led campaigns.
- Higher **online purchase activity among younger age groups** can support more targeted digital marketing and channel-specific campaign strategies.
- Clear **seasonal shifts in colour and pattern preferences** provide inputs for merchandising calendars, creative planning, and seasonal promotions.
- **Top-selling individual products** can be leveraged as anchor items for promotions, bundles, and cross-selling efforts to maximize visibility and conversion.

## Assumptions and Caveats
- **Currency** was not specified in the dataset; all monetary values are assumed to be in **Euros (€)**.
- **Sales Channel Mapping** was assumed as:
  - Sales Channel ID 1 = In-store
  - Sales Channel ID 2 = Online
- **Seasonality** was inferred from transaction dates using month-based logic:
  - Spring: March–May
  - Summer: June–August
  - Fall: September–November
  - Winter: December–February
- Duplicate rows in transaction data were treated as **multiple purchases of the same item**, not data errors.
