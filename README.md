## Kraków Real Estate – Otodom Scraper & Analysis

Scraping apartment listings from Otodom and analysing prices in Kraków. Finding deals: total price vs area



### Key insights
* **Typical market range:** The highest concentration of listings falls between **14,000 and 17,000 PLN/m²**, reflecting standard properties across both the primary and secondary markets. 47 listings were found priced well below the market average.
* **Limitations of the mean:** The average price stands at **16,634 PLN/m²**, but it is **not a reliable indicator of a typical property**. Due to a clear **right skew** (positive skewness), high-end listings over 25,000 PLN/m² pull the mean upward.
* **Median as a robust metric:** At **15,856 PLN/m²**, the median provides a far more accurate baseline for an "average" apartment, as it reflects the midpoint of the distribution and remains unaffected by extreme outliers.
* **Outliers:** The long right-hand tail (above 25,000 PLN/m²) highlights premium apartments and luxury properties located in Kraków's city center.


## How it works
 1. Downloads listing pages from Otodom.pl using requests.
 2. Extracts the listing data from the JSON embedded in each page (__NEXT_DATA__) with BeautifulSoup.
 3. Cleans and analyses the data with pandas and creates charts with matplotlib / seaborn.
 4. Results
![Finding deals: total price vs area](output%20.png)

# How to run
bash
pip install -r requirements.txt

Then open OtodomPiwowarczykŚmigas.ipynb and run all cells.