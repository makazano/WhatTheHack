# Challenge 01 - Multimodal RAG Architecture & Data Exploration - Coach's Guide

[< Previous Solution](./Solution-00.md) - **[Home](./README.md)** - [Next Solution >](./Solution-02.md)

## Notes & Guidance

In this challenge, the participants are asked to conceptualize a multimodal RAG pipeline using magazine images (unstructured data) and sales data (structured data) in Azure. The diagram below highlights a typical approach for combining a vision service, indexing, a large language model, and a front-end chat interface. Here’s how you can guide them through the solution and what you should look for when validating their approach:

- They should be thinking about using OCR or image embedding to handle the magazine images.  
- They need to consider how to join or correlate the extracted image data with the relational sales table.  
- They must identify or at least propose an indexing strategy that allows LLMs to retrieve relevant data from both images and structured tables.

Below is a reference architecture that your students might propose or approximate. Encourage them to fill in the service details as they learn more about Azure’s offerings:

![Reference Architecture: Shows a typical flow involving image storage, a vision API, sales dataset, an indexing service, a multimodal model, and a web-based chat interface.](./Solutions/architecture.png)

1. **Storage**  
   - A place to hold the raw images (e.g., Azure Blob Storage).  
   - A relational store (e.g., Azure SQL Database) to keep sales data.  

2. **AI Foundry**  
   - A pipeline (or multiple pipelines) that uses a Vision API (like Florence or other Computer Vision) to extract embeddings or text from the images.  
   - Processes or merges these embeddings with the sales dataset so they can be indexed together.

3. **Indexing**  
   - A search service (e.g., Azure Cognitive Search) for storing vector embeddings and structured data fields to enable hybrid search (text + embeddings).  

4. **Multimodal Model**  
   - A GPT-like model capable of handling both text and image contexts.  
   - Communicates with the index to fetch relevant data before generating an answer.

5. **Chat/Front-End**  
   - A user interface that can capture queries and display responses, possibly using a web UI or chat client.

---

 Ensure they highlight how images relate to the sales data by using a shared identifier (e.g.,  ID).  
- Have them provide some detail on any data transformation steps (e.g., normalizing text, generating embeddings) needed to effectively combine these different data types.  
- Look for explicit mention of how or where they plan to store embeddings (in the search index, separate vector database, or a custom store).

---

In more detail:

- The pipeline typically begins by **uploading the images** to Azure Blob Storage.
  - Then a **Vision API** is called to either perform OCR or generate embeddings (or both).
    - Some participants might choose a custom approach that uses a pretrained model for embedding generation.

- **Sales data** could be stored in an **Azure SQL Database** (or any relational DB).  
  - They should identify how they’d unify or correlate the structured data with the image-based info—such as by linking product IDs or references.

- **Indexing** often involves **Azure AI Search**:
  - Encouraging them to combine textual fields from the sales table with extracted metadata or embeddings from the images in a single index can be optimal for a retrieval-based pipeline.

- For the **LLM**, the group may propose using **Azure OpenAI GPT-4** in a multimodal capacity:
  - The LLM receives an initial user query, calls out to the index (via semantic search, vector search, or a combination) for the relevant snippets/images/structured data, and then composes the final response.

- The final step is a **Chat Web** interface:
  - This can be as simple as a web page with text input and output or a more elaborate chat framework.
  - They might also add features like chat history or citations referencing the source of each piece of retrieved information.

---

- Remind participants to address any **scaling considerations**:
  - They should discuss how they'd handle an increase in images or queries.
  - Potential usage of additional caching layers or more robust hosting for the indexing service.

- They may also mention possible **real-time updates** to the data or model.  

- Finally, look out for any mention of **data governance or security**, especially since images may contain sensitive info or the sales data might be confidential.
