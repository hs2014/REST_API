# Apex REST API Quick Start
##Introduction: 
Salesforce out-of-box SOAP and REST APIs contains all generic methods and calls to help developers connect their apps to Salesforce. However, there are situations when some business logic or a transaction needs to be written in Salesforce as a code and needs to be exposed as a web-service to ease integration and keeping business logic centralized. 

You can expose your Apex class and methods so that external applications can access them using the REST architecture. Following steps are required to accomplish this: 

1. Defining your class with @RestResource annotation, thus exposing it as a REST Resource
2. Add annotations to your specific methods, e.g. @HttpGet to expose them as REST methods. 

##Create an Apex Class and Method 

1. Login into your Salesforce Developer/Sandbox Org
2. Open Developer Console by clicking on your name on top-right and selecting Developer Console.
3. Click on File | New | Apex Class
4. Give your class a name HelloWorld
5. Type in the code below. This simulates a usual Apex class for a simple logic of returning a concatenated string
6. Save your code

##Convert your class to be a REST Resource

1. Mark your class and method Global
2. Add @RestResource annotation to the class. This step also requires you to add a URL to your class. This would be the URL that external applications would use to access your REST Resource
4. Add @HttpGet annotation to your method as external applications would access it via a GET request
5. You need to remove the parameter from the method as @HttpGet annotation cannot handle
6. See screenshot below for the end-result 

##Test the webservice using Workbench

1. Navigate to workbench and select Production if you are using a developer org, or select sandbox if you are using a sansbox. 
https://workbench.developerforce.com/
2. Accept the terms of service and proceed to Login 
3. Once logged in, select REST Explorer, and click Select
4. Once in the REST screen, type your REST webservice URL and provide the parameter as well. 
5. The result shows the string concatenated with the parameter. The web-service is successfully working ! 

##Summary 

In this exercise, you learnt how to create a REST Web Service and covered: 

1. create a Apex class with a simple method
2. convert that class to expose it as a REST resource and method
3. test it using Workbench. 

The class can contain complex business logic and can also pass complex data parameters as well. 

##References

Force.com Apex Developer Guide 



