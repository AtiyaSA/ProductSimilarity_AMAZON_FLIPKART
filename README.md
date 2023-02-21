# ProductSimilarity_AMAZON_FLIPKART

This code is a Python script for web scraping data from Amazon and Flipkart websites for a list of similar products specified in an Excel file. Similarity of the products is determined by checking the similarity of the product images.

The script uses the Pandas library to read data from the "Scrappingproject.xlsx" file, which contains product titles and Amazon URLs.

Then, the script uses the Selenium library and the ChromeDriver to open a Chrome browser window and navigate to the specified Amazon URL for each product.

The script clicks on the main product image to open the image viewer and scrapes the image URLs from the image viewer.

The script then uses the Requests and PIL libraries to download and open each image and compare it with the images from the same product on Flipkart using the imagehash library.

The script then stores the similarity score and Flipkart URL of the most similar product for each Amazon product in a dictionary.

Finally, the script navigates to each Flipkart URL to scrape the product title and stores all the scraped data in a list of dictionaries.

Prerequisites
To run this script, you need to install the following Python libraries:

1. Pandas
2. Selenium
3. ChromeDriverManager
4. Requests
5. Pillow
6. ImageHash

Google Chrome browser must be installed in the machine.

How to Use
To use this script, you need to provide the following input:
1. An Excel file named "Scrappingproject.xlsx" containing product titles and Amazon URLs.
2. Update the range in the for loop to the range of the rows in your Excel file that you want to scrape.
3. Update the similar variable to set the minimum similarity score between Amazon and Flipkart images required to consider them as matching products.
4. Then, simply run the script and it will automatically open a Chrome window and start scraping the data. The scraped data will be stored in a list of dictionaries named lt.
