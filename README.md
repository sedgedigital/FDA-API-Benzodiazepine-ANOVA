# openFDA API - Exploring Adverse Event Reports for Medications

The project used the FDA Adverse Event Reporting System (FAERS) database containing information on adverse event and medication error reports submitted to the FDA (https://open.fda.gov/apis/drug/event/).

## The analysis addresses two components of the data:
1. Evaluating seasonality in the Benzodiazepine pharmacological class of medications.
2. Jaime - add a description of your project here !

## The data was used to answer two questions:
Question 1: Are there more adverse event reports for benzodiazepine medications during the winter season?
Question 2: Jamie - Fill in your question here!

## Benzodiazepine Analysis
### Medication
Benzodiazepines are a pharmocological class of medications used to treat a variety of conditions, including panic disorders, anxiety disorders, epilepsy, and insomnia. They are one of the mostly widely prescribed drug in the United States (Source: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3684331/).  They include some of the more commonly known drug names: Xanax (alprazolam), Klonopin (clonazepam), Ativan (lorazepam), and Valium ((diazepam).


Creating the Benzodiazepine dataset: Based on the structure of the the API, the sheer size of the database, the 1000 record limit per call, the 'count' function in the API callquery was used. This was instead of 'paging' through the 500,000 or more records that matched the search. The API calls for this analysis are the same with the exception of male and female, and age. The API calls are set up to loop through each age (min to max) for males and females. The pharmalogical class of Benzodiazepine is used as search criteria, along with the years of 01/01/2015 to 10/31/2021. Then the two datasets (male and female) are combined and used for the analysis.
