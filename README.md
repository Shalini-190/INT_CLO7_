# **Week 7: Serverless Web App with AWS Lambda**

## **Overview**  
This project demonstrates a **serverless web application** architecture implemented using **AWS Lambda**, **API Gateway**, and **DynamoDB**. It includes **CRUD operations** for managing data and provides an interactive backend for a web application. The architecture leverages serverless technologies to ensure scalability, reliability, and cost-efficiency.

---

## **Features**  
- **AWS Lambda**: Server-side logic for handling HTTP methods (GET, POST, PUT, DELETE).  
- **API Gateway**: Exposes RESTful endpoints to interact with Lambda functions.  
- **DynamoDB**: Scalable database for storing application data.  
- **Event-Driven Architecture**: Lambda functions triggered by HTTP requests.  

---

## **Prerequisites**  
- AWS Account  
- IAM Role with the necessary permissions  
- Basic knowledge of AWS services  

---

## **Steps to Implement**  

### 1. **Create IAM Role**  
- Navigate to the **IAM Console** and create a new role.  
- Attach the following policies:  
  - `AWSLambdaBasicExecutionRole`  
  - `AmazonDynamoDBFullAccess`  
- Note the **Role ARN** for Lambda configuration.

### 2. **Set Up DynamoDB Table**  
- Go to the **DynamoDB Console**.  
- Create a table:  
  - Table Name: `AppData`  
  - Primary Key: `id` (String).  

### 3. **Develop Lambda Functions**  
- Navigate to the **AWS Lambda Console**.  
- Create Lambda functions for each operation:  
  - **Create**: Add new entries to DynamoDB.  
  - **Read**: Fetch data from DynamoDB.  
  - **Update**: Modify existing entries in DynamoDB.  
  - **Delete**: Remove entries from DynamoDB.  
- Use Python 3.x for the functions and configure the IAM Role.  

### 4. **Configure API Gateway**  
- Navigate to the **API Gateway Console**.  
- Create a REST API and define resources for CRUD operations.  
- Link each method (GET, POST, PUT, DELETE) to the corresponding Lambda function.  
- Deploy the API and note the **Invoke URL**.

### 5. **Frontend Integration**  
- Develop a simple HTML/JavaScript interface to interact with the API Gateway endpoints.  

### 6. **Testing**  
- Use **Postman** or **curl** to test each API endpoint.  
- Verify data changes in the DynamoDB table.

---

## **Outcome**  
The project successfully implements a serverless web app with full **CRUD functionality** using AWS services. It demonstrates the use of **Lambda**, **API Gateway**, and **DynamoDB** for building scalable, event-driven applications.  

---

