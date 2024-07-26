## Overview
This is a replication package for the paper "The Review Linkage Graph for Code Review Analytics: A Recovery Approach and Empirical Study".
This package is comprised of four folders that correspond to the analyses that we conducted in our four research
question (RQ1-RQ4).

## Code Snapshot

Download the repository from Figshare at: https://doi.org/10.6084/m9.figshare.7010474.v5

### Set Up Environment and Execute scripts
To install necessary libraries, execute this:
> tcsh INSTALL.sh

To replicate our studies, execute this:
> tcsh RUN.sh

### Review Linkage Extraction (RQ1)
The RQ1 folder contains the scripts that can be used to reproduce the results of the linkage prevalence and trends
analysis.
The Python script (`linkageTrend.py`)  generates the content of Table 2 (i.e., the log from the script) and the data for Figure 1 (i.e, `linkTrend_rq1.pdf`).
The R script (`plotLinkTrend.R`) generates Figure 1 (i.e, `linkTrend_rq1.pdf`) in data directry.

### Linkage Type Analysis (RQ2)
The RQ2 folder contains the samples from our manual analysis.
Our CSV file (`mr_fse2019_submission_with_additional_description.csv`) contains the manually assigned labels and details about each label.

### Automated Linkage Type Classification (RQ3)
The RQ3 folder contains the scripts to train and analyze machine learning classifiers to label review links.
The script (`multi_class_classifiers.py`) shows how we use the classifiers in this study, which allows users to replicate the automation study. Note that each execution may generate different performance values since our bootstrap approach randomly selects the set of training and testing data.
The csv file (`multi_class_1000.txt`) shows our performance values from 1,000 iterations of bootstrap procedure.

### Review Analytics Impact Analysis (RQ4)
The Python script (`recommender_performance.py`) reproduces the results of our reviewer recommendation comparison between our linkage-aware approaches and cHRev (Table 5). This script also shows the Overlapping Reviewer Rate (ORR) values for Nova and Neutron projects.
The Python script (`identicalOutcomeRate.py`) computes the Identical Outcome Rate (IOR) for Nova and Neutron projects.
Moreover, the Python script (`outcome_prediction.py`) reproduces the review outcome prediction and computes the misclassification rate.
