
# Module 1 Code Challenge

This code challenge is designed to test your understanding of the Module 1 material. It covers:

- Python Fundamentals
- Pandas
- Data Visualization
- Exploring Statistical Data

_Read the instructions carefully._ You will be asked both to write code and respond to a few short answer questions.

### Note on the short answer questions

For the short answer questions _please use your own words_. The expectation is that you have **not** copied and pasted from an external source, even if you consult another source to help craft your response. While the short answer questions are not necessarily being assessed on grammatical correctness or sentence structure, you should do your best to communicate yourself clearly.

---
## Part 1: Python Fundamentals [Suggested Time: 20 min]
---

In the first section, we will work with various Python data types and try to accomplish certain tasks using some fundamental data structures in Python. Below, we've defined a dictionary with soccer player names as keys for nested dictionaries containing information about each player's age, nationality, and a list of teams they have played for.   


```python
# Run this cell without changes

players = {
    'L. Messi': {
        'age': 31,
        'nationality': 'Argentina',
        'teams': ['Barcelona']
    },
    'Cristiano Ronaldo': {
        'age': 33,
        'nationality': 'Portugal',
        'teams': ['Juventus', 'Real Madrid', 'Manchester United']
    },
    'Neymar Jr': {
        'age': 26,
        'nationality': 'Brazil',
        'teams': ['Santos', 'Barcelona', 'Paris Saint-German']
    },
    'De Gea': {
        'age': 27,
        'nationality': 'Spain',
        'teams': ['Atletico Madrid', 'Manchester United']
    },
    'K. De Bruyne': {
        'age': 27,
        'nationality': 'Belgium',
        'teams': ['Chelsea', 'Manchester City']
    }
}
```

### 1.1) Create a `list` of all the keys in the `players` dictionary. Store the list of player names in a variable called `player_names` to use in the next question.

Use Python's documentation on dictionaries for help if needed. 


```python
# Replace None with appropriate code to get the list of all player names

player_names = None
```


```python
# Run this cell without changes to check your answer

print(player_names)
```

### 1.2) Great! Now that we have the names of all players, let's use that information to create a `list` of `tuples` containing each player's name along with their nationality. Store the list in a variable called `player_nationalities`.


```python
# Replace None with appropriate code to generate list of tuples such that 
# the first element is a players name and the second is their nationality 
# Ex: [('L. Messi', 'Argentina'), ('Christiano Ronaldo', 'Portugal'), ...]

player_nationalities = None
```


```python
# Run this cell without changes to check your answer

print(player_nationalities)
```

### 1.3) Define a function called `get_players_on_team()` that returns a `list` of the names of all the players who have played on a given team.

Your function should take two arguments: 

- a dictionary of player information
- the team name (as a `string`) you are trying to find the players for 

**Be sure that your function has a `return` statement.**


```python
# Code here to define your get_players_on_team() function 

```


```python
# Run this cell without changes to check your answer

players_on_manchester_united = get_players_on_team(players, 'Manchester United')
print(players_on_manchester_united)
```

---
## Part 2: Pandas [Suggested Time: 15 minutes]
---

In this section you will be doing some preprocessing for a dataset for the videogame [FIFA19](https://www.kaggle.com/karangadiya/fifa19). The dataset contains both data for the game as well as information about the players' real life careers.


```python
# Run this cell without changes

import pandas as pd
import numpy as np
import warnings
warnings.filterwarnings('ignore')
```

### 2.1) Read the CSV file into a pandas DataFrame

The data you'll be working with is in a file called `'./data/fifa.csv'`. Use your knowledge of pandas to create a new DataFrame, called `df`, using the data from this CSV file. 

Check the contents of the first few rows of your DataFrame, then show the size of the DataFrame. 


```python
# Replace None with appropriate code
df = None
```


```python
# Code here to check the first few rows of the DataFrame

```


```python
# Code here to see the size of the DataFrame

```

### 2.2) Drop rows with missing values for `'Release Clause'`
    
Drop rows for which "Release Clause" is none or not given. This is part of a soccer player's contract dealing with being bought out by another team. After you have dropped them, see how many rows are remaining.


```python
# Code here to drop rows with missing values for 'Release Clause'

```


```python
# Code here to check how many rows are left 

```

### 2.3) Convert the `'Release Clause'` Price from Euros to Dollars

Now that there are no missing values, we can change the values in the `'Release Clause'` column from Euro to Dollar amounts.

Assume the current exchange rate is `1 Euro = 1.2 Dollars`


```python
# Code here to convert the column of euros to dollars

```

---
## Part 3: Data Visualization [Suggested Time: 20 minutes]
---

Continuing to use the same FIFA dataset, plot data using whichever plotting library you are most comfortable with.


```python
# Run this cell without changes

import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```

### 3.1) Find the top 10 countries with the most players (using the `'Nationality'` column). Create a bar chart showing the number of players in those 10 countries.

Don't forget to add a **title** and **x axis label** to your charts.

If you are unable to find the top 10 countries but want the chance to demonstrate your plotting skills use the following dummy data to create a bar chart: 

```
Country Name  | Num Players
============  | ===========
Country A     | 100
Country B     | 60
Country C     | 125
Country D     | 89
```


```python
# Code here to get the top 10 countries with the most players

```


```python
plt.figure(figsize=(10, 6))

# Code here to plot a bar chart

```

### 3.2) For the below scatter plot, how would you describe the relationship between these two features?

Describe the relationship between the player stats `StandingTackle` and `SlidingTackle` shown below.


```python
# Run this cell without changes

plt.scatter(df['StandingTackle'], df['SlidingTackle'])
plt.title('Standing Tackle vs. Sliding Tackle')
plt.xlabel('Standing Tackle')
plt.ylabel('Sliding Tackle')
plt.show()
```


```python
"""
Written answer here
"""
```

---
## Part 4: Exploring Statistical Data [Suggested Time: 20 minutes]
---

### 4.1) What are the mean age and the median age for the players in this dataset?

In your own words, how are the mean and median related to each other and what do these values tell us about the distribution of the column `'Age'`? 


```python
# Code here to find the mean age and median age
```


```python
"""
Written answer here
"""
```

### 4.2) Who is the oldest player in Argentina and how old is he?


```python
# Code here to find the oldest player in Argentina
```


```python
"""
Written answer here
"""
```
