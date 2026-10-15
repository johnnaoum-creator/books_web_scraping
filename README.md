# Books to Scrape - Web Scraping Project

## Project Overview

This project focuses on building a web scraper using Python to collect structured book data from [Books to Scrape](https://books.toscrape.com/).

The scraper navigates through multiple book categories and pages, extracts relevant information from the website's HTML, organizes the collected records into a Pandas DataFrame, and exports the final dataset to an Excel file.

The project demonstrates practical web scraping techniques, including HTTP requests, HTML parsing, CSS selectors, category navigation, and automatic pagination.

## Project Objectives

- Automate the collection of book information from a website.
- Extract structured data from HTML elements using CSS selectors.
- Collect data across multiple categories and pages.
- Handle pagination automatically to retrieve records beyond the first page.
- Organize the extracted information into a structured dataset.
- Export the collected data to Excel for easy access and further use.

## Data Collected

The scraper extracts the following information for each book:

| Column       | Description                                    |
| ------------ | ---------------------------------------------- |
| Book Name    | The title of the book.                         |
| Category     | The category to which the book belongs.        |
| Rating       | The book's rating as displayed on the website. |
| Price        | The listed price of the book.                  |
| Availability | The availability status of the book.           |

## How the Scraper Works

### 1. Sending HTTP Requests

The Requests library is used to send HTTP requests to the website and retrieve the HTML content of its pages.

### 2. Parsing HTML

BeautifulSoup is used to parse the retrieved HTML and locate the elements containing book information.

CSS selectors help identify the relevant elements, including book titles, ratings, prices, and availability statuses.

### 3. Navigating Book Categories

The scraper navigates through multiple book categories and collects the relevant information from each category.

The category name is extracted from the page heading and stored alongside the corresponding book records.

### 4. Handling Pagination

The scraper follows the website's pagination links to access additional pages within each category.

It identifies the next-page link, uses `urljoin()` to construct the next page URL, and continues scraping until no further pages are available.

This approach allows the scraper to collect data across multiple pages instead of stopping at the first page of each category.

### 5. Organizing and Exporting Data

Pandas is used to store the collected records in a DataFrame, providing a structured tabular representation of the data.

The final dataset is exported to an Excel file for convenient access and reuse.

## Technologies Used

- **Python:** Core programming language used to implement the scraper.
- **Requests:** Retrieves HTML content from the website.
- **BeautifulSoup:** Parses HTML and extracts the required information.
- **Pandas:** Organizes the extracted records into a DataFrame.
- **Jupyter Notebook:** Provides the development environment for writing and running the code.
- **Excel:** Stores the final dataset in a convenient tabular format.

## Project Structure

```text
books_web_scraping/
├── books_scraper.ipynb
├── books_data.xlsx
├── requirements.txt
└── README.md
```

## Installation and Usage

### Prerequisites

Make sure Python is installed on your machine.

### 1. Clone the Repository

```bash
git clone https://github.com/johnnaoum-creator/books_web_scraping.git
```

### 2. Navigate to the Project Directory

```bash
cd books_web_scraping
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Notebook

Open `books_scraper.ipynb` in Jupyter Notebook or Visual Studio Code and run the cells in order.

After execution, the scraper collects the book information and exports the resulting dataset to an Excel file.

## Key Learnings

Through this project, I gained practical experience with:

- Sending HTTP requests and retrieving web page content.
- Parsing HTML and using CSS selectors to extract information.
- Navigating website categories and page links.
- Implementing automatic pagination.
- Organizing scraped records using Pandas.
- Exporting structured data to Excel.
- Working with web scraping workflows in Python.

## Future Improvements

Potential improvements for this project include:

- Adding error handling and retry logic for failed requests.
- Validating the extracted data before exporting it.
- Improving the scraper's logging and progress reporting.
- Loading the collected data into a database for further processing.

## Repository

GitHub: [Books to Scrape - Web Scraping Project](https://github.com/johnnaoum-creator/books_web_scraping)

## Author

**John Naoum**

Software Engineering Student | Learning Python and Data Engineering

[LinkedIn Profile](https://www.linkedin.com/in/john-naoum-8b0675225/)
