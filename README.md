# Postman API Testing Assignment: Comprehensive API Workflow 🚀

**Hello and welcome to my Postman API Testing Portfolio!** This repository contains a Postman Collection meticulously crafted to fulfill the requirements of Assignment No. 1, demonstrating a robust understanding of API testing principles using the Postman Desktop App.

*This assignment was diligently completed by Esha Israr.*

## 🌟 Project Overview

This project showcases a practical application of Postman for comprehensive API testing. It covers essential HTTP methods (GET, POST, PUT, PATCH, DELETE) and integrates advanced Postman features to create a dynamic and verifiable API testing workflow.

## ✨ Key Features & Assignment Requirements Addressed

The `EshaIsrar_API_Testing.postman_collection.json` collection within this repository successfully addresses all the following assignment requirements:

### 1. Base URL as a Variable 🌐

The API's base URL (`https://reqres.in`) is set as a Postman environment variable (`{{baseUrl}}`). This variable is consistently used across all API requests within the collection, ensuring flexibility and ease of management.

### 2. Random Data Generation 🎲

Pre-request scripts are utilized to generate dynamic, random data (e.g., `randomName`, `randomJob`). This ensures that POST requests send unique payloads, simulating real-world data creation scenarios.

### 3. JSON Response Parsing & Logging 📝

Test scripts for relevant requests (e.g., `GET - List Users`, `Creating a new user`) parse the JSON response bodies. Key property values (like `email`, `id`, `createdAt`) are then logged to the Postman Console for immediate inspection and debugging.

### 4. Chai Assertion Library for Verification ✅

The Postman Chai Assertion Library is extensively used in test scripts to verify various aspects of the API responses, including:

* **HTTP Status Codes** (e.g., `200 OK`, `201 Created`, `204 No Content`).
* **Response Body Structure** (e.g., `to.be.an('object')`, `to.have.property()`).
* **Data Types** (e.g., `to.eql('string')`, `to.eql('number')`).
* **Value Verification** (e.g., `to.eql('ExpectedValue')`, `to.be.above(0)`).

### 5. Deliberate Test Case Failure ❌

A specific test case (`Deliberate Fail Test - Job Mismatch`) is intentionally included in the `Creating a new user` request's test script. This assertion is designed to fail, demonstrating the ability to identify and report test failures, which is crucial for robust testing.

### 6. Pre-request & Tests Section Variable Handling 🔄

Variables (e.g., `randomName`, `randomJob`) are set in **Pre-request scripts** before the API request is sent.

These variables are then reset (`unset`) in the **Tests section** after the request has completed, ensuring a clean state for subsequent runs or iterations.

### 7. Dynamic Variable Passing & API Chaining 🔗

The collection demonstrates **API request chaining**.

* The `Register User` POST request receives a `token` in its response. This token is then extracted and set as a Postman variable (`userToken`).
* This `userToken` is subsequently used as an **Authorization header** parameter in the `Delayed Response with Token` GET request, showcasing how the output of one API call can serve as input for another. Both chained APIs are designed to pass successfully.

### 8. Usage of All API Methods 🕐

The collection includes at least one example of each essential HTTP method:

* **GET**: `GET - List Users`, `List Users By Query Params`, `Delayed Response with Token`
* **POST**: `Creating a new user`, `Register User`
* **PUT**: `Update User`
* **PATCH**: `Partial Update`
* **DELETE**: `New Request (Delete User)`

## 💻 API Used

The Postman collection interacts with the Reqres.in API.

* **Base URL**: `https://reqres.in`
* **Description**: Reqres.in is a popular online REST API used for testing and prototyping. It provides mock data and simulates various HTTP methods.

**Important Note:** While Reqres.in is excellent for demonstrating API interactions, it does not persist data created via POST requests. This means that data "created" will not be retrievable in subsequent, independent GET requests. However, the chained requests within the collection (`Register User -> Delayed Response with Token`) are designed to work within this mock behavior.

## 🚀 How to Use This Postman Collection

To explore and run this Postman collection on your local machine:

### Install Postman

Download and install the Postman Desktop App.

### Clone the Repository

**If you have GitHub CLI installed (recommended):**

```bash
gh repo clone EshaIsrarX01/Postman-API-Testing-Assignment
cd Postman-API-Testing-Assignment
```

**Alternatively, using Git:**

```bash
git clone https://github.com/EshaIsrarX01/Postman-API-Testing-Assignment.git
cd Postman-API-Testing-Assignment
```

### Import the Collection

1. Open the Postman Desktop App.
2. Click on **File > Import**.
3. Select the `EshaIsrar_API_Testing.postman_collection.json` file from your cloned repository.

### Set Up the Environment Variable

1. After importing, you'll see the `EshaIsrar_API_Testing` collection in your Postman sidebar.
2. In the top-right corner of Postman, click the **"Environments" eye icon** (or select **"Manage Environments"**).
3. Find the environment (e.g., `EshaIsrar_API_Testing`).
4. Ensure the `baseUrl` variable is set:

   * **Variable**: `baseUrl`
   * **Initial Value**: `https://reqres.in`
   * **Current Value**: `https://reqres.in`
5. **Save** the environment and select it in the dropdown.

### Run the Collection

1. In the sidebar, hover over `EshaIsrar_API_Testing`.
2. Click the **Run** (play) icon.
3. In the Collection Runner, ensure all requests are selected.
4. Click **"Run EshaIsrar\_API\_Testing"**.
5. Observe the test results in the Collection Runner and Postman Console.

## 📈 Test Results Summary

The `EshaIsrar_API_Testing.postman_test_run.json` file provides a detailed report of a previous execution. It confirms:

* Successful execution of most test cases
* Intentional failure of `Deliberate Fail Test - Job Mismatch` assertion

## 🤝 Contribution

Feel free to explore, use, and adapt this Postman collection for your learning or projects. If you have suggestions or issues, open an issue or PR — feedback is highly appreciated!

## ✉️ Contact

For questions or professional inquiries, reach out:

**Esha Israr**
\[https://www.linkedin.com/in/eshaisrar08] \[eesha.israr08@gmail.com]

## 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
