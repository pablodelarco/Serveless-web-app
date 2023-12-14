# Serverless Web App in AWS: UnicornRides

## Description
UnicornRides is a web application for requesting unicorn rides from Wild Rydes. It showcases serverless AWS technologies, offering user authentication and real-time ride management.

## Features
- User Authentication
- Interactive Ride Booking
- Real-time Ride Management

## Technologies Used
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- Amazon Cognito
- AWS Amplify Console

## Application Parts

1. **Static Web Hosting**
   AWS Amplify hosts static web resources like HTML, CSS, JavaScript, and images.

2. **User Management**
   Amazon Cognito provides user management and authentication.

3. **Serverless Backend**
   Amazon DynamoDB offers a persistence layer for the API's Lambda function.

4. **RESTful API**
   JavaScript in the browser interacts with a backend API using Lambda and API Gateway.

## Application Architecture
The serverless architecture for this web application is built upon several AWS services:
- **AWS Amplify**: Hosts the static web resources that the browser loads.
- **Amazon Cognito**: Manages user authentication within the app.
- **AWS Lambda**: Executes the application code in response to HTTP requests via the API Gateway.
- **Amazon DynamoDB**: Acts as the database service for storing and retrieving application data.
- **Amazon API Gateway**: Functions as the doorway for dynamic API calls made over HTTPS by the web client.

The user journey begins with interacting through the browser, authentication via Cognito, and making API requests through API Gateway, which invokes Lambda functions. These functions then interact with DynamoDB to manage data as needed.

## Setup and Installation
<details>
<summary>Click to expand!</summary>
<p>

Detail the steps required to set up and run the application locally, including AWS configuration, local environment setup, and any other necessary instructions.

</p>
</details>

## License
[Your chosen license]

## Screenshots/Demo
Include images/screenshots of the app in action.

