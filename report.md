# Phase 1

## After df.info()

- Need to change Column datatypes
    Student_ID to str
    Year_of_Study to int64

## After df.isnull().sum()

- There are no missing values in whole dataset.
    No action needed for null values

## After df.describe()

- Nothing Significant
    No actionable step found

### After df.duplicated().sum()

- NO Duplicates found
    No action needed for duplicates

# Phase 2

No missing value, duplicates, weird values and no impossible values.
Data is Trustworthy.

# Phase 3

**Column Understanding** and **Dataset Story**

## Column Table 
                                Meaning                         Type        Importance      Role
Student_ID                      serial numbers                  Identifier  Low             Identifier
Major_Category                  Field of Study                  String      Low             Studt Background
Year_of_Study                   College year                    String      Low             Studt Background
Pre_Semester_GPA                Previous Semester GPA           Float       Low             Studt Background
Weekly_GenAI_Hours              Avg AI usage per week           Float       High            Input
Primary_Use_Case                Which task performed by AI      String      Normal          Studt Background
Prompt_Engineering_Skill        Prompt input skill              String      High            AI usage
Tool_Diversity                  No. of tools being used         Integer     Normal          AI usage
Paid_Subscription               Subsc. used by student          Boolean     High            AI usage
Traditional_Study_Hours         Study hrs without AI            Float       High            Studt Background
Perceived_AI_Dependency         Their perception on dependence  Integer     High            AI usage
Institutional_Policy            If academy enourages or not     String      High            Environment
Anxiety_Level_During_Exams      student anxiety                 Integer     Normal          Environment
Post_Semester_GPA               GPA after AI help in study      Float       High            Output
Skill_Retention_Score           Absorb and retention            Float       Normal          Environment
Burnout_Risk_Level              Burnout from AI                 String      High            Environment

## Dataset Story

1) Which columns are outcomes?
A) Post semester GPA is the only outcome

2) Which columns might influence those outcomes?
A) Weekly_GenAI_Hours, Prompt_Engineering_Skill

3) Which columns are just identifiers?
A) Student_ID

4) Which columns seem important?
A) 

5) Which columns seem less important?
A) 

# Phase 4

#### Do students study more or less when using AI?
