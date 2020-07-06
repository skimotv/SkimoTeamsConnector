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

Retrieve a list of teams that the user is a member of

Retrieve a list of items in the selected team's drive 

Retrieve a list of calls from the items in the drive

Display a list of teams calls on the skimo website for the user

Allow user to select a recording and upload recording to the Skimo server

# Specific Functions 
For each function - summarize step by step how the function works at a user level (UI inputs outputs)
                  
                  - summarize the code used to achieve said functionality 
## Microsoft Login using OAuth 2.0
Must use a registered Microsoft work/school account

## Retrieving List of Joined Teams  
Use GET https://graph.microsoft.com/v1.0/me/joinedTeams : *will produce a list of joined teams containing the **team id***

## Retrieving List of Items in Team Drive 
Use GET https://graph.microsoft.com/v1.0/groups/{group-id-for-teams}/drive/root/children : *the **group id** will be the **team id** obtained prev.* 

## Retrieve List of Calls from Items 

## Display List of Calls in Skimo

## Teams Call Select and Upload 

# Contributing and Support
We'd love that you contribute to the project. Before doing so, please contact admanchi1@gmail.com for more info. 
