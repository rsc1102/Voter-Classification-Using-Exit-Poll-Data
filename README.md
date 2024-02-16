# Voter Classification Using Exit Poll Data
Developed a K-Nearest Neighbors (KNN) model to predict a voter’s vote in the 2020 U.S. presidential election, based on their demographic data and opinions on certain key issues. Trained on [2020 National Election Day Exit Poll](https://ropercenter.cornell.edu/ipoll/study/31119913) dataset.

Due to the presence of NaN values in features, the model uses a custom distance metric that can satisfy the following conditions:
1.  if two samples are identical, the distance between them should be zero.
2.  as the extent of *difference* between two samples increases, the distance should increase.
3.  as the extent of *similarity* between two samples increases, the distance should decrease.
4.  if in a pair of samples one or both have a NaN value for a given feature, the similarity or difference of this feature is *unknown*. The distance metric should compute a smaller distance for a pair of samples with many similarities (even if there is some small difference) than for a pair of samples with mostly unknown similarity.

Mutual information (MI) is used to calculate the feature weights.

### Downloading the data and documentation

The exit poll data is not freely available on the web, but is available to those with institutional membership.
1. Open the Study Record for [2020 National Election Day Exit Poll](https://ropercenter.cornell.edu/ipoll/study/31119913).
2. Click on the “Downloads” tab, and then click on the CSV data file in the “Datasets” section of this tab. Press “Accept” to accept the terms and conditions. Find the file `31119913_National2020.csv` in your browser’s default download location.
3. After you download the CSV file, scroll down a bit until you see the “Study Documentation, Questionnaire and Codebooks” PDF file. Download this file as well.

