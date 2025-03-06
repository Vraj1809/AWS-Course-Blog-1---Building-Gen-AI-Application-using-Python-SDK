# Generative AI with Amazon Bedrock using Boto3 and Comparing Model Responses

This project demonstrates how to build **Generative AI applications** using **Amazon Bedrock** and the **AWS SDK for Python (Boto3)**. It provides a simple script to invoke **Anthropic's Claude 3 Sonnet** on Amazon Bedrock and process the generated text.

## 🚀 Features
- **Interact with Amazon Bedrock** programmatically using Boto3  
- **Invoke Foundation Models (FMs)** such as Claude 3 Sonnet  
- **Customize AI responses** with parameters like `temperature`, `max_tokens`, `top_k`, and `top_p`  
- **Process AI-generated responses** and integrate them into applications  

## 📋 Prerequisites
Before running the script, ensure you have:

- ✅ An **AWS account** with access to Amazon Bedrock  
- ✅ **AWS CLI installed** ([Download Here](https://aws.amazon.com/cli/))  
- ✅ **IAM user with API access**  
  - Create an **IAM user** in the AWS Console with appropriate permissions for Amazon Bedrock  
  - After creating the user, go to **IAM → Users → [Your User] → Security Credentials**  
  - In **Security Credentials**, create an **Access Key**  
  - **Important:** Note down the **Access Key ID** and **Secret Access Key** as they will not be visible again after creation  
- ✅ **Configure AWS CLI with IAM credentials**  
  - Open a terminal and run:  
    ```sh
    aws configure
    ```
  - When prompted, enter:  
    - **AWS Access Key ID**  
    - **AWS Secret Access Key**  
    - **Default Region Name** (e.g., `us-east-1`)  
    - **Default Output Format** (press Enter to skip or set as `json`)  
- ✅ **Boto3 installed** (`pip install boto3`)  
- ✅ **Python 3.8+** installed  

## 🛠 Running the Script
If you are using **Jupyter Notebook**, simply install `boto3` and run the provided `code.ipynb` script:

```sh
pip install boto3
```

## 🔍 Model Comparison
In this project, we are going to use two models:
- **Amazon Titan Express**
- **Llama 3 8B Instruct**

We will set the same inference parameters for both models and compare their responses. This will help us analyze the differences in their outputs and determine which model performs better for our use case.

## 🆚 Comparison of Model Responses
We tested the models with a simple query:

**Prompt:** "Explain the importance of AI in modern technology."

### 🔹 Response from Amazon Titan Express:
```
AWS is a cloud computing platform offered over the internet by Amazon Web Services. Its services include compute, storage, databases, analytics, networking, mobile, developer tools, management tools, IoT, security, and enterprise applications. With an emphasis on automation, AWS aims to provide a scalable and cost-effective way for businesses to access various computing resources.
```

### 🔹 Response from Llama 3 8B Instruct:
```
AWS stands for Amazon Web Services, which is a comprehensive cloud computing platform provided by Amazon. It offers a wide range of services, including computing power, storage, databases, analytics, machine learning, and more, to help individuals, companies, and governments build, deploy, and manage applications and workloads in the cloud. AWS is widely used by businesses, developers, and governments to build and deploy scalable, secure, and high-performance applications and workloads.

AWS provides a wide range of services, including:

1. Compute Services: AWS offers various compute services, including EC2 (Elastic Compute Cloud), Lambda (serverless compute), and Elastic Container Service (ECS), to help you run and manage your applications and workloads.
2. Storage Services: AWS provides various storage services, including S3 (Simple Storage Service), Elastic Block Store (EBS), and Elastic File System (EFS), to help you store and manage your data.
3. Database Services: AWS offers various database services...
```

## 📊 Analysis of Differences
| Feature                 | Amazon Titan Express | Llama 3 8B Instruct |
|-------------------------|---------------------|---------------------|
| **Conciseness**         | Short, high-level summary | More detailed, structured response |
| **Depth of Information** | Limited, focuses on AWS services | Covers multiple aspects in-depth |
| **Readability**         | Simple and easy to read | More technical with structured points |
| **Use Case Suitability** | Best for quick overviews | Best for detailed explanations |

## 🏆 Which Model is Better?
- Use **Amazon Titan Express** if you need short, to-the-point responses with minimal details.
- Use **Llama 3 8B Instruct** if you require detailed, structured, and informative answers with examples and explanations.

By experimenting with different prompts and models, you can choose the best model suited for your specific AI application needs.
