# Ex.No:04   FIT ARMA MODEL FOR TIME SERIES
```
Developed by: M.Vivek reddy
Reg No:212221240030
```

### AIM:
To implement ARMA model in python.
### ALGORITHM:
1. Import necessary libraries.
2. Set up matplotlib settings for figure size.
3. Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

4. Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using
plot_acf and plot_pacf.
5. Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

6. Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using
plot_acf and plot_pacf.
### PROGRAM:
```
from pandas import read_csv
from pandas import datetime
from matplotlib import pyplot
from pandas.plotting import autocorrelation_plot
from pandas import DataFrame
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.arima_process import ArmaProcess
import matplotlib.pyplot as plt
import numpy as np
import warnings
warnings.filterwarnings('ignore')
import matplotlib.pyplot as plt
import numpy as np

plt.rcParams['figure.figsize'] = [10, 7.5]

ar1 = np.array([1,0.33])
ma1 = np.array([1,0.9])
ARMA_1 = ArmaProcess(ar1,ma1).generate_sample(nsample = 1000)
plt.plot(ARMA_1)
plt.title('Simulated ARMA(1,1) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_1)
plot_pacf(ARMA_1)
ar2 = np.array([1, 0.33, 0.5])
ma2 = np.array([1, 0.9, 0.3])
ARMA_2 = ArmaProcess(ar2, ma2).generate_sample(nsample=10000)
plt.plot(ARMA_2)
plt.title('Simulated ARMA(2,2) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_2)
plot_pacf(ARMA_2)
```
### Output:
![image](https://github.com/Vivekreddy8360/TSA_EXP4/assets/94525701/1f717fd1-b7cf-43dd-a742-e6ad3d7ed532)

![image](https://github.com/Vivekreddy8360/TSA_EXP4/assets/94525701/138c74ff-3826-4643-b806-23a82e72f93e)

![image](https://github.com/Vivekreddy8360/TSA_EXP4/assets/94525701/a816cf37-36a6-465e-9209-17e27c3c46b1)

![image](https://github.com/Vivekreddy8360/TSA_EXP4/assets/94525701/cb0ecac9-2e51-4b49-8257-ecb425d1f607)

![image](https://github.com/Vivekreddy8360/TSA_EXP4/assets/94525701/d4ce3668-502e-4456-be7e-a6b94590409c)


### RESULT:
Thus, a python program is created to fir ARMA Model successfully.
