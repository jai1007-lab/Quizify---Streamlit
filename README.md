# Quizify

## Overview
Quizify is an interactive application designed to assist students in revising their study material by generating quizzes based on uploaded content. The application leverages Google Cloud's Vertex AI, Streamlit, and various other libraries to process documents, generate quiz questions, and manage quizzes effectively.

## Key Features
- **Document Ingestion**: Upload PDF files containing study material.
- **Text Embeddings**: Use Google Cloud's Vertex AI to embed text for quiz generation.
- **Quiz Generation**: Automatically generate quiz questions based on the uploaded material.
- **Interactive Quiz Management**: Navigate through quiz questions, select answers, and receive immediate feedback.

## Installation
### Prerequisites
Before you begin, ensure you have the following installed on your system:

- Python 3.6 or higher
- Google Cloud SDK (for authentication)
- Streamlit
  
### Step-by-Step Installation Guide
**Clone the Repository**

Start by cloning the repository to your local machine. Use the following command:

```bash
git clone https://github.com/your-username/quizify.git
cd quizify
```

**Set Up a Virtual Environment** (Optional but recommended)

It's a good practice to create a virtual environment for your Python projects. This keeps your project dependencies isolated. If you have virtualenv installed, create a new environment with:

```bash
virtualenv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
**Install Dependencies**
Inside the virtual environment, install all necessary dependencies by running:

```bash
pip install -r requirements.txt
```

**Authentication with Google Cloud**

Ensure you have a Google Cloud project set up with the Vertex AI API enabled. Authenticate using the following command, replacing path/to/your-service-account-key.json with the path to your service account key file:

```bash
gcloud auth activate-service-account --key-file=path/to/your-service-account-key.json
```
## Running the Application
After the installation, you can start the Streamlit application by navigating to the project directory and running:

```bash
streamlit run main.py
```
### Accessing the Application

With the server running, you can access the application at **http://localhost:8501.**

## Project Structure
- **tasks/**: Contains individual task scripts for processing documents, generating embeddings, creating the Chroma collection, and managing quizzes.
- **main.py**: The main entry point for running the Streamlit application.
- **requirements.txt**: Lists all the dependencies required for the project.
- **gitignore**: Please make sure you add your authentication.json file to gitignore to prevent it from accidentally getting pushed to the public GIT repo.
  
### Usage
- **Document Ingestion**:
Upload PDF files containing your study material. The application will process these documents and prepare them for quiz generation.

- **Quiz Generation**:
Specify the topic and the number of questions to generate. The application will use the embedded text to create relevant quiz questions.

- **Quiz Management**:
Navigate through the generated quiz questions, select answers, and receive immediate feedback on your responses.

### Contributing

If you wish to contribute to this project, please fork the repository and submit a pull request.
