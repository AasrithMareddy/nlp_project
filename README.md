# Financial Report Summarization using NLP

This project focuses on using Natural Language Processing (NLP) techniques to automatically summarize financial reports for stocks listed on the NSE (National Stock Exchange) India. The project involves data collection, organization, and summarization of annual financial reports in a structured manner for efficient analysis.

## Weekly Progress Summary

---

### Week 1: Research and Stock Selection
*Objective*: Gather stock codes for NSE-listed companies.  
*Summary*:  
- Researched stocks listed on NSE India and compiled a list of stock codes for 1800 companies.  
- Organized the stock codes into an array to serve as the basis for data collection in subsequent weeks.  

---

### Week 2: Data Collection and Report Downloading
*Objective*: Automate the download of financial reports for each stock.  
*Tools Used*: Selenium (with Firefox in headless mode) for web scraping and automation.  
*Setup Details*:  
- Configured a headless Firefox browser for background operation, optimizing data retrieval speed.  
- Adjusted download settings to save PDF files automatically into a downloads folder within the project directory, bypassing manual prompts.  
- For each stock code, the program generated a Screener-specific URL (e.g., https://www.screener.in/company/{stock_code}/consolidated/) for automated access and download of annual financial reports.  
*Result*:  
- Successfully downloaded and organized PDFs for each stock, laying the groundwork for the NLP summarization phase.  

---

### Week 3: Initial Data Processing
*Objective*: Rename and organize downloaded files for efficient access.  
*Details*:  
- Renamed each downloaded PDF to include the stock code and financial year (e.g., 20MICRONS_2022.pdf for the 2022 report of the company 20MICRONS).  
- Ensured a systematic file-naming convention to allow easy reference and prepare files for subsequent NLP processing.  

---

### Week 4: Text Extraction and Preprocessing
*Objective*: Extract text data from PDFs and preprocess it for NLP analysis.  
*Tools Used*: PyPDF2 and NLP preprocessing libraries (nltk, re).  
*Details*:  
- Extracted text data from the renamed PDFs and stored it in text files for easier manipulation.  
- Implemented preprocessing steps:
  - Converted text to lowercase.
  - Removed special characters and redundant spaces.
  - Tokenized and lemmatized the text for semantic consistency.
  - Filtered out stopwords to focus on meaningful content.  
*Result*:  
- Generated clean, structured text files for use in the Named Entity Recognition (NER) and summarization phases.  

---

### Week 5: Named Entity Recognition (NER)
*Objective*: Identify and classify financial entities from the processed text.  
*Tools Used*: Fine-tuned BERT-based NER model.  
*Details*:  
- Trained the NER model on a financial dataset to extract entities such as:
  - *Revenue*
  - *Profit After Tax (PAT)*
  - *EBITDA*  
- Mapped extracted entities to their context within the text to ensure relevance and accuracy.  
*Result*:  
- Produced structured datasets of extracted financial metrics for each stock.  

---

### Week 6: Summarization
*Objective*: Generate concise summaries of financial reports.  
*Tools Used*: BART-large-CNN model from Hugging Face.  
*Details*:  
- Used the cleaned text and extracted financial metrics as inputs for the summarization model.  
- Fine-tuned the BART model for the financial domain to ensure summaries captured critical insights.  
- Evaluated output summaries using readability metrics such as:
  - *Flesch Reading Ease*
  - *Gunning Fog Index*
  - *Semantic Similarity*  
*Result*:  
- Generated summaries highlighting key performance indicators and trends, making reports accessible to a broader audience.  

---
 ## References
 BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
 Devlin, J., Chang, M.-W., Lee, K., & Toutanova, K. (2018).
 https://arxiv.org/abs/1810.04805
 
 BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension
 Lewis, M., Liu, Y., Goyal, N., Ghazvininejad, M., Mohamed, A., Levy, O., Stoyanov, V., & Zettlemoyer, L. (2019).
 https://arxiv.org/abs/1910.13461
 
 An Exploration of Automatic Text Summarization of Financial Reports
 Abdaljalil, S., & Bouamor, H. (2021).
 https://aclanthology.org/2021.finnlp-1.1.pdf
 
 Beyond Pure Text: Summarizing Financial Reports Based on Both Textual and Tabular Data
 Jin, H., Zhang, Y., Meng, D., Wang, J., & Tan, J. (2023).
 https://arxiv.org/abs/2302.13412 (Assumed source since it wasn't provided directly.)
 
 Practices of Natural Language Processing in the Finance Sector
 Bozyiğit, F., & Kılınç, D. (2021).
 https://link.springer.com/chapter/10.1007/978-981-16-8997-0_9
 
 Automating File Downloads with Selenium and Python - Complete Guide
 https://www.33rdsquare.com/automating-file-downloads-with-selenium-and-python-the-complete-guide/
 
 5 Best Ways to Automatically Download a PDF with Selenium WebDriver in Python
 https://blog.finxter.com/5-best-ways-to-automatically-download-a-pdf-with-selenium-webdriver-in-python/
 
 Screener - Financial Reports and Data
 https://www.screener.in/


