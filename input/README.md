# Data Source Description

The data we will use for this research project is the 2018 wave of the [National Survey on Drug Use and Health](https://www.datafiles.samhsa.gov/study/national-survey-drug-use-and-health-nsduh-2018-nid18757) (NSDUH), sponsored by the Center for Behavioral Health Statistics and Quality, Substance Abuse and Mental Health Services Administration of the US Federal government. The NSDUH is a large national survey of the civilian non-institutionalized US population aged 12 and over and asks a variety of questions related to drug use, including the use of illegal drugs and the mis-use of prescription drugs. We will use the adult subsample (those 18 and older) of the entire sample because many variables we want to look at are not available for the underage population.

From the full data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `nsduh`. 

* **drug_use**: A TRUE/FALSE variable indicating whether the respondent had used any of the following drugs in the last twelve months: cocaine, crack, heroin, methamphetamine, or inhalants (e.g. sniffing gas). You can treat this as a categorical variable. When we use models for the final analysis, this variable will be treated as a 1/0 variable where 1 is for TRUE and 0 is for FALSE. This means that you can interpret output from models as the change in the probability of drug use by a change in a given covariate.
* **income**: The personal income of the respondent, reported in 1000s of US dollars. Originally this was coded into income brackets (e.g. $20,000-29,999). To make it quantitative for our purposes, I gave each observation the midpoint of the income bracket and then added a little random noise. 
* **age**: the age of the respondent in several categorical brackets.
* **gender**: The gender of the respondent. The survey only allowed for the responses of male and female.
* **sexual_identity**: The reported sexual identity of the respondent. The categories are heterosexual, gay/lesbian, and bisexual. 
* **education**: The highest educational degree of the respondent. The categories are less than high school, high school diploma, associate's degree, and bachelor's degree or greater.
* **emp_status**: the employment status of the respondent. The categories are employed, unemployed, and out of the labor force.
* **mil_service**: Has the respondent ever served in the military (including currently)? The responses are yes and no. 
