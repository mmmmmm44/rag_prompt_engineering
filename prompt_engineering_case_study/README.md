# Prototyping a LLM supported component: A case study

This is the folder for the medium article "Prototyping a LLM supported component: A case study".

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

2. Run the jupyter notebooks according to different sections in the article.

## Folder Structure

|Folder|Description|
|---|---|
|reviews|Stores reviews in text files|

|File|Description|
|---|---|
|prototype_v0.ipynb|Technical demo displaying the capability of LLM with RAG.|
|prototype_v1.ipynb|1st iteration of the component. Breaking the task into two prompts and using different prompting techniques to improve the prompt for better results.|
|prototype_v1_short.ipynb|1st iteration of the component. Tested with a short review instead of a long one|
|prototype_v2.ipynb|2nd iteration of the component. Prompting for more aspects with a long review.|
|prototype_v3.ipynb|3rd iteration of the component. Optimizing the prompt calling to save token usages.|
|prototype_v4.ipynb|4th iteration of the component. Combining two prompts to a single one and further instruct the LLM to produce JSON output.|