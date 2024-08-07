# Gen-AI-PDF-chatbot

This project is a Streamlit application that allows users to upload PDF files and ask questions based on the content of these PDFs. The application uses Google Generative AI models to process the text and provide answers to user queries. The solution employs FAISS for efficient similarity search within the text chunks extracted from the PDF documents.

## Features

- Upload multiple PDF files
- Extract and process text from PDF files
- Ask questions and get answers based on the uploaded PDFs
- Uses Google Generative AI models for text embedding and question answering
- Efficient similarity search using FAISS
- Streamlit interface for ease of use

## Requirements

- Python 3.7 or higher
- Streamlit
- PyPDF2
- Langchain
- FAISS
- Google Generative AI

## Installation

1. Clone the repository:

```sh
git clone https://github.com/SohilThakur/Gen-AI-PDF-chatbot
cd Gen-AI-PDF-chatbot
```

2. Create a virtual environment and activate it:

```sh
python -m venv env
source venv/bin/activate # On Windows, use `venv\Scripts\activate`
```

3. Install the required packages:

```sh
pip install -r requirements.txt
```

4. Set up your Google API key:

- Create a `.env` file in the root directory of the project.
- Add your Google API key to the `.env` file:

```
GOOGLE_API_KEY=your-google-api-key
```

## Usage

1. Run the Streamlit application:

```sh
streamlit run app.py
```

2. Open your web browser and go to the URL provided by Streamlit (typically `http://localhost:8501`).

3. Upload your PDF files using the file uploader in the sidebar.

4. Click on the "Submit & Process" button to process the PDFs.

5. Ask your questions in the text input field and get answers based on the content of the uploaded PDFs.

## Code Overview

### `app.py`

This is the main script for the Streamlit application. It includes the following functions:

- `get_pdf_text(pdf_docs)`: Extracts text from the uploaded PDF files.
- `get_text_chunks(text)`: Splits the extracted text into manageable chunks.
- `get_vector_store(text_chunks)`: Creates a FAISS vector store from the text chunks using embeddings from Google Generative AI.
- `get_conversational_chain()`: Sets up the question-answering chain using Google Generative AI.
- `user_input(user_question)`: Handles user input and retrieves the answer based on the processed PDF content.
- `main()`: The main function that sets up the Streamlit interface and handles user interactions.



## Acknowledgements

This project uses the following open-source libraries and APIs:

- [Streamlit](https://streamlit.io/)
- [PyPDF2](https://pypi.org/project/PyPDF2/)
- [Langchain](https://github.com/hwchase17/langchain)
- [FAISS](https://github.com/facebookresearch/faiss)
- [Google Generative AI](https://cloud.google.com/vertex-ai)

