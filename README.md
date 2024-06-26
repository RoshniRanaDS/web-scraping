# NASA on Mars 
(News Articles And Weather data)

# Web-Scraping and Data Analysis

This data analysis work consists of two technical products. 

Deliverable 1: Scrape titles and preview text from Mars news articles.  
Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

# Background
have learned to identify HTML elements on a page, 
identified their id and class attributes, and used this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup.  
Also have learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.

As have worked on this, has strengthened the same core skills that i have been developing until now:   
collecting data, organizing and storing data, analyzing data, and then visually communicating insights.

# Instructions
# Part 1: Scrape Titles and Preview Text from Mars News
#Jupyter Notebook file "part_1_mars_news_Roshni.ipynb"  
have work on this code as followed the steps below to scrape the #Mars News website.  
#

1.Used automated browsing to visit to an external data site link.     
Note that the URL is "https://static.bc-edx.com/data/web/mars_news/index.html"      
Inspected the page to identify which elements to scrape by using chrome DevTools. 
  
2.Created a Beautiful Soup object and used it to extract text elements from the website. 

3.Extracted the titles and previewed text of the news articles that have scraped.  
  Stored the scraping results in Python data structures as follows:
  
4.Stored each title-and-previewed pair in a Python dictionary and, gave each dictionary two keys: title and preview.  
 
 An example is the following:
" {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}"

5.Stored all the dictionaries in a Python list. 

6.Printed the list in notebook.   
7.stored the scraped data in a file (to ease sharing the data with others).  
8.exported the scraped data to a JSON file. ("mars_news_data_Roshni.json")

# Part 2: Scrape and Analyze Mars Weather Data
#Jupyter Notebook file "part_2_mars_weather_Roshni.ipynb"  
worked in this code as to follow the steps below to scrape and analyze Mars weather data.
#
1.Used automated browsing to visit the Mars Temperature Data SiteLinks to an external site.    
Inspected the page to identify which elements to scrape.     
Note that the URL is "https://static.bc-edx.com/data/web/mars_facts/temperature.html"

2.Created a Beautiful Soup object and used it to scrape the data in the HTML table.    
this can also be achieved by using the Pandas "read_html" function.   
However, used Beautiful Soup here to continue sharpening web scraping skills.

3.Assembled the scraped data into a Pandas DataFrame.  
The columns have the same headings as the table on the website.  

Here’s an explanation of the column headings:
#
>id:> 'the identification number of a single transmission from the Curiosity rover'    
>terrestrial_date:> 'the date on Earth'    
>sol:> 'the number of elapsed sols (Martian days) since Curiosity landed on Mars'    
>ls:> 'the solar longitude'    
>month:> 'the Martian month'      
>min_temp:> 'the minimum temperature, in Celsius, of a single Martian day (sol)'    
>pressure:> 'The atmospheric pressure at Curiosity's location'    
#
4.Examined the data types that were currently associated with each column.   
Necessarily, casted (or converted) the data to the appropriate datetime, int, or float data types.  

5.Analyzed dataset by using Pandas functions to answer the following questions:
#
a.How many months exist on Mars?  
b.How many Martian (and not Earth) days worth of data exist in the scraped dataset?    
c.The coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:  
d.The average minimum daily temperature for all of the months.  
e.Ploted the results as a bar chart.  

f.Which months have the lowest and the highest atmospheric pressure on Mars?  
To answer this question:  
    1.Found the average daily atmospheric pressure of all the months.    
    2.Ploted the results as a bar chart.  
    
g.How many terrestrial (Earth) days exist in a Martian year?  
To answer this question:  
    1.Considered how many days elapse on Earth in the time that Mars circles the Sun once.  
    2.Visually estimated the result by plotting the daily minimum temperature.  
    
h.Exported the DataFrame to a CSV file. "mars_weather_data_Roshni.csv"
