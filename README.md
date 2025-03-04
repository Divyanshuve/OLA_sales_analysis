# OLA_sales_analysis
This is my latest Data Analyst project on OLA sales Analysis Dashboard.
I utilized MYSQL, DAX, Power BI, and Excel to create an insightful sales dashboard for OLA Sales  and Here’s a glimpse into the process and the outcomes:
Process:
1. Data Collection: Gathered sales data from various sources and consolidated it into Excel.
2. Data Cleaning: Ensured data accuracy and consistency by cleaning and transforming the data in Excel.
3. Data Import: Importing the data on MYSQL for further solutions for the objectives by writing some queries.
4. Data Modeling: Used DAX to create calculated columns and measures for deeper analysis.
5. Visualization: Leveraged Power BI to design an interactive and visually appealing dashboard.
   
SQL Question (Queries)

1. Retrieve all successful bookings:
SELECT * FROM bookings WHERE Booking_Status = 'Success';

2. Find the average ride distance for each vehicle type:
SELECT Vehicle_Type, AVG(Ride_Distance) as avg_distance FROM bookings GROUP BY
Vehicle_Type;

3. Get the total number of cancelled rides by customers:
SELECT COUNT(*) FROM bookings WHERE Booking_Status = 'cancelled by Customer';

4. List the top 5 customers who booked the highest number of rides:
SELECT Customer_ID, COUNT(Booking_ID) as total_rides FROM bookings GROUP BY
Customer_ID ORDER BY total_rides DESC LIMIT 5;

5. Get the number of rides cancelled by drivers due to personal and car-related issues:
SELECT COUNT(*) FROM bookings WHERE cancelled_Rides_by_Driver = 'Personal & Car
related issue';

6. Find the maximum and minimum driver ratings for Prime Sedan bookings:
SELECT MAX(Driver_Ratings) as max_rating, MIN(Driver_Ratings) as min_rating FROM
bookings WHERE Vehicle_Type = 'Prime Sedan';

7. Retrieve all rides where payment was made using UPI:
SELECT * FROM bookings WHERE Payment_Method = 'UPI';

8. Find the average customer rating per vehicle type:
SELECT Vehicle_Type, AVG(Customer_Rating) as avg_customer_rating FROM bookings
GROUP BY Vehicle_Type;

9. Calculate the total booking value of rides completed successfully:
SELECT SUM(Booking_Value) as total_successful_value FROM bookings WHERE
Booking_Status = 'Success';

10. List all incomplete rides along with the reason:
SELECT Booking_ID, Incomplete_Rides_Reason FROM bookings WHERE Incomplete_Rides =
'Yes';

POWER BI SOLUTIONS:-  
1. Objectives and Solutions:-
A. Objective: Identify the overall booking performance for July 2024.
Solution: The dashboard reveals a total of 103,024 bookings with a total booking value of ₹56.53M. This indicates strong demand and successful customer engagement.

2. Booking Success Rate:
Succeeded Bookings: 63,967 (62.09%)
Cancelled Bookings: 39,057 (37.91%)
The significant percentage of cancellations highlights the need to address driver availability and customer cancellation issues.

3. Revenue Analysis by Payment Method
Cash: ₹18M (majority)
UPI: ₹12M (growing digital payment adoption)
Debit Card: ₹2M (moderate usage)
Credit Card: ₹1M (limited use)

4. Daily Revenue Analysis
Daily booking values range between ₹40K and ₹60K.
 4.1 Customer Preferences and Loyalty
Cash payments are preferred, highlighting the importance of maintaining cash handling processes.
 4.2 Significant use of UPI suggests a shift towards digital payments. Enhancing these options could attract more customers.
 4.3 Identifying top customers allows targeted marketing strategies to enhance loyalty and increase repeat bookings.

5. Key Metrics
Total Bookings: 1,03,024
Succeeded Bookings: 63,967 (62%)
Cancelled Bookings: 39,057 (38%)

6. Analysis of Cancellations
Primary Reasons:
Drivers Not Moving Towards Pickup: 3.18K (30.24%)
Drivers Asking to Cancel: 2.67K (25.43%)
Change of Plans: 2.08K (19.82%)
AC Not Working: 1.57K (14.93%)
Wrong Address: 1.01K (9.57%)
This suggests possible operational inefficiencies or communication issues.
Cancellations due to personal and car-related issues constitute the largest portion at 35.49%, indicating vehicle maintenance or driver availability problems.

Recommendations/Solution:-
1. Improving Driver Efficiency: Address the issue of drivers not moving towards pickups promptly. Implement better tracking and communication systems.
2. Customer Communication: Enhance communication with customers to reduce cancellations due to misunderstandings or miscommunications.
3. Vehicle Maintenance: Regularly maintain and inspect vehicles to prevent cancellations due to car-related issues.
4. Customer Satisfaction: Address specific complaints, such as non-functioning AC and wrong addresses, to improve the overall customer experience
