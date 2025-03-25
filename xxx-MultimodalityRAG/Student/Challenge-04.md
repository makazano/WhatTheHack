# Challenge 04 - RAG with Multimodality

[< Previous Challenge](./Challenge-03.md) - **[Home](../README.md)** - [Next Challenge >](./Challenge-05.md)

## Pre-requisites (Optional)

- Azure Speech Services to do voice search
- A Python environment with required libraries (`pip install -r requirements.txt`).
- `.env` file containing the required credentials.


## Introduction

Retrieval-Augmented Generation (RAG) is a powerful method for grounding Large Language Models (LLMs) with external knowledge sources. In this challenge, we extend RAG beyond textual data to include multimodal elements such as **images and voice search**.

Many businesses rely on **image-based data** for decision-making, such as magazine publishers analyzing cover image impact on sales. Additionally, enabling **voice-based queries** can enhance accessibility and improve user experience when interacting with AI-powered systems.

## Description

In this challenge, you will:
- Revisit the fundamentals of **RAG** and how it enhances LLM responses.
- Introduce **voice-based search** using speech-to-text capabilities.
- Enable a **chat-with-your-images** experience, allowing users to query image data effectively.
- Understand how **multimodal retrieval** combines different data types to generate relevant responses.

You will implement these capabilities by integrating **voice inputs, image embeddings, and AI Search** to power an advanced RAG pipeline.

## Success Criteria

To complete this challenge successfully, you should be able to:
- Demonstrate the ability to **retrieve relevant data using voice queries**.
- Show how **image-based RAG retrieval** improves contextual understanding.
- Validate multimodal RAG by combining structured and unstructured data.
- Build a simple Flask-based **visualization app** to display retrieval results.

## Learning Resources

- [Building a Multimodal RAG System](https://learn.microsoft.com/en-us/azure/search/cognitive-search-knowledge-store)
- [Azure AI Services for Speech-to-Text](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/speech-to-text)
- [Using Image Embeddings for Search](https://learn.microsoft.com/en-us/azure/search/vector-search-overview)

## Tips

*This section is optional and may be omitted.*

*Add tips and hints here to give students food for thought. Sample IoT tips:*

- IoTDevices can fail from a broken heart if they are not together with their thingamajig. Your device will display a broken heart emoji on its screen if this happens.
- An IoTDevice can have one or more thingamajigs attached which allow them to connect to multiple networks.

## Advanced Challenges (Optional)

Looking for an extra challenge? Try these:
- Improve the **speech-to-text pipeline** for better voice query accuracy.
- Implement **image-based responses** that leverage both textual and visual information.
- Evaluate the **performance of multimodal RAG** and explore optimization techniques.
