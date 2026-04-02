# Vortex Project Milestones

## Milestone 1: Core Engine and CLI Switchboard
- [x] Implement help display using heredoc for clean terminal output.
- [x] Build the command line argument funnel using getopts to handle project names and types.
- [x] Develop the directory architecture engine to automate project folder creation.
- [x] Inject professional boilerplates to generate starting files for Python and JavaScript.

## Milestone 2: System Guards and Resource Monitoring
- [x] Integrate disk storage checks using df and awk to prevent installation on full drives.
- [x] Build a memory monitor to verify available RAM before project initialization.
- [x] Develop a dependency check using the command utility to verify Git, Node, and Docker.
- [x] Implement error handling logic to halt execution if system requirements are not met.

## Milestone 3: Ghost Essentials
- [x] Develop a background Git watcher using systemd.timer for 5-minute interval polling.
- [x] Create a Discord notification system that triggers on 50+ line insertions.
- [x] Implement a state file in /tmp/ to track notifications and prevent duplicate pings.
- [x] Build a setup flow in lib/ghost that prompts for the Discord Webhook URL on the first run.
- [x] Move script execution to a systemd service with environment-agnostic pathing.

## Milestone 4: Production Deployment
- [ ] Integrate automated Docker containerization for project environments.
- [ ] Develop the live portal feature to provide instant public URLs for previews.
