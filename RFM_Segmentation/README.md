# RFM (Recency, Frequency and Monetary Value) Segmentation
## Project Overview

The objective of this project was to do a segmentation of the customers based on transactional data which was for a Online Retail Store. Here I have done RFM Segmentation of the customers on the basis of which we can create loyalty programs for our customers which can be helpful in efficiently utlising our marketing expense. 

![image](https://github.com/Subham-here/KNIME-Workflows/assets/170924246/838a181e-ceb2-4270-ab0a-12f60626625f)

The dataset contains fields like InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID and Country. Which tells us about the kind of transactions happened over the period of time. We can check what kind of Item has been purchased by customers from which country, and by what amount the product has been purchased. This is a detailed transactional data of the items purchased by different customers and the order value has also been captured.

## Data pre-processing and Modelling

In the dataset, most of the trnsaction have been captured for United Kingdom and very few have been captured for countries like France and others. So, as the majority of the transactions are from United Kingdom only, I have filtered out the Country for United Kingdom. Then I have checked for any missing values in the UnitPrice column, because as we are dealing with the monetary value, value as a '0' will not contribute to our analysis. So we have filtered out the rows with 0 and ignored the rows with missing values.

Created new Fields of Total Sales (UnitPrice x Quantity) for monetary value, DateTimeDifference (For calculating how recent the transaction is. Lower the number, more recent the transaction is) and grouped by InvoiceNo to find out how frequent the customers have purchased items.
Then I have clustured them randomly using auto binner node based on recencyxFrequencyXMonetary Value

![image](https://github.com/Subham-here/KNIME-Workflows/assets/170924246/b743febf-60fb-4858-abdf-80e6d66bdecf)


## Interpretation
reating a loyalty program using the RFM (Recency, Frequency, Monetary) recommender system for a telecom company like Airtel involves analyzing customer behavior based on these three dimensions to identify segments and tailor marketing strategies accordingly. Here's how you can interpret the analysis results and allocate your marketing budget:

## RFM Analysis Interpretation:

**Recency (R)**: Measures how recently a customer has made a purchase or interacted with Airtel services. Customers with a lower recency value are more likely to be engaged and responsive to marketing efforts.

**Frequency (F)**: Indicates how often a customer purchases or makes a transaction. Higher frequency customers are typically more loyal.

**Monetary Value (M)**: Represents the total monetary value of a customer's transactions with Airtel. This can include monthly bill amounts, recharge amounts, and additional services they subscribe to.

### Segmentation and Targeting:

High-Value Customers (R1F1M1): These are customers who have recently made frequent and high-value transactions. They are your most valuable customers and should be targeted with premium offers, personalized rewards, and exclusive benefits to enhance their loyalty.

Loyal but Less Frequent (R1F0M1): These customers have made significant transactions but are not very frequent. Offer them incentives to increase their engagement, such as bonus data or minutes for recharges, referral rewards, or discounts on add-on services.

New Customers (R1F1M0): These are new customers who have recently made transactions but haven't spent much yet. Focus on providing them with a seamless onboarding experience, welcome bonuses, and incentives to encourage repeat transactions.

At-Risk Customers (R2F2M2): Customers in this segment have not engaged recently, have lower frequency, and spend less. Implement reactivation campaigns, targeted promotions, and personalized offers to win them back.

Low-Value Customers (R3F3M3): These customers have low recency, frequency, and monetary value. They may not be very profitable individually, but collectively they can still be valuable. Use cost-effective strategies such as targeted messaging, cross-selling, or bundle offers to increase their value.

### Marketing Budget Allocation:

**High-Value Segment**: Allocate a significant portion of your marketing budget to retain and enhance the loyalty of these customers. Invest in personalized communications, loyalty rewards, and VIP programs.

**At-Risk Segment:** Allocate resources to re-engage these customers. Utilize targeted promotions, win-back offers, and proactive customer support to prevent churn.

**New Customers**: Invest in onboarding campaigns, welcome offers, and educational content to nurture these relationships and encourage repeat transactions.

**Loyal but Less Frequent:** Design campaigns to increase their frequency of interactions, such as usage-based rewards, special promotions tied to specific actions, and reminders of the value they receive from the Retail chain

**Low-Value Segment:** Use cost-efficient channels like email marketing, SMS campaigns, and targeted digital ads to promote relevant offers and increase their value over time.







