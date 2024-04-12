# React AWS CodePipeline Setup

This repository contains a guide and configuration files to set up a continuous deployment pipeline for a React application using AWS CodePipeline.

## Steps to Setup

### Step 1: Create buildspec.yml

- Create a `buildspec.yml` file in the project's root directory.
- Add commands necessary to build and deploy the app according to the provided YAML code.

### Step 2: Push Code to GitHub

- Push your project to GitHub repository.

### Step 3: Create S3 Bucket

- Create an AWS S3 Bucket to host the React JS build.
- Configure bucket properties for static web hosting and permissions for public access.

### Step 4: Create AWS CodePipeline

- Navigate to AWS CodePipeline and create a new pipeline.
- Specify a name and choose a new service role.
- Proceed to the next step without advanced settings.

### Step 5: Create Source Provider

- Select GitHub as the source provider.
- Connect to GitHub and choose the repository and branch.
- Enable GitHub webhooks for change detection.

### Step 6: Create CodeBuild

- Choose AWS CodeBuild as the build provider and select the region.
- Create a project with appropriate settings and configurations.
- Use the `buildspec.yml` file for build specifications.

### Step 7: Create Deployment Stage

- Select Amazon S3 as the deploy provider and choose the region.
- Specify the S3 Bucket created in Step 3.
- Enable the option to extract files before deployment.

### Step 8: Review and Create Pipeline

- Review all configurations and settings.
- Click on Create pipeline to finalize the setup.

## Viewing Pipeline Progress

- The pipeline starts automatically upon creation.
- Monitor the pipeline stages and check details for any errors.
- After successful deployment, visit the Endpoint URL from Step 3 to view the live web application.

