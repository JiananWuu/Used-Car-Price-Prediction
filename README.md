# Used-Car-Price-Prediction

**Model Evaluation**
- Linear Regression Model: 0.36
- Lasso Model MSE: 0.36
- Ridge Model with (degree =2): 0.2; Ridge Model with (degree =1): 0.37
In comparison, the Ridge Model with degree=2 has the smallest error. However a higher degree won't make the model very explainable. Some of the combinations just don't make much sense in terms of business context.
For the Linear Regression model, top positive features include: transmission_other, year, type_truck, condition, transmission_manual, type_coupe, type_pickup, cylinders. Top negative features includ: fuel_gas,drive_fwd, type_sedan, odometer.
For the Lasso Model, top positive features include:transmission_other,year, condition,cylinders,type_truck. Top negative features includ: drive_fwd, fuel_gas,type_sedan,odometer
We can see they have very similar feature rankings.

**To be revisited later**
- Missing values imputation: I just dropped the missing values for now. Considering the percentage of missing values are quite high around 20%-30%, there probably should be a better way to deal with those data.
- Explore other ways to select features like sequential selection. See if they can generate better models. For now the featares are quite a lot.
- More data collection on other type of transmisson and fuel. The transmission_other and fuel_other coefficient, however this value is quite obscure.

**Business Insights**

- Car type, Transmission, Year, Condition,cylinders are the top drivers of the price.
- The type of car is important in deciding the car price. Some types are naturally at a very high price, like truck, coupe, pickup. Others like sedan has relatively low price.
- Front-wheel drive vehichles are less valued compared to other types
- Non-standard transmissions can add values like dual-clutch. Its coeficient is very high.
- Gas car may have lower prices compared to other types.
- Title status, number of cylinders, Manufacturer doesn't have much influencing power.

**Recommendations**
- Collect more high-price types, like truck, coupe, pickup. Offer promotions to those less welcome like sedan
- Adjust the price of the car in the inventory, increase those that are welcome and decrease those that are less welcome so that they can be sold quickly, like the Front-wheel drive vehichles.

Jupyter Notebook Link: https://github.com/JiananWuu/Used-Car-Price-Prediction/blob/main/What_Drives_the_Price_of_a_Car.ipynb
