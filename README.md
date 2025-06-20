# 📱 Mobile Phones Search Automation on Online Shopping Website

## 🚀 Overview

This project automates the process of searching for **mobile smartphones under ₹30,000** on a leading online shopping website (e.g., [Amazon India](https://www.amazon.in)). The automation ensures that only **newly arrived smartphones** are displayed, validating various interface elements and behaviors as specified in the requirements.

---

## 📝 Problem Statement

**Objective:**  
Automate the search functionality for mobile phones on an online shopping platform, ensuring the following criteria:
- **Price:** Less than ₹30,000
- **Category:** Newly arrived smartphones
- **Platform:** Amazon India (default) or any other legitimate shopping website

---

## 📋 Functional Requirements

1. **Browser Launch**  
   - Launch browser (Chrome/Firefox) as per configuration.
   - Read application URL from configuration settings.

2. **Navigation & Search**  
   - Open the homepage.
   - Enter the search term:  
     `"mobile smartphones under 30000"`
   - Validate the displayed result summary, including:
     - Search string
     - Number of pages (e.g., `1-24`)
     - Total items (e.g., `over 1,000 results`)

3. **Sorting**  
   - Click on the "Sort by" dropdown/listbox.
   - Validate that four sorting options are displayed.
   - Select "Newest Arrivals".
   - Confirm that "Newest Arrivals" is correctly selected.

4. **Cleanup**  
   - Close the browser after test execution.

---

## 🛠️ Key Automation Scope

- **Cross-browser support:** Chrome & Firefox
- **Synchronization:** Robust waits for elements and page states
- **Dropdown/Listbox handling:** Accurate interaction and validation
- **Exception handling:** Graceful error management and detailed logging
- **Element location:** Reliable and maintainable selectors

---

## ⚙️ Configuration

- **Browsers Supported:** Chrome, Firefox
- **Configurable URL:** Set in `config.properties` (default: `https://www.amazon.in`)
- **Test Data:** Search term and filters can be modified in the config file

---

## 🏗️ Project Structure

```plaintext
.
├── src/
│   ├── main/
│   │   └── java/
│   │       └── ... (automation code)
│   └── test/
│       └── java/
│           └── ... (test scripts)
├── resources/
│   └── config.properties
├── README.md
└── ... (build files)
```

---

## 💻 Setup & Execution

### 1. Prerequisites
- Java 8+ (for Java-based frameworks)
- Maven/Gradle
- ChromeDriver and/or GeckoDriver (for Firefox)
- [Selenium WebDriver](https://www.selenium.dev/) or similar automation library

### 2. Configuration
Edit `resources/config.properties`:
```properties
browser=chrome        # chrome or firefox
url=https://www.amazon.in
search.term=mobile smartphones under 30000
```

### 3. Run the Test
```bash
# If using Maven
mvn clean test
```
*Or use your preferred test runner.*

---

## ✅ Validation & Checks

- **Result Message:**  
  - Confirms presence and accuracy of the result summary (`1-24 of over 1,000 results for "mobile smartphones under 30000"`).

- **Sort By Dropdown:**  
  - Ensures exactly four options are present.
  - Selects **Newest Arrivals** and verifies selection.

- **Synchronization:**  
  - Uses explicit waits to handle dynamic content loading.

- **Error Handling:**  
  - All exceptions are caught and logged for analysis.

---

## 📦 Extensibility

- **Alternate Sites:** Update the `url` in config to use a different shopping platform.
- **Additional Filters:** Easily add more search criteria or validations.

---

## 🏅 Best Practices Followed

- Modular, maintainable, and scalable code structure
- Externalized configuration for easy updates
- Detailed logging and robust error handling
- Page Object Model (POM) recommended for large-scale automation

---
