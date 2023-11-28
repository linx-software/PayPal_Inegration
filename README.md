# PayPal Reporting Integration - Linx 

  

## Description 

This repo contains a Linx 6 solution that shows how you can integrate with the [PayPal REST API](https://developer.paypal.com/api/rest/). The sample contains 3 functions. One to authenticate, one to get all balances and one to get all transactions. You can add additional calls as required. You can create a [Sandbox account](https://developer.paypal.com/api/rest/sandbox/accounts/#link-createapersonalsandboxaccount) to test with.   

You can download this sample and manipulate it to suit your integration using [Linx 6](https://linx.software/). 

  

## Installation 

This is a Linx 6 solution, so you will need an installed version of the [Linx 6 designer](https://linx.software/) to work on this solution and to add in your own logic.  

 

## Usage 

 The solution has the following settings that needs to be set: 

- PayPal_ClientID: Your PayPal client ID 

- PayPal_ClientSecret:  Your PayPal client secret. 

- PayPal_BaseURL: The Base URL for the PayPal API. You can use https://api-m.sandbox.paypal.com to test on the sandbox. Else you will need to use the official PayPal API 

  

The solution has 3 main functions: 

  

#### PayPal_Authenticate: 

This function will get the access token by sending the client ID and client secret. The token is combined with the token typ (bearer) and is returned as the return parameter which is used in all other calls to the API.  

#### PayPal_Get_Reporting_Balance:   

This function will get the access token by calling the PayPal_Authenticate and will then call the Balance endpoint. It is perfect for retrieving all balances. You can add additional parameters to filter your results – view options on the official documentation linked above.  

#### SendMessage_Interactive 

This function will get the access token by calling the PayPal_Authenticate and will then call the Transactions endpoint. It is perfect for retrieving all transactions between two dates. The Start_date and End_Date parameters must be entered, and they must be in [Internet date](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6) format (for example 2022-02-20T23:59:59.999Z). You can add additional parameters to filter your results – view options on the official documentation linked above. 

 

 

## Contributing 

For questions please ask the [Linx community](https://linx/software/community). 

  

## License 

[MIT](https://github.com/linx-software/template-repo/blob/main/LICENSE.txt) 

 
