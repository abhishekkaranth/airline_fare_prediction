# airline_fare_prediction

A model stacking approach to determine the search prices of various airlines across different departure dates.

Airline pricing is one of the most complex problems in the industry and varies on various factors. Pricing too high will result in lesser passengers and too low will result in loss. It needs to take into account competitors pricing as well on the same market.
Predicting the of price for a given departure week in different search weeks will help in competitor study and also helps in demand and revenue forecasting.
This exercise aims to predict the price of a ticket of an airline based on features such as search date, departure date, origin, destination, no. of passengers, cabin class, airline etc.
We use a a Stacking Method where a second model is trained based on the output of many models such as Random Forest, XGBoost, LightGBM and the final result is predicted by this stacked model.

NOTE:
- The orign, destination, airline, currency, aircraft, country are encoded to maintain confidentiality of the data. As these are categorical, the encoding in no way affects the working of the model. It only masks the actual categories these columns represents.
- The price column in present in different currencies. The output should also be in the currencies present in test dataset. But we convert all prices to a single currency, build the model and then convert back to respective currencies.
- We use MAPE as the evalation metric.
