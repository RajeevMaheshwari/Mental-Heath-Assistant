# LLM Mental Health Assistant 🧠

This application is designed to facilitate mental health support through interactive question-and-answer sessions using an LLM-based chatbot. Built with **Pathway's LLM-App** for natural language understanding and **Streamlit** for the user interface, it provides users with personalized responses for mental health queries, offering emotional support and mental wellness tips.

## Video Demo of the APP 🎥

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/US7dEV-rPe0/0.jpg)](https://www.youtube.com/watch?v=US7dEV-rPe0)

Video Link: https://youtu.be/US7dEV-rPe0


## Description 📝

The **LLM Mental Health Assistant** is based on the modification of an existing LLM-App and iterates upon it to create a supportive environment for users seeking mental health advice or emotional support. 

By leveraging Pathway’s LLM capabilities, the app can engage in meaningful conversations, provide mental health guidance, and recommend self-care practices. The core strength lies in its ability to perform real-time text-based interactions that are empathetic and supportive, making it ideal for users who need guidance or someone to "talk to."

Pathway’s LLM component enhances the experience by efficiently processing user inputs, generating context-aware responses, and retrieving helpful information without the need for a vector database. **Streamlit** offers a smooth, user-friendly experience, making it easy to interact with the assistant.

The app also integrates with the **Gemini API**, offering enhanced NLP tasks such as summarization and response aggregation to deliver more cohesive answers.

## Features 🎁

- Interactive mental health support chatbot
- Empathetic and personalized responses
- Mental wellness tips and advice
- User-friendly interface powered by Streamlit
- Docker-based deployment for easy setup and scalability
- Integration with Gemini API for LLM tasks

## Summary of Available Endpoints 📊

This app exposes six core endpoints, divided into two categories: document indexing and LLM-based response generation.

### Document Indexing Capabilities
- `/v1/retrieve` – Perform similarity search for relevant mental health content.
- `/v1/statistics` – Get basic stats about the app’s document indexer health.
- `/v1/pw_list_documents` – Retrieve metadata of all files currently processed by the indexer.

### LLM and RAG Capabilities
- `/v1/pw_ai_answer` – Ask mental health-related questions and get responses from the LLM.
- `/v1/pw_ai_summary` – Summarize key mental health topics or answers.
- `/v1/pw_ai_aggregate_responses` – Aggregate responses from different sources for a comprehensive answer.

## Prerequisites 📋

Before running the app, ensure you have the following installed:

- Python 3.x
- Git
- Docker

## Setup with Docker 💻

1. Clone the repository:

  ```bash
  git clone https://github.com/RajeevMaheshwari/Mental-Heath-Assistant.git
  cd Mental-Heath-Assistant
  ```

2. Generate a key from [GEMINI_API_KEY](https://aistudio.google.com/app/apikey) and add it to a .env file in project directory:

  ```
  GEMINI_API_KEY=<YOUR_API_KEY>
  ```

3. Build and run the Docker Image:

  ```bash
  docker compose up
  ```
Note: Build can take upto 20-30 minutes. Please wait for it to finish.

4. Access the app in your browser at `http://localhost:8501`.

![App Preview](image2.png)

5. To close the program:

  ```bash
  docker compose down
  ```

## Setup Locally 💻

1. Clone the repository:

  ```bash
  git clone https://github.com/RajeevMaheshwari/Mental-Heath-Assistant.git
  cd Mental-Heath-Assistant
  ```

2. Generate a key from [GEMINI_API_KEY](https://aistudio.google.com/app/apikey) and add it to a .env file in project directory:

  ```
  GEMINI_API_KEY=<YOUR_API_KEY>
  ```

3. Create a venv and install all dependencies
  ```
  python3 -m venv venv
  source venv/bin/activate
  pip install -r requirements.txt
  pip install -r ui/requirements.txt
  pip install "numpy<2.0"
  python3 nltk_dependencies.py
  ```

4. Run The UI and backend separately
  For streamlit UI run
  ```
  streamlit run ui/server.py --server.port=8501 --server.address=0.0.0.0
  ```
  And for backend run
  ```
  python3 app.py
  ```



5. Access the app in your browser at `http://localhost:8501`.

![App Preview](image2.png)


## Future Improvements 🚀

- Add ability to fetch real-time mental health resources
- Incorporate visual inputs for enhanced user interaction
- Advanced emotional sentiment analysis
- Improve summarization and aggregation of multiple responses

Made with love 💕by Rajeev