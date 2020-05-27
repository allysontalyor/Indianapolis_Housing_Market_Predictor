# Indianapolis Housing Market Predictor

Housing market data, compiled monthly, was used to show trends in the Indianapolis Housing Market.  A machine learning model using a neural net was then created to predict housing prices for 2020 based on the zip code, number of bedrooms, and month the user selected.  Final results are displayed on a website that can be viewed at: https://allysontalyor.github.io/Indianapolis_Housing_Market_Predictor/.

A dashboard was created using past housing data to answer questions that buyers might ask.  Some of these questions included:

What is the median list price in each zip code?


How does the median list price vary over the course of a year (for a single zip code)?
Which zip codes had the greatest percent change over the past year?

Data was obtained from Zillow, using a free api call from Quandl.  Data was missing inconsistently throughout the dataset, and instead of eliminating all rows missing data, missing data was filled in using a machine learning model.  A linear regression model using sklearn with three input variables was created for each zip code and each month.  Four zip codes were selected for prediction representing a zip code on the north, south, east, and west side of Marion County, Indiana.

The machine learning model used a TensorFlow neural net (Sequential), with three input variables: number of bedrooms, zip code, month, and year.  These variables were one-hot encoded using .get-dummies.  Predicted variables were: median list price per number of bedrooms, median list price per zip code, and median home value (single family home).  The predicted results were displayed in table format and on a map, giving the user the chance to input the desired month, zip code, and number of bedrooms.

The model was evaluated by plotting the predicted values alongside past values.  Next steps would include modifying the model to evaluate overfitting, creating a second model for comparison using a linear regression in sklearn, and modifying the layers of the neural net.
