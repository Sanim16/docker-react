## Guide to Build a React App, test and Deploy Application in AWS EBS using Github Actions
# docker-react
This project demonstrates integration between Github Actions and AWS Elastic Beanstalk service. A React app is deployed via AWS Elastic Beanstalk after been tested using a docker image.

# Boilerplate React App
This application was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# Application Details
Simple React Application created using create-react-app


Steps To Deployment
1. Build react app and Dockerise it then push to GitHub Repo
2. Create a Github Actions workflow which is triggered on push to main branch       
3. The Workflow runs on a github hosted runner(Ubuntu-Latest) which
    - The runner builds the docker image based on the Dockerfile.dev
    - The runner runs and tests the just built Docker image
4. The workflow then creates an artifact from step 3 above. A zip file for deployment to EBS
5. The artifact is then copied to an existing S3 bucket using AWS CLI or a new bucket could be created
6. Create an ElasticBeanStalk Application using the AWS CLI
7. Configure all the environment variables :
    ```
          EB_APPLICATION_NAME: "YOUR_EBS_APPLICATION_NAME" created in #6
          EB_APP_ENV_NAME: "YOUR_EBS_APPLICATION_ENVIRONMENT NAME" created in #6
          DEPLOY_PACKAGE_NAME: "YOUR_APPLICATIO_NAME-${{ github.sha }}.zip" // using github.sha makes sure you have a different package name for each deployment
          AWS_REGION_NAME: "YOUR_AWS_REGION" where all aws components are created 
          AWS_BUCKET_NAME: "YOUR_BUCKET_NAME" from #5
     ```
     
 - `Note: Ensure all the AWS components are created in same region`
