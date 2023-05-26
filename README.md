# camunda-connectors
This repository contains the Camunda Connectors developed by Incentro

## Alfresco connector
Alfresco Content Servces (ACS) is a very popular Open Source Document Management System (DMS). And if you might know: every process contains a document so to have an integration between Camunda and Alfresco is relevant. Incentro is an Alfresco partner for years and have a lot of experience with the platform.

## How it works
Luckily ACS comes with an extensive REST API. Therefore we were able to create this connector using the REST protocol connector from Camunda, which means only configuration was required and no coding. For more information about the Alfresco API please have a look here: [https://api-explorer.alfresco.com/api-explorer/#/](https://api-explorer.alfresco.com/api-explorer/#/) 
To install this connector: add a connector template to your BPMN project and use the contents of the alfresco-connector.json file. Now you are ready to use the connector in your BPMN diagrams.

## Authentication
Currently only basic authentication is supported. You can set the username and password when configuring an Alfresco task. Please use secrets and do not put any credentials directly into your running processes. The base URL refers to your Alfresco instance, for example: [https://www.example.com/alfresco](https://www.example.com/alfresco)

## Supported operations
- Create a folder

### Create a folder operation
To create a folder in ACS you need to provide the nodeId of the parent folder and a name for the folder. If a folder with the name already exists ACS will automatically rename it.

## Contact
If you have any questions or want to contribute please contact Maarten van Veelen (maarten.vanveelen@incentro.com) or use Github to reach me.
