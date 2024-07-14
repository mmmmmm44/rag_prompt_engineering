# Mastering RAG: Step-by-Step Instructions to Create a Powerful RAG System

This is the folder for the medium article "Mastering RAG: Step-by-Step Instructions to Create a Powerful RAG System".

## Usage
1. Follow the article's instruction to install required packages.

    In particular, install pytorch (CPU only or GPU support), transformer, sentence-transformer, Langchain and Chroma to your Python virtual environment.

    ```
    # install pytorch with optional GPU support before installing transformers and sentence-transformers
    pip install transformers
    pip install -U sentence-transformers

    pip install langchain
    pip install chromadb
    ```

    Then install Docker to your computer and pull the Ollama offical Docker image. Create a container and install Llama2-7B-chat using Ollama inside the container.

    ```
    # download the quantized Llama2:7B model
    ollama pull llama2:7b-chat-q4_K_M

    # list all models available in your container to check whether the pull is successful
    ollama list
    ```

2. The code is in `rag_introduction.ipynb`

## Folder Structure

|Folder|Description|
|---|---|
|cyberpunk_2077_phantom_liberty|Contains 5 critic reviews of the game Cyberpunk2077 with source included|

|File|Description|
|---|---|
|rag_introduction.ipynb|The code of the article|