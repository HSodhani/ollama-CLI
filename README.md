# ollama CLI for LLAMA3 and Mistral

The ollama CLI tool is designed to facilitate the seamless integration and interaction with powerful Large Language Models (LLMs) such as LLAMA3 and Mistral, directly from your local machine. This tool allows users to run and interact with the models using simple command-line inputs, making it ideal for researchers, developers, and enthusiasts interested in exploring the capabilities of state-of-the-art language models.

# Features
Easy Model Management: Download and switch between LLAMA3 and Mistral models with a single command.
Local API: Set up a local server to interact with the models via a RESTful API.
Secure and Private: All processing is done locally on your machine, ensuring data privacy and security.
Getting Started
Prerequisites
Before you begin, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package installer)

# Installation
To install the ollama CLI, run the following command in your terminal:


```pip install ollama-cli```

# Download and Run a Model:

To download and start a model server, use the following command:

```ollama run <model_name>```

Replace ```<model_name>``` with ```llama3``` or ```mistral``` to use the respective model.

# Interact with the Model:

After the model server is running, you can ask questions or send prompts using curl. For example:

``` 
curl -X POST -H "Content-Type: application/json" -d '{
    "model": "llama3",
    "prompt": "Why is the sky blue?",
    "stream": false
}' "http://localhost:11434/api/generate"
```

This command sends a question to the LLAMA3 model running locally on your machine.

# API Reference
The ollama CLI exposes a RESTful API to interact with the models. The main endpoint is:


```POST /api/generate```

# Request Parameters
- *model*: The model you want to interact with (llama3 or mistral).
- *prompt*: The text prompt or question you want to send to the model.
- *stream*: Whether the response should be streamed (set to false for a single response).

# Response
The API responds with the generated text from the model, based on the input prompt.

# Examples
Here are more examples of how you can use the ollama CLI to interact with different models:


Asking Mistral a question
```
curl -X POST -H "Content-Type: application/json" -d '{
    "model": "mistral",
    "prompt": "What are the implications of quantum computing?",
    "stream": false
}' "http://localhost:11434/api/generate"
```
# Youtube Link
https://youtu.be/_qC5K3MLC5E

# Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

- Fork the Project
- Create your Feature Branch (git checkout -b feature/AmazingFeature)
- Commit your Changes (git commit -m 'Add some AmazingFeature')
- Push to the Branch (git push origin feature/AmazingFeature)
- Open a Pull Request
