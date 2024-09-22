# Azure-resume
Hands-on technical project combining Front-end static website, API function and CosmosDB
following [The Cloud Resume Challenge](https://cloudresumechallenge.dev/docs/the-challenge/azure/)

## Building the frontend

- Frontend folder contains the website
- main.js contains visitor counter code

Scope:
Purpose of the project (e.g. what problem needed to be solved and what was the significance/impact of the problem)
Explain the challenges you encountered and the solutions you discovered/created, including the benefits to the user
Highlight the impact of your project on the users and yourself
Explain the relevance of the project to potential new employer(s)

## Building the backend
1.Setting up Cosmos DB account resource group and adding a container 
I went with Serverless capacity mode in terms of usage and pricing

2.Setting up Azure Function
Invoking Azure Function in order to retrieve vistior counter data
Functions has this feature called bindings allowing us to connect other resources to my function i.e Azure Cosmos DB bindings to the function
and viewing counter data via the function
A simple HTTP trigger function command in the terminal runs the Azure function

3.Setting up CosmosDB bindings
Multiple challenges:
a.Having to search package dependencies and read Microsoft documentation because there were new updates
b.Functions extension require installing correct versions from new packages Nuget (Microsoft.Azure.WebJobs.Extensions.CosmosDB)
c.Code Error due to outdated attribute properties

CosmosDB bindings worked with code running locally on the browser

4.Deploying to Azure
a.Deploying my local function to Azure


b.Deoplying website to Blob Storage

c.Setting up with Azure CDN for HTTPS and custom domain