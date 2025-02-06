# What The Hack - MultimodalityRAG

## Introduction

The Multimodality with RAG What The Hack is the next stepping stone after you've mastered the RAG Pattern. There is plenty of information regarding "Chat with your Data", but most of the time it is just the RAG Pattern over PDF. The most common scenario is going over a set of documents and ask questions about them. For example, if you have documentation about your company-specific insurance plan, you can build a chat-bot experience that enables you to ask relevant questions.
In this scenario, we want to take it a step beyond and not only dealing with PDF documents. We want to introduce the concept of multimodality by enabling a user to ask a question using Speech-to-text and retrieve an answer that goes beyond a PDF. We want to be able to ask questions on images as well as SQL-like data. Imagine you want to ask questions about the performance of a specific asset and the information is on an image. We can ask something about the image and pair it with structured data to respond the query.

## Learning Objectives

In this hack you will be solving the common business problem that companies who rely on image data have. The magazine industry for example relies on asking questions about specific covers and how the different images may influence sales.

1. Master the art of the RAG Pattern while enhancing with multimodality.
2. Efficiently query structured and unstructure data via voice commands.
3. Build your own visualization app with Flask.
4. Build your own visualization app with Flask.

## Challenges

- Challenge 00: **[Prerequisites - Ready, Set, GO!](Student/Challenge-00.md)**
	 - Prepare your workstation to work with Azure.
- Challenge 01: **[Architecture Overview and Data Exploration](Student/Challenge-01.md)**
	 - Get ready to dive deep into the Architecture for this WTH.
	 - Understand the core components of the architecture.
	 - You will make an Exploratory Data Analysis of the dummy data that can be found on the /resources folder.
- Challenge 02: **[Data Processing](Student/Challenge-02.md)**
	 - Create SQL table and insert Sales data.
	 - Explore and upload the image files to Azure Data Lake Storage gen2.
	 - Explore the speech-to-text API.
- Challenge 03: **[Indexing with AI Search](Student/Challenge-03.md)**
	 - Integrated Vectorization for images
	 - Learn about indexing strategies and types of search (semantic, keyword, hybrid, etc.)
- Challenge 04: **[RAG with multimodality](Student/Challenge-04.md)**
	 - Revisit RAG Fundamentals
	 - Adding a layer of complexity with Voice search
	 - Chat with your Images
- Challenge 05: **[Visualization Layer](Student/Challenge-05.md)**
	 - Build a Flask Web App that showcases query results from both structured and unstructured data combined.
- Challenge 06: **[Title of Challenge](Student/Challenge-06.md)**
	 - Description of challenge
- Challenge 07: **[Title of Challenge](Student/Challenge-07.md)**
	 - Description of challenge
- Challenge 08: **[Title of Challenge](Student/Challenge-08.md)**
	 - Description of challenge
- Challenge 09: **[Title of Challenge](Student/Challenge-09.md)**
	 - Description of challenge

## Prerequisites

- Your own Azure subscription with Owner access
- Visual Studio Code
- Azure CLI
- Access to deploy Azure OpenAI Models (embeddings and GPT)


## Contributors

- Casey Kriutzfield
- David Florez Fernandez
- Esthela Gallardo
- Manasa Ramalinga
- Oscar Shimabukuro
