# Serverless Web App in AWS: UnicornRides

## Description
UnicornRides is a web application for requesting unicorn rides from Wild Rydes. It showcases serverless AWS technologies, offering user authentication and real-time ride management.

## Features
- User Authentication
- Interactive Ride Booking
- Real-time Ride Management

## Technologies Used

- ![AWS Lambda Logo](URL_TO_LOGO) AWS Lambda
- ![Amazon API Gateway Logo](URL_TO_LOGO) Amazon API Gateway
- ![Amazon DynamoDB Logo](URL_TO_LOGO) Amazon DynamoDB
- ![Amazon Cognito Logo](URL_TO_LOGO) Amazon Cognito
- ![AWS Amplify Console Logo](URL_TO_LOGO) AWS Amplify Console


## Application Architecture
The serverless architecture for this web application is built upon several AWS services:
- **AWS Amplify**: Serves as the foundation, hosting the static web content. It's the first interaction point for users, delivering HTML, CSS, and JavaScript to their browsers.
- **Amazon Cognito**: The second layer of user interaction, handling authentication. It ensures that users are securely logged in before interacting with backend services.
- **Amazon API Gateway**: Acts as the intermediary for all dynamic API calls over HTTPS from the client, enabling communication between the web browser and AWS Lambda.
- **AWS Lambda**: The compute layer, it processes the application logic in response to API calls and interacts with the database.
- **Amazon DynamoDB**: Maintains a robust NoSQL database for storing ride data, interacted with by Lambda functions.

  ![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/f6b5af36-3b71-4b1b-8e36-58541b4f2915)




The user journey begins with interacting through the browser, authentication via Cognito, and making API requests through API Gateway, which invokes Lambda functions. These functions then interact with DynamoDB to manage data as needed.

## Setup and Installation
<details>
<summary>Click to expand!</summary>
<p>

Detail the steps required to set up and run the application locally, including AWS configuration, local environment setup, and any other necessary instructions.

</p>
</details>

## Screenshots/Demo
Include images/screenshots of the app in action.

