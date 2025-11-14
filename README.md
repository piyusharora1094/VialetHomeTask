**Vialet Home Task – API Automation (Postman)**

This repository contains the Postman Collection and Environment file used to automate the API tests for the Vialet Home Task application.
It also includes setup steps for running the backend and frontend locally, along with details of the automation framework, folder structure, test data, reusable scripts, and instructions for cloning & running everything end-to-end.

**🔧 Prerequisites**

Before starting, make sure you have the following installed:

Node.js v14 or higher
npm or yarn
Postman (latest version)

**📥 Clone the Repository**

Run the following command:

git clone https://github.com/piyusharora1094/VialetHomeTask

🚀 Project Setup – Running Locally
Backend Setup

Navigate to the server directory:
cd server
Install dependencies:
npm install
Start the backend API:
npm start

The server will be running at:
👉 http://localhost:3000

Frontend Setup
Navigate to the client directory:
cd client
Install dependencies:
npm install
Start the React application:
npm start

The UI will be available at:

👉 http://localhost:3001

🧪 API Automation Using Postman

This repository includes:
✔ Postman Collection:

VialetHomeTask.postman_collection.json
✔ Covers full user journey:

Create user
Get user details
Upload KYC documents
Verify KYC within 20 seconds
Negative test cases (missing email, phone, password, invalid email, etc.)

✔ Postman Environment:

QA.postman_environment.json
Includes variables:
baseUrl
email
password
phone
userId
documentType
kycUploadTime

🎯 What Was Achieved?

Automated complete user onboarding workflow with validations at every step.

Added KYC verification time check, ensuring the API verifies documents within 20 seconds.

End-to-end execution in seconds, giving extremely fast feedback on regression tests.

🏗 Framework Explanation
📁 Folder Structure
postman/
│── VialetHomeTask.postman_collection.json
│── QA.postman_environment.json
test-data/
│── sample-kyc-documents/
README.md

What it Contains

Postman Collection: All request definitions + pre-request scripts + test scripts

Environment File: Dynamic variables used during execution

Test Data: Includes sample documents used for KYC upload

Readme: Setup and execution guide

🔁 Reusable Code
Pre-request Scripts
Dynamically generate email, password, phone
Reset environment between runs
Avoid duplicate failures
Test Scripts
Wrapper validations (success flag, message, data object)
Field-level validations (email, phone, createdAt, status transitions)
KYC timing validation (upload time vs. verifiedAt)

These reusable blocks reduce duplicate code and make the test suite easy to scale.

**📂 Test Data**

KYC sample documents can be added into:

test-data/sample-kyc-documents/

▶️ How to Run the Collection
Option 1: Run inside Postman

Import the Postman Collection
Import the Environment
Select QA environment
Click Run Collection

✅ Conclusion

This Postman framework provides a clean, reusable, and automated approach to validating the Vialet Home Task API.
It enables fast execution, dynamic data handling, reliable validations, and smooth integration into CI/CD pipelines.
