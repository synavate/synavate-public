# 📚 Synapse Architecture Summary
***Progressive integration of services is underway as at v0.0.2***

### Current Version: v0.0.3 (Service Refactor)

The architecture for Synapse v0.0.3 is structured for scalability and modular development, focusing on a robust backend, ML operations, and a user-centric front end. The deployment targets Google Cloud Platform (GCP), leveraging its tools for a scalable and staged deployment approach. Here’s a concise overview of the stack and architecture:

### Core Operations 🌐
- **APIGatewayService**: Utilizes NestJS Microservice API Gateway as the primary entry point, with plans to migrate to Kong. Kubernetes is employed for dynamic scaling and resource management.

### Backend Service Libraries 🔧
- **Backend Logic & Testing**: The stack includes Python for backend logic, with Poetry and PyEnv for dependency management and environment isolation. Testing is conducted with pytest.
- **ML Model Libraries**: Machine learning development leverages Scikit-learn, PyG, and PyTorch for model building and experimentation.
- **MLOps**: ML operations integrate WandB and MLFlow for experiment tracking and model versioning, supplemented with custom Python scripting for model retraining. Live monitoring solutions are to be confirmed.
- **LLM Orchestration and Ops**: Utilizes LLamaIndex and Langchain for orchestrating Large Language Model tasks, with Humanloop for human-in-the-loop workflows and continuous LLM evaluations.
- **Application Server**: FastAPI serves as the backbone for RESTful APIs, interfacing with the API Gateway.

### Backend Database and Caching 🗄️
- **Databases**: Employs a mix of MongoDB for testing, along with REDIS, QDrant, Memgraph, and Neo4J (to be decided) for various data storage and graph database needs.
- **Cloudflare AI Gateway**: A customized fork from Portkey for enhanced AI capabilities at the edge.

### Frontend User UI & Data Visualization 🖥️
- **User Account & Security**: Exploration of Verida and Spruce for secure data management and authentication.
- **User UI**: Built with NextJS and Typescript for a modern, scalable frontend.
- **Data Visualization**: Integrates D3 for data visualization, with custom styling and integration with Memgraph Orb for graph-based visualizations.
- **Application Server**: An Express-based TypeScript API handles frontend server operations.

### Key Services 🔑
- **KnowledgeGraphGen**: Dedicated to knowledge graph creation and management.
- **MLInferenceService**: Offers machine learning inference capabilities.
- **LLMProcessingService**: Specialized in processing requests for Large Language Models.
- **BusinessLobsterService**: Focused on generating business intelligence reports.
- **DataProcessingService**: Manages preprocessing of data for analytical readiness.
- **DataPipelineService**: Orchestrates data storage and management solutions across platforms.

### Frontend Technologies 🌟
- **UserAccountService**: Oversees user authentication and account management.
- **UserDashboard**: Developed with Next.js, providing a user interface for interacting with the system.
- **DataVizService**: Facilitates the creation of data visualizations for insights and analysis.

This architecture emphasizes flexibility, scalability, and a microservices approach, designed to facilitate rapid development and deployment on GCP with a focus on robust ML and LLM operations.