# Overview

## SkimoTeamsConnector
This repository has the connector to connect to the Microsoft Teams conference service provider. 

The connector extends the SkimoConnectorTemplate, which utilizes Springboot and Thymeleaf 

(refer to the template README for more info)

The connector uses the Microsoft Graph REST API to obtain data from a Teams' drive. 

Visit the [Skimo Website](https://skimo.tv/) to test functionality. 

## Functional Capabilities
**FULL ELABORATION FOR FUNCTIONS LISTED IN NEXT SECTION**

Allow users to login to Microsoft account using OAuth 2.0

Retrieve a list of all Items in a User's OneDrive

Retrieve a list of calls from a specific folder in OneDrive

Display a list of teams calls on the skimo website for the user

Allow user to select a recording and upload recording to the Skimo server

# Specific Functions 
For each function - summarize step by step how the function works at a user level (UI inputs outputs)
                  
                  - summarize the code used to achieve said functionality 
## Microsoft Login using OAuth 2.0
Must use a registered Microsoft work/school account

## Retrieving List of all items in OneDrive 
Use GET https://graph.microsoft.com/v1.0/me/drive/root/children : *will produce a list of items in Drive containing the **driveId** and **itemId***

## Retrieving List of calls in a folder in OneDrive
Use GET https://graph.microsoft.com/v1.0//drives/{drive-id}/items/{item-id}/children : *insert **driveId** and **itemId** from prev step* 

## Display List of Calls in Skimo

## Teams Call Select and Upload 

# Contributing and Support
We'd love that you contribute to the project. Before doing so, please contact admanchi1@gmail.com for more info. 
