# Flight Price Prediction: EDA and Feature Engineering

## Project Overview

This project aims to predict flight prices using a dataset with various features. Through exploratory data analysis (EDA) and feature engineering, we clean the data, extract meaningful insights, and prepare it for modeling.

## Features

The dataset consists of the following features:

1. **Airline**: The name of the airline company. It is a categorical feature with 6 different airlines.
2. **Flight**: Information regarding the plane's flight code. It is a categorical feature.
3. **Source City**: The city from which the flight takes off. It is a categorical feature with 6 unique cities.
4. **Departure Time**: A derived categorical feature created by grouping time periods into bins, storing information about the departure time with 6 unique time labels.
5. **Stops**: A categorical feature with 3 distinct values indicating the number of stops between the source and destination cities.
6. **Arrival Time**: A derived categorical feature created by grouping time intervals into bins, storing information about the arrival time with 6 distinct time labels.
7. **Destination City**: The city where the flight will land. It is a categorical feature with 6 unique cities.
8. **Class**: Information on seat class, having two distinct values: Business and Economy.
9. **Duration**: A continuous feature displaying the overall amount of time it takes to travel between cities in hours.
10. **Days Left**: A derived feature calculated by subtracting the trip date from the booking date.
11. **Price**: The target variable storing information on the ticket price.

## Data Cleaning and Feature Engineering

### Steps Followed

1. **Import Libraries**: Necessary libraries for data manipulation, visualization, and preprocessing.
2. **Read Data**: Load the dataset.
3. **Data Summary**: Check for missing values and data types, and obtain statistical summaries.
4. **Feature Engineering**:
   - Split `Date_of_Journey` into separate Date, Month, and Year columns.
   - Split `Arrival_Time` and `Dep_Time` into hours and minutes.
   - Handle `Duration` by splitting it into hours and minutes.
   - Map values in `Total_Stops` to numerical values.
5. **Encoding Categorical Features**: Use OneHotEncoder for `Airline`, `Source`, `Destination`, and `Additional_Info`.
6. **Combining Data**: Combine encoded features with the original dataset.

## Exploratory Data Analysis

### Distribution of Flight Prices

- **Histogram**: Visualize the distribution of flight prices.

### Flight Prices by Airline

- **Boxplot**: Compare flight prices across different airlines.

#### Insight: 

The minimum price for Jet Airways Business is higher than the maximum price of other airlines, indicating that Jet Airways Business class is significantly more expensive.

### Average Flight Price Over Time

- **Line Plot**: Show the trend of average flight prices over time.

#### Insight: 

Flight prices show an increasing trend initially, followed by a sudden decrease over time.

## Conclusion

This project involves extensive data cleaning and feature engineering to prepare the dataset for flight price prediction. EDA reveals important insights into flight prices by airline and over time, helping to understand the factors affecting flight pricing.

## Future Work

- **Modeling**: Train machine learning models to predict flight prices.
- **Hyperparameter Tuning**: Optimize model performance.
- **Feature Importance**: Identify the most influential features affecting flight prices.

## Repository Structure

- `flight_price.xlsx`: Dataset file.
- `flight_price_prediction.ipynb`: Jupyter notebook with code for data cleaning, feature engineering, and EDA.
- `README.md`: Project documentation.

## Libraries and Tools Used

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn

---

For any questions or suggestions, please feel free to open an issue or submit a pull request.
