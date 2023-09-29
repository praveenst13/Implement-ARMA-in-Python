# EX-no:7 Implement-ARMA-in-Python
## AIM :
To Write a Program to ARMA in Python
## Procedure:
1.Import necessary libraries

2.Simulate an ARMA(1,1) Process

3. Plot the ARMA(1,1) Data

4.Plot Autocorrelation and Partial Autocorrelation Functions for ARMA(1,1)

5.Simulate an ARMA(2,2) Process and Plot Its ACF and PACF
## PROGRAM:
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
plt.rcParams['figure.figsize'] = [10, 7.5]
ar1 = np.array([1, 0.33])
ma1 = np.array([1, 0.9])
ARMA_1 = ArmaProcess(ar1, ma1).generate_sample(nsample=1000)
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
## OUTPUT:

### plt.plot(ARMA_1)
![image](https://github.com/praveenst13/Implement-ARMA-in-Python/assets/118787793/06f76696-1072-48a7-ac54-4af8d318e2e6)
### plot_acf(ARMA_1)
![image](https://github.com/praveenst13/Implement-ARMA-in-Python/assets/118787793/4dbb751e-04e8-4d50-a6fa-ff4b6ea04f23)
### plot_pacf(ARMA_1)
![image](https://github.com/praveenst13/Implement-ARMA-in-Python/assets/118787793/a94c177b-d3e2-48d2-9641-9c67c953e8e2)
### plt.plot(ARMA_2)
![image](https://github.com/praveenst13/Implement-ARMA-in-Python/assets/118787793/27264835-df28-47da-98ce-3975b550246f)
### plot_acf(ARMA_2)
![image](https://github.com/praveenst13/Implement-ARMA-in-Python/assets/118787793/38dbb390-156e-476a-996f-3964ec96a0d2)

### plot_pacf(ARMA_2)
![image](https://github.com/praveenst13/Implement-ARMA-in-Python/assets/118787793/1ab2075e-9043-4eb2-9d12-14be5935bfbd)

 
## RESULT:
 
Thus the program to ARMA model is written and verified using python programming.
