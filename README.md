# QSR-FMCG
Quick Service Restaurant" and "FMCG" stands for "Fast-Moving Consumer Goods"
# Crunchy Corner Business Optimization & Budgeting Dashboard

![Image](https://github.com/user-attachments/assets/365b72d1-280f-4543-868e-02b730b2229b)

## Project Overview  
This project analyzes and optimizes the financial performance of **Crunchy Corner**, one of India's largest fast-food restaurant chains. The goal is to create an interactive Power BI dashboard to monitor key metrics, analyze budget variance, and identify optimization opportunities using advanced DAX calculations.  

![Image](https://github.com/user-attachments/assets/11725d41-8f58-4027-9181-0e93c7c5ee3e)

### Key Objectives  
- Analyze historical financial data for performance trends.  
- Optimize business operations through gross profit and SKU analysis.  
- Conduct budgeting and variance analysis.  
- Implement dynamic visualizations (Pareto charts, Mekko charts, conditional formatting) for actionable insights.  

---

## Data Sources  
- **Unclean Data**: [Google Drive Folder](https://drive.google.com/drive/u/2/folders/1RqLzgf_5P2n4-XBNThF-18j9NpeKS9XS)  
- **Cleaned Data**: [Google Drive Folder](https://drive.google.com/drive/u/2/folders/1fm-456LUYxFk_5JKYNZJ97p1B2bXxw4n)  

---

## Presentation Overview ([PPTX](https://drive.google.com/drive/u/2/folders/1fm-456LUYxFk_5JKYNZJ97p1B2bXxw4n))  
The PowerPoint deck outlines the project workflow, including:  
1. **Data Preparation**: Cleaning and structuring raw data.  
2. **Financial Performance Analysis**:  
   - Actual vs. Budget comparisons using DAX.  
   - Gross Profit Margin calculations.  
3. **Business Optimization**:  
   - Pareto Analysis (Top SKUs by sales and profit).  
   - Dynamic Gross Profit vs. Volume comparisons.  
4. **Budgeting Analysis**:  
   - Variance analysis and PVM (Price-Volume-Mix) metrics.  
5. **Advanced DAX Functions**:  
   - Time intelligence (YTD, monthly sales).  
   - Running totals, cumulative percentages, and ranking.  
   - Conditional formatting for profit/loss visualization.  

---

## Dashboard Features ([PBIX](https://drive.google.com/drive/u/2/folders/1fm-456LUYxFk_5JKYNZJ97p1B2bXxw4n))  
The Power BI dashboard includes:  
### Key Visualizations  
- **Financial Performance**: Actual vs. Budget variance charts.  
- **Pareto Analysis**: Top 20% SKUs contributing to 80% of revenue.  
- **Mekko Chart**: SKU sales distribution across regions.  
- **Quadrant Analysis**: Gross profit vs. sales volume.  
- **Time-Based Metrics**: Monthly/YTD sales trends.  

### Technical Highlights  
- **DAX Measures**:  
  ```dax  
  -- Cumulative Sales %  
  Cumulative % = 
  VAR sales = SUM(OrderBreakdown[Sales])
  RETURN
  DIVIDE(
    CALCULATE(SUM(OrderBreakdown[Sales]),
    FILTER(ALLSELECTED(ListOfOrders[State]),
      CALCULATE(SUM(OrderBreakdown[Sales])) >= sales)),
    [Total Sales])  
  ```
  ```dax  
  -- Conditional Formatting for Profit  
  Conditional Formatting = 
  IF(SUM(OrderBreakdown[Profit]) > 0, "Green", "Red")  
  ```
- **Dynamic Filters**: Timeframe (Monthly/YTD), Top N SKUs, and regions.  

---

## How to Use  
1. **Data**: Download the cleaned dataset from the Google Drive folder.  
2. **Dashboard**: Open the `.pbix` file in Power BI Desktop.  
3. **Presentation**: Review the PDF/PPTX for methodology and insights.  

---

## Conclusion  
This dashboard empowers Crunchy Corner’s stakeholders to:  
- Track financial health in real-time.  
- Identify underperforming SKUs and regions.  
- Optimize budgets and resource allocation.  


---

**Links Summary**  
- Unclean Data: [Link](https://drive.google.com/drive/u/2/folders/1RqLzgf_5P2n4-XBNThF-18j9NpeKS9XS)  
- Clean Data, PPTX, PDF, PBIX: [Link](https://drive.google.com/drive/u/2/folders/1fm-456LUYxFk_5JKYNZJ97p1B2bXxw4n)

Contact Me

- LinkedIn: [Link](https://www.linkedin.com/in/rashid-khan-analyst/)  
- GitHub: [Link](https://github.com/Rashidengg) 
