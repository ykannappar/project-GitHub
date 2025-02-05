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
