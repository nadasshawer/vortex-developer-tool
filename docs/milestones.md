# Vortex Project Milestones

## Milestone 1: Core Engine and CLI Switchboard
- Implemented help display using heredoc for clean terminal output.
- Built the command line argument funnel using getopts to handle project names and types.
- Developed the directory architecture engine to automate project folder creation.
- Integrated a boilerplate injector to generate starting files for Python and JavaScript.

## Milestone 2: System Guards and Resource Monitoring
- Integrated disk storage sentry using df and awk to prevent installation on full drives.
- Built a memory monitor to verify available RAM before project initialization.
- Developed a dependency detective using the command utility to verify Git, Node, and Docker.
- Implemented error handling logic to halt execution if system requirements are not met.

## Milestone 3: Ghost Essentials (COMPLETED - April 2026)
- [x] **Automated Activity Monitoring**: Engineered a background Git watcher using `systemd.timer` for 5-minute interval polling.
- [x] **Smart Discord Integration**: Developed a webhook-based notification system that triggers only on 50+ line insertions.
- [x] **State-Aware Logic**: Implemented a temporary state file in `/tmp/` to track notification history and prevent redundant pings.
- [x] **Interactive Configuration**: Created a first-run setup flow in `lib/ghost` that prompts for and persists the Discord Webhook URL.
- [x] **Systemd User-Space Architecture**: Migrated script execution from manual loops to a `oneshot` systemd service with environment-agnostic pathing (`%h`).

## Milestone 4: Production Deployment (IN PROGRESS)
- [ ] Integration of automated Docker containerization for project environments.
- [ ] Development of the live portal feature to provide instant public URLs for previews.
