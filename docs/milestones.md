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

## Milestone 3: Ghost Essentials
- Development of a background file watcher to monitor project activity.
- Implementation of the ghost committer to provide automated git reminders.
- Creation of the time machine module for automated local backups.

## Milestone 4: Production Deployment
- Integration of automated Docker containerization for project environments.
- Development of the live portal feature to provide instant public URLs for previews.
