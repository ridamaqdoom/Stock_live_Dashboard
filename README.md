# 📈 Artificial Intelligence & Machine Learning Application


📝 Overview
This project features a fully functional Live Stock Dashboard designed to provide real-time stock market insights using data fetched from Yahoo Finance. With its user-friendly interface and SQL-powered backend, this dashboard allows users to track stock performance, view historical trends, and analyze key metrics effortlessly.

💡 Core Features
1. Real-Time Data Integration
Yahoo Finance API: Fetches live and historical stock data for user-selected companies.
Dynamic Dropdown Menu: Users can select specific companies or stock symbols to generate reports.

3. Stock Analysis Metrics
Last Close Price: Displays the most recent closing market price for selected stocks.
Variation Metrics:
Variation #: Calculates the absolute change in stock value over a selected period.
Variation %: Displays the percentage change in stock value, including upward or downward trends with visual arrows.
Weighted Moving Averages: Includes customizable time periods (e.g., 20, 30, 40, 50 days) for detailed trend analysis.

5. Custom Time Periods
Users can select a custom time range (e.g., 1 day, 1 month, 1 year, 5 years) to analyze stock data trends.

7. Data Visualization
Candlestick Graphs: Displays Bullish and Bearish Candles for visual trend analysis.
RSI (Relative Strength Index): Visualized on a percentage scale to highlight stock momentum over time.

9. Advanced Queries
The dashboard utilizes SQL queries and algorithms for precise data analysis, such as:

Calculating the Last Close Price:

Last Close Price = 
VAR _LastDate = CALCULATE(MAX(Stocks[Date]), ALLSELECTED(Stocks))
RETURN
CALCULATE( AVERAGE( Stocks[Close] ), Stocks[Date] = _LastDate)
Computing Variation:
Variation % = 
VAR _Variation = DIVIDE([Last Close Price], [BeginingPeriodPrice]) - 1
VAR _Arrow = IF(_Variation > 0, UNICHAR(129033), UNICHAR(129035)) & " "
RETURN
_Arrow & FORMAT(ABS(_Variation), "0.00%")

📂 Technology Stack
API Integration: Yahoo Finance API for live stock data.
Backend: SQL queries for data manipulation and analysis.
Frontend:
Intuitive UI for easy data visualization.
Dropdown menus and interactive reports.

📊 How It Works
Fetch Stock Data: Using Yahoo Finance API, the dashboard retrieves stock data for a custom time range.
Generate Reports: SQL queries process the data to display key metrics such as closing prices, variations, and averages.
Visual Representation: Candlestick charts and RSI graphs make it easier to understand trends and stock performance.

📚 Key Learning Outcomes
Integrated Yahoo Finance API for real-time stock data fetching.
Designed advanced SQL queries for precise financial analysis.
Developed intuitive visualizations to simplify stock market data interpretation.

