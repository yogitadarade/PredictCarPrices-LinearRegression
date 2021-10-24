

# Predict Car Prices  Using LinearRegression.
Performed following task
1.    Define the problem and perform an Exploratory Data Analysis
2.    Illustrate the insights based on EDA.
3.    Data pre-processing
4.    Model building - Linear Regression
5.    Test assumptions of linear regression model
6.    Model performance evaluation
7.    Actionable Insights & Recommendations

To check the Notebook click [here](https://github.com/yogitadarade/PredictCarPrices-LinearRegression/blob/fec6fc28e1b34caba71c5143a7a8ed6af8815904/predict-used-car-prices-linearregression.ipynb)

**Context** 

There is a huge demand for used cars in the Indian Market today. As sales of new cars have slowed down in the recent past, the pre-owned car market has continued to grow over the past years and is larger than the new car market now. Cars4U is a budding tech start-up that aims to find footholes in this market.
In 2018-19, while new car sales were recorded at 3.6 million units, around 4 million second-hand cars were bought and sold. There is a slowdown in new car sales and that could mean that the demand is shifting towards the pre-owned market. In fact, some car sellers replace their old cars with pre-owned cars instead of buying new ones. Unlike new cars, where price and supply are fairly deterministic and managed by OEMs (Original Equipment Manufacturer / except for dealership level discounts which come into play only in the last stage of the customer journey), used cars are very different beasts with huge uncertainty in both pricing and supply. Keeping this in mind, the pricing scheme of these used cars becomes important in order to grow in the market. We have to come up with a pricing model that can effectively predict the price of used cars and can help the business in devising profitable strategies using differential pricing.

**Objective**

Using Cars4U dataset, need to come up with a pricing model that can effectively predict the price of used cars and can help the business in devising profitable strategies using differential pricing.

**Observations from the model**

1. With our linear regression model we have been able to capture ~89 variation in our data.
2. The model indicates that the most significant predictors of price of used cars are - 
    - Age of the car
    - Number of seats in the car
    - Power of the engine
    - Mileage
    - Kilometers Driven
    - Location
    - Fuel_Type
    - OwnerType
    - Transmission - Automatic/Manual
3. Newer cars sell for higher prices. 1 unit increase  in age  of the car leads to [ exp(0.1123) = 1.12 Lakh ] decrease in the price of the vehicle, when everything else is constant.
4. As the number of seats increases, the price of the car increases - exp(0.05) = 1.05 Lakhs
5. Mileage is inversely correlated with Price. Generally, high mileage cars are the lower budget cars.    
6. Kilometers Driven have a negative relationship with the price which is intuitive. A car that has been driven more will have more wear and tear and hence sell at a lower price, everything else being 0.
7. The categorical variables are a little hard to interpret. But it can be seen that all the car_category variables in the dataset have a negative relationship with the Price and the magnitude of this negative relationship decrease as the brand category moves to lower brands. 
 
**Recommendation**

- Our final Linear Regression model has a MAPE of 23% on the test data, which means that we are able to predict within 23% of the price value. This is a very good model but can be further improved.
- Some southern markets tend to have higher prices. It might be a good strategy to plan growth in southern cities using this information. Markets like Kolkata(coeff = -0.2) are very risky and we need to be careful about investments in this area.
  
- Based on Analysis,  we can to divide our cars into 3 segment Low, Medium and High budget.
    
- Brands like Maruti, Hyundai ,Honda are low budget and very popular brands in used car market.
    
- Brands  like BMW, Bentley, Jaguar, Land Rover, Mercedes Benz,Porche,Mini Cooper are high budget cars and are mostly bought by car enthusiast who are ready to buy a  two user owned car at higher price as well. 
    
- Brands  like Toyota,Volvo can be Medium budget cars.
    
- Mumbai and Hyderbad seems to be more popular in Used car market, need to verify this with more data from other demographic regions. The next step post that would be to cluster different sets of data and see if we should make multiple models for different locations/car types. 
    
- Need to acquire more Automatic cars  to earn more profits, as this car sell at higher prices.
    
- With Increasing petrol rates diesel car are in more demand  in recent years, acquiring and selling them can high profits
    
- Along with this we can include scheme like take a test drive for  half day to pursue customer to buy.
    
- We can provide Car maintenance packages where  customers  pays a small upfront fees and   can bring the car for servicing anytime in a year to attract more customers.
  
**Important points**

- There are more soft parameters which also should be considered when buying a car, the wear and tear the car has been through and how much the company will have to work on car to make it ready for sale.
    
- If the car as already been in some kind of accident that would also effect the price.
    
- Other good to have feature like AC,Moon roof,Airbags can also have impact on the price.
    
- Car model that are too old will depreciate a lot  can impact the demand .
  
 
