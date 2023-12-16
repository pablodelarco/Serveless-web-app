# AWS Serverless Web App: HorsesRides


  <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/7ee5a785-4846-4a3b-bef3-234a19b727d6" width="600"/>

## Description
HorsesRides is a web application for requesting rorses rides from Wild Rydes. It showcases serverless AWS technologies, offering user authentication and real-time ride management.

## Features
- User Authentication
- Interactive Ride Booking
- Real-time Ride Management

## AWS Services

- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/5ded8d7c-b121-40c1-ab71-d2c5fd00237c" width="22"/> CodeCommit
- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/993d8de3-ab69-4e2e-9f14-ea8dd1b09110" width="22"/> Identity and Access Management (IAM)
- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/20a5464d-db29-4af6-86b4-b5d7581a64da" width="22"/> Amplify
- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/305d1a9d-1115-4932-abd2-123ed67adcec" width="22"/> Cognito
- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/58025426-86dc-41ab-8fc7-e2741dd4eb0e" width="22"/> API Gateway
- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/ed3c7b3d-02b1-4232-860c-84112024ebc2" width="22"/> Lambda
- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/56dc546f-99f0-476d-ba73-f6be672b44d7" width="22"/> DynamoDB









## Application Architecture
The serverless architecture for this web application is built upon several AWS services:
- **AWS Amplify**: Serves as the foundation, hosting the static web content. It's the first interaction point for users, delivering HTML, CSS, and JavaScript to their browsers.
- **AWS Cognito**: The second layer of user interaction, handling authentication. It ensures that users are securely logged in before interacting with backend services.
- **AWS API Gateway**: Acts as the intermediary for all dynamic API calls over HTTPS from the client, enabling communication between the web browser and AWS Lambda.
- **AWS Lambda**: The compute layer, it processes the application logic in response to API calls and interacts with the database.
- **AWS DynamoDB**: Maintains a robust NoSQL database for storing ride data, interacted with by Lambda functions.


## Setup and Installation
<details>
<summary>Part 1: Host a Static Website</summary>
<p>
  
**AWS Services:** 
- AWS CodeCommit for code storage.
- AWS IAM for permission handling.
- AWS Amplify for web hosting.

**1. Create a Git Repository:**
- Start by creating a repository named “wildrydes-site” in AWS CodeCommit.
- In AWS IAM, create a new user, e.g., *TTTAdmin*, and attach the `AWSCodeCommitPowerUser` policy for CodeCommit access.
- Generate Git credentials for HTTPS connections to CodeCommit.

**2. Configure the Git Repository:**
- Clone your new repository using AWS CloudShell.
- Use Git commands to copy static files from S3, then add, commit, and push these files.

**3. Enable Web Hosting with AWS Amplify:**
- Set up a new web app in AWS Amplify linked to your CodeCommit repository.
- Follow the prompts to deploy your website.
  
</p>
</details>

<details>
<summary>Part 2: Create User Pool in Cognito</summary>
<p>

**AWS Service:** AWS Cognito for user management.

**1. Create an AWS Cognito User Pool:**
- Create a user pool named “WildRydes” with default settings.
- Save the User Pool ID and Client ID.

**2. Update the Website Config File:**
- Adjust `js/config.js` with the `userPoolId` and `userPoolClientId` from Cognito.

</p>
</details>

<details>
<summary>Part 3: Build a Serverless Backend</summary>
<p>
  
**AWS Services:** 
- AWS DynamoDB for data storage.
- AWS Lambda for backend processing.

**1. Create an Amazon DynamoDB Table:**
- Create a table named “Rides” with “RideId” as the partition key.

**2. Create an IAM Role for Lambda:**
- Set up a role in IAM for Lambda, granting necessary permissions for DynamoDB access.

**3. Create a Lambda Function:**
- In AWS Lambda, establish a function named “RequestUnicorn.”
- Assign the IAM role and deploy the function with `requestUnicorn.js` code.

</p>
</details>


<details>
<summary>Part 4: Deploy a RESTful API</summary>
<p>
  
**AWS Service:** AWS API Gateway.

**1. Create a REST API:**
- In API Gateway, establish a new API named “WildRydes.”

**2. Create an Authorizer:**
- Set up a Cognito authorizer and test it with an Authorization Token.

**3. Create a New Resource and Method:**
- Add a 'ride' resource with a POST method, integrated with the Lambda function.
- Set the Cognito authorizer for the method.

**4. Deploy Your API:**
- Deploy the API by creating a stage named 'dev'.
- Note the Invoke URL for future use.

**5. Update the Website Config:**
- In `js/config.js`, update the `invokeUrl` with the URL from the API Gateway.

</p>
</details>

## Screenshots/Demo

<img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/9bf42832-ce28-419f-962d-ee6466cfc9ce" width="500"/>

<img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/280b182f-d63a-448c-a355-7a138567b5b1" width="505"/>

<img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/0391b1d7-64fb-4f61-9ac9-3595f1258236" width="505"/>

<img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/64dc087c-40d5-4e75-a357-74fe9d9fa6fc" width="505"/>



## Acknowledgments
For a more detailed tutorial, I have created this guide in a Notion page: [https://shorturl.at/dnoM0](url)

This project was inspired by the AWS tutorial on building a serverless web application: [Build a Serverless Web Application](https://aws.amazon.com/getting-started/hands-on/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/?nc1=h_ls).


