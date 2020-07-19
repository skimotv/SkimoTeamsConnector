# Flow of Code for SinglePageButton Directory
##### The following explanation limits the summarization of the code to information only pertininent to users wanting to modify which endpoints and subsequent data are obtained and displayed from the Microsoft Graph REST API
## authConfig.js
**loginRequest** - ID token for Microsoft Identiy Platform Endpoints

**tokenRequest** - Access token for Microsoft Graph API Endpoints: *modify scopes as given in the Microsoft Graph Explorer*

## authPopup.js
Information about user validation availble at [this link](https://docs.microsoft.com/en-us/azure/active-directory/develop/tutorial-v2-javascript-auth-code) under section titled "How this Code Works" (towards bottom of page)

**function seeProfile() & readMail()**  - call the function **callMSGraph** defined in **graph.js**

**callMSGraph** requires 3 parameters -  **endpoint, token, and callback**

The **token** is obtained from the access token given in the **getTokenPopup** response 

### graphConfig.js
Contains information for the first parameter of **callMSGraph**, the **endpoint**

Allows user to add endpoints as needed for Microsoft Graph API services

Ex: **https://graph.microsoft.com/v1.0/me** - returns JSON response of information about user 

### ui.js
Contains information for the third parameter of **callMSGraph**, the **callback**

**function updateUI(data, endpoint)** - updates the response on the website based on which endpoint was selected

This is the function passed in as the **callback**

## index.html
Calls the **signIn()** method from **authPopup.js** as well as additional methods used to format information from the endpoints 

    *For now, these additional methods are seeProfile() and readMail*


