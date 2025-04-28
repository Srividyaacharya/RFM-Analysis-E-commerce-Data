# E-commerce Customer Segmentation using RFM Analysis

## Problem Statement

In the e-commerce industry, identifying and understanding different customer segments is crucial for optimizing marketing efforts, improving customer retention, and increasing revenue.  
Traditional segmentation methods often fail to capture customer behavior patterns dynamically and accurately.
![image](https://github.com/user-attachments/assets/53d118f0-917a-403f-abfe-6f25f333bd49)

The objective of this project is to apply **RFM (Recency, Frequency, Monetary)** analysis to segment customers based on their purchasing behavior, enabling the business to:

- Categorize customers into meaningful groups (e.g., Platinum, Gold, Silver, Bronze).
- Personalize marketing campaigns for different segments.
- Identify high-value customers and strategize retention efforts.
- Predict customer churn and take proactive actions.
- Maximize marketing ROI by focusing on profitable segments.

## Data Source

- **File**: `E-com_Data.csv`
- **Rows**: 2925
- **Columns**: 12

The dataset contains transaction data with the following columns:

- **CustomerID (float64)**: Unique identifier for each customer.
- **Item Code (object)**: The code for the purchased item.
- **InvoiceNo (float64)**: Unique invoice number for each transaction.
- **Date of purchase (object)**: The date when the purchase was made.
- **Quantity (float64)**: Quantity of items purchased.
- **Time (object)**: Time of purchase.
- **Price per Unit (float64)**: Price of a single unit of the item.
- **Price (float64)**: Total price for the items purchased (Quantity * Price per Unit).
- **Shipping Location (object)**: The location where the product was shipped.
- **Cancelled_status (object)**: Whether the order was cancelled (if applicable).
- **Reason of return (object)**: The reason for a return (if applicable).
- **Sold as set (float64)**: Whether the items were sold as part of a set.

## Approach

1. **Data Exploration**:
   - Checked dataset shape, data types, unique values, missing values, and duplicates.
   - Converted `Date of purchase` into datetime format.
   - Cleaned unnecessary columns for focused analysis.

2. **Feature Engineering**:
   - Calculated RFM metrics (Recency, Frequency, Monetary) for each customer.

3. **RFM Scoring**:
   - Each customer was assigned an RFM score (1 to 5) based on quantiles.

4. **Customer Segmentation**:
   - Applied **K-Means Clustering** to group customers into four distinct segments:
     - **Platinum**, **Gold**, **Silver**, and **Bronze**.

5. **Visualization**:
   - Used `Matplotlib` and `Seaborn` to visualize customer distributions, RFM distributions
     
## Customer Segmentation Insights

The four customer segments identified are:

| Segment   | Characteristics | Strategy |
|-----------|------------------|----------|
| **Platinum** | Very recent purchases, frequent buying behavior, high monetary value | Loyalty rewards, exclusive offers, premium services |
| **Gold**     | Recent buyers, good frequency, good spending | Special discounts, targeted upselling |
| **Silver**   | Moderate recency, lower frequency, moderate spending | Retargeting, promotional campaigns to boost loyalty |
| **Bronze**   | High recency (long time since last purchase), low frequency and low spending | Win-back campaigns, reactivation offers |

✅ **Platinum** customers are your **best** customers and should be prioritized for retention and upsell strategies.

✅ **Gold** customers are also valuable and can be moved to Platinum through loyalty initiatives.

✅ **Silver** customers need encouragement to become more active.

✅ **Bronze** customers are at risk of churn and require targeted marketing to reactivate.

Uploaded data after segmentation in this file ([Segmentation_Customer_details.csv](https://github.com/Srividyaacharya/RFM-Analysis-E-commerce-Data/blob/main/Segmentation_Customer_details.csv))

## Technologies Used

- Python
- Pandas, NumPy (Data manipulation and preparation)
- Matplotlib, Seaborn (Data visualization)
- Jupyter Notebook

## Conclusion

By using RFM analysis and clustering:

- Customers were segmented into four meaningful groups: Platinum, Gold, Silver, and Bronze.
- The business can now implement **targeted marketing strategies** for each segment.
- High-value customers can be **nurtured and retained**, while at-risk customers can be **re-engaged** through tailored campaigns.
- This segmentation improves marketing efficiency, customer lifetime value, and overall profitability.

The project showcases a **data-driven**, **scalable**, and **actionable** approach to customer segmentation in the e-commerce domain.
