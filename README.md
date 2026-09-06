# College Knowledge Assistant

## Problem Statement

Students frequently ask repetitive questions related to college policies and rules. Finding the correct information from institutional documents can take time.

The College Knowledge Assistant provides answers to college-related questions using a Retrieval-Augmented Generation (RAG) approach. It retrieves relevant information from the college knowledge base and uses an OpenAI language model to generate a grounded response.

## Project Objective

The objective of this project is to build an AI-powered college assistant that can answer questions related to:

- Academic information
- Attendance policies
- Placement policies
- Hostel rules

The system is designed to answer using information retrieved from the college knowledge base rather than relying only on the language model's general knowledge.

## Architecture

The overall flow is:

Student Query  
↓  
AI Agent  
↓  
RAG / Vector Store  
↓  
OpenAI LLM  
↓  
Response with Sources

### RAG Pipeline

College Documents  
↓  
Data Loader  
↓  
OpenAI Embeddings  
↓  
Vector Store  
↓  
Relevant Context  
↓  
AI Agent / LLM  
↓  
Answer

## Key Features

- AI-powered college question answering
- Retrieval-Augmented Generation (RAG)
- Vector-based semantic search
- OpenAI embeddings
- OpenAI language model
- AI Agent for processing queries
- Conversation memory
- Webhook endpoint for receiving queries
- Knowledge-base-grounded responses
- Fallback response when information is not found

## Technologies Used

- n8n
- OpenAI
- RAG
- Vector Store
- OpenAI Embeddings
- AI Agent
- Conversation Memory
- Webhook

## How the System Works

1. A student submits a college-related question.
2. The AI Agent receives the question.
3. The agent searches the connected college knowledge base using the student's question.
4. Relevant document information is retrieved from the vector store.
5. The retrieved context is provided to the OpenAI language model.
6. The model generates an answer based on the retrieved college information.
7. If the required information cannot be found in the knowledge base, the assistant informs the user instead of generating an unsupported answer.

## Prompt Design

The AI Agent is instructed to:

- Act as a College Knowledge Assistant.
- Search the college knowledge base before answering college-related questions.
- Use the student's question as the search query.
- Avoid answering college-specific questions from its own knowledge.
- Generate the answer using retrieved college documents.
- Inform the user when the required information is not available in the knowledge base.

## Conversation Memory

The workflow includes conversation memory to maintain context between messages and support better follow-up interactions.

## Evaluation

The system can be evaluated using questions from different college-related categories such as:

| Category | Example Question |
|---|---|
| Academic | What are the academic requirements? |
| Attendance | What percentage of attendance is required for the final examination? |
| Placement | What are the placement eligibility requirements? |
| Hostel | What are the hostel rules? |
| Unknown | What is the admission process? |

The evaluation focuses on whether the assistant retrieves relevant information and provides answers grounded in the college knowledge base.

## Challenges

- Preparing institutional documents for retrieval
- Obtaining relevant document chunks from the vector store
- Designing prompts that encourage grounded answers
- Handling questions for which information is not available
- Maintaining conversation context

## Future Enhancements

- Add more institutional documents
- Improve query routing between Academic, Placement and Hostel domains
- Add a dedicated frontend for students
- Improve source citation and document references
- Add authentication for students and staff
- Use a production-grade vector database
- Expand the evaluation dataset
- Improve retrieval accuracy using advanced retrieval and reranking techniques

## Project Files

- `My workflow 3.json` — n8n workflow export
- `College Knowledge Assistant Workflow.png` — architecture/workflow diagram
- `README.md` — project documentation

## Demo

A 3–5 minute demonstration video will show the workflow, RAG retrieval process, and question-answering capability.

## License

This project is developed for academic/educational purposes.
