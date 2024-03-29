# challenge11
Data Scraping Mars Challenge 11

# Author:
Emily L Sims

# Instructions

## Part 1: Scrape Titles and Preview Text from Mars News
Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. You will work in this code as you follow the steps below to scrape the Mars News website.
1. Use automated browsing to visit the Mars news site Links to an external site.. Inspect the page to identify which elements to scrape.
2. Create a Beautiful Soup object and use it to extract text elements from the website.
3. Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
- Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview. An example is the following:
{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
- Store all the dictionaries in a Python list.
- Print the list in your notebook.
4. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. (Note: there will be no extra points for completing this.)
## Part 2: Scrape and Analyze Mars Weather Data
Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.
1. Use automated browsing to visit the Mars Temperature Data Site Links to an external site.. Inspect the page to identify which elements to scrape. Note that the URL is https://static.bc-edx.com/data/web/mars_facts/temperature.html.
2. Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
- id: the identification number of a single transmission from the Curiosity rover
- terrestrial_date: the date on Earth
- sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
- ls: the solar longitude
- month: the Martian month
- min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
- pressure: The atmospheric pressure at Curiosity's location
4. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
5. Analyze your dataset by using Pandas functions to answer the following questions:
- How many months exist on Mars? 12 months
- How many Martian (and not Earth) days worth of data exist in the scraped dataset? 1867 days. 
- What are the coldest and the warmest months on Mars (at the location of Curiosity)? On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest.
-- To answer this question:
--- Find the average minimum daily temperature for all of the months.
  month
1    -77.160920
2    -79.932584
3    -83.307292
4    -82.747423
5    -79.308725
6    -75.299320
7    -72.281690
8    -68.382979
9    -69.171642
10   -71.982143
11   -71.985507
12   -74.451807
  
--- Plot the results as a bar chart.
  Image 1: Mars coldest and the warmest months
<img width="1233" alt="MARS coldest & warmest months" src="https://github.com/emilys28/challenge11/blob/6d46c713bc677877c9346aa3a453154be626edf8/graphs/avgmintemp_bymonth.png">

- Which months have the lowest and the highest atmospheric pressure on Mars? Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.
-- To answer this question:
---  Find the average daily atmospheric pressure of all the months.
  month
1     862.488506
2     889.455056
3     877.322917
4     806.329897
5     748.557047
6     745.054422
7     795.105634
8     873.829787
9     913.305970
10    887.312500
11    857.014493
12    842.156627
  
--- Plot the results as a bar chart.
  <img width="1233" alt="MARS atmosphere pressures" src="https://github.com/emilys28/challenge11/blob/429df88e82674a4c316cd6a91c66873392055b75/graphs/mars_avg_atmosphere_pressure.png">
  
- About how many terrestrial (Earth) days exist in a Martian year? The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.
-- To answer this question:
---  Consider how many days elapse on Earth in the time that Mars circles the Sun once.
--- Visually estimate the result by plotting the daily minimum temperature.
  <img width="1233" alt="MARS days" src="https://github.com/emilys28/challenge11/blob/429df88e82674a4c316cd6a91c66873392055b75/graphs/terrestrialdays.png">
6. Export the DataFrame to a CSV file.

# Requirements

## Part 1: Scrape Titles and Preview Text from Mars News (40 points)

- Automated browsing (with Splinter) was used to visit the Mars news site, and the HTML code was extracted (with Beautiful Soup). (10 points)
- The titles and preview text of the news articles were scraped and extracted. (20 points)
- The scraped information was stored in the specified Python data structure—specifically, a list of dictionaries. (10 points)

## Part 2: Scrape and Analyze Mars Weather Data (60 points)

- The HTML table was extracted into a Pandas DataFrame. Either Pandas or Splinter and Beautiful Soup were used to scrape the data. The columns have the correct headings and data types. (15 points)
- The data was analyzed to answer the following questions: (10 points)
- How many months exist on Mars? (5 points)
  12
- How many Martian days' worth of data are there? (5 points)
  1867 days
- The data was analyzed to answer the following questions, and a data visualization was created to support each answer: (30 points)
- Which month, on average, has the lowest temperature? The highest? (10 points)
  On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest.
- Which month, on average, has the lowest atmospheric pressure? The highest? (10 points)
  Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.
- How many terrestrial days exist in a Martian year? A visual estimate within 25% was made. (10 points)
  The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot.
- The DataFrame was exported into a CSV file. (5 points)
  See file: mars.csv
  https://github.com/emilys28/challenge11/blob/d4abfa69e04c337c34890f25cd37d4ff5ac82671/mars.csv
  
# References
The Mars News website Links to an external site. is operated by edX Boot Camps LLC for educational purposes only. The news article titles, summaries, dates, and images were scraped from NASA's Mars News Links to an external site. website in November 2022. Images are used according to the JPL Image Use Policy Links to an external site., courtesy NASA/JPL-Caltech.
