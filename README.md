# Mnemonic Scraper for Mammoth Memory

This project contains a web scraper that extracts mnemonic data from the Mammoth Memory website. The script uses **Selenium** and **BeautifulSoup** to scrape and store mnemonics from different subject areas such as Chemistry and Physics.

## 📌 Features

- **Scrapes mnemonics** from selected pages on [Mammoth Memory](https://mammothmemory.net/)
- **Extracts important information** such as:
  - Words/concept pair (e.g., vocabulary term + definition, chemical element + symbol)
  - Mnemonic description
  - Highlighted text (if present)
  - Images (if available)
- **Saves data in JSON format** (`mnemonics.json`)

## 📥 Installation

### 1️⃣ Prerequisites

Ensure you have **Python 3.x** installed. You will also need **Google Chrome** and **ChromeDriver** for Selenium.

### 2️⃣ Install Dependencies

Run the following command to install required Python packages:

```sh
pip install selenium beautifulsoup4 requests
```

### 3️⃣ Setup ChromeDriver (if needed)

- **Linux/macOS:**
  ```sh
  sudo apt-get install chromium-chromedriver  # (for Ubuntu/Debian)
  brew install chromedriver  # (for macOS with Homebrew)
  ```
- **Windows:**  
  Download the latest ChromeDriver from [here](https://sites.google.com/chromium.org/driver/) and add it to your system path.

## 🚀 Usage

Run the script to scrape mnemonics:

```sh
python scraper.py
```

After execution, a `mnemonics.json` file will be created containing the scraped data.

## 📜 Data Extracted

For each mnemonic entry, the JSON file contains:

```json
[
  {
    "name1": "Element Name",
    "symbol_mobile": "Element Symbol",
    "p1": "Mnemonic text",
    "red_content": {"red1": "Highlighted text"},
    "img1_src": "https://mammothmemory.net/image.jpg"
  }
]
```

## 🛠 How It Works

1. **Loads the target web pages** using Selenium.
2. **Extracts mnemonic information** from the HTML using BeautifulSoup.
3. **Processes and cleans the data** to remove unnecessary text and duplicates.
4. **Saves the data in JSON format** for further use.

## 🔗 Target Pages

The scraper currently extracts mnemonics from the following pages:

- [Chlorine Mnemonics](https://mammothmemory.net/chemistry/periodic-table/elements-of-the-periodic-table/elements-of-the-periodic-table.html#chlorine)
- [Speed Formula](https://mammothmemory.net/physics/physics-formulas/speed/speed.html)
- [Electron](https://mammothmemory.net/chemistry/atomic-structure/electron/electron.html)
- [Force Formula](https://mammothmemory.net/physics/physics-formulas/force/force.html)

## 👨‍💻 Author

This project was developed by **[Hyunwoo Jae]**.
