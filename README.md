# Plate Recognizer Deployment Guide with Docker Compose
This guide will walk you through deploying Plate Recognizer using Docker Compose.

## Prerequisites
- A valid Plate Recognizer API key and license key, which can be obtained from https://app.platerecognizer.com
- Docker and Docker Compose installed on your machine
- An API Gateway (such as Kong) with authentication and rate-limit modules configured

## Deployment Steps
1. Clone or download the Plate Recognizer repository from GitHub.
2. Rename the default.env file to .env and update the ```TOKEN``` and ```LICENSE_KEY``` variables with your Plate Recognizer API key and license key.
3. Run ```docker-compose up -d``` to start the Plate Recognizer container.
4. Configure your API Gateway to use the Plate Recognizer container as a service and enable authentication and rate-limiting as necessary.
5. Do not publish the Plate Recognizer container's port to the public IP address.

## Access
Once the Plate Recognizer container is running, You can access it using the following URL: http://ip:port/v1/plate-reader/

## Conclusion
By following these steps, you have successfully deployed Plate Recognizer using Docker Compose, and have added an extra layer of security with an API gateway.

[More information about Plate Recognizer](https://guides.platerecognizer.com/docs/snapshot/getting-started)

[Documentation](https://platerecognizer.com/docs/)

[API Reference](https://platerecognizer.com/api/v1/)

## Plate Recognizer Course
- [RACKSYNC CO., LTD.](https://racksync.com)
