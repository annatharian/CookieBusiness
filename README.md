# Create a dashboard to analyse the sales data for a cookie business

The main goal of this project was to apply DAX formulae to create explicit measures and columns to aid the analysis. 

### DAX Formula used for this project:

1. Total Number of Cookies Sold = SUM(Orders[Units Sold])
2. Total Profit = SUM(Orders[Revenue]) - SUM(Orders[Cost])
3. Profit = Orders[Revenue] - Orders[Cost]
4. Profit Margin = [Total Profit]/SUM(Orders[Revenue])
5. Has chocolate = IF(FIND("Chocolate", Orders[Product],1,0)>0,"Has Chocolate", "No chocolate")
6. Distinct Customers = DISTINCTCOUNT(Orders[Customer ID])
7. Day of Week = WEEKDAY(Orders[Date],1)
8. Count of Orders = COUNTROWS(Orders)
9. Total Profit per Cookie = SUMX('Cookie Types', 'Cookie Types'[Units Sold]*('Cookie Types'[Revenue Per Cookie]-'Cookie Types'[Cost Per Cookie]))

### The Power BI dashboard:

![cookie business dashboard](https://github.com/user-attachments/assets/393be0a9-08d5-4720-a7f5-e1171cb80f9b)
