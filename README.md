## Image uploads and downloads with React, AWS Amplify, AWS AppSync, and Amazon S3

This is an example project showing how to upload and download images from S3 using AWS Amplify, AWS AppSync, and Amazon S3

### The question

How do I securely upload images using GraphQL with AWS AppSync?

### The solution

There are a few parts to this solution:

* You must first upload the image to a storage solution (Amazon S3)
* After you have finished uploading the image, you will then be given a `key` to reference this image. You then need to store this reference in a database using a GraphQL mutation.
* When you want to view this image, you need to do two things:
  * First, query the image reference from your database using GraphQL
  * Get a signed URL for the image from S3

In this example, I show how to:

1. Store images using GraphQL, AppSync, and S3
2. Fetch a list of images and render them in a React application

> To view the main code for this app, open [src/App.js](https://github.com/dabit3/react-amplify-appsync-s3/blob/master/src/App.js)

## To deploy this app

1. Clone the project and change into the directory

```sh
git clone https://github.com/dabit3/react-amplify-appsync-s3.git

cd react-amplify-appsync-s3
```

2. Install the dependencies

```sh
npm install

# or

yarn
```

3. Initialize and deploy the amplify project

```sh
amplify init

amplify push
```

4. Run the app

```sh
npm start
```