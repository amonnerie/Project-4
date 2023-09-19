# Project-4: Energy Consumption Price Prediction
By Ginger Francione, Joan Montilla, Omar Hadi, and Andrea Monnerie

## Links
DATA SOURCE from Kaggle: https://www.kaggle.com/datasets/nicholasjhana/energy-consumption-generation-prices-and-weather?select=energy_dataset.csv

Google slides: https://docs.google.com/presentation/d/1QCjKRqpy0dGl5xraQjm-LX3O7kyIpQxmvOhClCFGCc0/edit?usp=sharing
Tableau Public: https://public.tableau.com/app/profile/andrea.monnerie/viz/Project4_16945501784050/pricevsloadbytime

## Summary
This project created a machine learning model to predict the price of energy consumption. The data used was energy consumption and generation, the price changes, and the weather for five major cities in Spain combined (though the cities were recorded for the weather portion); the data came from Kaggle by Nicholas Jhana (link above). The data is cleaned up, Visulaized using Tableau, and create a machine learning model using XGBoost to predict the prices. Knowing the pricing means energy consumption can be predicted and from which source (wind power, coal, fossil fuel, etc.).

The data was cleaned up first by Excel to get a first glance, but the most work was using SQL in order to merge the weather data with the energy consumption and generation (with pricing) data. Then the data was saved to be used to creating the machine learning model in Python. At this point the data had some columns removed was it found to be futile; for instance two columns were completed filled with null values and weather description is unnecessary as the cloud covering and rain data is recorded. Also the rows with at least one column with numm variables were removed.

There are some obvious trends from step 2. It either consumers most mostly nonrenewable energy or renewable energy. The spring time is when renewable energy is mostly used: probably due to the weather and the reminder of using green energy such as Earth Day. Also the price seems to have a direct relationship with the consumption of nonrenewable energy while price have a indirect relationship with renewable energy. This is critical as this prediction model will predict prices, it will essentially predict the consumption of renewable energy (when prices are low).

This project used XGBoostRegressor as the tool to make the prediction model. The pricing was the dependent variable and the rest were the independent variables. The model resulted to be very accurate with a 93.8% accuracy. Also we determined the feature importances which helped uncover the leading factors that helps predict the price: the top 3 leading factors was the consumption of fossil gas, hour, and month.

To optimized the model we decided to keep the rows with at least one columns of nulls. This improved the model by about +0.002%.

If the government or electrical company wants comsumers to use more renewable energy, there are several factors that is needed to consider. Pricing and weather seem to be major contributors for people to use renewable energy. However with the demand of energy increase in the from summer to winter, there needs to be more source of energy such as constructing more wind turbine generators and more hydropower plants especially the latter since this is not as influenced by the weather.  
