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

![honeycomb (1)](https://user-images.githubusercontent.com/117948251/224611533-f03ef706-2bbf-4291-9e83-6bb59a8c6862.png)


### **added additional ports in our gitpod.yml file so they open automatically:**
- The gitpod.yml file is used to configure the Gitpod workspace.
- adding additional ports to the gitpod.yml file, I can automatically open these ports when the workspace is launched. 
- This can be useful for running applications that require specific ports to be open.

```
ports:
  - name: frontend
    port: 3000
    onOpen: open-browser
    visibility: public
  - name: backend
    port: 4567
    visibility: public
  - name: xray-daemon
    port: 2000
    visibility: public
```


### **instrumented AWS X-Ray with the help of the video:**
- AWS X-Ray is a service that allows you to trace requests across multiple services and applications. 
- By instrumenting AWS X-Ray, you can get a detailed view of how requests are flowing through your system and identify any bottlenecks or issues.
- Watching the video helped me understand how to instrument AWS X-Ray for distributed tracing.

- From this I was able to create an xray group and sampling rule though this;

![created xray group_edit_226363907194625](https://user-images.githubusercontent.com/117948251/224612400-02f1cd32-a281-45e1-ba52-2ac040aa52c5.png)

![created a sampling rule_edit_226168859229030](https://user-images.githubusercontent.com/117948251/224612415-ee975d58-b7d3-4d0a-b544-70b4d2728319.png)

- I was initally unable to recieve data in aws xray, but that was fixed as it seemed that I had not added "logger" to my code as shown below;

![data not showing fixed_edit_226441187909718](https://user-images.githubusercontent.com/117948251/224612716-774bc80f-0491-4d2d-9eb4-58e038119d67.png)

- I could later see the following data in the aws console.

![can see data_edit_226385822473268](https://user-images.githubusercontent.com/117948251/224612947-e8fc0162-6a2c-4c5e-8cf4-bd1ac7a0e538.png)

### **tried to configured the custom logger to send to cloud watch logs:**
- Configuring a custom logger to send logs to CloudWatch, allows me to centralize my log data and use CloudWatch's built-in tools to analyze and troubleshoot issues. 
- This can help you to identify and fix problems in your system more quickly.


### **Integrated Rollbar and capture and error:**
- Rollbar is an error tracking and monitoring tool. 
- Integrating Rollbar into the application, you can capture errors and exceptions that occur and receive alerts when they happens.
- This helps to quickly identify and resolve issues in your code.

Import for Rollbar

```py
import rollbar
import rollbar.contrib.flask
from flask import got_request_exception
```

```py
rollbar_access_token = os.getenv('ROLLBAR_ACCESS_TOKEN')
@app.before_first_request
def init_rollbar():
    """init rollbar module"""
    rollbar.init(
        # access token
        rollbar_access_token,
        # environment name
        'production',
        # server root directory, makes tracebacks prettier
        root=os.path.dirname(os.path.realpath(__file__)),
        # flask already sets up logging
        allow_logging_basic_config=False)

    # send exceptions from `app` to rollbar, using flask's signal system.
    got_request_exception.connect(rollbar.contrib.flask.report_exception, app)
```

### **tested the Rollbar integration:**
- Testing the Rollbar integration ensures that Rollbar is set up correctly and is capturing errors as expected. By testing the integration
- also ensures that I receive alerts when errors occur and that you can use Rollbar's tools to troubleshoot and fix any issues.



