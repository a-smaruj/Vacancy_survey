# Vacancy_survey

## General
The purpose of the project “vacancy survey” was to estimate the labour demand by eliminating over-coverage errors. The data was extracted from [Central Job Offers Database](https://oferty.praca.gov.pl) (known as CBOP) from October 2020 to the end of the January 2022 and is not published due to the confidential reasons. 

## Technology
The whole survey was written with R language using packages like:
- tidyverse
- data.table
- RcppSimdJson

## Structure
Project consists of two folders:

-	Phone_calls_survey

    Includes analysis of the samples selected to the phone calls. There was a need to explore CBOP, as well as Pracuj.pl, which is a private and competitive job offers posting website. Consequently, there are two analysis files for each. Phone calls aimed to verify the validity of the visible offers on the website with the actual status of the recruitment process. The obtained results were used to create a model to asses an offer's validity.

-	CBOP_2020-22_survey

    Having focused on admin data, firstly there was a phase of cleansing it, and then analysing it. Therefore, in this folder we can distinguish two files: 
    
    - data_cleansing 

        Concerns preparing data for further analysis. Firstly, the data were transformed from json format to rds. Then, with the object of removing over-coverage errors, we selected suitable data and eliminated duplicates. The last task was to collect data for statistical reasons.
    
    - data_analysis
    
        Involves creating a logistic regression model and performing a multivariate visualisation of the results.
    
## Results

The bachelor's thesis with the results obtained can be found [here](https://github.com/a-smaruj/Vacancy_survey/blob/main/bachelors_thesis.pdf).
