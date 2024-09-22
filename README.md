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
A HTTP triggered Azure Functions with Cosmos DB input and output binding. 
The Function is triggered, it retrieves the CosmosDB item, add +1 to it, and saves it and returns its value to the caller.

3.Setting up CosmosDB bindings
Multiple challenges:
a.Having to search package dependencies and read Microsoft documentation because there were new updates
b.Functions extension require installing correct versions from new packages Nuget (Microsoft.Azure.WebJobs.Extensions.CosmosDB)
c.Code Error due to outdated attribute properties

CosmosDB bindings worked with code running locally on the browser

## Deploying to Azure
a.Deploying my local function to Azure


b.Deploying website to Azure Storage succesfully!
https://getresumecounterivan.z23.web.core.windows.net

c.Setting up with Azure CDN for HTTPS and custom domain
Required to map a custom domain to an Azure Storage endpoint
by creating a canonical name (CNAME) record with your domain provider.
Challenge:
I was not able to create a new endpoint with Azure CDN due to being constrained by my student account

## Building a CI/CD Pipeline
Before that, I had to use brew to install azure cli in VSC and login to Azure.
I also had to create a new repository actions secret on Github.
Challenge: Encountered an error - 'Directory permission is needed for the current user to register the application. For how to configure, please refer 'https://docs.microsoft.com/azure/azure-resource-manager/resource-group-create-service-principal-portal'. Original error: Insufficient privileges to complete the operation'

Unable to resolve error as Microsoft EntraID is not available to me which maybe due to the student account.


1.Creating my frontend workflow
Found a workaround: It is to deploy using Azure Static web apps which 


2.Implement unit testing to test my Azure Functions code as part of the deployment workflow



3.Creating my backend workflow


