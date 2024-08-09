## Overview
- We'll create a QA system that understands both text and images
- We'll build this system using Vertex AI

* **Focus on Fundamentals**: We will start with the essential design pattern of "Retrieval Augmented Generation" (RAG) – a way to find and use relevant info to answer questions.
* **Work with Text and Images**: We will expand RAG to handle both text and images found in PDF documents.
* **Use Vertex AI**: We will use Vertex AI Embeddings API and Vertex AI Gemini API.

By the end of this guide, we will have a solid foundation in building multimodal QA systems.

## Gemini
- Gemini is a family of GenAI models that is designed for multimodal use cases. 
- The Vertex AI Gemini API gives us access to:
    - Gemini 1.0 Pro Model
    - Gemini 1.0 Pro Vision Model
    - Gemini 1.5 Pro Model
    - Gemini 1.5 Flash Model

## Comparing text-based and mRAG
Multimodal RAG (mRAG) offers several advantages over text-based RAG:
1. **Enhanced knowledge access:** mRAG can access and process both textual and visual info, providing a richer and more comprehensive knowledge base for the LLM.
2. **Improved reasoning capabilities:** By incorporating visual cues, mRAG can make better informed inferences across different types of data modalities.

## How to implement RAG 
We will implement RAG using:
- Vertex AI Gemini API
- Vertex AI Embeddings API
  - [text embeddings](https://cloud.google.com/vertex-ai/docs/generative-ai/model-reference/text-embeddings)
  - [multimodal embeddings](https://cloud.google.com/vertex-ai/docs/generative-ai/model-reference/multimodal-embeddings), to build a doc search engine.

## Objectives
This notebook provides a guide to building a doc search engine using mRAG, step by step:
1. Extract and store metadata of docs containing both text and images, and generate embeddings the docs
2. Search the metadata with text queries to find similar text or images
3. Search the metadata with image queries to find similar images
4. Using a text query as input, search for contextual answers using both text and images

## Costs
- [Vertex AI pricing](https://cloud.google.com/vertex-ai/pricing)
- [Pricing Calculator](https://cloud.google.com/products/calculator) (generates a cost estimate)

