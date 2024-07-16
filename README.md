# Survey-Analysis

Objective
To understand how respondents' demographics influences their behavior towards companies' involvement in social issues.

Questions to answer
1. How do gender and age affect purchase likelihood from socially aligned companies?
2. How does ethnicity influence seeking supportive companies?
3. How are social issues distributed across age groups?
4. How does education level relate to social issue resonance?
5. How does household income impact opinions on companies' responsibility to speak out?

Steps followed for the analysis:




Data Exploration

Columns:
The dataset has 40 columns. Each column represents a specific aspect of the respondents' demographics or their opinions on companies' involvement in social issues. There are 216 entries for each column.

| Column Name                           | Description                                                                                           | Entries |
|---------------------------------------|-------------------------------------------------------------------------------------------------------|---------|
| Respondent identifier                 | Unique identifier for each respondent                                                                 | 216     |
| Start time                            | Time when the survey started                                                                          | 216     |
| End time                              | Time when the survey ended                                                                            | 216     |
| State                                 | State of the respondent                                                                               | 216     |
| Region                                | Region of the respondent                                                                              | 216     |
| City                                  | City of the respondent                                                                                | 216     |
| GPS coordinates                       | GPS coordinates of the respondent                                                                     | 216     |
| Login parameters                      | Parameters used for login                                                                             | 216     |
| S1 - Total                            | Total respondents                                                                                     | 216     |
| S2 - Between 35 and 50 (Age)          | Respondents aged between 35 and 50                                                                    | 216     |
| S3 - Female (Gender)                  | Female respondents                                                                                   | 216     |
| S4 - Male (Gender)                    | Male respondents                                                                                     | 216     |
| S5 - Over 50 (Age)                    | Respondents aged over 50                                                                              | 216     |
| S6 - Under 35 (Age)                   | Respondents aged under 35                                                                             | 216     |
| CHQ1 - Feelings strength towards SI   | Strength of feelings towards social issues                                                            | 216     |
| CHQ2 - Day of Week Trap               | Day of the week trap question                                                                         | 216     |
| CHQ3 - Types of SI                    | Types of social issues respondents are passionate about                                               | 216     |
| OEQ1 - Other SI                       | Other social issues respondents are passionate about                                                  | 216     |
| CHQ4 - Company ability                | Respondents' belief in companies' ability to make positive social changes                             | 216     |
| OEQ2 - How to make positive change    | Ways companies can make positive social changes                                                       | 216     |
| OEQ3 - Why no positive change         | Reasons for believing companies cannot make positive social changes                                   | 216     |
| CHQ5 - Activism concerns              | Concerns about companies' activism                                                                    | 216     |
| OEQ4 - Concern type                   | Types of concerns about companies' activism                                                           | 216     |
| CHQ6 - Company responsibility         | Belief in companies' responsibility to speak out on social issues                                     | 216     |
| OEQ5 - Why responsible                | Reasons for believing companies are responsible for speaking out on social issues                     | 216     |
| OEQ6 - Specific responsibility        | Specific social issues companies are responsible for                                                  | 216     |
| OEQ7 - Why not responsible            | Reasons for believing companies are not responsible for speaking out on social issues                 | 216     |
| CHQ7 - Specific non-responsibility 1  | Specific social issues companies should not speak out on (part 1)                                     | 216     |
| OEQ8 - Specific non-responsibility 2  | Specific social issues companies should not speak out on (part 2)                                     | 216     |
| CHQ8 - Purchase likelihood agree      | Likelihood of purchasing from companies that align with respondents' social issues                    | 216     |
| CHQ9 - Purchase likelihood disagree   | Likelihood of purchasing from companies that oppose respondents' social issues                        | 216     |
| CHQ10 - Purchase likelihood undisclosed | Likelihood of purchasing from companies that do not disclose their stance on social issues            | 216     |
| CHQ11 - Company search                | Tendency to seek out companies that support social issues                                             | 216     |
| CHQ12 - Age                           | Age of the respondent                                                                                 | 216     |
| CHQ13 - Gender                        | Gender of the respondent                                                                              | 216     |
| CHQ14 - Ethnicity                     | Ethnicity of the respondent                                                                           | 216     |
| CHQ15 - Education level               | Highest education level attained by the respondent                                                    | 216     |
| CHQ16 - Income                        | Total annual household income of the respondent                                                       | 216     |
| CHQ17 - Political views               | Respondents' rating of their political views                                                          | 216     |
| ES1 - Complete                        | Completion status of the survey                                                                       | 216     |

Checking for missing values:

Filters were applied to the entire dataset to check for missing values in specific columns. Missing values were found in the title header, with some columns having 3 missing values while others had 2.

Typing errors:

The city column contains typos, with two values stored as '?'.

Duplicates:
The dataset has no duplicates.

Data cleaning

We noticed that the title header had merged cells, which would prevent us from creating a pivot table for data analysis. 
To solve this, the cells were unmerged, and the column names were edited to a single row and later simplified for better readability. 
After unmerging the cells and simplifying the column names for better readability, here are the updated column names in a clear table format:

After unmerging the cells and simplifying the column names for better readability, here are the updated column names in a clear table format:

| Column Name                                           | 
|-------------------------------------------------------|
| Respondent identifier                                 | 
| Start time                                            | 
| End time                                              | 
| State                                                 | 
| Region                                                | 
| City                                                  | 
| GPS coordinates                                       | 
| Login parameters                                      | 
| S1 - Total                                            | 
| Between 35 and 50 years                               | 
| Female                                                | 
| Male                                                  | 
| Over 50 years                                         | 
| Under 35 years                                        | 
| Which of the following statements resonates with you most? | 
| Climate change & other environmental issues          | 
| Civil rights & racial discrimination                  | 
| Gender inequality                                     | 
| Healthcare inaccessibility                            | 
| Gun violence                                          | 
| Poverty & food insecurity                             | 
| Unemployment                                          | 
| Other social issues                                   | 
| What other social issue(s) are you passionate about?  | 
| Companies ability to make positive change            | 
| How companies can make positive change               | 
| Reasons for no positive social change                | 
| Activism concerns towards a company                  | 
| Concern type                                          | 
| Companies responsibility to speak out on social issues | 
| Why companies should speak out on social changes     | 
| Specific issues to be addressed by companies         | 
| Why companies should not speak on social issues      | 
| Specific social issues companies should not speak out on, Y/N | 
| Specific issues companies should not speak out on   | 
| Purchase likelihood agree                             | 
| Purchase likelihood disagree                          | 
| Purchase likelihood undisclosed                       | 
| Actively Seek Supportive Companies When Purchasing   | 
| Age                                                   | 
| Gender                                                | 
| Black or African American                             | 
| White                                                 | 
| Asian                                                 | 
| Hispanic                                              | 
| Middle Eastern                                        | 
| Native American or Alaska Native                      | 
| Native Hawaiian or Pacific Islander                   | 
| Other Ethnicity                                       | 
| Undisclosed Ethnicity                                 | 
| Education level                                       | 
| Annual Household Income                               | 
| Political views                                       | 

Missing values
After formatting the title header, it was discovered that each column contained three missing values, which were subsequently filtered out.

Typing error
Cells in the City column that contained '?' as data were filtered out.

Data formatting

In the dataset, these columns had stored respondent responses as either "INCLUDED" or "NOT_INCLUDED".

![image](https://github.com/user-attachments/assets/dff3e34c-2eee-4e75-a7f2-5c00a3b61ef7)

When creating a pivot table, I need these columns to display the specific issues selected by respondents. 
For instance, if a respondent chose "Over 50 years", I want to count all instances of "Over 50 years" and have it displayed accordingly. To achieve this, I used ```CTRL+H``` to find and replace all occurrences of "INCLUDED" with the column names, and "NOT_INCLUDED" with blanks.

![image](https://github.com/user-attachments/assets/349a1e42-2cd6-42d2-8665-f551e13cf727)

Similarly, for the social issues that respondents are passionate about, instances marked as "SELECTED" were replaced with the respective column name, while instances marked as "NOT_SELECTED" were replaced with blanks.

![image](https://github.com/user-attachments/assets/07cd7e62-1d17-464c-8c49-1498dde346ba)

![image](https://github.com/user-attachments/assets/cb0e7c26-7da8-4b32-b5c6-fcd5c7b41dd8)

Same foe the ethnicity, the responses are stored as "SELECTED" and "NOT_SELECTED".
![image](https://github.com/user-attachments/assets/550b0f34-4607-4ea3-b606-eef5c0aab764)

The "SELECTED" responses were replaced with the column names while the "NOT_SELECTED" were replaced with blanks.
				
![image](https://github.com/user-attachments/assets/7d66d70e-0c3c-4e95-a46f-d0e8f472d8c6)


Transforming wide data to long data

There are three data groups that will be tranformed from wide to long format for easier data analysis.

1. Social issues that respondents are passionate about.
   
The data is currently in wide format, where each column represents a social issue. This format makes it difficult to count the occurrence of each social issue that respondents are passionate about. Especially respondents who selected more than one issue.
			
![image](https://github.com/user-attachments/assets/d7c59fb5-2d2e-406d-add5-2475dc5d0bac)

By transforming the data to long format, each respondent's selection is represented in a separate row, Social issues. This makes it possible to count the total number of times each social issue was selected.

![image](https://github.com/user-attachments/assets/ff9eb49a-4de1-4394-8fa3-a20e36dc80bd)


2. The age groupings
   
The age groupings are also stored in wide format distributed in 3 columns.

![image](https://github.com/user-attachments/assets/df6d88d0-e59c-4f01-9f23-3a239edeaed3)

Now, the data is aggregated into a single column rather than its initial three separate columns. 
For instance, to determine the distribution of age groups, I can simply count the number of rows in the new 'age2' column within each category.

![image](https://github.com/user-attachments/assets/32ac5966-0d58-4f24-94b5-535b95221a5a)

3. Ethnicity
   
The respondents had 9 ethnicity options from which they were supposed to pick only one.
				
![image](https://github.com/user-attachments/assets/6bb9eee8-434e-426f-9a54-25a15139fcf1)

TThe wide format is redundant  because each respondent can only choose one ethnicity, yet there's a column for each of the nine ethnicities. This redundancy wastes space and makes the data file larger.  
Transforming the data to long format eliminates these unnecessary columns, making the data file more compact.

![image](https://github.com/user-attachments/assets/1671d07d-8f0d-4e07-a390-a89548af2902)

Data grouping

Data grouping was done on the following columns;

1. Companies responsibility to speak out on social issues
The responses in this column were initially represented as "Somewhat agree", "Strongly agree", "Somewhat disagree", "Strongly disagree" and "Neutral". For the purpose of simplifying the analysis, I grouped these responses into broader categories: "Agree," "Disagree," and "Neutral."

```
=IF(Q5="Somewhat agree", "Agree", IF(Q5= "Strongly agree", "Agree", IF(Q5="Somewhat disagree", "Disagree", IF(Q5="Strongly disagree", "Disagree","Neutral"))))
```
This transformation helps in streamlining the analysis by reducing the number of categories.

2. Purchase likelihood
Purchase likelihood agree, purchase likelihood disagree and purchase likelihood undisclosed contained detailed responses such as "Very likely," "Somewhat likely," "Very unlikely," "Somewhat unlikely," and "Neutral." These were grouped into broader categories: "Neutal" ,"Likely" and "Not Likely."

```
=IF(AB7="Somewhat likely", "Likely", IF(AB7= "Very likely", "Likely", IF(AB7="Somewhat unlikely", "Not unlikely", IF(AB7="Very unlikely", "Not unlikely","Neutral"))))
```

3. Educational level

The education column was grouped as follows: "High School Degree or Equivalent" and "Less Than A High School Diploma" as "High School or Less," "Bachelor's degree" as "Bachelor's degree," "Some college" and "Associate degree" as "Some college," "Postgraduate degree (Master's, Doctorate, etc.)" as "Advanced degree," and "Prefer not to say" as "Others." 

```
=IF(OR(AF106="High School Degree or Equivalent", AF106="Less Than A High School Diploma"), "High School or Less",
 IF(OR(AF106="Some college", AF106="Associate degree"), "Some College",
 IF(AF106="Bachelor’s Degree", "Bachelor's Degree",
 IF(AF106="Postgraduate degree (Master's, Doctorate, etc.)", "Advanced Degree",
 "Others"))))
```

4.Annual Household Income
The categories were grouped as follows, "$100,000 to $149,999" and "$150,000 or more" as "Higher Income," "$50,000 to $74,999," "$75,000 to $99,999," "$35,000 to $49,999," and "$25,000 to $34,999" as "Middle Income," "Less than $25,000" as "Low Income," and "Others" as "Others."

```
=IF(OR(AH2="$100,000 to $149,999", AH2="$150,000 or more"), "High Income",
  IF(OR(AH2="$50,000 to $74,999", AH2="$75,000 to $99,999", AH2="$35,000 to $49,999", AH2="$25,000 to $34,999"), "Middle Income",
    IF(AH2="Less than $25,000", "Low Income", "Others")))
```
The data is ready for analysis.


DATA ANALYSIS






