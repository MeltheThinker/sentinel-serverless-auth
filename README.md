# sentinel-serverless-auth

This repository contains resources and instructions for building a serverless authentication system using Amazon Cognito and AWS Lambda. The project demonstrates how to set up a user pool with a hosted UI, configure sign-in and sign-up, create a Lambda function for pre-sign-up validation, and attach it as a trigger.

## Overview

We use Amazon Cognito to create a user directory and hosted login page. Sign-in identifiers (such as email or phone) and self-registration options are configured when the user pool is created. A Lambda function written in Python (for example, `CIS192-Auth-Handler`) is created to run custom logic before user sign-up completes. This function is attached as a pre-sign-up trigger in the Cognito user pool's Extensions tab.

## Steps covered

1. **Define your application**: create a new Cognito user pool and configure sign-in identifiers. Enable self-registration and specify a return URL.
2. **Complete setup**: view your hosted login page via the quick setup guide and review sample integration code.
3. **Create a Lambda function**: author a new function using AWS Lambda (Python 3.12) and the default execution role.
4. **Attach the trigger**: add the Lambda function as a pre-sign-up trigger in Cognito to customize registration.

A more detailed report describing each step is available in `docs/cis192_auth_setup_report.md`. Feel free to consult it for guidance and screenshots.
