## Overall
This is a replication package for the paper "The Review Linkage Graph for Code Review Analytics: A Recovery Approach and Empirical Study" that has been published in ESEC/FSE2019.
Our package is comprised of four analyses following RQ1-RQ4.

### Set Up Environment and Execute scripts
To install necessary libraries, execute this:
> tcsh INSTALL.sh

To replicate our studies, execute this:
> tcsh RUN.sh

The RUN.sh file runs our analyses.

### Review Linkage Extraction (RQ1)
The package of RQ1 provides with the scripts and results of linkage prevalence and trends.
The Python script (linkageTrend.py)  generates the content of Tab. 2 (i.e., the log from the script) and the data for Fig. 1 (i.e, linkTrend_rq1.pdf).
The R script (plotLinkTrend.R) generates Fig. 1 (i.e, linkTrend_rq1.pdf) in data directry.

### Linkage Type Analysis (RQ2)
The package of RQ2 shares the samples of our manual analysis.
Our csv file (mr_fse2019_submission_with_date.csv) shows our labels and the details.

### Automated Linkage Type Classification (RQ3)
The package of RQ3 provides with the scripts and results for our classification.
The script (multi_class_classifiers.py) shows how we use the classifiers in this study, which allows researchers and practitioners to replicate the automation study. Note that each classification process may generate different performance values since our bootstrap approach randomly selects the set of training and testing data.
The csv file (multi_class_1000.txt) shows our performance values from 1,000 iterations of bootstrap procedure.

### Impact Analysis on Reviewer Recommenders and Outcome Predictions (RQ4)
The Python script (recommender_performance.py) shows the result of our comparison study (Tab. 5) between our approach and cHRev. This script also shows the Overlapping Reviewer Rate (ORR) values for Nova and Neutron projects.
The Python script (identicalOutcomeRate.py) computes the identical outcome rate (IOR) for Nova and Neutron projects.
Moreover, the Python script (outcome_prediction.py) performs the outcome prediction and computes the misclassification rate.
