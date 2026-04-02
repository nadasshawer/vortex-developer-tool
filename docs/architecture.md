# Vortex: Infrastructure-as-Code CLI Engine

Vortex is a modular Bash-based automation tool designed to standardize project initialization, system health monitoring, and remote repository synchronization. Built for developers who value speed and system resilience, Vortex ensures that every project starts with a healthy environment and a professional directory structure.

## Key Features

### 1. Multi-Stack Blueprinting
Vortex eliminates repetitive setup by injecting professional boilerplates for five major technology stacks:
* **Web (HTML/CSS/JS)**: Standard frontend structure with linked assets.
* **Node.js**: Backend environment with package.json and environmental config.
* **Python**: Clean virtual environment (.venv) setup with entry-point logic.
* **C++**: Professional build system including Makefile, header guards, and bin/build separation.
* **Express (TypeScript)**: Full-scale API architecture with controllers, routes, and tsconfig integration.

### 2. Intelligent System Guards
Before any project is initialized, Vortex performs a pre-flight check to prevent system failure:
* Blocks installation if available disk space is below 1GB.
* Verifies a minimum of 256MB of RAM to ensure smooth build processes.
* Detects missing binaries and provides installation hints for Debian systems.

### 3. Automated Git and GitHub Orchestration
Vortex handles the tedious parts of version control:
* Checks git config and prompts for setup if identity is missing.
* Initializes local repositories, handles initial commits, and pushes to remote branches.

### 4. Ghost Mode: Background Guard
Vortex includes a background engine that monitors project activity:
* Monitors uncommitted changes using a systemd timer without slowing down the terminal.
* Sends Discord alerts when significant work (50+ lines) has not been committed.
* Auto-provisions configuration by prompting the user for a webhook on the first run.

---

## Technical Architecture

Vortex follows a modular design to keep the core engine lightweight:

* **vortex**: The main entry point using getopts for flag parsing.
* **lib/guard**: The system health and resource monitoring module.
* **lib/ghost**: The background monitoring engine triggered via systemd.
* **lib/github_setup**: The logic layer for Git initialization and remote connectivity.
* **lib/blueprints/**: Scripts for injecting Web, Node, C++, Python, and Express files.

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
* Initialize a C++ Project: `./vortex -n my_engine -t cpp`
* Check System Health: `./vortex -m`

_Author: Nada Shawer_
_Platform: Developed for Debian/Linux Environments_
