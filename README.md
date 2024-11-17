**AI Agent Dashboard
Project Overview**

The AI Agent Dashboard is a user-friendly application that enables users to extract valuable information from datasets and perform web searches to retrieve and process       specific details for each entity in a given column. The app integrates with Google Sheets, SerpAPI, and OpenAI to automate and streamline the extraction and processing of data.
This project was developed as part of the BreakoutAI Assessment, showcasing skills in machine learning, API integration, and prompt engineering.

**Key Features
Data Input:**
    Upload a CSV file or connect to a Google Sheet for data input.
    View and select the primary column for entity-based queries.
    
**Dynamic Query Input:**
    Define custom prompts (e.g., "Get me the email address of {company}") for specific information retrieval.
    
**Automated Web Search:**
    Perform web searches for each entity using SerpAPI and retrieve relevant results.
    
**Information Extraction:**
    Leverage OpenAI's language models to parse search results and extract structured information.
    
**Results Visualization and Export:**
    Display extracted data in a tabular format.
    Download results as a CSV file.
    
**Error Handling:**
    Handles failed API calls gracefully with user-friendly error messages.


**Requirements
Python Libraries
Install the required Python libraries:**

                pip install streamlit pandas google-api-python-client google-auth langchain openai serpapi


**API Keys**
**SerpAPI:**
      Obtain your API key from SerpAPI Dashboard.
**OpenAI:**
      Obtain your API key from OpenAI.

**Google Sheets:**
    Create a service account in Google Cloud and download the service account JSON file.
    Setup Instructions
**1. Clone the Repository**

**git clone https://github.com/ABBANADURGAPRASAD/BrokenOutAi_Ass
cd ai-agent-dashboard**


**2. Configure Environment Variables
Create a .env file in the project directory to store API keys securely:**

                    OPENAI_API_KEY=your_openai_api_key
                    SERPAPI_API_KEY=your_serpapi_api_key


**3. Run the Application
Start the Streamlit app using:**

                    streamlit run app.py

**Usage Guide**
**Step 1: Data Input**
    Upload a CSV file or connect to a Google Sheet by providing the URL and your service account JSON file
    
**Step 2: Define a Query**
    Enter a custom prompt (e.g., "Get me the contact details of {company}") to define what information to extract.
    
**Step 3: Perform Web Search**
    Click the "Process" button to perform a web search for each entity in the selected column.
    
**Step 4: Extract Information**
    The app uses OpenAI's API to extract relevant details from the search results.
    
**Step 5: View and Export Results**
    View the extracted data in a table format.
    Download the results as a CSV file for further use.


**Advanced Features**
**Google Sheets Output:**
    Automatically write extracted data back to the connected Google Sheet.
    
**Batch Processing:** Handle large datasets in smaller batches to avoid API rate limits.


Loom Video Walkthrough
Watch the Demo Video
                https://drive.google.com/file/d/17da6OQkaxeSxEYCGm0CPavGwq-AuINPm/view?usp=sharing

**Potential Enhancements**

**Advanced Query Templates:** Allow multiple fields to be extracted in a single prompt.

**Error Handling:** Add more robust error-handling mechanisms for failed API calls.

**Real-Time Monitoring:** Track the progress of large datasets.

**Acknowledgments**
    This project was developed as part of the BreakoutAI assessment. Special thanks to Breakout Consultancy Private Limited for the opportunity.

Contact: **kapil@breakoutinvesting.in**
