# Microservices Configuration Repository

This repository contains centralized configuration for all microservices in the e-commerce application.

## Files

- `application.yml` - Common configuration for all services
- `customer-service.yml` - Customer Service specific configuration
- `product-service.yml` - Product Service specific configuration
- `order-service.yml` - Order Service specific configuration
- `api-gateway.yml` - API Gateway specific configuration
- `eureka-server.yml` - Eureka Server specific configuration

## Usage

These configuration files are consumed by the Spring Cloud Config Server running on port 8888.

## Setup Instructions

1. Create a new GitHub repository named `microservices-config-repo`
2. Copy all YAML files from this directory to the repository root
3. Commit and push to GitHub
4. Update the Config Server's `application.yml` with your GitHub repository URL
5. Start the Config Server
6. Start microservices - they will fetch configurations from the Config Server

## Environment-Specific Configurations

To create environment-specific configurations (dev, prod, etc.), create files with the pattern:
- `customer-service-dev.yml`
- `customer-service-prod.yml`
- etc.

## Security Note

**IMPORTANT:** Update database passwords and other sensitive information before pushing to GitHub. Consider using encryption for sensitive data in production.
