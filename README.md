# AIML
*Task 1* : #clean and prepare raw data for ML

I have used pandas, scikit-learn, and kagglehub.
Kagglehub is used for loading the database from Kaagle
For performing various operation on data we used scikit package
Pandas for using the DataFrame feature

for installing Dependancies :
pip install pandas scikit-learn kagglehub

Fine Name : "Titanic-Dataset.csv"

Load_Dataset() to get additional arguments of database
.info() to get the details of dataSet
.isnull().sum() to get the details of total numbers of null datas in each columns 


Result :

<ipython-input-7-55606d19da4f>:15: DeprecationWarning: load_dataset is deprecated and will be removed in a future version.
  hf_dataset = kagglehub.load_dataset(
Hugging Face Dataset: Dataset({
    features: ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked'],
    num_rows: 891
})

Initial Dataset Info:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 891 entries, 0 to 890
Data columns (total 12 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   PassengerId  891 non-null    int64  
 1   Survived     891 non-null    int64  
 2   Pclass       891 non-null    int64  
 3   Name         891 non-null    object 
 4   Sex          891 non-null    object 
 5   Age          714 non-null    float64
 6   SibSp        891 non-null    int64  
 7   Parch        891 non-null    int64  
 8   Ticket       891 non-null    object 
 9   Fare         891 non-null    float64
 10  Cabin        204 non-null    object 
 11  Embarked     889 non-null    object 
dtypes: float64(2), int64(5), object(5)
memory usage: 83.7+ KB

Missing values before cleaning:
PassengerId      0
Survived         0
Pclass           0
Name             0
Sex              0
Age            177
SibSp            0
Parch            0
Ticket           0
Fare             0
Cabin          687
Embarked         2
dtype: int64

Processed data information:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 891 entries, 0 to 890
Data columns (total 17 columns):
 #   Column         Non-Null Count  Dtype 
---  ------         --------------  ----- 
 0   Age            891 non-null    object
 1   Fare           891 non-null    object
 2   Pclass_1       891 non-null    object
 3   Pclass_2       891 non-null    object
 4   Pclass_3       891 non-null    object
 5   Sex_female     891 non-null    object
 6   Sex_male       891 non-null    object
 7   Embarked_C     891 non-null    object
 8   Embarked_Q     891 non-null    object
 9   Embarked_S     891 non-null    object
 10  Embarked_None  891 non-null    object
 11  Cabin          891 non-null    object
 12  Name           891 non-null    object
 13  Parch          891 non-null    object
 14  PassengerId    891 non-null    object
 15  SibSp          891 non-null    object
 16  Ticket         204 non-null    object
dtypes: object(17)
memory usage: 118.5+ KB

Missing values after cleaning:
Age                0
Fare               0
Pclass_1           0
Pclass_2           0
Pclass_3           0
Sex_female         0
Sex_male           0
Embarked_C         0
Embarked_Q         0
Embarked_S         0
Embarked_None      0
Cabin              0
Name               0
Parch              0
PassengerId        0
SibSp              0
Ticket           687
dtype: int64

First 5 rows of processed data:
    Age     Fare Pclass_1 Pclass_2 Pclass_3 Sex_female Sex_male Embarked_C  \
0  22.0     7.25      0.0      0.0      1.0        0.0      1.0        0.0   
1  38.0  71.2833      1.0      0.0      0.0        1.0      0.0        1.0   
2  26.0    7.925      0.0      0.0      1.0        1.0      0.0        0.0   
3  35.0     53.1      1.0      0.0      0.0        1.0      0.0        0.0   
4  35.0     8.05      0.0      0.0      1.0        0.0      1.0        0.0   

  Embarked_Q Embarked_S Embarked_None Cabin  \
0        0.0        1.0           0.0     1   
1        0.0        0.0           0.0     2   
2        0.0        1.0           0.0     3   
3        0.0        1.0           0.0     4   
4        0.0        1.0           0.0     5   

                                                Name Parch PassengerId  \
0                            Braund, Mr. Owen Harris     1           0   
1  Cumings, Mrs. John Bradley (Florence Briggs Th...     1           0   
2                             Heikkinen, Miss. Laina     0           0   
3       Futrelle, Mrs. Jacques Heath (Lily May Peel)     1           0   
4                           Allen, Mr. William Henry     0           0   

              SibSp Ticket  
0         A/5 21171   None  
1          PC 17599    C85  
2  STON/O2. 3101282   None  
3            113803   C123  
4            373450   None  

Training data shape: (712, 17)
Testing data shape: (179, 17)
Training target shape: (712,)
Testing target shape: (179,)

