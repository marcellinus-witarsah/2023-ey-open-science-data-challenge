# 2023-ey-open-science-data-challenge
This repository contain all works for 2023 EY Open Science Data Challenge
**1. Include a brief description your approach to building the model?**

Answer:
For the approach of building the model, I started to explore different models from Logistic Regression, Support Vector Machine, Random Forest, Gradient Boost, Ada Boost, Naive Bayes (Bernoulli), and K-Nearest Neighbor for 1x1 bounding area box. In this case Random Forest is the best one, then I continued to work with bounding box area of 3x3, 5x5, 7x7, and 10x10. Until I found the best bounding box area which is 10x10. Next, I used Voting Classifier for enhancing model performance using top 5 models (based on performance score using K-Fold Cross Validation) which are **Support Vector Machine, Random Forest, Gradient Boost, Ada Boost, and K-Nearest Neighbor**.

For the data, I try to grasp as many bands as I can from multiple satellite products that are being recommended by EY Open Science Data Challenge team. One of which is Sentinel 2 L2A product, where I extract Red, Green, Blue, NIR and SWIR for calculating NDVI, NDWI, and PSRI (vegetation indices). However these vegetation indices wasn't good enough to be a predictor for paddy rice crop classification. That's why I stick with Sentinel 1 RTC products such as VH and VV bands. 

| Date | Activity |
| --- | --- |
| 19th February 2023 - 26th February 2023 | Learn about crop phenology from `Learning Hub` |
| 27 February 2023 - 30th February 2023 | Learn about the `Benchmark Notebook` and download sentinel 1 RTC data|
| 1st February 2023 - 2nd February 2023 | Experimenting using VH and VV band annual data from Sentinel 1 RTC|
| 5th February 2023 - 6th February 2023 | Experimenting using VH and VV band annual data for 3x3 data from Sentinel 1 RTC|
| 7th February 2023 - 9th February 2023 | Experimenting using VH and VV band annual data for 5x5 data from Sentinel 1 RTC|
| 10th February 2023 - 11th February 2023 | Experimenting using VH and VV band annual data for 7x7 data from Sentinel 1 RTC, using Voting Classifier|
| 11th February 2023 - 12th February 2023 | Experimenting using RVI vegetation indices annual data for 3x3 data from Sentinel 1 RTC|
| 11th February 2023 - 12th February 2023 | Experimenting using NVDI, NDWI, PSRI vegetation indices annual data for 3x3 data from Sentinel 2 L2A|
| 13th February 2023 | Experimenting using VH and VV band annual data for 10x10 data from Sentinel 1 RTC, using Voting Classifier|


**2. Did you use other data sets than those provided?**

Answer:
Yes, I try to experiment using Sentinel 2 L2A data for calculating vegetation indices from NDVI, NDWI, and PSRI.

**3. If so, are these free/open to the public?**

Answer:
Yes, the data is open for public by Planetary Computer.
