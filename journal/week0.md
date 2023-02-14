# Week 0 — Billing and Architecture


**Link to Architecture Diagram AND Logical CI/CD Pipeline:**

https://lucid.app/lucidchart/a27a7347-3fd1-4422-be66-ce63b2910602/edit?viewport_loc=-598%2C-226%2C3328%2C1582%2C0_0&invitationId=inv_658cd443-fb66-4a82-8610-86e75e99028c

**Conceptual Diagram on a Napkin:**


![WhatsApp Image 2023-02-14 at 09 40 32](https://user-images.githubusercontent.com/63907253/218699317-a8b89bfa-8979-4121-853b-16c6a1cb422f.jpeg)


**Root user has MFA enabled and no active access keys:**

![image](https://user-images.githubusercontent.com/63907253/218700277-48664ce3-88da-4caf-8b34-244ec4648f98.png)

**Two Budgets created:**

One **_Zero Spend Budget_** (notifies me once my spending exceeds 0.01 USD which is above the AWS Free Tier limits).

One **_Monthly Cost Budget_** (when the actual cost is greater than 85.00% (8.00 USD) of my budgeted amount (10.00 USD), the alert threshold will be exceeded. Also, there is a second alert for a _forecast_ of reaching 100% of the budget amount, and finally a third alert when exceeded over 100% of the full budget amount).

![image](https://user-images.githubusercontent.com/63907253/218704260-08928d80-879b-4647-96fd-3ac3cbdf6bee.png)

**Billing Alarm created:**

**_AWS Bootcamp DailyEstimatedCharges_**. Alarm condition - if the threshold value is greater than 1.5 USD for a period of 1 day.

![image](https://user-images.githubusercontent.com/63907253/218708396-913100f1-49a0-47e2-9c62-5e9e311ecd78.png)

User created named **_Bishop_** and added to the **Admin** User Group which was also created in this account. **'AdministratorAccess'** and **'Billing'** AWS defined policies have been attached to the Admin group and therefore also attached to the user:

![image](https://user-images.githubusercontent.com/63907253/218709710-2348eb2e-a89c-4868-bdcd-44eddf947deb.png)

**MFA** is also enabled for the user alongside a **Secret Access Key** and **Access Key ID** (exported .csv file locally).
