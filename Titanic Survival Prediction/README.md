# Titanic Survival Prediction
## EDA:
  To understand the dataset better,we did an Exploratory Data Analysis using pandas and Numpy.
### About the DataFrame:
  * From that, we have observed that the Titanic train Dataset has a total of 891 rows and the test Dataset has a total of 418 rows. 
  * Each of the before mentioned Datasets initially have 6 dependent features (X) viz-a-viz ` PassengerId, Name,	Pclass,	Age,	SibSp,	Parch and	Fare.` 
  * Additionally, the train Dataframe has the Independent Target (y) namely Survived. 
  * The train Dataset has a total of 899 values throughout the Dataframe. 
  * The test on the other hand has 414 null values. In order to avoid overfitting, bith train and test are maintained separetely.
 - - - - - 
### Handling Null data:

#### Exhibit A: `Age` - Continous Value: 
    Replacing Null with mean, because at null, the plot is more centre aligned 
#### Exhibit B: `Embark` - Discrete Value:
    Replacing Null with Top 
#### Exihibit C: `Cabin` - Discrete Value(Common with a catch):
    The problem with Cabin is the fact that it has way too many NaN values to the point it is the Top most value. Ergo Cabin would eventually not be selected for the features.

 - - - - -  - - - - - 
### Deriving Features:
  There was a possibilty to derive the Cabin_Type, Name_Title, Family from Cabin and Name respectively. 
##### *Cabin_Type:*
        1. Cabin_Type would simply take the alphabetical character at the start of the string.
        2. It would contribute to the Type of Cabin
        3. Cabin_Type has not been created in this solution because of the large volume of NaN values.
##### *Name_Title:*
        1. It takes the honorific of a given name such as Mr. and Mrs.
        2. It is created to contribute to the analyse the Survival rates of Nobility over the working class.
        3. Name_Titles with same meanings (Mlle, Ms. and Mme., Mrs.) have been replaced with the commonly ocured Name_Title(Ms. an Mrs.)
##### *Family:*
        1. It combines the values of Parch and SibSp to create a single attribute
## Plots:
#### Sex vs Survived

