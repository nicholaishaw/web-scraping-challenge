# Data Analysis With Web Scraping

## Background
In this challenge, I am taking on a full web-scraping and data analysis project for a fictional company. Throughout my data analysis education, I have learned to identify HTML elements on a page, identify their id and class attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. I have also learned to scrape various types of information, including HTML tables and recurring elements—like multiple news articles on a webpage.

In this challenge, I am working on two deliverables:
* Deliverable 1: Scrape titles and preview text from Mars news articles.
* Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

## Deliverable 1: Scrape Titles and Preview Text from Mars News
In the Jupyter folder, the file named deliverable_1_mars_news.ipynb will be used for this section. To scrape the Mars News website, I followed the steps below:

1. I used automated browsing to visit the [Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html). Inspect the page to identify which elements to scrape using chrome developer tools.
2. I created a Beautiful Soup object and use it to extract text elements from the website.

![image](https://github.com/nicholaishaw/web-scraping-challenge/assets/135463220/d70daa34-1dc8-4854-988f-183d8124b94e)

**Figure 1.**

4. I extracted the titles and preview text of the news articles. I stored the scraping results in Python data structures as follows:
    * Stored each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview. An example is the following:
<EXAMPLE HERE>
    * Stored all the dictionaries in a Python list.
    * Printed the list in your notebook.
    * An example of this output is as follows:
5. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file.

## Deliverable 2: Scrape and Analyze Mars Weather Data
In the Jupyter folder, the file named part_2_mars_weather.ipynb will be used for this deliverable. To scrape and analyze Mars weather data, I will complete the following steps:

1. Use automated browsing to visit the [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html). Inspect the page to identify which elements to scrape.
2. Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
3. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
    * id: the identification number of a single transmission from the Curiosity rover
    * terrestrial_date: the date on Earth
    * sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
    * ls: the solar longitude
    * month: the Martian month
    * min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
    * pressure: The atmospheric pressure at Curiosity's location
4. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
5. Analyze your dataset by using Pandas functions to answer the following questions:
    * How many months exist on Mars?
    * How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    * What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
        * Find the average minimum daily temperature for all of the months.
        * Plot the results as a bar chart.
    * Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
        * Find the average daily atmospheric pressure of all the months.
        * Plot the results as a bar chart.
    * About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
        * Consider how many days elapse on Earth in the time that Mars circles the Sun once.
        * Visually estimate the result by plotting the daily minimum temperature.
6. Export the DataFrame to a CSV file.
