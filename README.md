# Ollama MCP Bridge 🌉

Welcome to the **Ollama MCP Bridge** repository! This project serves as a bridge API service that connects Ollama with Model Context Protocol (MCP) servers. This integration allows for seamless communication between different AI models and applications, enhancing the capabilities of both platforms.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-blue.svg)](https://github.com/Reti0/ollama-mcp-bridge/releases)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The **Ollama MCP Bridge** provides a robust solution for developers looking to integrate AI models with the Model Context Protocol. By using this bridge, you can easily manage and deploy AI models locally or in the cloud. This service is built on FastAPI, ensuring high performance and easy scalability.

## Features

- **Seamless Integration**: Connect Ollama and MCP servers with minimal setup.
- **FastAPI Framework**: Built on FastAPI for quick responses and low latency.
- **Local AI Support**: Run models locally for quick testing and deployment.
- **MCP Compatibility**: Fully compliant with Model Context Protocol standards.
- **Proxy Capabilities**: Acts as a proxy between different AI models and applications.
- **Easy to Use**: Simple API endpoints for common tasks.

## Installation

To install the **Ollama MCP Bridge**, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Reti0/ollama-mcp-bridge.git
   cd ollama-mcp-bridge
   ```

2. **Install Dependencies**:

   Make sure you have Python 3.7 or higher installed. Then, run:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**:

   Start the server with:

   ```bash
   uvicorn main:app --reload
   ```

4. **Access the API**:

   Open your browser and navigate to `http://localhost:8000/docs` to view the API documentation.

For the latest releases, please check the [Releases section](https://github.com/Reti0/ollama-mcp-bridge/releases).

## Usage

Once the application is running, you can interact with the API. Here are some example requests:

### Get Models

To retrieve a list of available models:

```http
GET /models
```

### Add a Model

To add a new model to the bridge:

```http
POST /models
Content-Type: application/json

{
  "name": "example-model",
  "type": "llm",
  "description": "An example language model."
}
```

### Delete a Model

To delete a model:

```http
DELETE /models/{model_id}
```

Replace `{model_id}` with the ID of the model you wish to delete.

## API Reference

### Authentication

The API uses token-based authentication. You can obtain a token by logging in through the `/login` endpoint.

### Endpoints

- **GET /models**: List all models.
- **POST /models**: Add a new model.
- **DELETE /models/{model_id}**: Remove a model.
- **GET /status**: Check the status of the bridge.

## Contributing

We welcome contributions to the **Ollama MCP Bridge**! If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push to your fork and create a pull request.

Please ensure your code adheres to the project's style guidelines and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please reach out to the maintainer:

- **Email**: maintainer@example.com
- **GitHub**: [Reti0](https://github.com/Reti0)

Feel free to visit the [Releases section](https://github.com/Reti0/ollama-mcp-bridge/releases) for updates and downloads.

---

Thank you for your interest in the **Ollama MCP Bridge**! We hope this project helps you in your AI development endeavors.