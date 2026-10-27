AI Docker App - Setup Instructions

Files included:
- app.py
- requirements.txt
- Dockerfile

Requirements:
- Docker Desktop installed and running.

Steps (Windows CMD):
1. Extract this ZIP file.
2. Open CMD in the extracted AI_Docker_App folder.
   Tip: Open the folder in File Explorer, click the address bar, type cmd, and press Enter.
3. Check Docker:
   docker --version
   docker run hello-world

4. Build the Docker image:
   docker build -t ai-app .

5. Check the image:
   docker images

6. Run the container:
   docker run -d -p 5000:5000 --name ai-container ai-app

7. Check the running container:
   docker ps

8. Open this URL in a browser:
   http://localhost:5000

Expected message:
AI Application is running inside Docker!

To stop and remove the container:
   docker stop ai-container
   docker rm ai-container

If a container named ai-container already exists, remove it before running again:
   docker rm -f ai-container

If you edit app.py, rebuild the image and recreate the container:
   docker build -t ai-app .
   docker rm -f ai-container
   docker run -d -p 5000:5000 --name ai-container ai-app

Note:
The Dockerfile must be named exactly "Dockerfile" (no .txt extension).
