Food Delivery Dataset

Primary audience – Operations / Logistics team

Questions Answered -
1.	What are the key factors that influence delivery time?
2.	How do delivery driver characteristics affect efficiency?
3.	How do environmental and situational factors contribute to delays?
4.	How accurately can delivery time be predicted based on available features?

Cleaning and Analysis
The step-by-step cleaning and analysis process is the Jupyter notebook uploaded to the github.

Analysis Conclusion
This project explored the operational, environmental, and driver-related factors influencing food delivery time, using a combination of exploratory analysis, feature engineering, and visualization. The following summarizes the key findings aligned to the four research questions.
1. Key Factors Influencing Delivery Time
The analysis shows that delivery duration is affected by several interacting factors rather than a single dominant variable.
The strongest contributors to longer delivery times include:
• Road Traffic Density (Strongest Factor)
•	Deliveries in High and Jam traffic conditions consistently take longer.
•	Traffic also increases delivery variability, making ETAs less predictable.
•	Correlation: +0.42 (highest in the dataset)
• Multiple Deliveries
•	Handling more than one order significantly increases delivery time.
•	Correlation: +0.39
• Delivery Distance
•	Delivery time increases with distance, but the relationship is not perfectly linear due to other operational delays.
•	Correlation: +0.32
• Vehicle Condition (Moderate Negative Impact)
•	Poor vehicle condition slightly correlates with longer delivery times.
•	Correlation: –0.24
Overall: Traffic, distance, and multi-order assignments are the primary drivers of increased delivery duration.

2. Impact of Driver Characteristics on Efficiency
Driver-related features show meaningful effects on delivery performance:
• Driver Ratings (Important Indicator)
•	Higher-rated drivers achieve faster and more consistent delivery times.
•	Lower-rated drivers show higher medians and more extreme delays.
•	Correlation: –0.36, demonstrating that driver quality matters.
• Driver Age
•	Minimal correlation overall, indicating that age is not a strong factor in delivery speed.
•	Correlation: +0.30 (weak and likely indirect)
Conclusion: Driver ratings, not age, are the useful predictor of efficiency. High-rated drivers deliver faster and with fewer extreme delays.

3. Environmental & Situational Factors Contributing to Delays
• Weather Conditions
•	Stormy, foggy, and cloudy weather lead to longer and more variable delivery times.
•	Sunny conditions are the fastest and most predictable.
• Rush Hour Times
•	Rush hour introduces modest delays but is less impactful than traffic intensity.
•	Correlation: +0.18
• Weekend vs Weekday
•	Minimal difference between weekend and weekday performance.
• Pickup Delay (Operational Delay)
•	Pickup delay shows a visual relationship with delivery time (higher delays → longer total time).
•	But due to rounded data (5, 10, 15 min), correlation appears artificially low.
Conclusion: Environmental factors such as weather and traffic, as well as operational delays like pickup time, significantly influence delivery performance.

4. Predictability of Delivery Time
Based on the correlations and visual patterns:
•	Delivery time is influenced by multiple moderate-strength predictors, meaning a predictive model would likely perform reasonably well.
•	No single feature fully explains delivery duration, but together:
o	traffic,
o	distance,
o	multi-order assignments,
o	pickup delay,
o	driver ratings
form a solid foundation for ETA prediction.
This supports the value of building machine-learning models (e.g., linear regression, random forest) to forecast delivery times with good accuracy.



