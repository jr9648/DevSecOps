# Dockerfile Policy Enforcement Tool
This Python script is designed to enforce various best practices and security measures within Dockerfiles. It analyzes a Dockerfile, provided in JSON format, and checks for violations against a set of predefined rules.

## Features
- Base Image Version Check: Ensures that the Dockerfile does not use outdated and vulnerable base images.
- Root Password Warning: Alerts against setting insecure passwords, specifically targeting the root user.
- Sensitive Data Detection: Detects and warns about hardcoded sensitive data in environment variables.
- Latest Tag Avoidance: Advises against using the 'latest' tag for the base image, promoting the use of specific versions instead.
- Non-Root User Recommendation: Recommends switching to a non-root user after creating it using 'adduser' or 'useradd'.
- Remote URL Usage: Encourages the use of COPY instead of ADD for local files to avoid security risks associated with fetching files from remote URLs.
## Usage
1. Provide the Dockerfile in JSON format named Dockerfile.json.
2. Run the script to analyze the Dockerfile and identify policy violations.