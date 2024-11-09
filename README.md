# BrokenOutAi_Ass
**AI Agent Dashboard**
  This project is an AI-powered information retrieval dashboard that allows users to upload a CSV file or connect to Google Sheets to extract specific data for each entity in a selected column. The AI leverages OpenAI's GPT API and SerpAPI to perform web searches and extract relevant information based on user-defined prompts.

**Block diagram**
                +-------------------------+
                |  User Interface (UI)    |
                |  - Streamlit Dashboard  |
                |  - File Upload / Google |
                |    Sheets Input         |
                +-----------+-------------+
                            |
                            |
                            v
              +------------+---------------+
              |  Data Source Selection     |
              |  - CSV File                |
              |  - Google Sheets API       |
              +------------+---------------+
                            |
                            |
                            v
              +------------+---------------+
              | Data Processing Component  |
              |  - Load Data               |
              |  - Select Main Column      |
              |  - Display Data Preview    |
              +------------+---------------+
                            |
                            |
                            v
              +------------+---------------+
              |  Query Template Input      |
              |  - User defines search     |
              |    query prompt with       |
              |    placeholders            |
              +------------+---------------+
                            |
                            |
                            v
              +------------+---------------+
              | Web Search API Integration |
              |  - SerpAPI (Web Search)    |
              |  - Retrieve Search Results |
              +------------+---------------+
                            |
                            |
                            v
              +------------+---------------+
              | LLM Processing Component   |
              |  - Pass results to OpenAI  |
              |    for data extraction     |
              |  - Extract specified info  |
              +------------+---------------+
                            |
                            |
                            v
              +------------+---------------+
              | Display & Export Data      |
              |  - Show Extracted Info     |
              |  - Download as CSV         |
              +----------------------------+

**Description of Each Block**
1)User Interface (UI): The front end of the application built with Streamlit, where users interact with the dashboard to upload files, connect to Google Sheets, and define queries.

2)Data Source Selection: The component that allows users to select the data source, either by uploading a CSV file or connecting to a Google Sheets document.

3)Data Processing Component: Loads and processes the selected data, enables users to choose the primary column (e.g., companies), and displays a data preview.

4)Query Template Input: Provides a field for users to enter a custom search query with placeholders (e.g., {company}) for automated search prompts.

5)Web Search API Integration: Integrates with SerpAPI to perform web searches based on the user-defined query for each entity, retrieves search results, and stores them.

6)LLM Processing Component: Uses OpenAI’s API to process search results, applying a prompt to extract specific information (like emails or addresses) from the web results for each entity.

7)Display & Export Data: Presents the extracted information in a structured format and provides a download button for exporting the data as a CSV file.
  
**Table of Contents**
    Project Overview
    Setup Instructions
    Usage Guide
    API Keys and Environment Variables
    Optional Features
    Loom Video Walkthrough
    Project Overview
    The AI Agent Dashboard enables users to upload a file or connect to Google Sheets, select a primary column (such as company names), define a query prompt, and automatically retrieve relevant data for each entity through web search results. This information is then processed by an AI model to extract details like email addresses, addresses, or other entity-specific information.

**Setup Instructions**
**1)Clone the Repository:**

    bash
    git clone https://github.com/yourusername/AI-Agent-Dashboard.git
    cd AI-Agent-Dashboard

**2)Install Dependencies:**

  Make sure Python is installed (version >= 3.8).

  3)Install required packages:

  bash
  pip install -r requirements.txt
  
**3)Add API Keys and Credentials:**

  Follow the instructions in API Keys and Environment Variables to set up your API keys.
**4)Run the Application:**

  bash
  streamlit run app.py

  **Usage Guide**
**1)Select Data Source:**

    Choose between uploading a CSV file or connecting to a Google Sheet.
    For Google Sheets, enter the sheet URL and authenticate using your Google service account.

**2)Define Main Column:**


After data is loaded, select the main column that contains the entities (e.g., company names) for which information will be retrieved.

**3)Set Up Query Prompt:**

Enter a prompt with placeholders like {company} (e.g., “Get the email address of {company}”) for each entity in the main column.
**4)Perform Web Search:**

Click "Perform Web Search" to retrieve search results for each entity.

**5)Extract Information:**

Click "Extract Information" to process results with OpenAI’s API, and display the extracted data.
Download results as a CSV file if desired.

**API Keys and Environment Variables**

**1)OpenAI API Key:**

Obtain your OpenAI API key from the OpenAI API dashboard.
Set it as OPENAI_API_KEY in the environment.

**2)SerpAPI Key:**

Sign up and get a SerpAPI key from SerpAPI.
Set it as SERP_API_KEY in the environment.

**3)Google Sheets Service Account:**

Set up a Google Cloud project and create a service account with access to Google Sheets.
Add the JSON credentials to your environment as GCP_SERVICE_ACCOUNT.

**Add the following environment variables in a .env file:**

    OPENAI_API_KEY="your_openai_api_key"
    SERP_API_KEY="your_serpapi_key"
    GCP_SERVICE_ACCOUNT="path_to_your_google_service_account.json"

**Optional Features**
  Support for batch processing large datasets.
  Retry logic for handling API connection errors.
  Downloadable results in CSV format.


