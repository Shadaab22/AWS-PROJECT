# AWS-PROJECT
Stocker – A Cloud based stock trading application using Flask and AWS

Stocker is a cloud-based stock trading application that I built to explore how modern trading platforms can be developed using Flask and AWS cloud services. The goal of this project was to simulate a simple trading environment where users can create accounts, perform stock buy/sell operations, and track their investment portfolios.

The backend of the application is built using Flask, which handles routing, authentication, and the core trading logic. I used boto3 to connect the Flask application with AWS services so the application can interact with cloud resources directly.

For hosting the application, I deployed the backend on an AWS EC2 instance. This allows the application to run on a cloud server instead of a local machine, making it more scalable and closer to how real-world web applications are deployed.

To manage the application data, I used Amazon DynamoDB, which is a NoSQL database provided by AWS. DynamoDB stores important information such as:
->user account details
->stock information
->transaction records
->user portfolio holdings

Using DynamoDB allowed me to store and retrieve data quickly without managing a traditional database server.

The project also integrates Amazon SNS (Simple Notification Service) to demonstrate how cloud-based notification systems can be used in financial applications. Notifications can be triggered when important events occur, such as user account activity or transaction updates.

Security and resource access are managed using AWS IAM (Identity and Access Management). IAM roles allow the EC2 instance running the Flask application to securely access DynamoDB and SNS without exposing sensitive credentials.

On the frontend side, I created a simple interface using HTML and CSS where users can register, log in, execute trades, and view their portfolio information. The interface communicates with the Flask backend to fetch and display data dynamically.

Through this project, I implemented several key features including:
->user registration and secure login system
->stock buy and sell transaction functionality
->portfolio tracking for each user
->transaction history management
->cloud database integration using DynamoDB
->deployment of the application on AWS EC2
->notification integration using AWS SNS

Building this project helped me understand how backend development, cloud services, and database systems work together to create scalable web applications. It also gave me hands-on experience with deploying applications on AWS and integrating multiple cloud services into a single system.

Overall, Stocker demonstrates how a basic stock trading platform can be designed using Flask for backend development and AWS for cloud infrastructure, making it a useful learning project for understanding cloud-native application development.
