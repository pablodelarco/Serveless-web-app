# Serverless Web App in AWS: UnicornRides

## Description
UnicornRides is a web application for requesting unicorn rides from Wild Rydes. It showcases serverless AWS technologies, offering user authentication and real-time ride management.

## Features
- User Authentication
- Interactive Ride Booking
- Real-time Ride Management

## AWS Services

- <img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/56dc546f-99f0-476d-ba73-f6be672b44d7]" width="22"/> CodeCommit
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

  ![image](https://github.com/pablodelarco/Serveless-web-app/assets/63775967/f6b5af36-3b71-4b1b-8e36-58541b4f2915)



## Setup and Installation
<details>
<summary>Click to expand!</summary>
<p>

Detail the steps required to set up and run the application locally, including AWS configuration, local environment setup, and any other necessary instructions.

</p>
</details>

## Screenshots/Demo

<img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/9bf42832-ce28-419f-962d-ee6466cfc9ce" width="500"/>

<img src="https://github.com/pablodelarco/Serveless-web-app/assets/63775967/280b182f-d63a-448c-a355-7a138567b5b1" width="505"/>


