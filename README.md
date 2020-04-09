# Digital Documentation Shipping Industry Solution Accelerator Guide

## About this repository
This accelerator was built to provide developers with all of the resources needed to quickly build an initial Digital Documentation for Shipping Quote system. Use this accelerator to jump start your development efforts with Blockchain in Azure.

This repository contains the steps, scripts, code, and tools to create a Blockchain application. 00_Resource_Deployment will create the necessary supporting resources in Azure (Functions, Blockchain Service, and Cosmos DB). 01_Solution_Deployment will configure and deploy the client app as well as the functions to the Azure resource. Finally 02_Application_Deployment will deploy and host your application either locally or in your subscription.

## Prerequisites
In order to successfully complete your solution, you will need to have access to and or provisioned the following:
1. Access to an Azure subscription
2. Visual Studio 2017 or 2019
3. AzureRM installed 


## Azure and Blockchain
The directions provided for this repository assume fundamental working knowledge of Azure, Cosmos DB, Azure Fuctions, Azure Blockchain Tokens, and Azure Blockchain Service.

For additional training and support, please see:
 1. [Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/introduction)
 2. [Functions](https://azure.microsoft.com/en-us/services/functions/) 
 3. [Blockchain Tokens](https://azure.microsoft.com/en-us/services/blockchain-tokens/)
 4. [Blockchain Service](https://azure.microsoft.com/en-us/services/blockchain-service/)

## Getting Started and Process Overview
Clone/download this repo onto your computer and then walk through each of these folders in order, following the steps outlined in each of the README files.  After completion of all steps, you will have a working end-to-end solution with the following architecture:

![Microservices Architecture](./References/architecture.JPG)


### [00 - Resource Deployment](./00_Resource_Deployment)
The resources in this folder can be used to deploy the required resources into your Azure Subscription. This can be done either via the [Azure Portal](https://portal.azure.com) or by using the [PowerShell script](./00_Resource_Deployment/deploy.ps1) included in the resource deployment folder.

After deployed, you will have a Cosmos DB account and database, Azure storage, and Kubernetes cluster deployed in your specified resource group.

### [01 - Solution Deployment](./01_Hyperledger_Fabric_Deployment)
This folder contains an Azure Pipeline. To prepare the environment and deploy the infrastructer run the [deploy script](./01_Hyperledger_Fabric_Deployment/deploy.ps1).

Running this script will deploy a basic fabric network consisting of two organizations: one peer organization and one orderer organization. To read more about hyperledger reference the [Hyperledger Fabric Documentation](https://hyperledger-fabric.readthedocs.io/en/release-1.4/).

### [02 - Hyperledger Fabric Client](./02_Hyperledger_Fabric_Client)
This folder contains the Kotlin Chaincode and Hyperledger Fabric server used to communicate with the blockchain network. The script in this folder will pull the Fabric Chaincode, Client, and gRPC server. This image will install the chaincode and allow the application to execute against the Blockchain network. Follow the provided instructions.

### [03 - Application Deployment](./03_Application_Deployment)
This folder contains the .net services for the proof content storage service, transaction tracker, transaction indexer, and gRPC Fabric Client. The Angular web application is also started and hosted with these services. Service Fabric is used to host this application.

## Links
Hosted Site: [Healthcare Blockchain Solution](http://healthcare-apphosting.southcentralus.cloudapp.azure.com/login)

*Use income less than 11000 and a NY Zip Code for a profile to qualify*

Video: [Healthcare Blockchain Solution Video](https://msit.microsoftstream.com/video/7f62ce8c-39e1-40d6-8adb-cbf298f31dfe)

*Or download [Healthcare Blockchain Solution Video](healthcare_solution_video.mp4)*


## License
Copyright (c) Microsoft Corporation

All rights reserved.

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ""Software""), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
