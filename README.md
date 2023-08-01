# SimpleWordSearch
This is the py script you need if you are seeking a particular word in a CSV file.

A list of Python packages needed to use this code:
```
import pandas as pd
```
## Reading in the file
First, you need to read your CSV file, in this case, the CSV is named "FIND.csv".
```
news_search = pd.read_csv("Find.csv")

print(news_search)
```
news_search uses the panda's function of read.csv to allow the data into Python.
A simple check can be carried out by simply allowing a print statement to display the news_search function.

## Wordsearch
Now you want to search this data. To start you need to call the function "news_search" and point out which column you want to search.
Once this data in the column has been called you need to search for that particular word you are searching for using "str.contains".

```
search = news_search[news_search['Summary'].str.contains('winner', regex=False)]
search.to_excel("outcome_winner.xlsx")
```

Once the summaries contain the particular word you are searching for you can then store the data in a separate excel file.
