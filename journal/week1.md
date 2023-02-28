# Week 1 — App Containerization

## The following is what I managed to get done in Week 1:

with the help of the videos, I:
- first added the docker extention to my gitpod
- containerized the app, both the backend and the frontend
- documented the notification endpoint of the Cruddur application
- Wrote the react page for the notification section of Cruddur
- Ran DynamoDB and Postgres Container

### **first added the docker extention to my gitpod:**
- The Docker extension is added to Gitpod to enable the creation and management of Docker containers directly from the Gitpod IDE. 
- This is important because Docker containers are lightweight and provide a consistent environment for developing and deploying applications. 
- By adding the Docker extension, I can easily create and manage containers without leaving the Gitpod IDE. 
- This helps to streamline the development process, making it faster and more efficient.

![docker extension-cropped](https://user-images.githubusercontent.com/117948251/221643253-6e461bfe-e3b2-488a-937e-95193c96c9ad.png)

### **containerized the app, both the backend and the frontend:**
- Containerizing the app involves packaging the application code and its dependencies into Docker containers.
- This is important because it allows the application to run consistently and reliably across different environments, such as development, testing, and production. 
- Containerizing the backend and frontend of the app, it makes it easy for me to deploy the app on any infrastructure that supports Docker, such as Kubernetes. 

**1. Backend verification:**

![backend containerize](https://user-images.githubusercontent.com/117948251/221643897-f95bbd2e-f243-4eef-b392-6c59ff806ddc.png)

**2. Frontend verification:**

![frontend verify-cropped](https://user-images.githubusercontent.com/117948251/221646241-331da8d6-ec5b-40ac-9f13-90066c79a3eb.png)

### **documented the notification endpoint of the Cruddur application:**
- Documenting the notification endpoint of the Cruddur application is important for several reasons. 
- First, it provides clear instructions on how to use the notification endpoint, making it easier for other developers to integrate with the application. 
- This can help to reduce the time and effort required to implement notifications in other applications. 
- Second, documenting the endpoint helps to ensure that the endpoint is used correctly and securely, helping to prevent security vulnerabilities that could compromise the application or its data.

```
/api/activities/notifications:
    get:
      description: 'Return a feed activity for people I follow'
      parameters: []
      responses:
        '200':
          description: returns an array of activities
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Activity'
```

### **Wrote the react page for the notification section of Cruddur:**
- This provides a user-friendly interface for managing notifications in the cruddur application. 
- By using React, this allows me to easily create dynamic and interactive user interfaces that are responsive to user input. This can help to improve the user experience and make the application more engaging. 
- Additionally, writing the React page for the notification section can help to identify and fix issues with the notification system, such as incorrect or inconsistent behavior, so they can be fixed - which happened.

![notifications page](https://user-images.githubusercontent.com/117948251/221648871-df9feaf5-d367-44e7-b2f8-702fa0454685.png)

### **Ran DynamoDB and Postgres Container:**
- Running DynamoDB and Postgres containers is important because it provides a consistent and isolated environment for testing and developing the application. 
- By running these databases in Docker containers, I can easily set up and tear down the databases as needed, without affecting the host system. This can help to reduce the risk of conflicts or compatibility issues with other applications running on the same system. 
- Running databases in containers can help to improve the scalability and resilience of the application, as multiple instances of the same container can be run simultaneously.

![postgress verify-cropped](https://user-images.githubusercontent.com/117948251/221651581-1217e617-55d9-4f73-92de-924ef6e92ec5.png)
