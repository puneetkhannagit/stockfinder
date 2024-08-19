Market Data Scraper
This project is a Spring Boot application that scrapes and stores quarterly profit and loss data for various stocks. It uses Jsoup for web scraping and persists the data in a relational database.

Key APIs
Scrape Profit and Loss for All Companies in a Category
Endpoint: POST /pl/scrape-profit-and-loss/all-in-category/{capitalCategory}
Description: Scrapes and stores profit and loss data for all companies within the specified capital category.
Path Variable:
capitalCategory: The category of companies to scrape (e.g., large-cap, mid-cap).
Scrape Profit and Loss for a Single Stock
Endpoint: POST /pl/scrape-profit-and-loss/{stockSymbol}
Description: Scrapes and stores profit and loss data for a specific stock based on its symbol.
Path Variable:
stockSymbol: The stock symbol for which to scrape the data (e.g., AAPL, MSFT).
How It Works
The application scrapes financial data from a specified URL using the stock symbol.
It parses the HTML to extract quarterly financial details such as net profit, operating profit, sales, etc.
The data is then stored in a database using JPA repositories.
Technologies Used
Spring Boot: Backend framework.
Jsoup: HTML parsing library.
JPA: For database interaction.
H2/MySQL: Database for storing scraped data.
Getting Started
Prerequisites
Java 8 or later
Maven
MySQL or H2 Database
Running the Application
Clone the repository:
git clone https://github.com/your-username/market-data-scraper.git
Navigate to the project directory:
cd market-data-scraper
Build the project using Maven:
mvn clean install
Run the Spring Boot application:
mvn spring-boot:run
Access the APIs using tools like Postman or curl.
Notes
Ensure compliance with the terms of service of the website you are scraping data from.
The application includes a delay mechanism to prevent overloading the target server.
License
This project is licensed under the MIT License - see the LICENSE file for details.
