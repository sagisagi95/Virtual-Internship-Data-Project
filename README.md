# Data Analytics in Quantium

**Source:** https://www.theforage.com/simulations/quantium/data-analytics-rqkb

## Task 1: Data Cleaning and Customer Analytics

## 📝Business Context
You are part of Quantium’s retail analytics team and have been approached by your client, the Category Manager for chips, who wants to better understand the types of customers who purchase chips and their purchasing behaviour within the region.

The insights from your analysis will feed into the supermarket’s strategic plan for the chip category in the next half year.

## 🎯Tasks
   - Analyze transaction and customer data to identify trends and inconsistencies.
   - Develop metrics and examine sales drivers to gain insights into overall sales performance.

### 🗂️Dataset Overview
2 tables: Transaction_Data.xlsx and Purchase_Behavior.xlsx

**Table Transaction_Data**
Rows: 246740; Columns: 8
| Column | Data Type | Description |
|:--|:--|:--|
| **date** | INT | Date of customer purchase. |
| **store_nbr** | INT | store number. |
| **lylty_card_nbr** | INT | Loyalty card number of customers. |
| **txn_id** | INT | Unique identifier for transaction. |
| **prod_nbr** | INT | Product number. |
| **prod_name** | TEXT | Product name. |
| **prod_qty** | INT | Product quantity. |
| **tot_sales** | FLOAT | Total sales. |

**Table Purchase_Behavior**
Rows: 72637; Columns: 3
| Column | Data Type | Description |
|:--|:--|:--|
| **lylty_card_nbr** | INT | Loyalty card number of customers. |
| **lifestage** | TEXT | customer segmentation by family status (e.g. Young singles/couples, New families, Retirees). |
| **premium_customer** | TEXT | customer segmentation by their spending (Budget/Mainstream/Premium). |

---

LIFESTAGE: Customer attribute that identifies whether a customer has a family or not and what point in life they are at e.g. are their children in pre-school/primary/secondary school.

PREMIUM_CUSTOMER: Customer segmentation used to differentiate shoppers by the price point of products they buy and the types of products they buy. It is used to identify whether customers may spend more for quality or brand or whether they will purchase the cheapest options.

Note: While the data set would not normally be considered large, some operations may still take some time to run. 

## Submission
[View SalesAnalysis.sql file here](SalesAnalysis.sql)
- Tools: MySQL
- Skills used: Converting Data Types, Manipulation syntax, String Expressions, Windows Functions, Joins, CTE

## 💡Key Findings 
1. As we can see from customer behavior patterns:
- Sales are coming mainly from budget-large households and younger mainstream Singles/Couples
- The chips category is a mainstream (mass-market) category, not driven by premium buyers

2. Budget–Older Families are the biggest sales drivers
Although they are not the largest customer group, they still contribute the highest share of total chips sales with the largest product quantity (in total).
-> This may suggest:
- Their behaviour is volume-driven rather than premium-driven: they don’t pay the highest price per pack, but they buy more.
- They buy in larger quantities per visit, and buy for households with multiple members.

3. Mainstream customers dominate the shopper base (>40%), Young Singles/Couples and Retirees within this segment keep their total sales contribution high.

4. Mainstream Singles/Couples are more willing to pay for chips
Both young and mid-age Mainstream Singles/Couples show higher willingness to pay per packet compared to Budget or Premium customers in the same lifestage.
-> This may suggest they value brand, quality, or preferred flavors over price sensitivity.
- There being fewer Premium mid-age and young singles/couples buying chips compared to their mainstream counterparts, despite being categorized as those buying higher-price products.
-> maybe due to premium shoppers being more likely to buy healthy snacks, and when they buy chips, this is mainly for entertainment purposes rather than their own consumption.
-> in the chips category, mainstream singles/couples show the real premium-like behaviour.

5. For 2 customer segments that contribute the most to sales: Kettle & Pringles was their top choices, and they prefer medium-sized packs of chips (175g and 150g)

## Some Recommendations
To further increase sales, we should:
- For Mainstream - Young singles/couples: Focus on increasing basket size, like flavor-driven bundles, new flavors innovation or brand loyalty rewards
- For Budget - Older Families: Focus on value-driven promos, upselling and cross-selling
- Consider promoting/prioritizing for placement the medium-sized packs of chips (175g and 150g)
