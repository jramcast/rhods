# Hands-on Lab: Hit the RHODS

In this exercise, you will create a complete data science project for fraud detection.

The lab materials include notebooks that implement part of the project workflow.
You task is to complete the missing parts of those notebooks and create a data science pipeline to achieve the lab specifications.

## Prerrequisites

The lab scenario assumes that the dataset is available in the S3 bucket that you have created in the [RHODS administration quick course](https://redhatquickcourses.github.io/rhods-admin/rhods-admin/1.33/index.html).
The dataset is a CSV file called `credictcard.csv`.

If you have not initialized your S3 store in the admin course, then you can follow these steps:

* Create the S3 object store.
You can create an s3 object store with Minio, by using this guide https://ai-on-openshift.io/tools-and-applications/minio/minio/.
You can use you S3 bucket to store the dataset, the trained model, and pipeline output reports.

* Download the dataset file from https://drive.google.com/file/d/1Gd-ENv1SdqcXYFf81KKIWAsSFwe0Z6ch/view?usp=sharing.
Alternatively, you can download the dataset from Kaggle (https://www.kaggle.com/code/janiobachmann/credit-fraud-dealing-with-imbalanced-datasets/input).

* Upload the dataset into the root of your S3 bucket.


## Specifications

* Perform your exercise in a Tensorflow workbench.
Make sure that the workbench includes a data connection.
Make sure that the workbench size is at least `Medium`.

* Clone the https://github.com/jramcast/rhods repository into your workbench.
The materials for this lab are located in the `notebooks/fraud-detection` directory.

* Collect data.
Use the `1.collect` notebook to collect the data from S3.
Download the `creditcard.csv` file into `data/creditcard.csv`.

* Explore and preprocess data.
Use the `2.exploration` and `3.preprocessing` notebooks.

* Train the model.
After training, export the model to ONNX format.
Using the `4.model_training` notebook.

* Upload the model to S3.
Using the `4.model_upload` notebook.

* Create a data science pipeline.
 Note that, in the [pipelines quick course](https://redhatquickcourses.github.io/rhods-pipelines/rhods-pipelines/1.33/index.html) you already created a pipeline for offline fraud detection, that is, for classification of live transactions given a pretrained model file.

 In this case, you must build a pipeline to train a model.
 This pipeline must collect training data, preprocess the data, train the model, and upload the trained model.

* Create a model server.
Expose the model via an external route.
The model framework must be `onnx` version 1.

* Test that you can consume the deployed model by using the `6.test` notebook.


You can find the solutions in the `solutions` directory.
