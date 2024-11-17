# Image Classification Model for Scones Unlimited

## Project Overview

In this project, I developed an image classification model for Scones Unlimited, a logistics company focused on scone delivery. The model is designed to identify the type of vehicle delivery drivers use, specifically distinguishing between bicycles and motorcycles. This capability enables optimized routing for delivery professionals, enhancing operational efficiency.

## Background

Image classifiers play a crucial role in computer vision, with applications across various industries, including autonomous vehicles, eCommerce, and diagnostic medicine. By automating the detection of delivery vehicles, Scones Unlimited can improve its logistics operations and better serve its customers.

## Project Steps

### Step 1: Data Staging
- Extracted data from a hosting service.
- Explored and transformed the CIFAR dataset into the appropriate shape and format.
- Loaded the processed data into Amazon S3.

### Step 2: Model Training and Deployment
- Utilized AWS's built-in image classification algorithm to train the model.
- Deployed the trained model to an endpoint and configured Model Monitor to track its performance.
- Conducted inference tests to validate the model endpoint. My very first inference gave a value of **b'[0.7304789423942566, 0.2695210874080658]'**, meaning it predicted the probability of being a bicycle is **73%** and being a motorcycle is **30%**.


### Step 3: Lambdas and Step Function Workflow
- Developed three AWS Lambda functions:
  1. **Data Generation**: Generates image data for processing.
  2. **Image Classification**: Classifies the images using the deployed model.
  3. **Filtering Low-Confidence Inferences**: Filters out predictions below a confidence threshold.
- Created a Step Function to orchestrate the Lambda functions and ensure smooth workflow execution.
- Submitted the code for each Lambda function in a Python script (`lambda.py`), along with a screenshot of the working Step Function and its JSON export.

### Step 4: Testing and Evaluation
- Performed multiple Step Function invocations using test dataset data to ensure expected success and failure outcomes.
- Created visualizations using captured data from SageMaker Model Monitor to monitor model performance.
![image_2024-11-15_115700914](https://github.com/user-attachments/assets/622f724b-80f4-4ba7-886d-2a54012a72e6)


### Step 5: Optional Challenge
- [Optional challenge details, if applicable]

### Step 6: Cleanup Cloud Resources
- Cleaned up AWS resources to avoid ongoing costs, including endpoints, models, and running instances in the SageMaker dashboard.
![image_2024-11-17_053309463](https://github.com/user-attachments/assets/e5fbc697-87ca-422d-8bf6-4eeafd1f90ee)


## Technologies Used
- **AWS Services**: Amazon SageMaker, AWS Lambda, AWS Step Functions, Amazon S3
- **Programming Language**: Python

## Conclusion
This project showcases my ability to build and compose scalable, ML-enabled applications using AWS services. The image classification model developed for Scones Unlimited demonstrates practical applications of machine learning in optimizing logistics operations.

## Acknowledgments
- Udacity's AWS Machine Learning Fundamentals Nanodegree program for providing the foundational knowledge and skills necessary to complete this project.
