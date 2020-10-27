# Managing Access Policies for data engineers
Deploy:

1. Navigate to the Cloudformation page on your AWS console
2. Click on create stack -> with new resources
3. Upload the file and follow the instructions to deploy

To test:

1. With admin access, create a user and add it to the group iam-group-data-engineer
2. Log in to your AWS panel with the credentials of that new user who has been added to the group.
3. Click on your user name in the top right menu
4. Click on Switch Roles
5. Fill in the fields:
    i. Account: your AWS account number (12 digits)
    ii. Role: role-production-data-engineer
    iii. Display Name: choose as you want ex: Data Engineer

Now that user has assumed the role role-production-data-engineer and only has the permissions described within the 
IamPolicyDataEngineer policy.

Use this to separate permissions for different groups of users: Analysts, Developers, Data Scientists, Admins, etc.