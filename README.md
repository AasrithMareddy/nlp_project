Weekly Summary for Financial Report Summarization Project
● Week 1: Research and Stock Selection
We began by researching stocks listed on NSE India and Screener, focusing on
gathering stock codes from 1800 companies. After compiling this list, we organized the
stock codes into an array, creating a foundation for efficient data collection in the
upcoming weeks.
● Week 2: Data Collection and Report Downloading
This week, we set up an automated scraping tool using Selenium with Firefox, running in
headless mode to speed up data retrieval. We fine-tuned the download settings to save
PDFs directly to a specific folder, bypassing the need for manual downloading. Using this
setup, we accessed each stock’s annual financial reports and saved the PDFs in a
structured format for further analysis.
● The code sets up a headless Firefox browser (meaning it runs in the background without
a visible window).
● It also customizes download settings to automatically save PDF files to a folder named
"downloads" within the current directory. This setup prevents any pop-ups asking where
to save files. For each stock code, the program builds a unique URL to access the
stock's page on Screener (e.g.,
https://www.screener.in/company/{stock_code}/consolidated/).
● Week 3: Initial Data Processing
With the reports downloaded, we focused on renaming each file based on the stock
code and financial year, which makes it easier to access and process each document
later. This organization step set up the data for our next phase, where we’ll apply NLP
techniques to summarize these financial reports.
● Once a PDF is downloaded, the code renames it using the stock code and the financial
year mentioned on the PDF link. This renaming organizes the files clearly, making it
easier to reference later.
● For example, a downloaded file for '20MICRONS' in '2022' would be saved as
20MICRONS_2022.pdf.
