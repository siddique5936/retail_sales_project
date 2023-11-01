# summary

Retail sales prediction is the process of forecasting future sales in the retail industry based on historical data, market trends, and various predictive models. This activity is essential for retailers to make informed decisions regarding inventory management, marketing strategies, and overall business planning.

# project description

Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. 

Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

# data description

Rossmann Stores Data.csv - historical data including Sales

store.csv - supplemental information about the stores

Data fields:
Most of the fields are self-explanatory. The following are descriptions for those that aren't.

Id - an Id that represents a (Store, Date) duple within the test set

Store - a unique Id for each store

Sales - the turnover for any given day (this is what you are predictin)

Customers - the number of customers on a given day

Open - an indicator for whether the store was open: 0 = closed, 1 = open

StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools

StoreType - differentiates between 4 different store models: a, b, c, d

Assortment - describes an assortment level: a = basic, b = extra, c = extended CompetitionDistance - distance in meters to the nearest competitor store

CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened

Promo - indicates whether a store is running a promo on that day

Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating

Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2

PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

# Observation

As per our model; Customer, store Type, CompetitionDistance and Promo are the most important features which are having the most impact on Target Variable i.e. Sales Column.

# Conclusion

By Looking at the evaluation metrices obtained on implementing different sort of regression model each model performing well having r2 score well that is more than 90% but comparison to all the models we decided to go with the Random Forest Tuned model.

beacause r2 was very close to 1 and the metrics like mse mae and rmse has very low value that explains well for the performance of the model

The maximum R^2 was seen in tuned Random Forest model with the value 0.97185. It means our best accurate model is able to explain approx/almost 97% of variances in the datasets.

where all models like decision tree has also high accuracy but incase we have to choose only the optimal model so we have to go through hyperparameter tuining for random forest

Based on our model; Customer, store Type, Promo & CompetitionDistance are the most impactful features which are driving the sales more as compared to other features present in the dataset.
