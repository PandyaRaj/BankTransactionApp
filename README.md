# Bank Transaction List App

## Overview

The Bank Transaction List App is a Spring-based application that provides RESTful APIs for managing bank transactions. It allows users to retrieve transaction lists and calculate total amounts based on transaction types. The application is built with Maven and uses Tomcat 7 as an embedded web container.

## Table of Contents

1. [Project Structure](#project-structure)
2. [Prerequisites](#prerequisites)
3. [Building and Running the Application](#building-and-running-the-application)
4. [API Endpoints](#api-endpoints)
5. [Authentication](#authentication)
6. [Testing](#testing)
7. [Logging](#logging)
8. [Development Notes](#development-notes)
9. [Contributing](#contributing)
10. [License](#license)

## Project Structure

The project follows a standard Maven structure:

- `src/main/java`: Java source files
- `src/main/resources`: Configuration files
- `src/test`: Test files
- `pom.xml`: Maven configuration file

## Prerequisites

- Java JDK (version not specified, recommend latest LTS version)
- Maven
- Tomcat 7 (embedded)

## Building and Running the Application

1. Ensure Maven is installed and added to your system PATH.

2. Clone the repository:

3. Clean the project:
  
4. Build and run the application using the embedded Tomcat:

5. 5. The application will be available at `http://localhost:8080`

## API Endpoints

All APIs are secured using HTTPS header authentication.

1. Get All Transactions:
- URL: `http://localhost:8080/transactions/getAllTransactionList`
- Method: GET

2. Get Transactions by Type:
- URL: `http://localhost:8080/transactions/getTransactionsListByTransactionType/{transactionType}`
- Method: GET
- Valid transaction types: `SANDBOX_TAN`, `sandbox-payment`, or `null`

3. Get Total Amount by Transaction Type:
- URL: `http://localhost:8080/transactions/getTotalAmountByTransactionType/{transactionType}`
- Method: GET
- Valid transaction types: `SANDBOX_TAN`, `sandbox-payment`, or `null`

## Authentication

All API endpoints require authentication. Include the following header in your HTTP requests:

Note: This authentication code is currently hardcoded for demonstration purposes. In a production environment, it should be generated dynamically through a secure method.

## Testing

The APIs can be tested using Postman or any other HTTP client. Remember to include the authentication header as mentioned in the [Authentication](#authentication) section.

Example Postman request:
1. Set the request URL to one of the API endpoints.
2. Add the authentication header.
3. Send the request and view the response.

## Logging

Log files are generated at:

## Development Notes

- The application uses Spring Framework.
- Maven is used for dependency management and build automation.
- The embedded Tomcat 7 is used as the web container for easy deployment and testing.
- Authentication is currently implemented using a simple header-based approach. This should be enhanced for production use.

## Contributing

We welcome contributions to the Bank Transaction List App! Here are some ways you can contribute:

1. Report bugs and suggest features by opening issues.
2. Submit pull requests with bug fixes or new features.
3. Improve documentation.

Please ensure that your code adheres to the existing style and that all tests pass before submitting a pull request.


.
