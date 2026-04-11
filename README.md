# 🌪️ Vortex: Infrastructure-as-Code CLI Engine

Vortex is a modular Bash-based automation tool designed to standardize project initialization, system health monitoring, and remote repository synchronization. Built for developers who value speed and system resilience, Vortex ensures that every project starts with a healthy environment and a professional directory structure.

## 🚀 Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/nadasshawer/vortex-developer-tool.git
   cd vortex-developer-tool
   ```

2. **Run the Installer:** This will set up your systemd timers, permissions, and background monitoring automatically.
    ```bash
    bash installer
    ```
    
3. **Create your first project:**
    ```bash
    ./vortex -n my_new_project -t node
    ```
    
**Note:** The first time you run a command or the Ghost monitor activates, you will be prompted to enter your Discord Webhook URL. This will be saved in `~/.vortex_config`.

---

## 📁 Project Structure

```text
vortex_project/
├── docs/                 # Project documentation and roadmap
│   ├── architecture.md
│   └── milestones.md
├── lib/                  # Core logic and modules
│   ├── blueprints/       # Project templates (C++, Express, etc.)
│   ├── docker            # Docker scaffolding logic
│   ├── ghost             # The "Ghost" background monitor script
│   ├── github_setup      # Automation for GitHub integration
│   └── guard             # Input validation and security checks
├── systemd/              # Service files for Linux automation
│   ├── vortex_ghost.service
│   └── vortex_ghost.timer
├── vortex                # Main executable entry point
└── README.md             # You are here!
```

---

## 🛠️ Key Features

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

## 🏗️ Technical Architecture

Vortex follows a modular design to keep the core engine lightweight:

* **vortex**: The main entry point using getopts for flag parsing.
* **lib/guard**: The system health and resource monitoring module.
* **lib/ghost**: The background monitoring engine triggered via systemd.
* **lib/github_setup**: The logic layer for Git initialization and remote connectivity.
* **lib/docker**: The logic layer for Docker containerization (creates the Dockerfile, docker-compose.yaml, and .dockerignore files).
* **lib/blueprints/**: Scripts for injecting Web, Node, C++, Python, and Express files.

---

## 📋 Usage Guide

### Flags
| Flag | Parameter | Purpose |
| :--- | :--- | :--- |
| -n | name | Sets the project name and root directory. |
| -t | type | Selects stack: web, node, cpp, py, or express. |
| -m | N/A | Generates a real-time Vortex System Report (Disk/RAM). |
| -d | N/A | Generates a containerized environment using Docker. |
| -h | N/A | Displays the help manual. |

### Example Commands
* Initialize a C++ Project:
`./vortex -n my_project -t node`

* Check System Health:
`./vortex -m`

* Create Docker container:
`./vortex -n my_project -t express -d`

* Full stack example:
`./vortex -n my_project -t python -m -d`

---

## 📈 Roadmap
- [x] **Milestone 1**: Core Engine and CLI Switchboard.
- [x] **Milestone 2**: System Guards and Resource Monitoring.
- [x] **Milestone 3**: Ghost Essentials (Systemd integration & Discord pings).
- [x] **Milestone 4**: Automated Docker containerization.

## 💡 Pro-Tips

### Streamline your GitHub Workflow
If you find yourself entering your GitHub credentials every time Vortex pushes a project, you can tell Git to remember you:
```bash
git config --global credential.helper store
```
