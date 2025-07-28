# Docker Environment for Nuxt Starter Projects

A lightweight, ready-to-use Docker environment for developing Nuxt 3 applications with minimal setup.

## Overview

This repository provides a Docker-based development environment for Nuxt.js projects. It allows developers to quickly bootstrap and run Nuxt 3 applications inside a containerized environment, ensuring consistency across different development machines and simplifying the setup process.

### Features

- ⚙️ **Node.js Alpine Container**: Lightweight and fast Node.js environment
- 🛠️ **Ready for Nuxt**: Pre-configured for initializing and running Nuxt 3 projects
- 🔄 **Hot-Reloading**: Volume mounting enables real-time code changes
- 🚀 **Port Forwarding**: Automatic exposure of Nuxt's development server
- 🧰 **Git Support**: Built-in Git for version control
- 🔒 **Isolated Environment**: Consistent development experience across machines

## Prerequisites

- Docker installed on your machine
- Docker Compose installed on your machine
- Basic knowledge of Docker and Nuxt.js

## Getting Started

### Installation

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd frontend-nuxt-docker
   ```

2. Start the Docker container:
   ```bash
   docker-compose up -d
   ```

### Creating a New Nuxt Project

Once the container is running, you can scaffold a new Nuxt application:

1. Access the container shell:
   ```bash
   docker exec -it nuxt-dev sh
   ```

2. Initialize a new Nuxt project:
   ```bash
   npx nuxi init .
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Access your Nuxt application at `http://localhost:3000`

### Using with an Existing Nuxt Project

1. Place your existing Nuxt project files in the `app` directory
2. Start the Docker container
3. Access the container shell and run your project as usual

## Configuration

### Docker Configuration

The environment uses:
- A Node.js Alpine image with Git support
- Volume mounting for the `/app` directory
- Port forwarding from container port 3000 to host port 3000

You can modify the `docker-compose.yml` file to adjust:
- Port mappings
- Volume mounts
- Container name
- Additional environment variables

### Nuxt Configuration

Nuxt configuration can be managed through the standard `nuxt.config.ts` file in your project.

## Troubleshooting

### Common Issues

- **Port conflicts**: If port 3000 is already in use on your host machine, modify the port mapping in `docker-compose.yml`
- **Permission issues**: Ensure proper permissions for the `app` directory
- **Hot-reload not working**: Check that volume mounting is correctly configured

## Contributing

Contributions to improve this Docker setup are welcome. Please feel free to submit issues or pull requests.

## License

This project is open-source and available under the [MIT License](LICENSE).
