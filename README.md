# Cloud Resume Challenge: Visitor Counter Project
Hands-on technical project combining Front-end static website, API function and CosmosDB
following [The Cloud Resume Challenge](https://cloudresumechallenge.dev/docs/the-challenge/azure/)

Here is the final outcome of my project: (https://gray-flower-05c101d00.5.azurestaticapps.net)

# Introduction

The Cloud Resume Challenge is a hands-on project designed to help individuals demonstrate their skills in cloud technologies, specifically using Microsoft Azure. This project aims to build a fully functional static website that tracks and displays the number of visitors using Azure services, including Azure Functions and Cosmos DB.

This project not only showcases my technical skills but also emphasizes my ability to solve real-world problems through cloud solutions. By leveraging Azure, I aimed to create a scalable, cost-effective solution that can serve as a portfolio piece for potential employers, illustrating my proficiency in cloud architecture, backend development, and DevOps practices.

This is also an extension of a preliminary project in the current curriculum program that I am enrolled in where I created a web app using the Flask framework with a log-in/logout functionality to implement a security feature coupled with a database to store a list of users and record comments. (https://ivanhcloudcareers.pythonanywhere.com)

# Project Scope

The primary goals of this project were to:

- Develop a static front-end website that effectively displays a visitor counter.
- Implement a back-end API using Azure Functions to manage visitor data.
- Store and retrieve visitor count data using Azure Cosmos DB.
- Deploy the application to Azure and establish a CI/CD pipeline for streamlined updates.



# Building the Frontend

### Frontend Overview
The frontend of the application is hosted in the frontend folder. 

The main components include:

- Static Website: A visually appealing interface where users can view the visitor count.
- Visitor Counter Code: Implemented in main.js, which fetches and displays the current visitor count.

### Impact on Users
This application provides users with a simple, user-friendly experience while allowing them to see real-time metrics. For potential employers, this project showcases my ability to create intuitive interfaces and implement dynamic features using cloud services.



# Building the Backend

### Setting up Azure Cosmos DB
I established a Cosmos DB account and created a container in Serverless capacity mode for optimal cost management. This choice enables automatic scaling, ensuring that I only pay for the resources consumed during peak times.

### Implementing Azure Functions
- Functionality: An HTTP-triggered Azure Function retrieves the visitor count data from Cosmos DB. It increments the count by 1 each time the function is invoked, then saves the updated count back to Cosmos DB.
- Bindings: The function utilizes Azure Cosmos DB bindings, facilitating seamless integration between the function and the database.

### Addressing Challenges
Several challenges were encountered during the implementation:

- Package Dependencies: I had to do countless research and integrate the correct NuGet package versions (Microsoft.Azure.WebJobs.Extensions.CosmosDB).
- Code Errors: Resolved issues related to outdated attribute properties, ensuring compatibility with the latest Azure SDK updates.
- Resources used: Stack Overflow, Chatgpt & Google search, Microsoft Documentation


# Deploying to Azure

### Deployment Overview
- Azure Function Deployment: Deployed the local function to Azure without issue.
- Website Deployment: Successfully deployed the static website to Azure Storage.
- Azure CDN: Set up Azure CDN for enhanced performance and secure HTTPS. However, I faced limitations due to constraints of my student account, which restricted the creation of a new CDN endpoint.
- As a workaround, I am considering using Cloudflare or another Azure account tier



# Building a CI/CD Pipeline

### Workflow Implementation
- Setting Up Azure CLI: Used Homebrew to install Azure CLI in Visual Studio Code, enabling interaction with Azure resources.
- Azure Static Web Apps: Leveraged Azure Static Web Apps for streamlined deployment of the frontend and to facilitate CI/CD integration, eliminating some permissions barriers.
- Unit Testing: Implemented unit tests for the Azure Functions code as part of the deployment workflow to ensure reliability and maintainability.



# Performance Metrics
To measure the success of the project, I plan to track the following metrics:

- Response Time: Analyzing the average response time for the API calls to ensure the system can handle traffic efficiently.
- Error Rate: Keeping track of any API errors to maintain a reliable user experience.
- Scalability Metrics: Assessing the application's performance during high-traffic events to ensure it can scale dynamically.


# Key Takeaways
The Visitor Counter Project not only demonstrates my technical abilities in cloud architecture and development but also highlights my problem-solving skills in overcoming challenges faced during implementation. This project serves as a testament to my readiness to contribute effectively in a professional cloud engineering role, providing potential employers with insights into my capabilities in delivering scalable, high-performance applications.


