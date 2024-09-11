# Web Scraping and Sentiment Analysis on Digikala Reviews

## Project Overview
This project involves web scraping reviews from the online shopping platform **Digikala**. The reviews are extracted for various products and analyzed based on their ratings to classify them into positive and negative sentiments.

## Dataset
The dataset is created by scraping customer reviews and ratings from Digikala. The data includes:
- **Rating**: The customer’s rating of the product, ranging from 1 to 5 stars.
- **Text**: The review text written by the customer.
- **Sentiment**: The sentiment of the review, classified as:
  - **1** for positive sentiment (rating >= 4 stars)
  - **0** for negative sentiment (rating < 4 stars)

The data is stored in a CSV file with three columns:
1. `rating`: Numeric value of the product rating (float).
2. `text`: The review written by the customer (string).
3. `sentiment`: The sentiment label (0 for negative, 1 for positive).

## Methodology
1. **Web Scraping**: I used the **Selenium** library with an undetected Chrome driver to navigate through Digikala's product pages and extract review information.
2. **Review Extraction**:
   - Product reviews are scraped from product pages using specific XPaths to locate the review elements.
   - For each review, the rating and text are extracted.
   - Based on the rating, reviews are labeled as positive or negative sentiment.
3. **Iterative Scraping**: To extract reviews across multiple pages, the code iterates through available pages and appends the reviews to a CSV file.
4. **Sentiment Analysis**: After the data is collected, the reviews are labeled with sentiment based on their ratings.

## How to Run the Project
Make sure to have **ChromeDriver** installed and compatible with your Chrome browser version.



## Example Output
A sample of the scraped data might look like this:

| Rating | Text                                                     | Sentiment |
|--------|-----------------------------------------------------------|-----------|
| 5.0    | "Great product! Very happy with the purchase."            | 1         |
| 2.0    | "The quality was lower than expected, not worth the money."| 0         |
| 4.5    | "Good value for money, but the delivery was late."        | 1         |
| 3.0    | "It's okay, but I've seen better products for the price." | 0         |

## Notes
- The project is designed to scrape up to a certain number of reviews and pages, but can be adjusted for larger datasets if necessary.
- Make sure to respect the terms of service of the website when scraping data.
