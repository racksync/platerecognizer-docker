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

## Advanced Configuration
The deployment includes several performance and monitoring features:

### Resource Limits
- CPU: Maximum 4 cores, minimum 2 cores
- Memory: Maximum 4GB, minimum 2GB

### Environment Variables
- `WORKERS`: Number of worker processes (default: 2)
- `MAX_REQUESTS`: Maximum number of requests per worker (default: 5000)
- `CONFIDENCE_THRESHOLD`: Minimum confidence score (default: 80)
- `REGION`: Region specific optimization (default: th)
- `LOG_LEVEL`: Logging verbosity (default: INFO)

### Health Checks
The container includes automatic health checks every 30 seconds.

### Logging
JSON format logs with rotation:
- Maximum file size: 10MB
- Keep last 3 log files

## Conclusion
By following these steps, you have successfully deployed Plate Recognizer using Docker Compose, and have added an extra layer of security with an API gateway.

[More information about Plate Recognizer](https://guides.platerecognizer.com/docs/snapshot/getting-started)


### Automation Training

- [สินค้าและบริการ](http://racksync.com)
- [เทรนนิ่งคอร์ส](https://facebook.com/racksync)

### Community

- [Home Automation Thailand](https://www.facebook.com/groups/hathailand)
- [Home Automation Marketplace](https://www.facebook.com/groups/hatmarketplace)
- [Home Automation Thailand Discord](https://discord.gg/Wc5CwnWkp4)

## RACKSYNC CO., LTD.

RACKSYNC Co., Ltd. specializes in automation and smart solutions of all scales. We are experts in designing, implementing, and monitoring sophisticated automation systems. Our team of specialists provides comprehensive consulting services and technical implementation for both residential and commercial projects. Beyond automation, we offer full-cycle Software as a Service (SaaS) development, helping businesses transform their operations through custom digital solutions. With our deep expertise in IoT, home automation, and enterprise systems, we deliver reliable and innovative solutions tailored to each client's unique requirements.

RACKSYNC COMPANY LIMITED    
Suratthani, Thailand 84000   
Email: devops@racksync.com   
Tel: +66 85 880 8885   

[![Home Automation Thailand Discord](https://img.shields.io/discord/986181205504438345?style=for-the-badge)](https://discord.gg/Wc5CwnWkp4) [![Github](https://img.shields.io/github/followers/racksync?style=for-the-badge)](https://github.com/racksync) 
[![WebsiteStatus](https://img.shields.io/website?down_color=grey&down_message=Offline&style=for-the-badge&up_color=green&up_message=Online&url=https%3A%2F%2Fracksync.com)](https://racksync.com)

