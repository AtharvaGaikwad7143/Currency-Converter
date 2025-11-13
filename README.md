# 💰 Simple & Real-Time Currency Converter

Welcome to the **Simple Currency Converter**! This project provides a clean, responsive web application built with **HTML**, **CSS**, and **vanilla JavaScript** to fetch and display **real-time currency exchange rates**. It's designed to be beginner-friendly, easy to understand, and fully functional without any backend setup.

---

### ✨ Features

* **Real-Time Exchange Rates:** Fetches live data using a public API.
* **Automatic Flag Updates:** Instantly updates country flags next to the dropdowns based on the selected currency.
* **Wide Coverage:** Supports **over 100 currencies** worldwide.
* **Simple & Responsive UI:** Clean, intuitive, and works well on different screen sizes.
* **Easy to Modify:** Built purely with front-end technologies for simple modification and learning.

---

### 🛠️ Technologies Used

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Main UI structure |
| **CSS3** | Styling and layout |
| **JavaScript (ES6)** | Core logic and interactivity |
| **Fawaz Ahmed Currency API** | Live exchange rate data |
| **FlagsAPI** | Generating country flag images |

---

### 📂 Project Structure

```text
currency-converter/
  |
  +-- index.html    (The main UI structure and layout)
  +-- style.css     (All styling, colors, and responsive design)
  +-- codes.js      (The mapping of currency codes to country codes)
  +-- app.js        (The core application logic: API calls, calculations, etc.)
  +-- README.md     (This documentation file)
```
---

### 🚀 Getting Started

Getting this converter running is straightforward:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/currency-converter.git](https://github.com/your-username/currency-converter.git)
    ```
2.  **Navigate into the Project Folder:**
    ```bash
    cd currency-converter
    ```
3.  **Run the Project:**
    Simply **open `index.html` in your web browser**. No server or special setup is required!

---

### 💡 How It Works

The core functionality is managed by `app.js`, orchestrating the following steps:

1.  **Currency List & Dropdown Population**
    * The `codes.js` file stores all supported currency codes.
    * `app.js` loops through this data to dynamically **populate both "From" and "To" currency dropdowns** on page load (Default: USD $\rightarrow$ INR).

2.  **Flag Update System**
    * Each currency maps to its ISO country code.
    * When a currency is selected, JavaScript generates a flag image URL (using FlagsAPI) and **instantly updates the flag image** next to the dropdown.

3.  **Fetching Live Exchange Rates**
    * The project uses the following API endpoint:
        ```bash
        [https://cdn.jsdelivr.net/gh/fawazahmed0/currency-api@1/latest/currencies](https://cdn.jsdelivr.net/gh/fawazahmed0/currency-api@1/latest/currencies)
        ```
    * `app.js` constructs the URL based on selections (e.g., `.../usd/inr.json`), fetches the JSON data containing the conversion rate, and calculates the final converted amount, displaying it in the `.msg` section.

4.  **Input Validation**
    * The input amount is validated. If the user enters an empty or invalid value, the amount automatically **defaults to 1** for conversion.

---

### 🤝 Contributing

Contributions are welcome!

You may submit **pull requests** for:
* Improvements to the core logic.
* UI/UX upgrades and styling enhancements.
* New features or functionality.
