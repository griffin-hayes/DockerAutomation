# Hello Docker and Java (with GitHub Actions)

This is a simple project that shows how to run a Java program using Docker and automatically build and push it using GitHub workflows 

## Steps

1. Write a Java program that prints a message.
2. Create a Dockerfile that uses a Java image and compiles the Java code.
3. Set the command in Docker to run the Java program.
4. Push the code to GitHub.
5. GitHub Actions automatically builds the Docker image and pushes it to Docker Hub.

## What Docker Did

1. Docker created an image that included the compiled Java code
2. The image was turned into a container that ran the program 
3. It printed the output like it would on any computer 

## What GitHub Actions Did

1. Watched the repository for code changes to the `master` branch  
2. Automatically built the Docker image using the Dockerfile  
3. Logged in to Docker Hub using saved secrets   
4. Pushed the image to Docker Hub with a tag based on the GitHub run number  

## Notes

- The Dockerfile must match the Java version you're using (we used OpenJDK 23)  
- You must save your DockerHub username and token as secrets in GitHub:
  - `DOCKER_USERNAME`
  - `DOCKER_PASSWORD` 
