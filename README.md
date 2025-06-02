# Elevate-Labs_Task5

This project performs an Exploratory Data Analysis (EDA) on the Titanic training dataset (train.csv) from Kaggle to extract insights into passenger survival patterns. Using Python (Pandas, Matplotlib, Seaborn), the analysis identifies trends, relationships, and anomalies through statistical summaries and visualizations. 

#### Dataset

The Titanic dataset (train.csv) contains 891 passenger records with features: PassengerId, Survived (0=No, 1=Yes), Pclass (1/2/3), Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked (C/Q/S).

source: https://www.kaggle.com/c/titanic/data?select=train.csv&utm_source=chatgpt.com

##### Missing Values:
Age: 177 missing (≈20%)

Cabin: 687 missing (≈77%)

Embarked: 2 missing (≈0.2%)

#### Data Preprocessing
Dropped Cabin due to excessive missing data.

Filled missing Age values with median (28).

Filled missing Embarked values with mode ('S').

#### Statistical Summary
Survival Rate: 38.4% survived, 61.6% did not.

Gender Distribution: 65% male, 35% female.

Passenger Class: 55% in 3rd, 24% in 1st, 21% in 2nd.

Port Embarkation:

          72%: Southampton (S)
          19%: Cherbourg (C)
          9%: Queenstown (Q)

Age: Mean = 29.7, Median = 28, Range = 0.42–80.

Fare: Mean = $32.20, Median = $14.50, Max = $512 (highly skewed)

#### Visual Analysis:
Age & Fare Distribution
     
         Age: Right-skewed; most passengers between 20–40 years.

         Fare: Highly right-skewed with a peak at low values.

Age and Fare by Class
           Age:

                1st Class: Median = 37
                3rd Class: Median = 25

            Fare:

                  1st Class: Median = $60
                  3rd Class: Median = $8

Survival Insights
              Sex:

                   Females: 74% survival rate
                   Males: 19% survival rate

              Class:

                    1st Class: 63% survived
                    2nd Class: 47% survived
                    3rd Class: 24% survived

              Embarked Port:

                     Cherbourg: 55% survived
                     Queenstown: 39% survived
                     Southampton: 34% survived

Pairwise Relationships
            
         Higher Fare correlates with survival.
             
         Small family size (1–2 SibSp/Parch) improves odds.

#### Correlation Highlights

                 Pair	         Correlation
                 Pclass vs Fare	    -0.55
                 Survived vs Fare	 +0.26
                 Pclass vs Survived	 -0.34
