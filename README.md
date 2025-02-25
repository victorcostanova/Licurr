# Licurr

A live currency conversion tool developed for the final project of CS50X-2025. Licurr leverages API integration with clean front-end technologies to provide real-time currency conversion with a focus on Bitcoin (including Satoshis) to various fiat currencies like USD, BRL, CAD, and many others.

The project is hosted using GitHub Pages, making it easily accessible for anyone to use without installation.

## 🌟 Project Overview

Licurr was born from the need for a simple, responsive, and accurate currency conversion tool that prioritizes Bitcoin conversions. As Bitcoin  continues to integrate into the global financial ecosystem, having a reliable tool to quickly convert between Bitcoin (down to Satoshi level) and FIAT becomes valuable.

This application stands out from other converters by:
- Focusing on Bitcoin's smallest unit (Satoshi)
- Providing real-time rates through reliable APIs
- Maintaining a clean, distraction-free interface
- Working seamlessly across all devices

## 📦 Technologies Used

### **HTML5**
Defines the structure of the page, including:
- **Divs for currency display** - Organized containers to display conversion results
- **Buttons for clearing and deleting input** - Intuitive controls for user input management
- **Dropdown menu for currency selection** - Comprehensive list of global currencies

I chose semantic HTML elements throughout the project to improve accessibility and SEO performance.

### **CSS3**
Handles the design and responsiveness:
- **Styled buttons, layouts, and menus** - Consistent visual language across the application
- **Flexbox & Grid Layouts** for adaptive positioning - Ensures content flows naturally on any screen size
- **Media queries** for responsive display across devices - Optimized experience from mobile to desktop

The design philosophy emphasizes clarity and functionality, with a color scheme that reduces eye strain during extended use.

### **JavaScript**
Manages all the functionality, divided into three scripts:

1. **`scripts.js`** – Handles:
   - **User interactions** (adding/removing currencies)
   - **Clear and delete button functions**
   - **Dynamic dropdown updates**
   - **Event listeners and DOM manipulation**

2. **`conversion.js`** – Manages:
   - **API requests for exchange rates**
   - **Validation & formatting of converted values**
   - **Error handling for API failures**
   - **Caching mechanism to reduce unnecessary API calls**

3. **`currencies.js`** – Contains:
   - **List of currency codes, symbols, and names** for dynamic selection
   - **Formatting rules for different currency displays**
   - **Search functionality for the currency selector**

I deliberated between using a single JavaScript file versus multiple specialized files. I ultimately chose the modular approach to improve code organization, maintainability, and to make future contributions more straightforward.

### **APIs Used**
- 🌍 **[ExchangeRate API](https://exchangerate-api.com/)** – Fetches live exchange rates for fiat currencies
- ₿ **[CoinGecko API](https://www.coingecko.com/en/api)** – Retrieves the real-time Bitcoin (BTC) price in USD

When selecting APIs, reliability and update frequency were the primary considerations. CoinGecko was chosen for Bitcoin rates due to its reputation for accuracy and substantial market coverage, while ExchangeRate API provides comprehensive global currency data with generous free-tier limits.

## 🛠️ Implementation Challenges & Solutions

Challenge 1: Dynamically Adding All Available Currencies
One of the major challenges was implementing a system to dynamically populate and manage the extensive list of global currencies. I created a solution that utilizes the currency codes and symbols from the currencies.js file, using JavaScript functions to populate dropdown options. This approach allows users to easily select from all available currencies without requiring hardcoded options in the HTML. Additionally, it makes future currency additions simple by just updating the currencies.js data file.

### Challenge 2: Satoshi Precision
Displaying Satoshi values (0.00000001 BTC) accurately required careful handling of JavaScript's floating-point limitations. I implemented custom precision handling to ensure values display correctly at all decimal levels, particularly when working with the smallest Bitcoin unit where precision is critical for accurate conversions.

### Challenge 3: Number Formatting with Commas
Implementing proper number formatting with comma separators for thousands proved challenging across different currencies with varying formatting conventions. I developed a custom formatting function that intelligently applies the appropriate thousand separators (commas) based on the currency standard, enhancing readability for large numbers while respecting locale-specific formatting rules.

## 🌍 Deployment

This project is hosted on **GitHub Pages**. You can try it out here:

🔗 [**Licurr**](https://victorcostanova.github.io/Licurr/)  
🔗 [**Video Demonstration**](https://youtu.be/qDj4zg3XUiI)

## 📜 License

This project is open-source and available under the **MIT License**.

## 💡 How to Contribute

If you would like to contribute to the project, follow these steps:

1. **Fork the repository**
2. **Create a new branch for your feature or fix**
3. **Make your changes and commit**
4. **Push your changes**
5. **Submit a pull request**



## 🙏 Acknowledgements

- CS50x for providing the educational foundation
- The open-source community for invaluable resources and inspiration
- Bitconheiros (waka waka)

