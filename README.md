# CI/CD Pipeline with Jenkins
![CI/CD Pipeline Workflow](https://i.postimg.cc/V6JzZSVs/white-modern-creative-Main-idea-Graphic-organizer.png)

This repository contains a simple CI/CD pipeline implemented using Jenkins. The pipeline is designed to automatically deploy a static HTML/CSS file to a Docker container and host it on port 8085.

## Prerequisites

Before setting up and running the CI/CD pipeline, make sure you have the following prerequisites installed:

- Jenkins: Install and configure Jenkins on your local machine or server.
- Docker: Install Docker to run the containerized deployment environment.
- GitHub account: Create a GitHub account to store your static HTML/CSS file.

## Getting Started

To set up the CI/CD pipeline, follow these steps:

1. Fork this repository: Click the "Fork" button at the top-right corner of this repository to create a copy in your GitHub account.
2. Clone the forked repository: Clone the forked repository to your local machine using the `git clone` command.
3. Update the HTML/CSS file: Replace the existing static HTML/CSS file (`index.html` and `styles.css`) with your own content.
4. Push changes to GitHub: Commit and push the updated file to the repository on GitHub.
5. Configure Jenkins: Set up a Jenkins job to build and deploy the HTML/CSS file.
   - Create a new Jenkins job and configure it as a pipeline.
   - Specify the GitHub repository URL and credentials.
   - Configure the Jenkins job to trigger on each push to the repository.
6. Run the Jenkins job: Start the Jenkins job and observe the pipeline's progress in the Jenkins dashboard.
7. Access the deployed application: Once the deployment is successful, access the hosted application in your browser at `http://localhost:8085`.

## Pipeline Workflow

The CI/CD pipeline follows this workflow:

1. Jenkins receives a webhook notification on each push to the GitHub repository.
2. Jenkins triggers the pipeline job based on the build steps
3. The pipeline job:
   - Checks out the latest changes from the GitHub repository.
   - Builds a Docker image with the static HTML/CSS files.
   - Runs a Docker container based on the created image, exposing port 8085.
4. The application is now accessible on `http://localhost:8085`.

## Customization

You can customize this pipeline according to your needs:

- Modify the Dockerfile: If you require additional dependencies or customizations for your application, update the Dockerfile accordingly.
- Adjust Jenkins job triggers: Instead of triggering the pipeline on each push, you can configure Jenkins to trigger the job based on specific branches or tags.
- Change the port number: If you prefer a different port for hosting the application, update the Dockerfile and Jenkins pipeline accordingly.

## Contributing

If you encounter any issues or have suggestions for improvement, feel free to open an issue or submit a pull request. Contributions are always welcome!

## License

This project is licensed under the [MIT License](LICENSE).

## Built Using

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
