# Hands-on Lab: Hit the RHODS

In this exercise, you will create a data science project for fraud detection.

The lab provides notebooks that implement the project workflow.
You might need to add code to those notebooks.

## Prerrequisites

The data file must be available in an S3 bucket.

* You can create an s3 object store with Minio, by using this guide https://ai-on-openshift.io/tools-and-applications/minio/minio/.


## Instructions

1. Create a Tensorflow workbench.
Make sure that the workbench includes a data connection.

2. Clone the https://github.com/jramcast/rhods repository.

3. Navigate to `notebooks/fraud-detection`.
This directory contains the materials for this lab.

4. Collect the data from S3.
Download the `creditcard.csv` file into `data/creditcard.csv`.

5. Preprocess the data.

6. Train the model.
After training, export the model to ONNX format.

7. Upload the model to S3.
You can create a notebook to upload the model.

5. Create a model server.
Expose the model via an external route.
The model framework should be `onnx` version 1.



