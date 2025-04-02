# Tic-Tac-Toe DevOps Project
## Check the `master` branch for all the code and configs!
## Overview
This project is a DevOps showcase featuring a Tic-Tac-Toe web app built with Flask. It uses a complete pipeline to automate building, testing, and deploying the app to a Kubernetes cluster. The app is live locally, versioned, and fully managed with modern DevOps tools.

- **GitHub**: [github.com/GeyasreeR/TicTacToe](https://github.com/GeyasreeR/TicTacToe)
- **Docker Hub**: [geyasreer/tictactoe](https://hub.docker.com/r/geyasreer/tictactoe)
- 
## What It Does
- Runs a Flask app displaying the version.
- Automatically builds and pushes Docker images when code is pushed.
- Deploys tagged versions (like `v0.3.1`) to a Kubernetes cluster.
- Sets up a VM to host everything.

## Tools Used
- **Git & GitHub**: For code and version control.
- **GitHub Actions**: Automates the pipeline.
- **Docker**: Packages the app into containers.
- **Kubernetes & Helm**: Runs and manages the app.
- **Vagrant**: Creates the VM.
- **Python & Flask**: Powers the app.
- **Pytest & Flake8**: Checks code quality.

## How It Works
1. **Code**: Write and push changes to GitHub (on `master` branch).
2. **Build**: GitHub Actions checks code quality, builds a Docker image, and pushes it to Docker Hub.
   - Pushes to `master` → `latest` image.
   - Tags like `v0.3.1` → versioned image (`0.3.1`).
3. **Deploy**: For tags, it connects to the VM and updates Kubernetes with the new version.
4. **Run**: The app runs on the VM, accessible via browser.

All code and config files are available on the `master` branch.

## Live App Screenshot
Here’s what the app looks like running at `http://192.168.56.14:30000`:

![Tic-Tac-Toe Live App](https://github.com/user-attachments/assets/a6c392a3-0bb2-4fa0-b7be-c54e30ba020c)

## Setup
- **VM**: A Vagrant-provisioned Ubuntu VM with Kubernetes and Helm.
- **Network**: Local IP `192.168.56.14`, app on port `30000`.
- **Pipeline**: Triggered by GitHub pushes, fully automated with port forwarding to the VM.

## Achievements
- Built and deployed `v0.3.1` successfully.
- Automated image building and pushing.
- Deployed to Kubernetes with Helm via GitHub Actions.

## Run It Yourself
1. Clone the repo from `master`.
2. Start the VM with `vagrant up`.
3. Deploy manually if needed (see `master` for details).
4. Visit `http://192.168.56.14:30000`.

## Wrap-Up
This project ties together coding, automation, and deployment, Check the `master` branch for all the code and configs!
