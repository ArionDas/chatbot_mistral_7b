# Mistral 7B
Mistral 7B is a 7.3B parameter model that:

Outperforms Llama 2 13B on all benchmarks
Outperforms Llama 1 34B on many benchmarks
Approaches CodeLlama 7B performance on code while remaining good at English tasks
Uses Grouped-query attention (GQA) for faster inference
Uses Sliding Window Attention (SWA) to handle longer sequences at a lower cost

Download it here from Huggingface : https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF/tree/main

Mistral 7B on being compared to the Llama 2 family:

![image](https://github.com/ArionDas/chatbot_mistral_7b/assets/117722561/2b273eff-694c-4b39-ad84-9a2886b28275)

An interesting metric to compare how models fare in the cost/performance plane is to compute “equivalent model sizes”. On reasoning, comprehension, and STEM reasoning (MMLU), Mistral 7B performs equivalently to Llama 2 that despite being one-third of its size.

![image](https://github.com/ArionDas/chatbot_mistral_7b/assets/117722561/6c46ad94-bb96-4fa1-bdf7-865bd28fa438)

For more details on how to finetune the model according to it's requirements : https://mistral.ai/news/announcing-mistral-7b/
Credit to Mistral.AI for the above facts.

# Steps Followed
1) Creating Python Environment, activating it
2) Installing and importing required libraries
3) Setting up Github Repository
4) Loading the PDF files
5) Splitting the text data into text chunks using a TextSplitter
6) Downloading the embeddings (I used Huggingface sentence transformers as its opensource) (To know more about text embeddings : https://medium.com/gopenai/text-embeddings-fa6e265312ce)
7) Storing the embeddings in a Vector Database (I used FAISS as Chromadb keeps updating it's docs, so this would go obsolete) (To know more about vector databases : https://medium.com/@ariondasad/vector-databases-777606ea437f)
8) Import the model and modify it according to requirements
9) Using a query retriever, we will generate a prompt for our query
10) Finally, creating a streamlit application as a proof of concept for our model.
