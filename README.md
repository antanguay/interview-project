# Interview Project
Small project to test developper skills. In this project you are required to deploy a simple
application then investigate and resolve a few issues that have been inserted for the purpose of this
exercise. The source files are provided. Once these issues have been resolved and the basic application
is working, you will write an new application to load additional data into the database.


## Deployment

Chose a Kubernetes environment of your choice like GKE, EKS, or AKS. Deploy the manifest included as
part of this project.

	kubectl apply -f manifest.yaml


## Expected Results

Once the application has been deployed and issues resolved, you should be able to port forward to the
`webapp` on port 5000.

	kubectl port-forward service/webapp 5000

Then from your browser navigate to `http://localhost:5000`. If everything is working as expected you
will see 1 row of data:

![](https://github.com/antanguay/interview-project/png/expected.png)

## Enhancements

With the base application working, your task is to create a new application that interacts with the
existing one. The new application should populate the database with data from a file located
in a blob store.

Here are the guidelines for the application:

- The application should run in its own namespace
- Use minio as the blob store or something like GCS, S3, etc
- Read a file from the blob store and write the data to postgres
- You can use any langage of your choice
- Deliver your solution as if it was a professional project

