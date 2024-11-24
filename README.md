## README: Retrieval Augmented Generation (RAG) with Gemini and BigQuery/Vertex AI

This repository demonstrates how to build a RAG system using Gemini and two different vector stores:

* **BigQuery Vector Store:** Ideal for prototyping and batch retrieval due to its seamless integration with BigQuery and serverless nature.
* **Vertex AI Feature Store:** Optimized for low-latency retrieval in production-ready, user-facing applications.

### What is RAG?

RAG is a technique that combines the power of Large Language Models (LLMs) like Gemini with the ability to access and retrieve information from external knowledge sources. This allows LLMs to generate more accurate and informed responses by grounding them in relevant data.

### Why BigQuery and Vertex AI Feature Store?

* **BigQuery:**
    * **Scalability:** Handles massive datasets with ease.
    * **Cost-effectiveness:** Serverless architecture ensures you only pay for what you use.
    * **Integration:**  Works seamlessly with other Google Cloud services.

* **Vertex AI Feature Store:**
    * **Low Latency:** Optimized for online serving and fast retrieval.
    * **Flexibility:** Supports both manual and scheduled data synchronization.
    * **MLOps Integration:**  Integrates with Vertex AI's MLOps capabilities for model management and monitoring.

### Project Structure

This repository contains two examples:

1. **`bigquery_rag`:** Demonstrates RAG using Gemini and BigQuery Vector Store and Vertex AI Feature Store

Each example includes:

* **Data Ingestion:** Code to ingest and embed data into the respective vector store.
* **Retrieval:** Code to perform semantic search and retrieve relevant information.
* **Gemini Integration:** Code to use retrieved information as context for Gemini prompts.

### Getting Started

1. **Prerequisites:**
    * A Google Cloud Project with billing enabled.
    * Necessary APIs enabled (BigQuery, Vertex AI, etc.)
    * Authentication set up (e.g., using service accounts)

2. **Installation:**
    * Install the required packages:
    ```bash
    pip install google-cloud-aiplatform langchain-google-vertexai langchain-google-community[featurestore] google-cloud-bigquery
    ```

3. **Data Preparation:**
    * Prepare your data in a format suitable for ingestion (e.g., CSV, JSON).
    * If necessary, perform any preprocessing steps (e.g., cleaning, formatting).

4. **Run the Examples:**
    * Follow the instructions in the respective example directories

### Key Considerations

* **Embedding Model:** Choose an appropriate embedding model for your data and task.
* **Data Synchronization:** For Vertex AI Feature Store, determine the optimal synchronization strategy (manual or scheduled).
* **Performance Optimization:** Fine-tune parameters like the number of nearest neighbors to retrieve.
* **Monitoring and Evaluation:** Track key metrics like latency and accuracy to ensure optimal performance.

### Further Exploration

* **LangChain:** This repository uses LangChain, a framework for developing applications powered by language models. Explore LangChain's documentation and features to enhance your RAG system.
