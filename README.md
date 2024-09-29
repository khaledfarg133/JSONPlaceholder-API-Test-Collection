# JSONPlaceholder API Test Collection

This repository contains automated tests for the JSONPlaceholder API using Postman and Newman. The tests validate several API endpoints, including fetching users, posts, and comments, creating and deleting posts, and more. The workflow is automated using GitHub Actions to run on every push or pull request.
## Table of Contents
    • Test Cases
    • Setup
    • Running Tests Locally
    • GitHub Actions Workflow
    • References

- [Test Cases](#test-cases)
- [Setup](#Setup)
- [Running Tests Locally](#running-tests-locally)
- [Github Actions Workflow](#github-actions-workflow)
- [References](#references)
## Test Cases
The following test cases are included in this Postman collection:
    1. **GET All Users:** 
       Fetches a list of all users and validates the response.
    2. **CREATE Post:** 
       Creates a new post for a user and validates the response structure.
    3. **DELETE Post:** 
       Deletes an existing post and validates the status code and response.
    4. **GET Post by ID:** 
       Fetches details of a specific post by ID and validates the structure.
    5. **GET All Comments from a Post:** 
       Fetches all comments for a post and checks the structure of each comment.
    6. **GET All Posts by User ID:** 
       Fetches all posts for a specific user by ID and validates the structure.
    7. **GET All Comments by User ID:** 
       Fetches all comments for a user by ID and validates the response structure.
## Setup
**Prerequisites**
To run these tests locally, you need:
    • Node.js installed
    • Newman installed globally
**Check Nodejs and npm**

```bash
node -v
npm -v
```
**Installing Newman**

```bash
npm install -g newman
```
**Export Postman Collection**
Make sure you have exported the Postman collection (Collection v2.1) from the Postman app and saved it in the root directory of this repository as postman_collection.json.
## Running Tests Locally
To run the tests locally using Newman, execute the following command in the terminal:
```bash
newman run [postman_collection.json] --reporters cli,html --reporter-html-export newman-report.html
```
This will:
    • Run the collection tests.
    • Output results in the terminal.
    • Generate an HTML report (newman-report.html) in the current directory.
## GitHub Actions Workflow
The repository is set up to run the Postman collection tests using Newman automatically via GitHub Actions on every push or pull request. The workflow file (.github/workflows/newman-tests.yml) defines the CI pipeline.



## References
    [Postman Documentation](https://learning.postman.com/docs/introduction/overview/)
    [Newman Documentation](https://github.com/postmanlabs/newman)
    [JSONPlaceholder API](https://jsonplaceholder.typicode.com/)
