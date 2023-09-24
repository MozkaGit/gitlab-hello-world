# GitLab Alpine Hello-World<br>[![CI/CD Pipeline](https://github.com/MozkaGit/gitlab-hello-world/actions/workflows/ci-cd.yaml/badge.svg)](https://github.com/MozkaGit/gitlab-hello-world/actions/workflows/ci-cd.yaml)</br>

This repository contains the necessary configuration and code to deploy an alpine-based docker application on Heroku using CI/CD pipeline. This project originally came from [my GitLab](https://gitlab.com/MozkaGit/alpine-helloworld) but I migrated it to GitHub and converted the `.gitlab.ci` to GitHub Actions.

## Local Deployment with Docker

1. Prerequisites
- Docker installed on your local machine.
- The project repository cloned to your local machine.

2. Building the Docker Image
- Navigate to the project directory in your terminal.
- Build the Docker image using the provided Dockerfile with the following command : `docker build -t hello-world .`

3. Running the Docker Container:
- Once the image is built, you can run the Docker container locally with : `docker run -p 80:5000 hello-world`

4. Accessing the Website
- Open a web browser and navigate to `http://localhost`.
- You should see your static website running locally.

## Deployment to Heroku:

### Main Files & Directories:
- `.gitlab-ci.yml`: This file contains the GitLab CI/CD pipeline configuration for building, testing, and deploying the static website.
- `.github/workflows/ci-cd.yaml`: This file contains the GitHub Actions workflow configuration for similar purposes as the GitLab CI/CD pipeline.

1. Prerequisites
- A GitLab or GitHub account.
- Git installed on your local machine.
- Setting Up your GitHub|GitLab Secrets

2. Pushing Changes
- The GitHub Actions workflow will handle deployment to Heroku.
- Once the job is completed, you can access the production environment to see your deployed website.