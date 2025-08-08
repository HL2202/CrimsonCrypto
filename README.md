# Crimson Crypto

This project, titled **Crimson Crypto**, is a comprehensive web application designed to help users navigate the world of cryptocurrency. It is a multi-page application built using **HTML** and **Tailwind CSS** for a modern, dark, and futuristic aesthetic. The user experience is enhanced with dynamic content loading via **JavaScript**, eliminating the need for full page reloads when navigating.

***

### Key Features

* **Multi-Page Navigation**: The application is structured with several key pages accessible from a side navigation bar: `Strategies`, `Performance`, `Insights`, `Portfolio`, `Learn`, `AI Assistant`, `About`, and `Contact`. Navigation between these pages is handled client-side using JavaScript to switch content blocks, providing a fast and seamless user experience.

* **Real-time Market Data & Insights**: The **Insights** page is a central hub for market analysis. It integrates a **TradingView widget** (`tv-dark`) to display real-time price charts and market data. Additionally, it features a custom-built, interactive gauge for the **Fear & Greed Index** to visualize current market sentiment.

* **AI Assistant**: A floating chat bot, acting as an AI Assistant, is accessible from any page. It is implemented with a chat window that allows users to type questions or select from predefined prompts to receive automated guidance and information.

* **Investment & Portfolio Management**: The **Strategies** page provides a list of investment strategies, each with a `View` button. Clicking this button opens a modal window for confirming an investment. The **Portfolio** page offers a visual representation of a user's holdings, displaying the total portfolio value, the 24-hour change, and a dynamic pie chart powered by **Chart.js** to break down assets by type.

* **User Authentication**: The application includes dedicated pages for user **Login** and **Sign-Up**. The underlying code makes calls to Firebase authentication methods (`signInAnonymously`, `signInWithCustomToken`), suggesting a secure backend is used to manage user-specific data and sessions.

* **Dynamic Notifications**: Pop-up notifications are a key part of the user experience. These include a `Trade Confirmation` notification that appears upon making an investment and a `Market News` alert that informs users of recent market developments.

***

### Technologies Used

* **Frontend**: The entire application is built on a foundation of **HTML5** and styled using the utility-first classes of **Tailwind CSS**, allowing for rapid and consistent UI development.
* **JavaScript**: JavaScript is heavily used to manage the single-page application experience, handle dynamic content loading, control modal windows, and interact with external libraries.
* **External Libraries**:
    * **TradingView Widget**: A script (`https://s3.tradingview.com/tv.js`) is used to embed a live, interactive chart for market data.
    * **Chart.js**: A script (`https://cdn.jsdelivr.net/npm/chart.js`) is utilized specifically on the portfolio page to render the user's investment breakdown in a pie chart format.
    * **Google Fonts**: The Inter font is imported (`https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap`) to ensure a consistent and modern typographical style throughout the application.
    * **Cloudinary**: The project's logo is hosted on Cloudinary (`https://res.cloudinary.com/...`), which is used to display the project branding.
    * **Firebase**: The code extensively references Firebase for its backend functionality. It uses `initializeApp`, `getAuth`, and `getFirestore` to connect to a user authentication and a NoSQL database. It also leverages `onSnapshot` for real-time updates and `setDoc`/`getDoc` for reading and writing user data.

***

### Setup & Usage

To get started with this project, you can simply open the `index.html` file in any modern web browser. However, for the full functionality, particularly the user authentication, portfolio management, and real-time market data (beyond the TradingView widget), a proper **Firebase backend configuration** is essential.

1.  **Open the File**: Open `index.html` in your browser.
2.  **Configure Firebase**: The JavaScript code expects a `__firebase_config` variable to be present. You must create and provide your own Firebase configuration object, which should include your project's API key, auth domain, project ID, and other credentials. Without this, user authentication and data persistence will not work.
3.  **Dependencies**: No local installation is required for the CSS (Tailwind) or the external libraries (Chart.js, TradingView), as they are loaded directly from their respective CDNs.
