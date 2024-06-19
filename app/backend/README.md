The backend of this project is a Python application that is hosted on Azure App Service, as defined in the infra/main.bicep file. It's configured to use a Python runtime and Gunicorn as the WSGI HTTP server.

The backend is set up with various roles for interacting with different Azure services. These roles are defined in the infra/main.bicep file and include roles for interacting with Azure Search, Speech, Storage, Computer Vision, and Document Intelligence services. The roles are assigned to the backend's managed identity, which is indicated by the backend.outputs.identityPrincipalId parameter.

The backend is also configured to be part of a virtual network as indicated by the isolation.outputs.appSubnetId parameter. This could be for security reasons, to ensure that the backend can only communicate with specific resources.

The backend's source code is located in the app/backend/ directory. However, without more information about the files in this directory, it's hard to provide more details about the functionality of the backend.

For local development, you can start the backend by running ./start.ps1 or ./start.sh in the app/ directory, as mentioned in docs/localdev.md. This will also enable hot reloading for the backend files.

For more information about customizing the backend, you can refer to docs/customization.md