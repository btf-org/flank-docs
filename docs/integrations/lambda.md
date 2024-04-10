# AWS Lambda
To expose your SQL Server stored procedure or function on Flank, follow these steps.
## 1. Create a role for Flank in AWS
   1. Navigate to IAM
   2. Create new role
   3. Select AWS Account for Trusted entity type
   4. Select Require external ID. Name the external ID whatever you’d like.
   5. Select AWSLambda_FullAccess
   6. Create role

## 2. Add your resource for the first time
   1. Navigate to Flank and click Add Resource, then AWS
   2. Nickname - Anything you want
   3. Fill in your newly created role’s arn
   4. Fill in your newly created role’s external Id
   5. TODO - S3
   6. Add resource

## 3. Add your Lambda to Flank
   1. Sync Commands
   2. Click on your newly added resource
   3. Choose which lambdas you’d like to add
   4. Add to my workspace

## 4. Configuring your command

## 5. Running your command

## 6. Share your command

## 7. See its history
