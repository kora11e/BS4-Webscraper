<h1> Wiki Data Webscraper </h1>

<h2> Overview </h2>

The project is the implementation of webscraping on Wiki Fandom website structure.

<h2> Motivation </h2>

Webscraper aims to utilize handful of Python tools and libraries to scrape data. The program can scroll through and download all valuable information, then store them into pandas dataframe (keywords, links, categories, statistics) and separate dedicated folder (images).
Usage of PySpark is to apply more efficient data warehouse storage.

<h2> Features </h2>

1. Selenium Webdriver (optional, needless for correct execution).
2. Website Crawler - a program that searches for crucial tags and fetches them.
3. Numpy data representation - every instance is stored in separate NParray.
4. Data framing - native Pandas DataFrame composition of gathered data.
5. Image downloader - snatches pictures on the website and stores their buffer representation in dedicated folder.
   
<h2> Instructions to run the program </h2>

!!Note!!
The Notebook was developed using built in VSCode Jupyter Extension on Python 3.3. Oder versions might not support all features.
In order to run the program use the following code snippet to install necessary libraries:
```python
pip install bs4 pathlib pandas numpy regex os requests selenium shutil pyspark
```

1. Download Jupyter Notebook or Visual Studio with community JN extension.
2. Install necessary packages  - pip install bs4 numpy pygame helper matplotlib collections -
3. Download the project and open it in the IDE
4. Move to the last cell and select option "Execute above cells" then execute the last cell separately.

<h2> Project Explanation </h2>
Webscraper provides code that first checks if the website uses captcha. Selenium module applies webdriver that controls presence or absence of the anti-bot tools. The project then fetches website by getting link(s) from txt file containing list of websites. 

Webscraper performs then data transformation, gradually preparing it for stadardization and warehouse storage. After that program combines multiple category and subcategory titles, urls storing them as Numpy arrays in pandas DataFrame and savving as .csv datasets. Scraper then performs a loop to find, encode and save image files into separate folder. 

As the final step the program stores them in local pyspark database using dataset schema.
