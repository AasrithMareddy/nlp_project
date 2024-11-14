# Financial Report Summarization using NLP

This project focuses on using Natural Language Processing (NLP) techniques to automatically summarize financial reports for stocks listed on the NSE (National Stock Exchange) India. The project involves data collection, organization, and summarization of annual financial reports in a structured manner for efficient analysis.

## Weekly Progress Summary

### Week 1: Research and Stock Selection
- **Objective**: Gather stock codes for NSE-listed companies.
- **Summary**: Researched stocks listed on NSE India and compiled a list of stock codes for 1800 companies, organized into an array. This list serves as the basis for data collection in the subsequent weeks.

### Week 2: Data Collection and Report Downloading
- **Objective**: Automate the download of financial reports for each stock.
- **Tools Used**: Selenium (with Firefox in headless mode) for web scraping and automation.
- **Setup Details**:
  - Configured a headless Firefox browser to operate in the background, optimizing the speed of data retrieval.
  - Adjusted download settings to automatically save PDF files into a folder named `downloads` within the project directory, avoiding manual save prompts.
  - For each stock code, the program generates a URL specific to the stock’s page on [Screener](https://www.screener.in/) (e.g., `https://www.screener.in/company/{stock_code}/consolidated/`), enabling automated access and download of annual financial reports.
- **Result**: Downloaded and organized PDFs for each stock, laying the groundwork for the NLP summarization phase.

### Week 3: Initial Data Processing
- **Objective**: Rename and organize downloaded files for efficient access.
- **Details**:
  - Each downloaded PDF was renamed to include the stock code and the financial year (e.g., `20MICRONS_2022.pdf` for the 2022 report of the company 20MICRONS).
  - This systematic file-naming convention ensures easy reference and prepares the files for subsequent NLP processing.

## Project Structure
