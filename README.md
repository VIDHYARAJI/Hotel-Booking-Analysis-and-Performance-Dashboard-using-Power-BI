# Hotel-Booking-Analysis-and-Performance-Dashboard-using-Power-BI

# Hotel Performance Analytics Dashboard - Power BI  
A comprehensive dashboard to monitor and analyze hotel revenue, occupancy, and operational metrics across multiple cities and properties.

---

## 📌 **Overview**  
This Power BI dashboard provides actionable insights into hotel performance metrics, enabling stakeholders to:  
- Track **revenue, occupancy rates, ADR (Average Daily Rate), and RevPAR** across cities (Delhi, Mumbai, Hyderabad).  
- Compare operational efficiency via **Realization %, Cancellation %, and Customer Ratings**.  
- Drill down into individual hotel properties and room types for granular analysis.  


## 🛠️ **Tools Used**  
1. **Microsoft Power BI**  
   - Dashboard design, data visualization, and interactive filtering.  
   - DAX formulas for metric calculations (e.g., RevPAR, Realization %).  
2. **Data Sources**  
   - Structured datasets (likely stored in **Excel** or **SQL databases**) containing hotel booking, revenue, and operational data.  
3. **Power Query**  
   - Data cleaning, transformation, and integration (e.g., merging city-wise data, handling null values).  



## 📊 **Key Metrics Analyzed**  
| Metric               | Description                                                                 |  
|----------------------|-----------------------------------------------------------------------------|  
| **Revenue**          | Total revenue generated (e.g., ₹0.14bn total in the sample).                |  
| **RevPAR**           | Revenue Per Available Room (e.g., 7,880 total).                             |  
| **Occupancy %**      | Percentage of rooms occupied (e.g., 61.92% average).                        |  
| **ADR**              | Average Daily Rate (e.g., ₹12.72K total).                                   |  
| **DSRN**             | Daily Scorable Room Nights (e.g., 2,528 total).                             |  
| **Realization %**    | Ratio of utilized vs. booked rooms (e.g., 70.26% average).                  |  
| **Cancellation %**   | Percentage of canceled bookings (e.g., 24.74% average).                     |  
| **Average Rating**   | Guest satisfaction score (e.g., 3.62/5 total).                              |  


## 📂 **Data Structure**  
The dataset includes:  
- **Hotel Properties**: 16+ properties across Delhi, Mumbai, and Hyderabad.  
- **Time Period**: 1M (1 month), 3M, 4M, 5M booking cycles.  
- **Key Dimensions**:  
  - City (Delhi, Mumbai, Hyderabad)  
  - Room Type  
  - Booking Duration  
  - Operational Metrics (DRN, DLRN, DURN)  


## 🚀 **Setup Instructions**  
1. **Prerequisites**:  
   - Install **Power BI Desktop** (free from Microsoft).  
   - Ensure datasets (e.g., `.xlsx`, `.csv`, or SQL tables) are structured with consistent columns.  
2. **Load Data**:  
   - Open the `.pbix` file in Power BI Desktop.  
   - Connect to your data source (replace sample data with your dataset).  
3. **Refresh & Customize**:  
   - Use **Power Query** to adjust data transformations if needed.  
   - Modify DAX formulas for metrics like RevPAR:  
     ```DAX  
     RevPAR = DIVIDE([Total Revenue], [Available Rooms])
     ADR = DIVIDE([Revenue], [Total bookings],0)
     DBRN = DIVIDE([Total bookings],[No of days])
     DSRN = DIVIDE([Total capacity], [No of days])
     DURN = DIVIDE([Total checked out], [No of days])
     ```
     
## 📸 **Dashboard Preview**  
[Power BI Dashboard](Power%20BI%20Dashboard.png)  
(Replace with your actual screenshot or describe visuals: revenue by category, trend charts, and metric cards.) 


## 📄 **License**  
This project is open-source under the [MIT License](LICENSE).
