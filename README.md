# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.


# docker-react
This project demonstrates integration between Github Actions and AWS Elastic Beanstalk service. A React app is deployed via AWS Elastic Beanstalk as a docker image.

# Boilerplate React App
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# Application Details
Simple React Application created using create-react-app

# Automation Steps
* Github Action API call into AWS Service
* Auto provision of AWS EC2 Instance 
* Auto creation of AWS S3 Bucket for service
* Auto creation of AWS Security groups and roles
* Auto creation of AWS Application Load Balancers
* Auto Build of specified NodeJS (AWS Variant) Docker image from AWS ECR
* Build Application in the specified container
* Exposing ports to open world on Edge Servers
* Route53 Integration possible if needed
* Auto Backup provisioning can be intergrated with S3 Glacier if needed
