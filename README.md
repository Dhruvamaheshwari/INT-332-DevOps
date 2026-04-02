<!-- @format -->

# DevOps Node.js App

A simple Node.js application that logs environment variables. This project is containerized using Docker.

## Prerequisites

- [Docker](https://www.docker.com/) installed on your machine
- (Optional) [Node.js](https://nodejs.org/) installed if running locally without Docker

## Application Summary

The application simply logs the values of `NAME` and `roll` environment variables:

- `NAME`: Your name
- `roll`: Your roll number (or identifier)

## How to Run

### Method 1: Using Docker (Recommended)

1. **Build the Docker image:**

   ```bash
   docker build -t devops-node-app .
   ```

2. **Run the container (passing the required environment variables):**
   ```bash
   docker run -e NAME="Your Name" -e roll="123" devops-node-app
   ```

### Method 2: Running Locally (Node.js)

1. **Install dependencies:**

   ```bash
   npm install
   ```

2. **Run the script (passing the required environment variables):**

   ```bash
   # Windows (PowerShell)
   $env:NAME="Your Name"; $env:roll="123"; node index.js

   # Linux/macOS
   NAME="Your Name" roll="123" node index.js
   ```

## Files

- `index.js`: Main application entry point.
- `Dockerfile`: Defines the Docker image (using Node 18 Alpine).
- `package.json`: Contains project metadata and dependencies.
- `Docker.txt`: Additional Docker notes/commands.
