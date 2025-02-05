# Troubleshooting Guide for GitHub REST API

**If you run into issues while using the API, the guide below offers straightforward steps to help you identify and fix them.**

## 5 Common Issues and Fixes

1. Issue: **"Not Found" (404)**

    **Probable Cause**: An incorrct endpoint or resource was used, which does not exist.

    **Probable Fix**: 

      * Double-check the endpoint URL (e.g., /users/{username}).

      * Check if the resource exists.


2. Issue: **"Unauthorized" (401)**

    **Probable Cause**: An authentication is required, but missing or invalid.

    **Probable Fix**: 

      * Add a Personal Access Token in your request. It can be obtained from your account on GitHub.

      * In Postman, add the token within the Authorization header.


3. Issue: **"Forbidden" (403)**

    **Probable Cause**: The API rate limit may have been exceeded, or lacks permission.

    **Probable Fix**:

      * Check rate limit status with: GET "https://api.github.com/rate_limit"

      * Wait for rate limit to reset, or authenticate with a Personal Access Token.


4. Issue: **"Unprocessable Entity" (422)**

    **Probable Cause**: The request may contain invalid data, even if it was properly formatted.

    **Probable Fix**: 

      * Ensure the data being sent is correct (e.g., check of repository name alreeady exists when creating a new repo.)

      * Check the GitHub's official API documentation for required parameters.


5. Issue: **"Internal Server Error" (500)**

    **Probable Cause**: There might be a problem on GitHub's server.

    **Probable Fix**: 

      * It could be a temporary issue. Wait a few minutes then retry the request again.

## How to Debug API Requests

* Check the API Response 

  * **Review the API response** - It should contain the HTTP status code (e.g., 404) and a message in JSON format.

  * **Verify the request** - Ensure the following is correct:
      * Endpoint URL
      * HTTP Method
      * Required parameters

  * **Test with Postman or cURL** 

  * **Authenticate properly** - Ensure that the Personal Access Token is included for endpoints that require necessary authentication.

  