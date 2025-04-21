# Porter – Neural Networks Regression

## Abstract
Porter is India’s largest intra-city logistics marketplace, serving over 150,000 driver‑partners and more than 5 million customers. To improve customer experience and operational efficiency, Porter wants to accurately estimate delivery times based on order details, delivery‑partner availability, and dynamic traffic conditions. This case study applies a neural network regression approach—leveraging features such as order timestamp, items ordered, pricing, partner availability, and traffic estimates—to predict delivery duration. The result will enable Porter to provide real‑time, accurate ETAs and optimize logistics operations.

## Problem Description
- **Objective**: Predict the delivery duration (in minutes) for each order instance.
- **Data**: Each record contains order metadata (timestamp, location, items, pricing) and delivery‑partner details (availability, historical performance), plus external traffic estimates.
- **Challenges**:
  - Extracting accurate “time to deliver” from raw timestamps.
  - Handling seasonal/weekly patterns and peak-hour traffic.
  - Feature engineering for categorical and time-based variables.
  - Dealing with outliers (e.g., extremely late deliveries).

## Business Questions
1. **Feature Importance**: Which variables most influence delivery time?  
2. **Prediction Accuracy**: How well can a neural network model estimate delivery duration?  
3. **Temporal Effects**: How do hour of day and day of week impact delivery efficiency?  
4. **Preprocessing Impact**: Which cleaning and outlier-removal steps yield the best performance gains?  
5. **Model Tuning**: What network architecture and hyperparameters (activation functions, optimizers, learning rates) produce the lowest MAE/RMSE?  
6. **Productionization**: How can this model be deployed to update ETAs dynamically for customers and partner apps?

## Dataset & Column Profiling
- **Order_ID**: Unique identifier for each order  
- **Order_Timestamp**: Date and time when the order was placed  
- **Pickup_Location**: Geocode or zone ID for pickup  
- **Dropoff_Location**: Geocode or zone ID for delivery  
- **Items_Count**: Number of items in the order  
- **Total_Amount**: Order value (INR)  
- **Partner_ID**: Delivery-partner unique ID  
- **Partner_Availability**: Boolean or categorical status at order time  
- **Traffic_Estimate**: Precomputed traffic delay in minutes  
- **Actual_Pickup_Time**: Timestamp when partner picked up the order  
- **Actual_Delivery_Time**: Timestamp when order was delivered  
- **Delivery_Duration**: Target variable (minutes between pickup and delivery)

