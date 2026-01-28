==============================================================================
AI NEWS WEB
==============================================================================

A lightweight Flask web application that aggregates real-time news about
Artificial Intelligence using the NewsAPI service. This project serves as a
news feed, search engine, and REST API provider for AI-related topics.

---

## FEATURES

- Live News Feed: Fetches the latest articles about "Artificial Intelligence".
- Search Functionality: Allows users to search for specific news topics.
- Pagination: Navigates through news results (up to 100 results/5 pages).
- Article Details: Dedicated view for reading article summaries.
- JSON API: Exposes a /api/news endpoint for external applications.
- Error Handling: Custom 404 and 500 error pages.

---

## TECH STACK

- Python 3.x
- Flask (Web Framework)
- Requests (HTTP Client)
- NewsAPI (External Data Source)
- HTML/CSS (Frontend Templates)

---

## PROJECT STRUCTURE

/
├── app.py # Main application logic
├── templates/ # HTML files
│ ├── index.html # Homepage (news feed)
│ ├── article_detail.html
│ ├── search.html
│ └── error.html
├── static/ # CSS, JS, and Images
│ └── placeholder.png # Fallback image for articles
└── README.txt

---

## INSTALLATION & SETUP

1. Clone the repository
   git clone https://github.com/patelpriyanshu8878-del/ai-news-aggregator.git
   cd ai-news-aggregator

2. Install Dependencies
   pip install flask requests

3. Configure API Key
   This project requires an API key from NewsAPI.org.
   - Sign up at https://newsapi.org
   - Open 'app.py'
   - Replace the generic key with your actual API key:
     NEWS_API_KEY = "YOUR_ACTUAL_API_KEY_HERE"

4. Run the Application
   python app.py

   Access the application in your browser at: http://127.0.0.1:5000

---

## API USAGE

The application provides a JSON endpoint for developers.

Endpoint: /api/news

Parameters:

- q: Search query (default: "artificial intelligence")
- page: Page number (default: 1)

Example Request:
GET http://127.0.0.1:5000/api/news?q=machine+learning&page=1

---

## SECURITY NOTE

Currently, the API key is stored directly in app.py. For production
environments, it is recommended to store sensitive keys in environment
variables or a .env file rather than hardcoding them.

---

## LICENSE

This project is open-source and available under the MIT License.
