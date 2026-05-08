# Secure Docker Build Action

Build and scan Docker images with integrated security best practices.

## Features

- Flexible Dockerfile path configuration
- Integrated security vulnerability scanning
- Detailed build and security reports
- Optimized for CI/CD pipelines
- Security-first design

## Usage

### Basic usage

```yaml
- name: Build and scan Docker image
  uses: myorg/secure-docker-build@v2
  with:
    dockerfile-path: "./Dockerfile"
    image-name: "my-app:latest"
```

### Advenced usage

```yaml
- name: Build with custom security settings
  uses: myorg/secure-docker-build@v2
  with:
    dockerfile-path: "./docker/Dockerfile.prod"
    image-name: "my-app:${{ github.sha }}"
    registry-url: "myregistry.azurecr.io"
    security-scan: "true"
    scan-severity: "MEDIUM"
```