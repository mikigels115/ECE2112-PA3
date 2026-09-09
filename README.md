# ECE-2112-PA-3
Made by: Mike Angelo P. Atienza | Section: 2ECE-B

This repository contains the Programming Assignment 3 for our course "Advanced Computer Programming and Algorithms" this S.Y. 2026-2027. This project contains three python programming problems focusing on Pandas.

# 1. POSITIONAL AND LABEL-BASED SLICING

Display the shape and complete list of column names of cars. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where
the first data row is row 1. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order specifically.

**Requirement**: The row selection in part (b) must use iloc; the column selection in part (c) must
use column labels.

**Functions and methods that were used here:** 

* **(`import pandas as pd`):** It is used to load pandas libraries.
* **(`pd.read_csv('cars.csv')`):** To display the list of cars in the table. 
* **(`cars.iloc[]`):** To display the cars from index 6 to 10.
* **(`cars_6_to_10[[]]`):** To specifically identify the columns of the variable "cars_6_to_10".
```
import pandas as pd
cars = pd.read_csv('cars.csv')
cars

cars_6_to_10 = cars.iloc[5:10]
cars_6_to_10 

cars_6_to_10[['Model','mpg','cyl','hp','gear']]

```

# 2. MODEL LOOKUP
Use Boolean indexing on the Model column to answer both instructions.

Display the complete row for Toyota Corolla. For Pontiac Firebird, display only Model, mpg, hp, and wt.
And then store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to
locate either model.

**Functions and methods that were used here:** 
* **(`import pandas as pd`):** It is used to load pandas libraries.
* **(`cars.loc[cars['Model'] == 'Toyota Corolla']`):** A Boolean index used to display the whole row of the variable "Toyota Corolla".
* **(`cars.loc[cars['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]`):** A Boolean index used to display the variable "Pontiac Firebird" with specific assigned rows only.

```
toyota = cars.loc[cars['Model'] == 'Toyota Corolla']
toyota

pontiac = cars.loc[cars['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]
pontiac

```



# 3. MULTI-MODEL SUBSETTING
Create a DataFrame named selected cars containing only the records for three models: Datsun 710,
Lotus Europa, and Ferrari Dino.

For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values
rather than by row numbers. Display selected cars and its shape.


**Functions and methods that were used here:** 

* **(`import pandas as pd`):** It is used to load pandas libraries.
* **(`cars.loc[cars['Model'].isin(['Datsun 710', 'Lotus Europa', 'Ferrari Dino']), ['Model', 'mpg', 'cyl', 'hp', 'gear']]`):** To display the three models and their specific columns by their model values rather than by row numbers.
* **(`print(selected_cars.shape)`):** To display the shape of the table.


```
selected_cars = cars.loc[cars['Model'].isin(['Datsun 710', 'Lotus Europa', 'Ferrari Dino']), ['Model', 'mpg', 'cyl', 'hp', 'gear']]
selected_cars

print(selected_cars.shape)

```
# README File Version History
September 9, 2026: Initial README file output uploaded.
