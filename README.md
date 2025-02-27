# Docker Compose Setup for LiteLLM, WebUI, MLflow, and Langflow

This repository provides a Docker Compose configuration to deploy the following components:

- **LiteLLM**: A unified interface to manage and interact with multiple Large Language Models (LLMs).
- **WebUI**: A user-friendly web interface for interacting with LLMs.
- **MLflow**: An open-source platform for managing the end-to-end machine learning lifecycle.
- **Langflow**: A low-code app builder for creating AI applications.

## Prerequisites

Ensure you have the following installed on your system:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

Follow these steps to set up and run the services:

### 1. Clone the Repository

```bash
git clone https://github.com/Vitorhbv/docker-compose-litellm-webui-mlflow-langflow.git
cd docker-compose-litellm-webui-mlflow-langflow
```

### 2. Configure LiteLLM

Modify the `litellm_config.yaml` file to include your API keys and desired LLM configurations (See [doc](https://docs.litellm.ai/docs/simple_proxy)

### 3. Start the Services

Run the following command to start all services:

```bash
docker-compose up -d
```

This command will download the necessary Docker images and start the containers in detached mode.

### 4. Access the Applications

- **WebUI**: Navigate to `http://localhost:3000` in your web browser.
- **MLflow**: Access the MLflow tracking UI at `http://localhost:5000`.
- **Langflow**: Open `http://localhost:7860` to start building AI applications.
- **LiteLLM API**: Available at http://localhost:4000.
- **Ollama**: Available at http://localhost:11434.

## Stopping the Services

To stop and remove the containers, execute:

```bash
docker-compose down
```

## Additional Notes

- **Environment Variables**: You can set environment variables in a `.env` file to configure API keys and other settings.
- **Logging**: Logs for each service can be accessed using `docker-compose logs -f`.
- **Scaling Services**: Modify the `docker-compose.yaml` file to scale specific services if needed.
- **Updating Containers**: To pull the latest images and restart the services, run:

```bash
docker-compose pull
docker-compose up -d --force-recreate
```

## Troubleshooting

If you encounter issues, consider the following:

- Ensure Docker and Docker Compose are installed and running correctly.
- Check the logs using `docker-compose logs` for any error messages.
- Verify that the required ports are not being used by other applications.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

By following this guide, you should have a functional environment with LiteLLM, WebUI, MLflow, and Langflow running via Docker Compose. These tools collectively provide a robust platform for managing and deploying AI applications.

