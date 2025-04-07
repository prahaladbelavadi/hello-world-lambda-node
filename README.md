# Hello World Lambda with API Gateway

A simple AWS Lambda function that returns "Hello World" through an API Gateway endpoint.

## Prerequisites

- AWS CLI installed and configured
- AWS SAM CLI installed
- Node.js 20.x
- npm or yarn

## Setup

1. Install dependencies:

```bash
npm install
```

2. Build the project:

```bash
npm run build
```

## Deployment

To deploy the application:

```bash
npm run deploy
```

This will start the guided deployment process. Make sure to:

- Select the appropriate AWS region (us-west-1 for Northern California)
- Provide a stack name
- Confirm the changes

## Testing

After deployment, you can test the API endpoint using curl:

```bash
curl https://<your-api-id>.execute-api.us-west-1.amazonaws.com/Prod/hello
```

The API Gateway is configured to proxy all requests to the Lambda function, so any path will work.

## Architecture

- Lambda Function: Node.js 20.x runtime
- API Gateway: HTTP API with proxy integration
- Region: us-west-1 (Northern California)
- Architecture: ARM64 (Graviton2)
