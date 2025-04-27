
# SkyRevenueInsights

## Overview
SkyRevenueInsights is a data analytics project focused on analyzing airline booking data to derive actionable insights for optimizing revenue, improving user experience, and enhancing operational efficiency. The project leverages a dataset of flight booking logs to perform exploratory data analysis, feature engineering, and strategic recommendations for airline operations.

## Project Objectives
- **Analyze Booking Patterns**: Understand booking volumes, revenue distribution, and cancellation rates across routes, airlines, and time periods.
- **Optimize User Experience**: Improve key metrics such as Conversion Rate (CR), Time to Purchase (TTP), and Seat Selection Success Rate to reduce friction in the booking process.
- **Strategic Recommendations**: Provide data-driven insights to balance airline partnerships, adjust pricing strategies, and manage peak-hour operations.

## Dataset Description
The dataset contains flight booking logs with the following characteristics:
- **Type**: Transactional data where each row represents a flight ticket.
- **Size**: 19,096 records with 20 columns.
- **Time Period**: Booking data from 2023, with the latest booking created on May 31, 2023.
- **Key Features**:
  - `seat_class`: Categorized into 4 classes (First Class, Business, Deluxe, Economy) after feature engineering.
  - Booking timestamps, routes, airline details, and pricing information.
  - Derived metrics such as net revenue, booking volume, and cancellation rates.

## Key Features
- **Exploratory Data Analysis (EDA)**:
  - Identified top routes (e.g., HCM-Hanoi) with high booking volumes and revenue.
  - Analyzed peak booking hours (5-8 AM, 5-7 PM) to manage operational load.
  - Highlighted routes with high cancellation rates for targeted interventions.
- **Feature Engineering**:
  - Consolidated 69 `seat_class` values into 4 categories: First Class (4), Business (16), Deluxe (41), Economy (18,913).
  - Calculated metrics like Conversion Rate, Time to Purchase, and Seat Selection Success Rate.
- **Strategic Insights**:
  - Recommended dynamic pricing for peak hours and flexible fare policies to reduce cancellations.
  - Proposed strategies to diversify airline partnerships, focusing on maintaining strong ties with the dominant airline (A1, contributing 57% of net revenue).
  - Suggested UX improvements, such as real-time seat availability updates, to reduce drop-offs during seat selection.


## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/SkyRevenueInsights.git
   cd SkyRevenueInsights
   ```
2. **Set Up a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Configure Environment**:
   - Set up access to Google Cloud Storage, Snowflake, or BigQuery.
   - Configure Kafka for real-time event ingestion (optional).

## Key Insights
- **Top Route Performance**: HCM-Hanoi leads in bookings (1,551) and net revenue (1,996 units), but its reverse route has higher fares, leading to fewer bookings.
- **Peak Hours**: High booking volumes at 5-8 AM and 5-7 PM create operational pressure, suggesting dynamic pricing or off-peak discounts.
- **Airline Dependency**: Airline A1 dominates with 57% of net revenue (~11.87 billion VND) and 12,518 bookings, necessitating strategies to diversify partnerships.
- **Cancellation Issues**: Routes like Đắk Lắk-Thanh Hóa and Khánh Hòa-Kiên Giang have high cancellation rates, requiring flexible fare policies.
- **UX Bottlenecks**: Seat selection errors contribute to booking drop-offs, addressed through real-time seat availability audits and A/B testing.

## Future Work
- **Machine Learning**: Implement dynamic pricing models and cohort analysis using scikit-learn and MLflow.
- **Real-time Features**: Enhance seat availability lookups with Redis or Druid for faster responses.
- **A/B Testing Expansion**: Test additional UX variants to further improve Conversion Rate and Seat Selection Success Rate.
- **Data Expansion**: Incorporate user interaction logs and conversion funnel data for deeper behavioral analysis.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, please reach out via GitHub Issues or email at [thanhvo.contact@gmail.com].
