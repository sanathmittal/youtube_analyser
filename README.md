# YouTube Analyser

YouTube Analyser is a fun, learning-focused project that leverages the Google YouTube API to fetch a user's liked videos, subscriptions, and uploads. It then uses OpenAI embeddings to store this data in a ChromaDB vector store and processes it with GPT to generate humorous comments and assign a final score to the YouTube account.

> **Note:** This project is a **learning project** intended for educational and experimental purposes only. It is not designed for professional use.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Frontend](#frontend)
- [Contributing](#contributing)
- [License](#license)

## Overview

The core idea behind YouTube Analyser is to provide a light-hearted, humorous analysis of a user's YouTube habits. By fetching data using the YouTube API, embedding the data with OpenAI embeddings, and storing it in a ChromaDB vector store, the project processes the data with GPT to generate witty observations and assign a final score. This project is built as a learning exercise and is not intended for production environments.

## Features

- **Data Fetching:** Retrieves a user's liked videos, subscriptions, and uploads using the Google YouTube API.
- **Embedding & Storage:** Uses OpenAI embeddings to convert textual data into vectors, stored in ChromaDB.
- **Humorous Analysis:** Processes the data with GPT to generate five humorous comments about the user's YouTube habits.
- **Scoring System:** Assigns a final score out of 100 based on uploads, subscriptions, liked videos, and content matching.
- **Gradio Frontend:** Provides an interactive web-based frontend for user authentication and analysis display.

## Dependencies

The project uses the following libraries and modules:

- `google_auth_oauthlib.flow` (InstalledAppFlow)
- `googleapiclient.discovery` (build)
- `google.oauth2.credentials` (Credentials)
- `google.auth`
- `openai`
- `chromadb`
- `python-dotenv` (for `.env` support)
- `langchain.text_splitter` (CharacterTextSplitter)
- `gradio`
- `time`
- `json`
- `os`

Install the dependencies via pip:
```bash
pip install google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client openai chromadb python-dotenv langchain gradio
```

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/YouTube-Analyser.git
   cd YouTube-Analyser
   ```

2. **Set up your environment:**
   - (Optional) Create a virtual environment:
     ```bash
     python -m venv venv
     source venv/bin/activate  # On Windows use: venv\Scripts\activate
     ```
   - Install the dependencies:
     ```bash
     pip install -r requirements.txt
     ```
     *(Alternatively, manually install the libraries as shown above.)*

3. **Configure Environment Variables:**
   - Create a `.env` file in the project root.
   - Add your OpenAI API key:
     ```
     OPENAI_API_KEY=your_openai_api_key_here
     ```

4. **Google API Setup:**
   - Ensure you have a `credentials.json` file in the project root, configured for the YouTube Data API.
   - Make sure your OAuth consent screen and redirect URIs are properly configured in the Google Cloud Console.

## Usage

Since the code is provided in a Jupyter Notebook (and also integrated with Gradio for a frontend), follow these steps:

1. **Open the Notebook:**
   - Launch Jupyter Lab or Jupyter Notebook in your project directory.
   - Open the Notebook file containing the code.

2. **Run the Notebook Cells:**
   - The Notebook includes functions for user authentication, data fetching, analysis, and a Gradio-based frontend.
   - Click the **"Login with YouTube"** button to authenticate via your browser.
   - Once authenticated, click the **"Analyze My Account"** button to see the humorous analysis and final score.

## Frontend

The project uses **Gradio** to create an interactive web interface:
- **Login Button:** Initiates Google OAuth for YouTube account login. The authentication flow opens in your default browser (configured to use Google Chrome).
- **Analyze Button:** Once authenticated, this button fetches your YouTube data and processes it.
- **Results Display:** The analysis results, including humorous comments and the final score, are displayed sequentially on the Gradio interface.

## Contributing

Contributions are welcome! Since this is a learning project, feedback, bug fixes, and improvements are encouraged. To contribute:
1. Fork the repository.
2. Create a new branch for your changes.
3. Commit your changes and open a pull request.
4. Ensure your changes are well documented.

## License

This project does not currently have a license.

---

Feel free to modify or expand upon this README to suit your needs. Enjoy exploring and learning with YouTube Analyser!
