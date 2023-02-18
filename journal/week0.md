# Week 0 — Billing and Architecture

## The following is what I managed to get done in Week 0:

### **- I created a new AWS account and an IAM admin user:**
This was my first step towards setting up my AWS infrastructure. An AWS account is required to access AWS services and an IAM admin user is needed to manage access and permissions for your account.
![iam user](https://user-images.githubusercontent.com/117948251/219868692-e38d7f0c-eceb-42e5-9bd0-fd7f837540a8.png)

### **- Set up MFA on my root account:**
Multi-factor authentication (MFA) adds an extra layer of security to your AWS account by requiring a code from my mobile device in addition to my password when logging in. It's a best practice to enable MFA on all accounts, especially the root account which has full access to my AWS services.

![root mfa_edit_53855399279281](https://user-images.githubusercontent.com/117948251/219868794-3d1fd1ed-e22d-46e2-97c9-9ae3c239a69d.png)

### **- Recreated the Cruddur Logical diagram in Lucid:**
A logical diagram is a visual representation of the architecture and design of the Cruddur application. 
[link] (https://lucid.app/lucidchart/34eced2d-27b2-4fed-9844-1212bd049720/edit?viewport_loc=-553%2C353%2C2692%2C1054%2C0_0&invitationId=inv_92dc6832-e9f3-4057-badc-2c71d95f5c8e)

![diagram recreation_edit_53805464383976](https://user-images.githubusercontent.com/117948251/219868808-c2bbaee4-bcd7-4feb-8792-a07a2930c5cc.png)

### **- Created a conceptual napkin design:**
A conceptual design is an overview of the high-level architecture and functionality of a system or application. This can be used to communicate the vision and goals of the project to stakeholders and to guide the development process.

![IMG_20230216_170254_edit_54328256787542-01](https://user-images.githubusercontent.com/117948251/219869095-5fa50151-c99d-4654-9a39-329fa444f083.jpeg)

### **- Installed AWS CLI:**
The AWS Command Line Interface (CLI) is a tool that allowed me to interact with AWS services from GitPod. Allowing me to further commit to my GitHub.

![cli installed_edit_53828576510014](https://user-images.githubusercontent.com/117948251/219868840-f106f02d-509d-42fb-a10a-883543d9bd88.png)

### **- Encountered an error when committing to Gitpod and fixing it:**
When working with Gitpod, I encountered an error related to permissions when trying to push changes to your GitHub repository. In this case, editing the GitHub permissions in Gitpod's settings can solved the problem.

![IMG_20230218_153057_edit_53790042549083](https://user-images.githubusercontent.com/117948251/219868873-3d3e6025-d85a-4fe5-9c30-e955633e47a4.png)

### **- Created a budget and a billing alert in the AWS console: **
AWS charges for the resources you use, so it was important for me to set up a budget to monitor my spending and avoid unexpected charges. I also set up alerts and notifications for when you reach a spending threshold of $10, as well as track my spending over time.

![budgets_edit_53874305119903](https://user-images.githubusercontent.com/117948251/219868856-030bad7c-4d35-449a-8086-27a21f22ae1d.png)

### **- Generated AWS credentials:** 
AWS credentials are used to authenticate my requests to AWS services. They consist of an access key and a secret access key, which should be kept secret and not shared with others - this is why I won't be providing proof of this. 

