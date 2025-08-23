Jules Agent & Tooling Guide
This document provides context for the Jules AI agent about the tools, scripts, and development workflow for this repository.

1. Project Overview
Purpose: This repository contains the source code for [Describe your project here, e.g., a static marketing website, a React-based single-page application, a Node.js API].

Primary Technologies: [List main technologies, e.g., HTML5, CSS3, JavaScript (ES6+), React, Node.js].

2. Development Workflow & Tools
This section details the primary commands and tools used for local development. The agent should use these scripts to perform tasks like testing, building, and linting.

Package Management

Tool: We use npm for package management.

Manifest File: All dependencies are listed in package.json.

Installation: To install all required dependencies, run the following command from the root directory:

npm install

Running the Development Server

Command: To start the local development server with hot-reloading:

npm run dev

Purpose: Use this for previewing changes during feature development or bug fixing.

Building for Production

Command: To create a production-ready build of the application:

npm run build

Output: The command generates optimized, static assets in the build/ (or dist/) directory. These are the files that get deployed.

Testing

Tool: [e.g., Jest, Cypress, Vitest] is used for automated testing.

Command: To run the entire test suite:

npm test

Convention: All new features or bug fixes should ideally be accompanied by corresponding tests. Test files are located in [e.g., the __tests__/ directory or alongside source files with a .test.js extension].

Linting and Formatting

Tools: We use ESLint for code analysis and Prettier for code formatting.

Command: To check for and automatically fix linting/formatting issues:

npm run lint

Purpose: This ensures code quality and consistency across the codebase. The agent should run this command before submitting any code changes.

3. Deployment
Method: Deployment to the live server is handled automatically via a Git push to the main branch.

Configuration: The deployment process is defined in the .cpanel.yml file in the root of this repository.

Process: The script in .cpanel.yml copies the necessary build artifacts (e.g., from the build/ directory) to the /home/bisonrec/public_html/ directory on the cPanel server. The agent does not need to run this deployment manually; it is triggered by the repository push.

