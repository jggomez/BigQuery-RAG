## Retrieval Augmented Generation (RAG) with Gemini and BigQuery/Vertex AI

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


Made with ❤ by  [jggomez](https://devhack.co).

[![Twitter Badge](https://img.shields.io/badge/-@jggomezt-1ca0f1?style=flat-square&labelColor=1ca0f1&logo=twitter&logoColor=white&link=https://twitter.com/jggomezt)](https://twitter.com/jggomezt)
[![Linkedin Badge](https://img.shields.io/badge/-jggomezt-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/jggomezt/)](https://www.linkedin.com/in/jggomezt/)
[![Medium Badge](https://img.shields.io/badge/-@jggomezt-03a57a?style=flat-square&labelColor=000000&logo=Medium&link=https://medium.com/@jggomezt)](https://medium.com/@jggomezt)

## License

    Copyright 2025 Juan Guillermo Gómez

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
