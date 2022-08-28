# Urban-Problem
Check for the affordability index of the flat

The csv file has data regarding the flats. The columns are:

	POSTED_BY
	UNDER_CONSTRUCTION
	RERA
	BHK_NO.
	BHK_OR_RK
	SQUARE_FT
	READY_TO_MOVE
	RESALE ADDRESS
	LONGITUDE
	LATITUDE
	TARGET(PRICE_IN_LACS)

This data is divided into two file:
	train.csv
	test.csv
which can be used for training and testing of the model respectively.

This data can be used to check for the affordability index of the flat which can help us make decisions based on the independent variables. This can be highly beneficially to the consumer in a globally available and regularly updating database and help to predict the trends in the flat systems.

Firstly, the model is trained against train.csv using two ML models:
	• Lasso Model
	• Random Forest Model
Both the models were checked for the scores and compared against each other. It shows that the Lasso model performs much worse than the Random Forest Model. Hence, we choose the RF model for the prediction of the test.csv file.

Now after the prediction an affordability index is formulated using all the parameters regarding the dataset. This is done by normalizing the data and bringing all the values in the input dataset in the range where each value has an impact on the final index and the result can be calculated based on those values.

Process followed:
• Importing of relevant modules
• Setting paths for both the training and testing data
• Storing both datasets in different dataframes
• Renaming the columns for both train.csv and test.csv
• Dropping the extra columns for train.csv
• Replacing any string values with float or int values for both train.csv and test.csv
• Set the independent and dependent columns in variables for train.csv
• Splitting the dataset into training and testing datasets for train.csv with 30% data for testing
• Creating a lasso model and checking for its performance
• Next, we create a Random for regressor model and check for its performance too.
• Now we can decide which model to choose from which in this case can be the RF regressor
• Now in order to get the prices for the test.csv we have to define the independent columns in a separate variable and predicting the values
• This result can be outputted in a new .csv file which can be used for further processing.
• Now for the affordability index calculation we first take the mean of price and area since these columns are not normalized according to the independent variables.
• Now we get the final affordability index for all the datasets and store it in different .csv files
• The higher the affordability index the better the quality of living in the respective flat.
