# Deploy-YoloV3-obj-detection-using-FastAPI

### This lab is all about seeing how it feels to deploy a YoloV3 model trained to detect common objects in images. Model is deployed on localhost using FastAPI

API is coded using FastAPI, but the serving is done using 🔗uvicorn, which is a really fast Asynchronous Server Gateway Interface (ASGI) implementation. Both technologies are closely interconnected. Knowing that uvicorn handles the serving is sufficient for the purpose of this lab.





**MORE INFO ON HOW FastAPI WORKS BEHIND THE SCENES**:

FastAPI is _high-performance_ **open source** web framework (_a collection of modules and packages used to develop software_) for creating APIs with Python 3.6. FastAPI was created using tools like **Starlette** and **Pydantic**.

**Key Features of FastAPI**:
1. Built on Starlette for async web handling.
2. Uses Pydantic for data validation and serialization.
3. Provides automatic OpenAPI and Swagger UI documentation.
4. Supports asynchronous programming with Python's **async** and **await**.
   

**Starlette**: A lightweight ASGI framework/toolkit for building high-performance web applications. FastAPI is built on top of Starlette, meaning all the request handling, middleware, and web-related functionality come from Starlette. 
    
    a. Provides the foundation for FastAPI.
    
    b. Handles routing, middleware, WebSockets, background tasks, etc. 
    
    c. Fully asynchronous and efficient.

**Pydantic**: A data validation and settings management library in Python. FastAPI uses Pydantic models to define request and response schemas, making data validation automatic and efficient.

    a. Uses Python type hints (str, int, List, etc.) to validate and parse data automatically.
    
    b. Ensures data integrity by enforcing strict types.
    
    c. Converts input data into well-structured Python objects.

**Uvicorn**: An ASGI server that runs FastAPI and other ASGI applications. FastAPI applications run on Uvicorn (or similar ASGI servers like Daphne or Hypercorn) to handle HTTP requests asynchronously.
  
    a. Built on uvloop (a fast event loop for asyncio).
    
    b. Provides excellent concurrency and speed.
    
    c. Works as an alternative to WSGI servers like Gunicorn but optimized for async applications.

**How They Work Together**:

1. FastAPI (Main framework) depends on Starlette (for web handling).

2. FastAPI uses Pydantic (for data validation and serialization).

3. FastAPI applications need Uvicorn (or another ASGI server) to run efficiently.

