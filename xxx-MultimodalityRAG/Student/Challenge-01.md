# Challenge 01 - Architecture Overview & Data Exploration

[< Previous Challenge](./Challenge-00.md) - **[Home](../README.md)** - [Next Challenge >](./Challenge-02.md)

## Pre-requisites

If you have any prerequisite steps (e.g., setting up your Azure Subscription or Resource Groups), please finalize it before starting with this new challenge.

---

## Introduction

In this first challenge, you will outline a high-level solution to build a multimodal Retrieval-Augmented Generation (RAG) pipeline with data coming from two sources:

1. **Magazine Images**: Scanned or digital pages containing text and visual elements.  
2. **Sales Data**: A relational data store with magazine IDs and sales metrics.

Start thinking about a common flow for your solution:

1. **Data Storage** of images and relational data.  
2. **AI Pipeline** that can:
   - Extract or generate vector embeddings for images (via a vision service/API).
   - Combine or correlate these embeddings with structured sales data.
   - Expose data for indexing.  
3. **Search & Retrieval**: An index or search service to efficiently retrieve relevant results based on queries.  
4. **Multimodal GPT** (or similar LLM) to process combined data (images + sales) and provide responses.  
5. **Web/Chat Interface** for end-user interaction with the system.


## Description

In this challenge, you are asked to:

- **Design** a high-level Azure-based solution that ingests and processes your images and relational data. First try to think abstractly, **not** need to specify exact Azure services or product names—just outline the functional components and how they might interact. Then make the exrcise of thinking about Azure tools to do those functions. 
  
- **Explore** the data:
  - Understand how the magazine images can be converted into a searchable format (e.g., embedding).
  - Get familiar with the columns in the relational sales data (e.g., product IDs, date ranges, metrics) and hypothesize how it might relate to the magazine content.

You are essentially laying the groundwork for a RAG application capable of answering queries with references to both textual and visual content from the magazines, as well as numeric or categorical details from the sales dataset.

**Key Considerations**:
- How would you **vectorize** or **index** your magazine images for retrieval?
- How does the **sales data** align with or link back to the images? (e.g., by product ID references or other identifiers)
- Where do you store these embeddings and structured data to make them readily searchable by your LLM?

---

## Success Criteria

To complete this challenge successfully, you should be able to:

- **Present** a high-level diagram or description of your intended architecture showing:
  - Data ingestion from images and sales data.
  - A pipeline or process for extracting or generating embeddings from the images.
  - A mechanism for combining or correlating image data with relational data.
  - A search/indexing service for retrieval.
  - An LLM or “multimodal” AI component for final query-answer generation.
  - A user interface or endpoint for queries and responses.
- **Describe** how you intend to handle:
  - Processing the images.
  - Basic linking between the images and the sales data table (e.g., referencing the same ID).
- **Explain** any initial thoughts on how you’d scale or update the architecture as more images or sales data are added.

---

## Learning Resources

Below are some resources that may help you conceptualize your solution:

- [Intro to Retrieval-Augmented Generation on Azure](https://learn.microsoft.com/azure/cognitive-services/openai/concepts/use-case-qna)
- [Overview of Vision AI Services](https://learn.microsoft.com/azure/applied-ai-services)
- [Azure Cognitive Search for AI-powered indexing](https://learn.microsoft.com/azure/search/search-what-is-azure-search)
- [Designing Enterprise Data & AI Solutions](https://learn.microsoft.com/learn/paths/azure-data-ai/)

---

## Tips (Optional)

- Consider using a **two-step** process: one for image processing (embedding) and one for text-based search/indexing.
- Keep your architecture modular, so you can swap out components if you discover different tools or services are a better fit.
- Think about how your solution might look if you added real-time data streams or more frequent image updates.

---

## Advanced Challenges (Optional)

Ready for more?

*- **Propose a method** for near real-time ingestion of new magazine pages or updated sales data without significant downtime.
- **Outline** how you might integrate advanced AI capabilities like image captioning, classification, or even brand/logo detection to enrich the data linked to the sales table.
- **Consider** adding a SQL database to keep the sales data and how that could be connected to the overall artchitecture.

