## Introduction
A sentiment analysis on the Health Insurance Reviews off a policy comparison website.

**Here we dont not use API or scraping, we are reading text from saved webpages. IMO, the method that never fails. 

For purposed related to speed and ease of processing, we are using 20 pages with 20 reviews each. The model should be linearly scalable fairly easily.

## Process-Flow:
1. We save and read all the files from the directory into a single file.
   We need codecs library to extract the source code from the html files.
   The file is a collection of objects, we add a space to seperate them. 

2. We use BeautifulSoup to parse the html files.
   If we look into the 
