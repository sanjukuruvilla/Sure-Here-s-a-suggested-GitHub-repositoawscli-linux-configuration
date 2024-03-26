---

# Configuring AWS CLI on Linux

## Overview

This guide provides step-by-step instructions for installing and configuring the AWS Command Line Interface (CLI) on a Linux system.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Verification](#verification)
- [Additional Configuration](#additional-configuration)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. **Update Package Manager**:
   - Ensure your package manager is up to date:
     ```bash
     sudo apt update
     ```

2. **Install AWS CLI**:
  
- You can clone the scripts from the repository below to install the awscli and Terraform:
      ```bash
      git clone https://github.com/sanjukuruvilla/scripts.git
      ```
- Navigate to the repository directory:
      ```bash
      cd scripts
      ```
- Make sure the script has executable permissions. If not, you can grant them
      ```bash
      chmod +x awscli.sh
      ```
- Execute the script
      ```bash
      bash awscli.sh
      ```
## Configuration

1. **Access AWS Management Console**:
   - Sign in to your AWS Management Console.

2. **Generate IAM User Access Key**:
   - Navigate to the IAM service.
   - Create or select an IAM user with necessary permissions.
   - Generate an access key for the IAM user.

3. **Configure AWS CLI**:
   - Run the configuration command and provide the access key, secret key, region, and output format:
     ```bash
     aws configure
     ```

## Verification

1. **Verify Configuration**:
   - Check if the configuration was successful:
     ```bash
     aws sts get-caller-identity
     ```

## Additional Configuration

1. **Customize Configuration**:
   - Modify the AWS CLI configuration as needed:
     ```bash
     aws configure --profile <profile-name>
     ```

2. **Credentials File**:
   - Manually edit the AWS credentials file located at `~/.aws/credentials`.

## Troubleshooting

- **Invalid Access Key or Secret Key**:
  - Ensure the correct access key and secret key are provided during configuration.
  - Verify that the IAM user has appropriate permissions.

- **Region Configuration Error**:
  - Double-check the specified region during configuration.

## Contributing

Contributions to this repository are welcome! If you find issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---
