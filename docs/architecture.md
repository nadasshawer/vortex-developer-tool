# Vortex: Infrastructure-as-Code CLI Engine

Vortex is a modular Bash-based automation tool designed to standardize project initialization, system health monitoring, and remote repository synchronization. Built for developers who value speed andsystem resilience, Vortex ensures that every project starts with a healthy environment and a professional directory structure.

## Key Features

### 1. Multi-Stack Blueprinting
Vortex eliminates repetitive setup by injecting professional boilerplates for five major technology stacks:
* Web (HTML/CSS/JS): Standard frontend structure with linked assets.
* Node.js: Backend environment with package.json and environmental config.
* Python: Clean virtual environment (.venv) setup with entry-point logic.
* C++: Professional build system including Makefile, header guards, and bin/build separation.
* Express (TypeScript): Full-scale API architecture with controllers, routes, and tsconfig integration.

### 2. Intelligent System Guards
Before any project is initialized, Vortex performs a pre-flight check to prevent system failure:
* Storage Sentry: Blocks installation if available disk space is below 1GB.
* Memory Monitor: Verifies a minimum of 256MB of RAM to ensure smooth build processes.
* Dependency Detective: Automatically detects missing binaries (e.g., g++, npm, pip3) and provides custom installation hints for Debian-based systems.

### 3. Automated Git and GitHub Orchestration
Vortex handles the tedious parts of version control:
* Identity Verification: Automatically checks git config and prompts for setup if identity is missing.
* Remote Linking: Initializes local repositories, handles initial commits, performs upstream rebasing, and pushes to remote branches in one fluid motion.

---

## Technical Architecture

Vortex follows a modular library design pattern to keep the core engine lightweight and maintainable:

* vortex: The main entry point using getopts for high-speed flag parsing.
* lib/guard: The system health and resource monitoring module.
* lib/github_setup: The logic layer for Git initialization and remote connectivity.
* lib/blueprints/: A specialized directory containing the environment-specific injection scripts for Web, Node, C++, Python, and Express.

---

## Usage Guide

### Flags
| Flag | Parameter | Purpose |
| :--- | :--- | :--- |
| -n | name | Sets the project name and root directory. |
| -t | type | Selects stack: web, node, cpp, py, or express. |
| -m | N/A | Generates a real-time Vortex System Report (Disk/RAM). |
| -h | N/A | Displays the help manual. |
| -v | N/A | Runs the dependency detective for the specified stack. |

### Example Commands
Initialize a C++ Project:
./vortex -n my_engine -t cpp

Check System Health:
./vortex -m

---

## Roadmap
* Milestone 3 (Ghost Essentials): Background file watching, auto-snapshots (Time-Machine), and Discord-integrated commit reminders.
* Milestone 4 (Production Deployment): Automated Docker containerization and one-command public URL tunneling.

Author: Nada Shawer
Platform: Developed for Debian/Linux Environments
