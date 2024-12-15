# URL Shortener

## Overview
This project is a URL shortener service written in Go. It allows users to shorten long URLs and redirect to the original URLs using the shortened versions.

## Features
- Shorten long URLs
- Redirect to original URLs using shortened versions
- Configuration management using YAML files
- Logging with different levels for local, development, and production environments
- SQLite database for storage

## Configuration
The application uses a YAML configuration file to manage settings. The configuration file should be specified using the `CONFIG_PATH` environment variable.

Example configuration (`config/local.yaml`):
```yaml
env: "local" #local, dev, prod
storage_path: "./storage/storage.db"
http_server:
  address: "localhost:8082"
  timeout: 4s
  idle_timeout: 60s
```