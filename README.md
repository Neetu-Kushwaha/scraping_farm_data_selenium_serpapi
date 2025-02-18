# SerpAPi, selenium scraping

# Project Overview
This project consists of four different tasks, each in its own folder, with a common `requirements.txt` file for all dependencies.

## Folder Structure & Tasks
1. **Scraping (SERPAPI)** - Scrapes search results using SERPAPI based on keywords.
2. **Web Scraping (Selenium)** - Generalized web scraping using Selenium.

## Installation
Ensure all dependencies are installed by running:

```bash
pip install -r requirements.txt
```

## Usage
### 1. Scraping (SERPAPI)
This script processes search keywords from an Excel file and saves results to CSV and JSON files.

#### How It Works
1. Reads keywords from `keyword_postcode_Organic_Farms.xlsx`.
2. Iterates through each keyword, formatting it into filenames.
3. Calls `serpapi_pages(keyword, filename_json)` to fetch search results.
4. Saves results in CSV using `write_to_csv(data1, filename_csv)`.

#### Running the Script
```bash
python scraping/main.py
```
Ensure `keyword_postcode_Organic_Farms.xlsx` exists in the directory.

### 2. Web Scraping (Selenium)
This script automates web scraping using Selenium to extract farm-related data and save it to an Excel file.

#### How It Works
1. Sets up the Selenium WebDriver using `setup_webdriver()`.
2. Scrapes data from multiple pages (`start_page = 1` to `end_page = 50`) using `scrape_data(driver, start_page, end_page)`.
3. Extracts `name`, `farm`, and `address` details from the target website.
4. Saves the scraped data into an Excel file (`farms.xlsx`).

#### Running the Script
```bash
python selenium_scraping/main.py
```
Ensure Selenium and WebDriver dependencies are correctly installed and configured.


## License
This project is licensed under the MIT License.

