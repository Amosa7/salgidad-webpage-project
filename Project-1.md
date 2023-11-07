### RUNNING A LOCAL WEB SERVER(HTTP SERVER) WITH DOCKER  🐳

### INTRODUCTION

This project demostrate how to serve a static website from localhost using Docker and Nginx. In today's digital age, web development and testing are integral parts of building successful online experiences. However, setting up a development environment to locally serve web content can be complex and resource-intensive.

 We aim to streamline the process by leveraging Docker, a powerful containerization tool, to create a local HTTP server. With this setup, developers can effortlessly serve and test their static websites as if they were live on the internet, all on their local machines. This not only enhances development efficiency but also ensures accurate testing before deploying to production.

<img src="doccker + Nginx.png" alt="Docker and Nginx" style="display: block; margin: 0 auto; max-width: 2000px;">

 

### STEP 1: CREATING A HTML AND CSS FILE

The initial step in web development is crafting the foundation of the website: the HTML (Hypertext Markup Language) and CSS (Cascading Style Sheets) file. HTML defines the structure and content of the web page, while CSS handles its visual styling.

![Alt text](<IMAGES/Screenshot (34).png>)

### STEP 2: CREATING A DOCKERFILE
After I designed the web page with HTML and CSS, the next crucial step is to create a Dockerfile. This file acts as a blueprint for building a Docker image, which encapsulates the web webpage and its environment.

In the Dockerfile, I defined:

- The base image: The foundational image upon which the webpage will run(I used Nginx:latest).
- COPY the web content to the Nginx web server directory at /usr/share/nginx/html
- EXPOSE port 80 for web traffic inside the container
 
![Alt text](<IMAGES/Screenshot (35).png>)

### STEP 3: LAUNCHING MY DOCKER DAEMON 🐳

Before I can start working with Docker and its containerization capabilities, I need to ensure that the Docker daemon is up and running. The Docker daemon is a background service responsible for managing and executing container operations.

![Alt text](<IMAGES/Screenshot (37).png>)

### STEP 4: BUILDING THE DOCKER IMAGE

With the Dockerfile prepared, the next vital step is to build a Docker image. This image encapsulates the webpage and its environment, ensuring consistency and portability.
![Alt text](<IMAGES/Screenshot (38).png>)

### STEP 5: RUNNING THE DOCKER CONTAINER

To bring the web project to life, I run a Docker container,  making the web content accessible on my local machine, and sets the stage for testing and development in a containerized environment.
![Alt text](<IMAGES/Screenshot (42).png>)
 

Here's what each part of the command I wrote does:

- -d: This runs the container as a background process, allowing me to continue using my terminal.

- -p 8080:80: It maps port 8080 on my host to port 80 in the container, so I can access the web server at localhost:8080.

- --name salgidad: This assigns a user-friendly name, "salgidad," to the container for easy reference.

- -v html-data:/usr/share/nginx/html: This creates a Docker volume named "html-data" and mounts it to the container's /usr/share/nginx/html directory, ensuring your web content is available even if the container is removed.

- salgidad:2.0: Specifies the Docker image to use for creating the container.

### FINAL STEP: TEST AND ACCESSING THE WEBPAGE
 After I successfully built and run the Docker container, which hosts my webpage, the final step is to test and access my web content via web browser on my local Machine 

![Alt text](<IMAGES/Screenshot (43).png>)


### CONCLUSION
You may have already used VS Code's Live Server to do something similar to this. However in this project, I streamline web development by harnessing the power of Docker, a containerization tool, and Nginx to set up a local HTTP server, which you can easily access from localhost (a way to describe your local computer's address). 





