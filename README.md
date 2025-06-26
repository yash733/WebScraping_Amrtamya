# Amrtamya.com Web Scraping Project

This project uses **Selenium** and **BeautifulSoup** to scrape product and category data from [amrtamya.com](https://amrtamya.com/). The script navigates through the site's main sections, extracts product details, and organizes the data into a structured Python dictionary.

---

## Features

- **Category Extraction:**  
  Scrapes all product categories from the shop page, including category names, links, and images.

- **Product Extraction:**  
  For each category, opens all products in new tabs and extracts:
  - Product name
  - Description
  - Price
  - Available sizes
  - Images
  - Reviews and ratings
  - Customer reviews
  - "You may also like" recommendations (with name, link, image, and price)

- **About and Contact Info:**  
  Extracts the About page and Contact information.

---

## Requirements

- Python 3.8+
- [Selenium](https://pypi.org/project/selenium/)
- [BeautifulSoup4](https://pypi.org/project/beautifulsoup4/)
- Chrome browser (portable or installed)
- Matching [ChromeDriver](https://googlechromelabs.github.io/chrome-for-testing/)

---

## Setup

1. **Clone this repository or copy the notebook files.**
2. **Install dependencies:**
   ```
   pip install selenium beautifulsoup4
   ```
3. **Download ChromeDriver** that matches your Chrome version and update the `chrome_driver_path` and `chrome_options.binary_location` in the script.
4. **Run the notebook** (`2nd_dft.ipynb` or similar) in Jupyter or VS Code.

---

## How It Works

- The script launches Chrome using Selenium.
- Navigates to the main site and shop page.
- Iterates through each category and product, opening each in a new tab for scraping.
- Collects all relevant data and stores it in the `scraped_data` dictionary.
- Closes tabs as it finishes scraping each product and category.

---

## Output

- All scraped data is stored in the `scraped_data` Python dictionary.
- CSV format data [amrtamya_products.csv](https://github.com/yash733/WebScraping_Amrtamya/blob/main/Scraping/amrtamya_products.csv)
---

## Notes

- The script uses `time.sleep()` and `WebDriverWait` to ensure pages are fully loaded before scraping.
- If the site structure changes, you may need to update the CSS selectors or XPaths in the script.
- For large-scale scraping, consider adding error handling, logging, and rate limiting.

---

## Disclaimer

This project was an acessment task.  

---
