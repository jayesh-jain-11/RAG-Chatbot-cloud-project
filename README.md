# 🧠 RAG Chatbot Cloud Project

A step-by-step guide to set up and run a Retrieval-Augmented Generation (RAG) chatbot application using AWS services, Python, and FastAPI.

---

## 📦 Prerequisites

### 1. Create AWS Resources

- Create a **Knowledge Base** and **S3 Bucket** in the **Ohio (us-east-2)** region.
- Generate **Access Key** and **Secret Key** from your **IAM Admin User**.

### 2. Install AWS CLI

Download and install the AWS CLI from the official site or using terminal commands for your OS.

---

## ⚙️ Configure AWS CLI

Run the following command and enter your credentials when prompted:

```bash
aws configure
```

---

## 🐍 Install Python & pip

### 1. Install Python 3

```bash
sudo apt update
sudo apt install python3 -y
```

### 2. Install pip

```bash
sudo apt install python3-pip -y
```

---

## 🧬 Clone the Repository

```bash
git clone https://github.com/your-username/RAG-Chatbot-cloud-project.git
cd RAG-Chatbot-cloud-project
```

---

## 🔐 Create a `.env` File

Create a `.env` file using `nano`:

```bash
nano .env
```

Add the following variables:

```env
AWS_REGION=
MODEL_ARN=
KNOWLEDGE_BASE_ID=
```

---

## 🧾 Get the Model ID

Run this command in AWS CloudShell to get the model identifier:

```bash
aws bedrock get-foundation-model --model-identifier
```

Copy the `model-identifier` and paste it into your `.env` file as `MODEL_ARN`.

---

## 🧪 Set Up Virtual Environment

### 1. Create the environment

```bash
python3 -m venv venv
```

### 2. Activate the environment

```bash
source venv/bin/activate
```

---

## 📦 Install Dependencies

Install all required packages:

```bash
pip3 install -r requirements.txt
```

---

## 🚀 Run the FastAPI App

### To run the backend API:

```bash
python3 -m uvicorn main:app --reload
```

### To run the web frontend:

```bash
python3 -m uvicorn web_app:app --reload
```

---

## ✅ You're Ready!

The chatbot app should now be running locally and ready to interact with AWS Bedrock and your knowledge base.
