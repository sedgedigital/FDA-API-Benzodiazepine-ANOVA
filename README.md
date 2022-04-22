# openFDA API - Exploring Adverse Event Reports for Medications

The project used the FDA Adverse Event Reporting System (FAERS) database containing information on adverse event and medication error reports submitted to the FDA (https://open.fda.gov/apis/drug/event/).

## The analysis:
1. Evaluating seasonality in the Benzodiazepine pharmacological class of medications.  The idea is that if there is an increase in adverse event reports during certain months then maybe that is tied to a greater number of prescriptions written during that period, and perhaps a seasonal need for the medication; like greater depression and anxiety during the winter months.


## The data were used to answer the following question:
1. Are there more adverse event reports for benzodiazepine medications during the winter months?


## Benzodiazepine Analysis
### Medication
Benzodiazepines are a pharmocological class of medications used to treat a variety of conditions, including panic disorders, anxiety disorders, epilepsy, and insomnia. They are one of the mostly widely prescribed drug in the United States (Source: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3684331/).  They include some of the more commonly known drug names: Xanax (alprazolam), Klonopin (clonazepam), Ativan (lorazepam), and Valium (diazepam).
### Analysis
Multiple API calls were used to create a dataset for analysis.  The API query was constructed to focus on the adverse reports submitted between 2015 and 2021, the gender of the patient, the pharmocological class of Benzodiazepines, and patient age.  These are the data steps:
1. create dataframe from API data
2. extract month and year columns for time analysis
3. boxplot of Benzodiazepine event counts by month
4. bar plot of Benzodiazepine event counts by month with all years combined
5. 1-way ANOVA of month by event count
6. pair-wise post-hoc Tukey test to find which months are significantly different
7. boxplot of event counts by patient age
8. 1-way ANOVA and Tukey test for significant months within the two highest age groups 50-59 and 60-69.
### Findings
The hypothesis was that there may be a greater number of adverse events for benzodiazapines in the winter months because more of the medication is prescribed during that time, perhaps related to seasonal depression in the winter.  Indeed, we found that there is an statistically significant increase in benzodiazapine adverse event reports during the winter months from 2015 - 2021 (specifically, December, January and February).  And the greatest number of reports came from patients between the ages of 50-69.  The patients in this age group also showed statistically significant higher adverse report counts during the same months.  Although the API doesn't provide data on count of prescriptions written, it is plausible to think that there is a seasonality effect in benzodiazepine issuance.


