# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:
1. [The Simple Frontend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-frontend)
A basic Ionic client web application which consumes the RestAPI Backend. [Covered in the course]
2. [The RestAPI Backend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-restapi), a Node-Express server which can be deployed to a cloud service. [Covered in the course]
3. [The Image Filtering Microservice](https://github.com/udacity/cloud-developer/tree/master/course-02/project/image-filter-starter-code), the final project for the course. It is a Node-Express application which runs a simple script to process images. [This assignment]

## Tasks done as part of this project

### Setup Node Environment

Created a new node server. Open a new terminal within the project directory and run:

1. Initialize a new project: `npm i`
2. run the development server with `npm run dev`

### Created a new endpoint in the server.ts file

Completed an endpoint in `./src/server.ts` which uses query parameter to download an image from a public URL, filter the image, and return the result.

Used the helper functions to handle some of these concepts and those are imported at the top of the `./src/server.ts`  file.

```typescript
import {filterImageFromURL, deleteLocalFiles} from './util/util';
```

Local run console message:

![Alt text](/deployment_screenshots/local-npm%20run%20dev-console.png "local-npm run dev-console")

Local run Postman Response:

![Alt text](/deployment_screenshots/local-npm%20run%20dev-response.png "local-npm run dev-response")

API Response of invalid request:

![Alt text](/deployment_screenshots/error%20handling.PNG "error handling")


### Deploying the system

Follow the process described in the course to `eb init` a new application and `eb create` a new environment to deploy your image-filter service! Don't forget you can use `eb deploy` to push changes.

EB environment after eb create:

![Alt text](/deployment_screenshots/ElasticBeanstalkDeployment.PNG "ElasticBeanstalkDeployment")


<b>Link to access:</b> 

http://udacity-udagram-dev.ap-south-1.elasticbeanstalk.com/filteredimage?image_url=https://upload.wikimedia.org/wikipedia/commons/c/c7/HEART.jpg

API Response of deployed app:

![Alt text](/deployment_screenshots/AWS%20deployed%20response.png "AWS deployed response")

<br>

