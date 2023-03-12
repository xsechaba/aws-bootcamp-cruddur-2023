# Week 2 — Distributed Tracing

## The following is what I managed to get done in Week 2:

- Instrumented Honey with OTEL with a minor tasks like setting honey environmental variables, flask instrumentation to send data to honeycomb 
- added additional ports in our gitpod.yml file so they open automatically 
- instrumented AWS X-Ray with the help of the video 
- tried to configured the custom logger to send to cloud watch logs 
- Integrated Rollbar and capture and error 
- tested the Rollbar integration 

### **Instrumented Honey:**
- By instrumenting Honeycomb with OTEL, I can track and monitor the performance of my applications and infrastructure, as well as troubleshoot any issues that arise.
- Setting Honey environmental variables and flask instrumentation help to send data to Honeycomb for analysis and tracking.


### **added additional ports in our gitpod.yml file so they open automatically:**
- The gitpod.yml file is used to configure the Gitpod workspace.
- adding additional ports to the gitpod.yml file, I can automatically open these ports when the workspace is launched. 
- This can be useful for running applications that require specific ports to be open.


### **instrumented AWS X-Ray with the help of the video:**
- AWS X-Ray is a service that allows you to trace requests across multiple services and applications. 
- By instrumenting AWS X-Ray, you can get a detailed view of how requests are flowing through your system and identify any bottlenecks or issues.
- Watching the video helped me understand how to instrument AWS X-Ray for distributed tracing.


### **tried to configured the custom logger to send to cloud watch logs:**
- Configuring a custom logger to send logs to CloudWatch, allows me to centralize my log data and use CloudWatch's built-in tools to analyze and troubleshoot issues. 
- This can help you to identify and fix problems in your system more quickly.


### **Integrated Rollbar and capture and error:**
- Rollbar is an error tracking and monitoring tool. 
- Integrating Rollbar into the application, you can capture errors and exceptions that occur and receive alerts when they happens.
- This helps to quickly identify and resolve issues in your code.


### **tested the Rollbar integration:**
- Testing the Rollbar integration ensures that Rollbar is set up correctly and is capturing errors as expected. By testing the integration
- also ensures that I receive alerts when errors occur and that you can use Rollbar's tools to troubleshoot and fix any issues.

