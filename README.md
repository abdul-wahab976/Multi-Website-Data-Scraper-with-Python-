# 🌐 Multi-Website Data Scraper with Python 🕵️‍♂️  

This project demonstrates how to **scrape and extract tabular data** from multiple websites — both **static** (Wikipedia) and **dynamic** (Worldometer) — using Python’s **Pandas** and **Requests** libraries.  
It follows a **two-step approach** to handle restricted pages and HTTP 403 errors gracefully.  

---

## 🔧 Features  

| Feature | Description |
|---------|-------------|
| 📄 **Wikipedia Scraper** | Extract structured tables directly using `pandas.read_html()` |
| 🛡 **403 Error Handling** | If `pandas.read_html()` fails, fallback to `requests.get()` with headers |
| 🌍 **Worldometer Scraper** | Retrieve dynamic population data with `requests` & `pandas` |
| 💾 **CSV Export** | Save extracted tables to `.csv` files for analysis |
| 🔍 **Reusability** | Easily adapt to other websites with minimal code changes |

---

## 🛠 Tech Stack  

- **Python 3.11+**
- **Libraries Used:**
  - `pandas` – Data extraction & manipulation  
  - `requests` – HTTP requests for dynamic pages  

---

## 📊 Workflow  

### **1️⃣ Wikipedia Scraper**  
- **Website:** [Wikimedia Foundation](https://en.wikipedia.org/wiki/Wikimedia_Foundation)  
- Step 1: Attempt to scrape directly with `pandas.read_html(url)`.  
- Step 2: If error occurs (like **HTTP 403 Forbidden**), use `requests.get()` with browser headers to retrieve the HTML and then pass it to `pandas.read_html()`.  
- Save output to `wiki.csv`.  

### **2️⃣ Worldometer Scraper**  
- **Website:** [World Population by Country](https://www.worldometers.info/world-population/population-by-country/)  
- Directly scraped using `requests.get()` with headers, parsed using `pandas.read_html()`.  
- Save output to `worldometer_population_by_country.csv`.  

---

## 📂 Output Files  

| File Name | Description |
|-----------|-------------|
| `wiki.csv` | Wikimedia Foundation table data |
| `worldometer_population_by_country.csv` | Country population statistics |

---

## 📸 Sample Output Preview  

### **`wiki.csv`**  
| Headquarters | Location | Revenue | Employees |
|--------------|----------|---------|-----------|
| San Francisco | USA | $108 million | 550 |

### **`worldometer_population_by_country.csv`**  
| Country | Population (2024) | Yearly Change |
|---------|-------------------|---------------|
| China   | 1,425,000,000      | 0.03% |
| India   | 1,420,000,000      | 0.67% |

---

## 🚀 Outcome  

By completing this project, I demonstrated:  
✅ Scraping with Pandas for quick table extraction  
✅ Handling 403 errors using Requests + headers  
✅ Data wrangling & CSV export  
✅ End-to-end dataset pipeline  

---


