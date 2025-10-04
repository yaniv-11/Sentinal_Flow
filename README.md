# Sentinal_Flow


Overview
This project provides an automated workflow to analyze customer reviews, determine sentiment (positive/negative), diagnose negative feedback, and generate personalized, empathetic responses using generative AI models (Gemini 2.5 Flash). It is designed for support automation, helping teams quickly triage user feedback and streamline the response process.

Features
Loads and processes individual text reviews.

Uses Google GenAI (Gemini) to classify review sentiment as positive or negative.

For positive reviews: Generates warm, thank-you responses and requests for further feedback.

For negative reviews: Diagnoses the issue, tone, and urgency using AI, then crafts empathetic, resolution-focused messages.

Visualizes the review handling workflow as a graph using the LangGraph library.

Workflow
<img width="390" height="432" alt="image" src="https://github.com/user-attachments/assets/8c1a754c-ba33-4b85-a3df-9aded58aa33e" />

Review Input: Enter or load a review string.

Sentiment Analysis: AI predicts 'positive' or 'negative' sentiment.

If positive, a thank-you and feedback request message is generated.

If negative, the AI diagnoses the issue and produces a customized resolution message.

Output: Displays the sentiment, diagnosis (if negative), and the generated response.

Technologies & Libraries
Python 3.9+

LangGraph (langgraph.graph)

Google GenAI API (genai, Gemini 2.5 Flash model)

Pydantic for data model validation

dotenv for environment/config loading

Jupyter Notebook for code development and demonstration

Usage
Setup:

Install required packages: pip install google-genai langgraph pydantic python-dotenv

Obtain and set your Google GenAI API key in a .env file.

Run:

Open review_analysis.ipynb in Jupyter Notebook.

Execute all cells step by step. Enter or modify review text in the appropriate cell.

Example:

Enter a review like I've been trying to log in for over an hour now, and the app keeps freezing...

The notebook will detect sentiment, diagnose the issue ("Technical Bug, Frustrated, Critical"), and output a helpful, personalized support message.
