# Amazon-Fashion-Product-Scraper---Mission-Discover

## Overview
This project is developed to systematically gather extensive product data from Amazon's Fashion category to analyze trends, popularity, and consumer preferences. Utilizing web scraping techniques, this scraper targets over 10 categories within the Fashion domain, aiming to retrieve critical data from a minimum of 1000 products in each category.

## Project Objective
The primary goal is to create a comprehensive collection of product information in JSON format, making it easy to analyze and process for insights into the current market trends on Amazon.

## Key Features
- Retrieves details such as Product URL, ID, Name, Description, Price, Brand, Colors, Images, and Reviews.
- Handles dynamic content and pagination using Selenium.
- Employs Beautiful Soup for efficient HTML parsing.
- Ensures compliance with Amazon’s web scraping guidelines.

## Prerequisites
- Python 3.6+
- Pip and virtualenv (optional but recommended for package management)

## Install Required Python Packages:
pip install pandas beautifulsoup4 selenium webdriver-manager fuzzywuzzy tqdm

## Selenium WebDriver:
Make sure the WebDriver for your browser is correctly set up. This script defaults to using Chrome.

## Configuration
Before running the scraper, ensure the config.py file contains the correct URLs and parameters for scraping:

- Modify the starting URL to focus on different sub-categories within Fashion.
- Adjust maximum product counts and categories as needed.


## Usage
To start scraping, run the script from the command line:
**python amazon_fashion_scraper.py**
The script will perform scraping across multiple categories and save the data in structured JSON format.

## Data Structure
Each JSON object includes:

- productUrl: Direct link to the product page.
- productId: Unique identifier for the product.
- gender: Specified if applicable, otherwise null.
- Category: Broad categorization of the product.
- description: Detailed information about the product.
- productName: Official name on Amazon.
- subCategory: More specific categorization derived via fuzzy matching.
- brandName: Manufacturer or seller.
- colours: Available color options and corresponding image URLs.
- images: Primary and secondary images of the product.
- price: Current price, with distinctions per color if applicable.
- Product reviews: Detailed reviews and ratings.

## Output
Data is saved as product_details.json in the project directory, formatted for easy integration into data analysis tools.

## Ethical Considerations
This scraper adheres to Amazon's robots.txt and scraping policies to ensure ethical data collection practices. Users must also respect Amazon's Terms of Service to avoid legal and ethical issues.

## Troubleshooting
Ensure all dependencies are installed and up to date.
Check internet connection and Amazon website availability as the scraper requires a stable network.
For any issues with Selenium drivers, verify the path and browser compatibility.

## Contribution
Contributions to improve the scraper are welcome. Please fork the repository, make your changes, and submit a pull request.

