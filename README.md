# golang-serverless-aws-lambda-rest-api-read-optimized
Rest apis in GoLang - MongoDB Dynamic Data READ Optimized - AWS Lambda Serverless

![golang-rest-apis-read-optimized](https://user-images.githubusercontent.com/102517671/206923009-18d5619c-3f34-44c6-a82d-f346e1e4efd1.png)

RESTful apis for optimizing read operations - Go Lang + MongoDB Integration via native driver + AWS Lambda - No Framework or Third party library used

- Create A Lambda function with Go Runtime :  Go 1.x
- AWS Lambda function :   main.zip </BR>
- Just upload "main.zip" to AWS Lambda directly via Lambda Code mangement console</BR>
- Configure lambda handler as:    main. </BR>
- Configure environment variable for MongoDB: </BR>

Environment Variable in AWS Lambda for MONGO_DB_URI = "{connection string}" </BR>
MongoDB Atlas is a great option for managed cloud mongodb cluster to start with - Free Tier is available </BR></BR>
Environment Variable in AWS Lambda for MONGO_DB_NAME = "{db name}"

How to configure?: https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html"

Dynamic E-Route to get the data from any collection from MongoDB Database with minimum latancy. both for Cold Start Time + Init Time. Execution time is also optimized to return the data from database in minimum time. No Framework OR Any Third party libray is used. MongoDB Integration is added using mongodb native driver for javascript. Complete pagination, filter and specific returned fields options for dynamic read e-Route without any changes to backend

</BR>

Golang Compiled to native binaries for Linux provide a very high-performance execution time compared to any other language for aws lambda serverless </BR>

[ GET ] /api/e/users?page=1&limit=10 </BR>

[ GET ] /api/e/users/6382c5ab8bfe8614c6d0df19 </BR>


</BR></BR>


We can use MongoDB Atlas Cloud managed solution - [Free Shared Instance](https://www.mongodb.com/blog/post/free-your-genius-on-mongodb-atlas-free-tier)
</BR></BR>
**e-Route** </BR>
Connect an API gateway with $default stage and only one route GET /{proxy+}: </BR>
Following Routes are available to access the resources from db: </BR>
[ GET ] /api/e/{entity} </BR>
[ GET ] /api/e/{entity}/{id} </BR>
</BR>
**READ**: Any Entity as json request can be read from the MongoDB database </BR>


</BR> **Working On** </BR>
- JWT authorization via:
  - APIGateway Authorizer for generic proxy route
  - Custom implementation is pretty much dynamic. Using JWT Library dependency but it may add an additional cold start time for boot up.
- </BR> CI/CD for one-click/command deploy updates to Lambda func 

</BR>Any Feedback, suggestion, improvisation is welcomed</BR>

</BR></BR>
**Created By**, </BR>
Furqan </BR>
(Software Developer / Solution Architect) </BR></BR>
