# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) @SGCARPRICE

## Project Overview

![](https://github.com/asyraftaha/dsiprojects/blob/main/sgcarprice/images/selling_process.JPG)

Selling a car can be a stressful situation for car owners. Not knowing the market price of their vehicles leave them comparing quotes between dealers and figuring out to sell the car directly. Not knowing the price of their vehicle can leave them vulnerable to being "under-quoted" by car agencies.

Having the knowledge of the market price of their vehicles would empower car-owners to be able to make informed decisions and review the trade off between selling to car agencies or selling directly. Knowing the difference in price would allow the car owners to evaluate the effort and time in dollars. That is what I intend to achieve with this project.

## Data Dictionary and Background

For this project, the data for the cars listing were scraped from [SG Car Mart](SGCarMart.com). The data was scraped on the 17th December 2020. The below table is the dictionary of the data that I will be working with. The scraping of data were done in a separate notebook as they are date sensitive. I have also scraped data on the 22nd January 2021 to validate my model on more recent listings in the website.

|**Feature**|**Type**|**Description**|
|---|---|---|
|model|object|Make & Model of the car|
|price|object|Price of Cars Listed|
|mileage|integer|The total distance the car has travelled|
|road_tax|integer|The amount of tax payable for a vehicle to use the roads in a year|
|coe|integer|The price of COE (latest) that was registered to the vehicle : note that COE expires every 10 years and subject to renewal or termination|
|eng_cap|integer|The engine capacity of a car|
|curb_weight|integer|The weight of the vehicle|
|manufactured|integer|The year the car was manufactured|
|transmission|object|Gear transmission of the car: Automatic or Manual|
|omv|integer|The machine price of the car (coe not included)|
|power|integer|Engine power|
|num_owners|integer|Toal number of owners (past & present): [1: 1 owner, 2: 2 owners, 3: 3 owners, 4: 4 owners, 5: 5 owners, 6: 6 owners, 7: 7 or more owners]|
|type|object|The vehicle types: [Hatchback, MPV, SUV, Luxury Sedan, Mid-Size Sedan, Sports Car, Stationwagon]|
|category|object|The categories of cars listing: [Premium Ad Car, COE Car, PARF Car, Almost New Car, Direct Owner Sale, STA Evaluated Car, sgCarMart Warranty Cars, Consignment Car, Rare & Exotic, Low Mileage Car]|

## Model Used and Tuning

In this project I explored some models, Linear Regression, Lasso Regression, Support Vector Regression, Gradient Boost Regressor and Random Forest Regressor. I realised for this project, the Gradient Boost and Random Forest performed the best.

When I limited the price and mileage, I saw an increase in the R2 score and the RMSE.

## Conclusion


### Findings
- **Gradient Boost Regressor** performed the best for this project.
- Limiting the `price` and `mileage` of the dataset to a more normalised distribution increases the model performance significantly.
- `omv`,`coe_balance_in_months` and `mileage` are the strongest features in predicting car price.
- Model performs well with newly scraped data.
- Car make preference not solely reliant on price. BMW and Mercedes proved that price is not a turn off when it comes to buying cars.

### Limitations
Although the model is able to account for **92.11%** of the validation data with a prediction error of **$7589.52**, it was achieved by setting a few limits such as:

- Car price of $143,600 and below
- Car mileage of 138,00km and below
- Car manufactured year 2000 and later

### Further Research
- More data on cars above $143,600 may help improve the model further.
- More data on cars with mileage above 138,000km may also help improve the model further.
- Factors such as condition of car or involvement in accidents would be able to reduce more errors as these are important factors when selling a car. More data on this would help improve the model further.
