# Amazon-scrap

﻿# AutoScraper: A Smart, Automatic, Fast and Lightweight Web Scraper for Python
 
 
 
<img width="817" alt="91968083-5ee92080-ed29-11ea-82ec-d99ec85367a5" src="https://user-images.githubusercontent.com/84532073/171902224-22c18b22-a6ee-411b-a521-e97fca666c5a.png">


This project is made for automatic web scraping to make scraping easy. It gets a url or the html content of a web page and a list of sample data which we want to scrape from that page. This data can be text, url or any html tag value of that page. It learns the scraping rules and returns the similar elements. Then you can use this learned object with new urls to get similar content or the exact same element of those new pages.

Installation
It's compatible with python 3.

Install latest version from git repository using pip:
$ pip install git+https://github.com/alirezamika/autoscraper.git
Install from PyPI:
$ pip install autoscraper
Install from source:
$ python setup.py install


How to use
Getting similar results
Say we want to fetch all related post titles in a stackoverflow page:


from autoscraper import AutoScraper

url = 'https://stackoverflow.com/questions/2081586/web-scraping-with-python'

# We can add one or multiple candidates here.
# You can also put urls here to retrieve urls.
wanted_list = ["What are metaclasses in Python?"]

scraper = AutoScraper()
result = scraper.build(url, wanted_list)
print(result)
