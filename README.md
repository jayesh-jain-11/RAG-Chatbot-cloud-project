# RAG-Chatbot-cloud-project
---
Create the knowlegde base and s3 bucket in ohio region.
Generate the access key and secret key in your IAM admin user.
download aws cli in your terminal.
---
# To configure your aws
--- 
run:`aws configure`
---
# Install python on your terminal
1. install python 
```bash 
sudo apt update
sudo apt install python3 -y
```
2. install pip
```bash 
sudo apt install python3-pip -y
```
---
# Clone the repo
---
`git clone <https:url>`
---
# Create a nano file .env
---
add 
**AWS_REGION=**
**MODEL_ARN=**
**KNOWLEDGE_BASE_ID=**
---
# To get the model id 
---
goto aws cloudshell and run:
```bash
aws bedrock get-foundation-model --model-identifier
```
copy the model id and paste it in .env
---
# Start the virtual environment
---
run:
```bash
python3 -m venv venv
```
and activate it by :
```bash
source venv/bin/activate
```
---
# Download the requirement.txt
---
run:
```bash
pip3 install -r requirements.txt
```
---
# To run the main app
run:
```bash
python3 -m uvicorn main:app --reload
```
---
# To run the web app
---
run:
```bash
python3 -m uvicorn web_app:app --reload
```

