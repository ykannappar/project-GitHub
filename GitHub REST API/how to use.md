# How to use GitHub's REST API

**The following steps are simplified for beginners to help you get started with the GitHub REST API.**




## What you need to get started

1. A GitHub Account.

2. An API Tool - You will use this to send API requests.
    * **Postman** is recommended for beginners.
    * **cURL** is efficient and fast.

3. A basic understanding of **HTTP Requests**.

4. Knowing how to retrieve a **Personal Access Token (PAT)** to access private repositories.


## Understanding how the REST API works

The **REST API** facilitates communication between the client (you) and GitHub. Thereby, acting as a **messenger**.

1. A request can be sent to GitHub's **API** to perform a specific **task** (e.g.,retrieving user details).

2. The request is directed to a specific **endpoint**, which represents a resource of functionality within the API (e.g., **/users/{username}** -> user details)

3. The type of **HTTP method** determines what action is performed on that specific endpoint (e.g., **GET** /users/{username} -> fetches user details)

4. The API processes the request, retrieves the data, and sends a response back in **JSON format**.


## Table 1.1

| **Task** | **HTTP Method** | **GitHub API Endpoint** | **What it does** |
|-----:|------------:|--------------------:|:-------------|                                                       
|Get user details|GET|/users/{username}|Fetches user profile|
|Get repo details|GET|/repos/{owner}/{repo}|Fetches repository info|
|Create a repository|POST|/user/repos|Creates a new repository| 
|Update repo settings|PATCH|/repos/{owner}/{repo}|Edits repository settings|
|Replace repo content|PUT|/repos/{owner}/{repo}/contents/{path}|Creates or replaces a file in a repository|
|Delete a repository|DELETE|/repos/{owner}/{repo}|Deletes a repository|


## Example: Using Postman to retrieve profile details on GitHub

1. Download Postman.

2. Enter *https://api.github.com/users/{username}* in the search bar, and input the desired *username*.

3. Select **GET** as the method.

4. Press **Send**, and data should be returned below in **JSON format** about the profile.
