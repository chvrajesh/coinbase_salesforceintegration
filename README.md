# coinbase_salesforceintegration

#Salesforce Work

Step 1: Create a Platform Event and add the custom fields to the Platform event. 

Step 2: Create the 'callAWSApiGateway' Apex Trigger and attach it to the Platform event created in step 1

Step 3: Create an Apex Class 'AWSCallout'

Step 4: Create a process builder, attach the case object and create an action that publishes the case whenever new case is created.


#AWS Work

Step 1: Create an S3 bucket with name 'coinbase-salesforce-caseInfo'

Step 2: Create a custome Role with s3PutObject role

Step 3: Create a lambda function with the code attached and assign the role to the funtion

Step 4: Create an api gateway

          API type: REST

          Authorization: NONE
          
          Method: POST
          
          Resource path: /savecase
          
          Stage: coinbaseStage

Step 5: Attach the api gateway to the lambda trigger

Step 6: Update the API gateway endpoint in Salesforce Apex Class 'AWSCallOut'

Step 7: Add a new remote site in Salesforce with the AWS API end point
 
