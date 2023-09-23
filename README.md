<p align="center">
<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
</p>
<h1 align="center">C4_deployment-3.1<h1> 

The Story
-----------------------------------------
We’re a tech start-up company with a URL shortener tool. We have a SLA with Nike to provide them access to our URL shortener. In the SLA, we are only allowed 20 minutes of downtime a year. If anything happens to the URL shortener, we must communicate any incidents to Nike.
 
Scenario
-----------------------------------------
A new hire was tasked with updating the URL shortener. The new hire committed version 2 of the application to the main branch. Which automatically triggered a build, test, and deploy to the production server, replacing version 1 of the application running on the server.

Post-incident report 
-----------------------------------------
- What was the reason for the incident?

 --The reason for the incident was a commit performed by a new hire of Version 2 of the application to the main branch, which triggered a Build, Test, Deploy to the
production environment, which replaced Version 1 of the application.  

- How long was the site down or malfunctioning?

The site malfunctioned for approximately 5 minutes from discovery to resolution.
  
- What steps were taken to resolve the incident?

--Step 1: Initial report of the incident and information gathering; initial options were to rollback or troubleshoot; troubleshooting was selected

--Step 2: Logged into the AWS instance and requested the error logs (last 100 rows), found errors relating to JSON

--Step 3: Look into the application.py file, look at the JSON configurations, and found an error with the syntax

--Step 4: Fixed the error and redeployed the application via Jenkins

- Was the incident fully resolved?

Yes, the error was fully resolved, and the application functioned properly.  Nike was notified of the incident and we will present a full Root Cause Analysis (RCA) 

- What steps would you take to prevent this from happening again?
  
-Include a review process of all code changes to ensure proper functioning before deployment

-Rollback instead of troubleshooting to reduce downtime.

-Restrict new hire ability to push changes to production.

  
