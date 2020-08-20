﻿# AzureFunctionNoiseMaker

## What is this?
This is a simple Azure Function that simply makes (HTTP) Noise.
This "HTTP Noise" includes 200 "I'M OK 😁", 404 "I'M NOT FOUND 😲" and my personal favourite 418 "I'M A TEA POT 🍵".

## Purpose
I use this in conjunction with Azure Monitor Alerts so that i can test my [Action Group actions](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/action-groups). (such as webhooks, logic apps, other azure functions etc.)  

## How to use...
### ...to Specify "HTTP Noise"
The Az Funciton accepts query string parameters to chagne the return Status Code.

### ...to Trigger Alerts
After deploying funciton to Azure. I use a [PostMan](https://www.postman.com/) Collection so have a easy way to fire off a couple API calls. 
I have created Alerts linked to the Application Insights resouce with the condition set to Server Requests and specify the code i want. 
