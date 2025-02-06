# Data-Collection-Challenge
Data collection and scrapping Challenge MOD 11 (week 11)
# Unit 11 Homework: Mission to Mars

Background

This web scraping challenge will identify HTML elements on a web page, identify their id and class attributes, HTML tables and recurring elements, like multiple news articles on a webpage and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup.

This challenge consists of two technical products in the form of Jupyter Notebooks with two final output files, one csv and one JSON. You will submit the following deliverables:

Part 1 "Mars News" 

Deliverable 1: Scrape titles and preview text from Mars news articles.

Part 1: Scrape Titles and Preview Text from Mars News
Jupyter Notebook starter code for part 1 is 'part_1_mars_news.ipynb'. You will work in this code as you follow the steps below to scrape the Mars News website.

- Use automated browsing to visit the Mars news site 'https://static.bc-edx.com/data/web/mars_news/index.html'. Inspect the page to identify which elements to scrape.
- Create a Beautiful Soup object and use it to extract text elements from the website.
- Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
	- Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview. An example is the following:
- Store all the dictionaries in a Python list.
- Print the list in your notebook.

Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. 
(Note: there will be no extra points for completing this.)

Part 2 "Mars Weather"

Deliverable 2: Scrape and analyze Mars weather data, which exists in a HTML table.

Jupyter Notebook starter code for part 2 is 'part_2_mars_weather.ipynb'.
- Use automated browsing to visit the Mars Temperature Data Site. Inspect the page to identify which elements to scrape. Note that the URL is https://static.bc-edx.com/data/web/mars_facts/temperature.html.
- Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
- Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
	- id: the identification number of a single transmission from the Curiosity rover
	- terrestrial_date: the date on Earth
	- sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
	- ls: the solar longitude
	- month: the Martian month
	- min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
	- pressure: The atmospheric pressure at Curiosity's location

Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
- all values were stored as 'Object data type". They were casted as follows:     
	terrestrial_date  datetime64[ns]
	sol               int32         
	ls                float64       
	month             int32         
	min_temp          float64       
	pressure          float64   

Analyze your dataset by using Pandas functions to answer the following questions:

- How many months exist on Mars?
12
- How many Martian (and not Earth) days worth of data exist in the scraped dataset?
1867 Martian days
- What are the coldest and the warmest months on Mars (at the location of Curiosity)? 
The coldest month on Mars is month 3.
The warmest month on Mars is month 8.	
- Which months have the lowest and the highest atmospheric pressure on Mars? 
The month with the lowest atmospheric pressure on Mars is month 6.
The month with the highest atmospheric pressure on Mars is month 9.
- About how many terrestrial (Earth) days exist in a Martian year?
There are approximately 2021 terrestrial days in a Martian year.

Minimum Temperature
The minimum temperature is -68.382979 average for month 8

Atmospheric Pressure
The month with the lowest atmospheric pressure on Mars is month 6.
The month with the highest atmospheric pressure on Mars is month 9.

Year Length
A Martian year length equal 2021 terrestrial earth days, or approximately 5 terrestrial years for 1 mars year.

Export the Data Frame to a CSV file. 'mars_weather_VHR.csv'

