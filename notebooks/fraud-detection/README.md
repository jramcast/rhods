# Hands-on Lab: Hit the RHODS

In this exercise, you will create a data science project for fraud detection.

The lab provides notebooks that implement the project workflow.
You might need to add code to those notebooks.

## Prerrequisites

The lab scenario assumes that the dataset is available in an S3 bucket.
The dataset is a CSV file called `credictcard.csv`.
To prepare the lab scenario, follow these steps:

* Create the S3 object store.
You can create an s3 object store with Minio, by using this guide https://ai-on-openshift.io/tools-and-applications/minio/minio/.
You can use you S3 bucket to store the dataset, the trained model, and pipeline output reports.

* Download the dataset file from https://drive.google.com/file/d/1Gd-ENv1SdqcXYFf81KKIWAsSFwe0Z6ch/view?usp=sharing.
Alternatively, you can download the dataset from Kaggle (https://www.kaggle.com/code/janiobachmann/credit-fraud-dealing-with-imbalanced-datasets/input).

* Upload the dataset into the root of your S3 bucket.


## Instructions

1. Create a Tensorflow workbench.
Make sure that the workbench includes a data connection.

2. Clone the https://github.com/jramcast/rhods repository into your workbench.

3. Navigate to `notebooks/fraud-detection`.
This directory contains the materials for this lab.

4. Collect the data from S3.
Download the `creditcard.csv` file into `data/creditcard.csv`.

5. Explore and preprocess the data.

6. Train the model.
After training, export the model to ONNX format.

7. Upload the model to S3.
You can create a notebook to upload the model.

8. Create a model server.
Expose the model via an external route.
The model framework should be `onnx` version 1.

9. Create a data science pipeline that collects, preprocesses, trains and uploads the model.


You can find the solutions in the `notebooks/fraud-detection/solutions` directory.
