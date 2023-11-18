# Hosting a Full-Stack Application

### Using Udagram app

---

In this project you will learn how to take a newly developed Full-Stack application built for a retailer and deploy it to a cloud service provider so that it is available to customers. You will use the aws console to start and configure the services the application needs such as a database to store product information and a web server allowing the site to be discovered by potential customers. You will modify your package.json scripts and replace hard coded secrets with environment variables in your code.

After the initial setup, you will learn to interact with the services you started on aws and will deploy manually the application a first time to it. As you get more familiar with the services and interact with them through a CLI, you will gradually understand all the moving parts.

You will then register for a free account on CircleCi and connect your Github account to it. Based on the manual steps used to deploy the app, you will write a config.yml file that will make the process reproducible in CircleCi. You will set up the process to be executed automatically based when code is pushed on the main Github branch.

The project will also include writing documentation and runbooks covering the operations of the deployment process. Those runbooks will serve as a way to communicate with future developers and anybody involved in diagnosing outages of the Full-Stack application.

# Udagram

This application is provided to you as an alternative starter project if you do not wish to host your own code done in the previous courses of this nanodegree. The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.

## Getting set up
- clone the project - `git clone https://github.com/huynhbacong/nd0067-c4-deployment-process-project-starter.git`

### Dependencies

```
- Node v16.20.2

- npm 8.19.4

- AWS CLI v2

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres. <Place holder for link to classroom article>
1. In AWS, provision a s3 bucket for hosting the uploaded files. <Place holder for tlink to classroom article>
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## Deploy 
### Configures
- [Circle CI configuring file](.circleci/config.yml)
- [Package json root file](package.json)

### Link to this hosted working frontend application:
- http://cong-udagram.s3-website-us-east-1.amazonaws.com/

## Screenshots 
- Last successful CircleCi build 
    1. [Build image](screenshots/build-success.png)
    1. [Build - hold - deploy flow image](screenshots/build-hold-deploy.png)
    1. [Deploy image](screenshots/deploy-success.png)

- AWS 
    1. [AWS RDS database overview image](screenshots/aws-rds-database-overview.png)
    1. [AWS ElasticBeanstalk image](screenshots/aws-eb-overview.png)
    1. [AWS S3 image](screenshots/aws-s3-overview.png)

## Documents
- An architecture diagram showing a high-level overview of the infrastructure [architecture diagram](docs/Udacity-highlevel-architecture.drawio)
- A diagram showing the overview of the pipeline [pipeline diagram](docs/pipeline-flow%20(1).drawio)
- [Infrastructure_description.md](docs/Infrastructure_description.md)
- [Pipeline_description.md](docs/Pipeline_description.md)
- [Application_dependencies.md](docs/Application_dependencies.md)