1. Root Account > AWS Console Home > IAM > User Groups -- Here you will see list of users present in your console
2. Now open an incognito tab, login to any admin user > AWS Console Home > IAM > Users -- This is present in admin console
3. Now From Root Account console, take a user and click on `Remove User` for which the group permission are removed for that user
4. IN Admin Account, reload that page which will throw permission issue
5. After above, undo the operation by clicking on that user > Add permissions > Add from exisiting policy > select `IAM read only  access`
6. Now again reload the Admin console, which will show you the page without any permissions issue
7. lets check a false case here, from the admin console > IAM > user Groups > click on `create group`.. this time you will face the permission issue again
---
## Attaching Policies to a user via direct attach

1. open AWS Console Home > IAM > Users > choose your user > then hit `Add Permission`, in the permission tab, you can directly attach the permission or policies directly to a user
---
## Attaching Policies to a user via groups

1. open AWS Console Home > IAM > User Groups > create a group called "Developers"
2. Furthur you will see the option to add the policies that has to be present to new group
3. Now add users to group where each user in group will inherit the policy of group
`A user having direct policies and group policies will inherit both`
---
## Creating our own Policy 

1. IAMConsole > Policy > hit `create policy` > Use Visual Editor for more simplicity (you can use json editor to create directly)
2. In services section, choose the services that you want to access
3. In Actions sections, choose the allowable actions you need
4. In Resources, you can pinpoint your resources access or specify all
5. In Request Condition, you can specify condition when to give access and revoke
6. Once you add all of your things in visual editor, you can see json editor to see json form of your policy
7. Save it for furthur use
---
## AWS Cli Hands on

### Creation of access keys (dont use your root account but only admin account)
IAM home -> Users -> click on `Security Credentials` tab -> Click on `Create access keys` -> Download your keys

### Now to Set your local aws cli with your account,
hit command on your terminal

    aws configure

Enter access key, secret key and your aws desired location to complete the setup. To Test the configuration, type

    aws iam list-users

This command should show the list of all users present in your aws account

---
## IAM Handson

1. IAM Home -> ROles -> Click on `create role`
2. choose `AWS Services` -> from Use Case section, choose `EC2` -> Next
3. Now in policy section, you need to attach the necessary policy to your ec2 instance, choose `IAM Read Only Access` -> Next
4. give a role name -> finally click `create`

---

## IAM Credentials Report
IAM Home -> Credentials Report -> click on `Download Report` . Youll get a csv files with list of all users and their info and their status of passwords

---

## IAM Access Advisor
IAM Console -> Choose any User -> click on tab `Access Advisor`