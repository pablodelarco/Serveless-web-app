# Serverless Web App in AWS: UnicornRides

## Description
UnicornRides is a web application for requesting unicorn rides from Wild Rydes. It showcases serverless AWS technologies, offering user authentication and real-time ride management.

## Features
- User Authentication
- Interactive Ride Booking
- Real-time Ride Management

## Technologies Used

- ![AWS Lambda Logo](![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/ed3c7b3d-02b1-4232-860c-84112024ebc2)) AWS Lambda
- ![Amazon API Gateway Logo](![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/58025426-86dc-41ab-8fc7-e2741dd4eb0e)) Amazon API Gateway
- ![Amazon DynamoDB Logo](![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/56dc546f-99f0-476d-ba73-f6be672b44d7)) Amazon DynamoDB
- ![Amazon Cognito Logo](![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/305d1a9d-1115-4932-abd2-123ed67adcec)) Amazon Cognito
- ![AWS Amplify Console Logo](![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/20a5464d-db29-4af6-86b4-b5d7581a64da)) AWS Amplify Console


## Application Architecture
The serverless architecture for this web application is built upon several AWS services:
- **AWS Amplify**: Serves as the foundation, hosting the static web content. It's the first interaction point for users, delivering HTML, CSS, and JavaScript to their browsers.
- **Amazon Cognito**: The second layer of user interaction, handling authentication. It ensures that users are securely logged in before interacting with backend services.
- **Amazon API Gateway**: Acts as the intermediary for all dynamic API calls over HTTPS from the client, enabling communication between the web browser and AWS Lambda.
- **AWS Lambda**: The compute layer, it processes the application logic in response to API calls and interacts with the database.
- **Amazon DynamoDB**: Maintains a robust NoSQL database for storing ride data, interacted with by Lambda functions.

  ![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/f6b5af36-3b71-4b1b-8e36-58541b4f2915)



## Setup and Installation
<details>
<summary>Click to expand!</summary>
<p>

Detail the steps required to set up and run the application locally, including AWS configuration, local environment setup, and any other necessary instructions.

</p>
</details>

## Screenshots/Demo
Include images/screenshots of the app in action.

