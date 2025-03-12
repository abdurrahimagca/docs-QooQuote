# First Time Setup

## Setting Up Your Environment

### Prerequisites

- Docker
- Bash/Zsh
- Git
- Browser (optional)

### Getting Started

1. Clone the repository

    ```bash
    git clone https://github.com/abdurrahimagca/qoo-quote-be.git
    ```

2. Change directory to the cloned repository

    ```bash
    cd qoo-quote-be
    ```

3. Create a `.env.development` file in the root directory of the project and add the environment variables from the `.env.example` file.

4. Make the `entrypoint.sh` script executable and run the following commands to start the application:

    ```bash
    chmod +x ./entrypoint.sh
    ./entrypoint.sh dev:build
    ./entrypoint.sh dev
    ```

If the application is running successfully, you should be able to visit the following URL in your browser to see the GraphQL playground:

[http://local.qq.api.com/graphql](http://local.qq.api.com/graphql)

