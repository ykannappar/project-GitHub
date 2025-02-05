# How to use GitHub's REST API

**The following steps are simplified for beginners to help you get started with the GitHub REST API.**




## What you need to get started

1. A GitHub Account.

2. An API Tool - You will use this to send API requests.
    * **postman** is recommended for beginners
    * **cURL** is efficient and fast

3. A basic understanding of HTTP Requests.

4. Knowing how to retrieve a **Personal Access Token (PAT)** to access private repositories.


## Understanding how the REST API works

The **REST API** facilitates communication between the client (you) and GitHub. Thereby, acting as a **messenger**.

1. A request can be sent to GitHub's **API** to perform a specific **task** (e.g.,retrieving user details).

2. The request is directed to a specific **endpoint**, which represents a resource of functionality within the API (e.g., **/users/{username}** -> user details)

3. The type of **HTTP method** determine what action is performed on that specific endpoint (e.g., **GET** /users/{username} -> fetches user details)

4. The API processes your request, retrieves the data, and sends a response back in **JSON format**.

