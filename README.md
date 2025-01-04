# Web Scraping Job Vacancies

## Overview
This project is a web scraper designed to extract job listings from the Germany-based job search platform [Absolventa](https://absolventa.de). It gathers job titles, companies, locations, and other relevant information from job postings. The scraped data is saved into a CSV file for further analysis or use.

## Features
- Extract job postings based on user-defined job position and location.
- Parse and display details such as job title, company name, and location.
- Save the extracted data to a CSV file for easy access and sharing.

## How It Works
### Steps:
1. **Import Required Libraries**: Load essential Python libraries such as `requests`, `BeautifulSoup`, and `csv`.
2. **Generate URL**: A function (`generate_url`) dynamically generates a URL based on the user's input for job position and location. The function returns a parsed `BeautifulSoup` object for further scraping.
3. **Scrape Job Data**: Another function (`job_posting`) extracts relevant details from job postings, including:
   - Job title
   - Company name
   - Job location
4. **Save Data**: The main function saves the extracted data into a CSV file called `job_postings_result.csv`.

### Example Usage:
Run the `main` function with the desired job position and location:
```python
main(position="data analyst", location="berlin")
```

The script will fetch and parse job postings for "Data Analyst" positions in Berlin and save the results in a CSV file.

Image of the CSV:
![results](https://github.com/user-attachments/assets/162dcb97-2506-42a4-b051-d6a7cb00e271)


## Limitations
- Some major job search platforms like Indeed, Monster, and Glassdoor employ anti-scraping measures, which resulted in HTTP 403 errors during testing. This project uses Absolventa.de as it allows scraping and provides straightforward URL parameters.
- The scraper may not capture all details if the website structure changes.

## Conclusion
This project demonstrates the fundamentals of web scraping using Python. Key lessons include handling websites with anti-scraping measures and structuring a scraper for modularity and flexibility. The three main functions (`generate_url`, `job_posting`, and `main`) encapsulate each step of the scraping process, making the tool user-friendly and adaptable.
