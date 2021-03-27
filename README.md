# Pre-Owned Car Sale Price Prediction
### This project involves developing a model to predict the appropriate selling price of a pre-owned vehicle based on several vehicle attributes.
### This is a standard `Regression Problem`.

## Tools and Libraries Used
- `SKlearn`
- `Matplotlib`
- `NumPy`
- `Pandas`

## Data
#### The dataset used for this project was retrieved from Kaggle at : https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho

**Data Features**
1. **Year** - year of manufacture.
2. **Present Price** - price of the vehicle if newly purchased from a dealership. ( In Indian Rupees (Lakhs)). Where 1 Lakh = 100,000 Rupees
3. **Kms_Driven** - the odometer in kilometers throuhgout the car's use.
4. **Fuel_Type** - type of fuel the vehicle runs on (Diesel/Petrol/CNG)
5. **Seller_Type** - mode through whcih the vehicle is being sold (Dealer/Individual)
6. **Transmission** - vehicle transmission type (Automatic/Manual)
7. **Owner** - number of previous owners.
8. **Selling_Price** - the price that the pre-owned vehicle was actually sold for. (In Indian Rupees (Lakhs)). Where 1 Lakh = 100,000 Rupees

#### In this particular case since I was prediciting selling price, the `Selling_Price` feature was the ground truth, leaving features 1-7 as the features from which the model would learn from.

## Modelling
Four different estimators were experimented with for this project. They were:-
1. Random Forest Regressor
2. Linear Regressor
3. Ridge Regressor
4. XGB Regressor (xgboost)

## Evaluation Metrics
A five-fold cross valdated R^@ and MSE score were used to evaluate the four models.

## Modelling Results
Of the four fitted and evaluated estimators, the XGB Regressor model performed the best (metric-wise)

## Insights
### Feature Importance
#### The feature importance analysis revealed:
1. The `Present_Price` (current new vehicle sale price) is the most important feature.
2. The `Age` of the vehicle eas the second most important feature.  
3. The `Kms_Driven` by the vehicle was the third most important feature.

### These findings fall right in line with the general vehicle value trends which are mainly determined by their depreciation due to their `off-the-lot price`, their `age` and `mileage`.
