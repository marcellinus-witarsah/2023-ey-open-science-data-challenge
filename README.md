# 2023-ey-open-science-data-challenge
This repository contain all works for 2023 EY Open Science Data Challenge
**1. Include a brief description your approach to building the model?**

Answer:
For the approach of building the model, I started to explore different models from Logistic Regression, Support Vector Machine, Random Forest, Gradient Boost, Ada Boost, Naive Bayes (Bernoulli), and K-Nearest Neighbor for 1x1 bounding area box. In this case Random Forest is the best one, then I continued to work with bounding box area of 3x3, 5x5, 7x7, and 10x10. Until I found the best bounding box area which is 10x10. Next, I used Voting Classifier for enhancing model performance using top 5 models (based on performance score using K-Fold Cross Validation) which are **Support Vector Machine, Random Forest, Gradient Boost, Ada Boost, and K-Nearest Neighbor**.

For the data, I try to grasp as many bands as I can from multiple satellite products that are being recommended by EY Open Science Data Challenge team. One of which is Sentinel 2 L2A product, where I extract Red, Green, Blue, NIR and SWIR for calculating NDVI, NDWI, and PSRI (vegetation indices). However these vegetation indices wasn't good enough to be a predictor for paddy rice crop classification. That's why I stick with Sentinel 1 RTC products such as VH and VV bands. 

| Date | Activity | Path |
| --- | --- | --- |
| 12th February 2023 - 18th February 2023 | Learn about crop phenology from `Learning Hub` | - |
| 19 February 2023 - 20th February 2023 | Learn about the `Benchmark Notebook` and download Sentinel 1 RTC data| 2023-ey-open-science-data-challenge-1/notebooks/20230219-notebook-benchmark.ipynb and 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/20230302-downloading-vv-vh-bands.ipynb|
| 21st February 2023 - 22th February 2023 | Experimenting using VH and VV band annual data for 1x1 area from Sentinel 1 RTC| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/vv-vh/20230221-vv-vh-bbox-1x1-1-year.ipynb |
| 23th February 2023 - 24th February 2023 | Experimenting using VH and VV band annual data for 3x3 area from Sentinel 1 RTC| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/vv-vh/20230223-vv-vh-bbox-3x3-1-year.ipynb |
| 25th February 2023 - 26th February 2023 | Experimenting using VH and VV band annual data for 5x5 area from Sentinel 1 RTC| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/vv-vh/20230225-vv-vh-bbox-5x5-1-year.ipynb |
| 27th February 2023 - 29th February 2023 | Experimenting using VH and VV band annual data for 7x7 area from Sentinel 1 RTC (using Voting Classifier), download Sentinel 2 L2A data| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/vv-vh/20230229-vv-vh-bbox-7x7-1-year-voting-classifier.ipynb and 2023-ey-open-science-data-challenge-1/notebooks/sentinel-2-l2a/20230302-downloading-sentinel-2-bands.ipynb|
| 30th February 2023 - 2nd March 2023 | Experimenting using RVI vegetation indices annual data for 1x1 area from Sentinel 1 RTC| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/rvi/20230302-rvi-bbox-1x1-1-year.ipynb |
| 3rd March 2023 - 7th March 2023 | Experimenting using NVDI, NDWI, PSRI vegetation indices annual data for 1x1 and 3x3 area from Sentinel 2 L2A| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-2-l2a/20230305-sentinel-2-bbox-1x1-1-year.ipynb and 2023-ey-open-science-data-challenge-1/notebooks/sentinel-2-l2a/20230305-sentinel-2-bbox-3x3-1-year.ipynb|
| 8th March 2023 - 13th March 2023 | Experimenting using VH and VV band annual data for 10x10 area from Sentinel 1 RTC (using Voting Classifier)| 2023-ey-open-science-data-challenge-1/notebooks/sentinel-1-rtc/vv-vh/20230313-vv-vh-bbox-10x10-1-year-voting-classifier.ipynb |


**2. Did you use other data sets than those provided?**

Answer:
Yes, I try to experiment using Sentinel 2 L2A data for calculating vegetation indices from NDVI, NDWI, and PSRI.

**3. If so, are these free/open to the public?**

Answer:
Yes, the data is open for public by Planetary Computer.

**4. Model Location**

Answer:
2023-ey-open-science-data-challenge-1/output/models/bbox-10x10-vt-classifier.pkl
