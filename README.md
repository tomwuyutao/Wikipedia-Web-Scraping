# Readme

## On ChatGPT usage

**I did not use ChatGPT at all in this summative.** I only used Google and forums such as Stackoverflow. That’s because I often find the ChatGPT results to be too complex and too *AI* for me to understand.

## Things to note

- Which Wikimedia source did I use?
- I used Wikipedia and Wikibooks.

- How many results do I have?
- The original search results is about 12000. After cleaning the results, there are still about 5700 results left.

- How do I filter the results?
- I filtered out results that are either duplicated, or if the information scraped from this link is `[]` (Nothing).

## How can you reproduce the code?

You need to install shapely and geopandas for the mapping part.

```
pip install shapely
pip install geopandas
```

You should run the `scraping.ipynb` file first. This will generate multiple csv files in the Data folder. The `battle.csv` file is the most important one It contains all the data scraped. Other files are the location data of each time period.

Then, you should run the `analysis.ipynb` file. It produces several graphs inside VSCode (or whatever software you are using). I also write my conclusions here.

**Warning when running the code**

The amount of data in the project is huge. There are about 12000 Wikipedia pages to be scraped. Running the code on all 12000 pages can take half an hour, so I adjusted the page number to 100 (that’s 100\*20 = 2000 results). 2000 results is enough to show the pattern on the graph. 

If you have time to run all 12000 results, please follow the instructions to change the code:

- Use command-F on you computer and look for the text `Change the page number here`.
- Can change the `100` inside `range()` into `630`. 630 is the total number of pages.
- Expect the code to run for an hour

If you just want to run the ’100’ version, you might want to have a look at what the full version can produce. There are two ways to do that:

- Run the `analysis.ipynb` first. This will use the data I uploaded.
- Or view the `Analysis of all 12900 battles.pdf` file.

## Description of my project

### Getting the data

In this coursework, I want to investigate historical battles. I found that on the Wikipedia page of each battle, there is always a table containing key information about this battle. I decided to scrape the name, date, location, and belligerents of each battle.

To do this, I created a function containing all scraping code. I experimented with a pagination method, and, finally, put the scraping function into the pagination code. The results are saved in a `battle.csv` file.


### Analyzing the data

Question 1: I investigate where all battles take place by extracting the location data. I then plot the data on a map using shapely and geopandas.

Question 2: I plot out when most data take place throughout history.

Question 3: I investigate who fought the most battles.

Question 4: I divide history into ancient history, post-classical history, and modern history. I investigated where most battles took place during each period of history.

Question 5: I investigate who fought the most battles in each period of history.

Question 6: I gather data from Wikibooks and find out which battles from Wikipedia also has a book describing it.
 
