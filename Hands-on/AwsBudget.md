# This hands on is to preserve/control the cost incurred during our learning on aws, and alert us on budget cross

# <center> Billing Board 
## give access of billing dashboard to admin account from root user account

1. open root account console -> Click on username on top right corner -> choose `Billing Dashboard`
2. open section `IAM User and Role Access to Billing Information` -> click on edit icon
3. choose `Activate IAM Access` -> Click update
4. Go back in to admin console.. and recheck the dashboard
---
## Setting Budget Limit on our account

1. admin console -> click on your username -> Billing Dashboard -> From side panel, select Budgets -> hit `create a budget`
2. choose type as `cost budget` ->hit next
3. Under recurrence, hit `monthly` (choose monthly payment) -> on how to budget, choose `Fixed`, under amount, enter the max amount that you can spend -> Lastly enter a name for your budget and hit next 
4. Configuring Alerts -- what to do when we reached end of our budget
   1. create a thershold
   2. when you reach 80% of your budget, send emails 
5. for each thersholds, you need to attach actions to thresholds ->click next
6. review -> create