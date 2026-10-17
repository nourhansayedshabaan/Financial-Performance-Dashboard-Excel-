# Financial Performance Dashboard (Excel)

An interactive Excel dashboard that analyses sales and profitability across segments, countries, products and discount levels, and pinpoints where the business loses money and why.

Show Image

Key finding

Enterprise is the only loss-making segment. It generates 16% of sales but runs a -3.3% margin (a $0.61M net loss on $18.76M of sales). Its average list price ($125/unit) sits only 4% above its average COGS ($120/unit), so any discount above about 4% turns an order into a loss.

What the data shows
Finding	Evidence
Profit is concentrated	Government delivers 67% of profit from 45% of net sales; Small Business adds 25% of profit.
The loss sits in one segment	58 of 95 Enterprise orders lose money; no other segment has a single loss-making order.
Discounts explain the losses	All 58 loss orders carry discounts of 5-15%; profitable Enterprise orders carry 0-3%.
Margin falls as discounts rise	Overall margin drops from 21.9% (no discount) to 9.1% (High band), and the same ordering holds inside every segment.
Growth is not profit	Like-for-like, Enterprise sales rose +40% while its net loss widened from $0.19M to $0.22M.
Company trend is healthy	Like-for-like (Sep-Dec), sales +36%, profit +40%, margin 14.7% to 15.1%, discount rate 7.5% to 6.4%.

Association, not proof of cause: the data cannot show why discounts were granted.

Dashboard features
Four dropdown filters (Period, Segment, Country, Product). Every KPI, chart and table recalculates; set all to All to reset.
Six KPI cards with like-for-like (LFL) change: Net Sales, Profit, Profit Margin, Discount Rate, Units Sold, Loss-Making Orders. Arrows are green when the change is favourable and red when unfavourable (a higher discount rate or a larger loss shows red).
Trend chart: net sales and profit columns with margin on a separate axis.
Waterfall: where each sales dollar goes (gross sales, discounts, COGS, profit).
Segment ranking and margin by discount band charts.
Heatmap (segment x discount band) separating the discount effect from segment mix.
Enterprise unit economics table and product / country performance tables.
Written insights, risks and recommended actions.
Dataset
Source: Company Financials dataset on Kaggle (sample data, not a real company).
Grain: one row = one segment x country x product x month sales record.
695 rows analysed (5 rows with errors in the Profit column were removed), 5 segments, 5 countries, 6 products, Sep 2013 to Dec 2014.
Data quality notes
2013 contains only Sep-Dec (175 rows), so a full-year comparison would be misleading. All comparisons use like-for-like Sep-Dec 2014 vs Sep-Dec 2013.
The Date column is unreliable (day and month are swapped). Year and Month_Number are used for all time analysis.
Text fields contain stray spaces (e.g. " Paseo "), so filters use wildcard matching.
Manufacturing_Price x Units_Sold does not equal COGS, and Sale_Price follows the segment rather than the product. COGS and Sales are used as reported; no costs were invented.
36 rows have fractional Units_Sold; kept as reported.
Source arithmetic holds for all rows: Gross Sales - Discounts = Sales, and Sales - COGS = Profit.
No targets, budgets or customer-level data exist, so no target comparisons are shown. The currency unit is not stated; values are shown with a $ symbol.
KPI definitions
KPI	Definition
Net Sales	Gross Sales - Discounts
Profit	Net Sales - COGS (gross profit, before operating costs)
Profit Margin	Profit / Net Sales
Discount Rate	Discounts / Gross Sales
Units Sold	Sum of Units_Sold
Loss-Making Orders	Orders with negative profit (count, share and total loss)
Recommendations
Review Enterprise pricing and discount policy: set an approval threshold near the break-even discount (about 4%) and re-test list price against COGS.
Re-check the 58 loss-making Enterprise orders: who approved the discounts, and were they tied to volume or strategic accounts?
Validate Channel Partners costs with finance. Its 73% margin on 1.5% of sales is unusually high; confirm it is real before treating it as an opportunity.
Reconcile COGS with Manufacturing_Price and fix the Date field at source.
Provide targets and full-year 2013 data so performance can be judged against plan.
Limitations
Gross profit only; no operating expenses, so this is not net income.
Sample data with inconsistent cost logic (see data quality notes); confirm cost data before acting on pricing decisions.
Partial prior period (4 months) limits trend conclusions.
How to use
Open Financial_Dashboard.xlsx in desktop Excel and enable editing.
Use the four dropdowns at the top of the Dashboard sheet.
Sheet guide: Dashboard (the report), Calc (all dashboard formulas), Lists (dropdown options), Notes (definitions, data quality, validation), Financials (source data), Detail1, Detail2, Sheet7 (original analysis sheets, kept as received).

The dashboard uses formulas (SUMIFS) rather than PivotTables, so it reads whole columns of Financials and appended rows are included. New months need a row in Calc; new segments, countries or products need rows in Lists and Calc.

Tools

Microsoft Excel: SUMIFS formulas, data validation dropdowns, conditional formatting, combo and waterfall-style charts, Power Query for data preparation.

Author

Nourhan Sayed 
