# CL-1 Lab Practicals

Python code for the two CL-1 lab subjects. Every script has run instructions at the top,
step-by-step comments, and theory + viva notes at the end.

All scripts are in the repo root; files are prefixed `ML_` or `DMV_` by subject.
Run any script with `python <file>.py` (or paste it into Jupyter).
Install: `pip install numpy pandas matplotlib scikit-learn openpyxl statsmodels requests`

## ML - Machine Learning (417525)
| No. | File | Topic |
|---|---|---|
| 1 | `ML_1_PCA_Wine.py` | PCA on Wine dataset |
| 2 | `ML_2_Regression_Uber.py` | Linear, Ridge, Lasso regression (Uber fares) |
| 3 | `ML_3_SVM_Digits.py` | SVM on handwritten digits |
| 4 | `ML_4_KMeans_Iris.py` | K-Means + elbow method (Iris) |
| 5 | `ML_5_RandomForest_Car.py` | Random Forest (car evaluation) |
| 6 | `ML_6_QLearning_TicTacToe.py` | Q-learning Tic-Tac-Toe |

## DMV - Data Modeling and Visualization
| No. | File | Topic |
|---|---|---|
| 1 | `DMV_1_Multi_Format_Sales.py` | Load CSV / Excel / JSON sales data |
| 2 | `DMV_2_Weather_API.py` | OpenWeatherMap API (set `OPENWEATHER_API_KEY`) |
| 3 | `DMV_3_Telecom_Churn_Cleaning.py` | Data cleaning and preparation |
| 4 | `DMV_4_RealEstate_Wrangling.py` | Data wrangling |
| 5 | `DMV_5_AQI_Visualization.py` | matplotlib visualisation (AQI) |
| 6 | `DMV_6_Retail_Sales_Aggregation.py` | Data aggregation |
| 7 | `DMV_7_Stock_TimeSeries.py` | Time series + ARIMA forecast |

## Datasets
Datasets live in https://github.com/MrNobody4869/datasets. Every script that reads a file has two options in its load step:

```python
# Option A: Fetch the dataset online from the datasets repo
url = "https://raw.githubusercontent.com/MrNobody4869/datasets/main/<file>.csv"
df = pd.read_csv(url)

# Option B: Load from a local copy kept next to this script
# Comment out Option A above and uncomment the line below to switch:
# df = pd.read_csv("<file>.csv")
```

Option A is active by default. To use a local file, comment out Option A and uncomment Option B.
(`ML_4_KMeans_Iris.py` uses scikit-learn's built-in Iris as Option A and a local `Iris.csv` as Option B.)

| Script | Dataset file |
|---|---|
| ML_1_PCA_Wine.py | `wine.csv` |
| ML_2_Regression_Uber.py | `uber.csv` |
| ML_5_RandomForest_Car.py | `car_evaluation.csv` |
| DMV_3_Telecom_Churn_Cleaning.py | `Telecom_Customer_Churn.csv` |
| DMV_4_RealEstate_Wrangling.py | `RealEstate_Prices.csv` |
| DMV_5_AQI_Visualization.py | `City_Air_Quality.csv` |
| DMV_6_Retail_Sales_Aggregation.py | `Retail_Sales_Data.csv` |
| DMV_7_Stock_TimeSeries.py | `Stock_Prices.csv` |

Other scripts need no file (built-in data, self-generated data, or an API).

Sources: Uber fares (Kaggle yasserh), MSFT stock prices (Kaggle jek1wantaufik), India city air quality (Kaggle rohanrao), Superstore sales (Kaggle vivek468, reduced to 5 columns), Wine (UCI/GeeksforGeeks), Car evaluation (UCI), Telco churn (IBM sample), California housing (ageron).
