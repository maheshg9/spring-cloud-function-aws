# Going serverless with Spring Function and AWS

Sample demo project to show the use of sprint cloud functions, create lambda function, deploy on AWS and write data to Dynamo DB. 
This project is part of an blog post that can be found in the link 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* Java JDK 8
* [Serverless Framework](https://www.serverless.com/framework/docs/providers/aws/guide/installation/) - The framework used for deploying the application
* [AWS CLI] (https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) - setup aws cli

### Installing

* Get the project from GIT
* Get amazon accesskey from your AWS account and set the value in project -> application.properties -> amazon.aws.accesskey
* Get amazon secretkey from your AWS account and set the value in project -> application.properties -> amazon.aws.secretkey
* Go to root of the project and run ".\mvnw clean package" - this will build the jar file

When the deployment process finish successfully as a result of the serverless deployment process link for the POST api gateway, we will use the link to trigger the aws lambda function

## Running the tests

.\mvnw clean package - command for running the junit tests

Junit test will start the project locally and trigger the function

## Deployment

serverless deploy --region us-east-1 --aws-profile YOUR_PROFILE - this command will start deploy the spring function on AWS, replace the YOUR_PROFILE with the "/.aws/credentials" file that is used for setup the AWS cli

## Built With

* [Spring Cloud Functions](https://spring.io/projects/spring-cloud-function)
* [Maven](https://maven.apache.org/) - Dependency Management
* [Serverless Framework](https://www.serverless.com/framework/docs/providers/aws/guide/installation/)

## Demo



## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

* **Nikola Popovski** - *Initial work* - [PurpleBooth](https://github.com/popovski)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details