In `sample.ipynb`, I sampled the train and test data from `FimaNfipPoliciesV2.parquet`, which I got from a much larger parquet file (70+ million rows), which I got from https://www.fema.gov/openfema-data-page/fima-nfip-redacted-policies-v2

Then in `datawrangling.ipynb`, I prepared the sampled train and test data for exploratory data analysis.

Then in `eda.ipynb`, I explored the data and the relationships among them.

Then in `preprocessing.ipynb`, I prepared the data for modeling.

Then in `modeling.ipynb`, I fit 6 different models, used them to predict on the test data, and produced `model_metrics.txt`.