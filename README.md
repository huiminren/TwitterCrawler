# TwitterCrawler
Crawl Tweets **without Twitter API** to avoid rate limits

Step:
1. Connect to the link
   a. Use Developer Tools (right click of 'Inspect' in Chrome).
   b. Click 'Network' to find the real link which includes the information you need. 
      Usually it is different from the website in your browser. In this case, the real link starts with 'timeline?'.
   c. Click 'Headers' to find 'Request Headers' and 'Query String Paramters', 
      which will be needed when you set header and param.
   d. Copy all the information in 'Request Headers' to header={}, except 'cookie'. 
      Note that 'user-agent' is the most import element in this method.
   e. Copy all the information in 'Query String Paramters' to param{}.
   f. Set response.
2. Parser html
   Use BeautifulSoup to parser html into DOM.
3. Store data
   Use Pandas to store data into dataframe and csv file.
