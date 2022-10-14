# GluNet - A Deep Learning Framework for Accurate Glucose Forecasting

### Metadata
authors: 
citation key: liGluNetDeepLearning2020
link to file: https://drive.google.com/file/d/18XWwnIxk0M3HTbksfijUAd9vYkUoD8BH/view?usp=sharing (here, Google Drive link - normally would link to local PDF file)
topics: #personalised-nutrition #glucose #time-series-forecasting
status: #status/complete 
type: #source/paper
date added: 2022-10-14

---

## Summary and high-level thoughts

- features: glucose measurements, meal information, insulin doses, 'other factors'
- patient population:
	- 1. ABC4D dataset - 10 people with T1DM
	- 2. OhioT1DM - 6 people with T1DM
- tested on 2 clinical data sets


## Highlights


"In this work, we introduce GluNet, a framework that leverages on a personalized deep neural network to predict the probabilistic distribution of short-term (30-60 minutes) future CGM measurements for subjects with T1D based on their historical data including glucose measurements, meal information, insulin doses, and other factors." ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"multi-layers of dilated convolution neural network (CNN)" ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"The results show significant improvements over existing methods in the literature through a comprehensive comparison in terms of root mean square error (RMSE) ( mg/dL) 8:88 0:77 with short time lag ( minutes) for prediction horizons 0:83 0:40" ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"addition, GluNet is also tested on two clinical data sets." ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

_What sort of dataset sizes? How compare with the ZOE dataset? ([note on p.414](zotero://open-pdf/library/items/XCG3LJZV?page=1))_

"In addition, machine learning (ML) techniques were extensively exploited, including support vector regression (SVR) \[12\], random forest (RF) \[13\] and grammatical evolution \[14\]." ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"There are a few works to date using DL for glucose forecasting" ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"using life-style data. These data include historical BG data from CGM, meal intake, insulin dosage." ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"Dilated CNNs are good at processing multi-dimensional long signals with a wider receptive field, and gated activation units capture the non-linearity of the probabilistic relations among several inputs. We modify PixelCNN/Wavenet accordingly to make it appropriate for glucose forecasting, and the DNN becomes a predictive model with fast implementation instead of a generative model." ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

"\[10\] and latent-variable-based statistical models \[11\]. In recent years many algorithms have been proposed for glucose forecasting \[8\], such as polynomial models (autoregressive (AR), autoregressive exogenous (ARX), autoregressive moving-average (ARMA)) \[9\], machine learning models The work was supported by EPSRC EP/P00993X/1." ([Li et al 2020:414](zotero://open-pdf/library/items/XCG3LJZV?page=1))

_Perhaps these are the types of models I should be thinking about? ([note on p.414](zotero://open-pdf/library/items/XCG3LJZV?page=1))_

"There are two clinical datasets. The first one was obtained from our ABC4D project \[21\]. T1D diabetic subjects participated and were monitored for 6 consecutive months with Dexcom CGM devices (San Diego, CA). Information on meals, insulin dosages were recorded by the patients themselves through a dedicated App." ([Li et al 2020:417](zotero://open-pdf/library/items/XCG3LJZV?page=4))

"The second dataset was provided by the Blood Glucose Level Prediction Challenge, namely the OhioT1DM dataset \[22\]. During eight weeks' period, six T1D subjects wore CGM devices and insulin pumps and reported their data regularly. A smart-phone app and a fitness band were used to collect daily events" ([Li et al 2020:417](zotero://open-pdf/library/items/XCG3LJZV?page=4))

"We compare our results with the neural network for predicting glucose algorithm (NNPG) in \[28\], the latent variable with exogenous input (LVX) statistical method proposed in \[29\], the auto regression with exogenous input (ARX) method \[30\], and the support vector regression (SVR) \[12\] method. 30 and 60 minutes PH are considered." ([Li et al 2020:418](zotero://open-pdf/library/items/XCG3LJZV?page=5))

"ABC4D Datasets: For the 10 adult subjects from the ABC4D project and considering 30 and 60 minutes prediction horizon, Table III demonstrates the forecasting performance in RMSE, MARD for three-month test data, corresponding to GluNet, NNPG, LVX, SVR, and the ARX algorithm." ([Li et al 2020:419](zotero://open-pdf/library/items/XCG3LJZV?page=6))

_Seems their dataset only has 10 people ([note on p.419](zotero://open-pdf/library/items/XCG3LJZV?page=6))_

"Table IV presents the 30-minute and 60-minute forecasting performance for six subjects" ([Li et al 2020:420](zotero://open-pdf/library/items/XCG3LJZV?page=7))

_And only 6 in the other ([note on p.420](zotero://open-pdf/library/items/XCG3LJZV?page=7))_

"Most importantly, GluNet has the shortest time lag and can capture the trend promptly." ([Li et al 2020:420](zotero://open-pdf/library/items/XCG3LJZV?page=7))

"We compare GluNet with existing algorithms to show its effectiveness, including NNPG, SVR, LVX, and ARX. Other algorithms published in literature have also been considered." ([Li et al 2020:420](zotero://open-pdf/library/items/XCG3LJZV?page=7))