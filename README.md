# Hotel Booking Insights Power BI Dashboard
Interactive Power BI dashboard for hotel bookings that surfaces stay trends, booking lead-time, weekday vs. weekend mix, and length-of-stay cohorts. 

🏨 Hotel Booking Insights Dashboard – Power BI
This Power BI project provides a visual analysis of hotel booking behavior for Velora Hotels. The dashboard helps stakeholders understand who is booking, when they're booking, and how they’re booking, enabling better decision-making across marketing, operations, and loyalty programs.

📥 Data Preparation Process

🔹 1. Importing Raw Data:

The dataset was imported from .csv and Excel files containing:
 - Booking details
 - Room pricing
 - Loyalty membership data
 - Booking channels (app, phone, website, etc.)
 - Stay dates and durations

🔹 2. Data Cleaning Techniques:

Using Power Query in Power BI Desktop, several cleaning operations were performed:
 -  Removing nulls in key columns (e.g., stay date, booking method)
 -  Text trimming and case formatting for consistency
 -  Replacing errors with default values (for invalid prices or loyalty levels)
 -  Converting data types (date, currency, numeric)
 -  Creating custom columns for:
      - Booking lead time
      - Loyalty labels
      - Weekday vs Weekend stays



🧮 Data Modeling & DAX Measures

🔹 3. Data Modeling:

Established relationships between fact tables (bookings) and dimension tables (dates, loyalty levels, channels)
Ensured star schema for optimized performance

🔹 4. DAX Measures Created:

Some key measures created using DAX:
 - Total Bookings = COUNT(Bookings[BookingID])
 - Cancellation % = DIVIDE([Cancelled Bookings], [Total Bookings])
 - Total Revenue = SUM(Bookings[Amount])
 - Average Room Rate = AVERAGE(Bookings[RoomPrice])
 - Loyal Customer Rate = DIVIDE([Loyalty Bookings], [Total Bookings])
 - Stay Trend = CALCULATE([Total Bookings], DATESINPERIOD(...))
These measures helped in creating interactive KPIs and trend visuals.



📊 Visualizations Used:

 - Card KPIs	Booking Count, Revenue, Avg. Room Rate
 - Line Chart	Stay trends over time
 - Bar Chart	Weekday vs Weekend bookings, Loyalty tiers
 - Pie Chart	Loyalty vs non-loyal customers, Stay type
 - Stacked Column	Booking lead time categories
 - Matrix Table	Booking channels by loyalty type
 - Slicers	Stay date filter


   
🎯 Key Business Insights:

 - Non-members dominate bookings — loyalty program needs promotion.
 - Most bookings happen within a week of stay, indicating last-minute planning.
 - Higher traffic is seen on weekdays, especially Wednesday and Thursday.
 - Phone and Velora.com are leading booking channels across loyalty levels.
 - Cancellation rate of 28.3% — needs attention to reduce lost revenue.

🛠 (For Refernce) Tools Used:

 - Power BI Desktop
 - Excel / CSV for raw data
 - Power Query
 - DAX (Data Analysis Expressions)
