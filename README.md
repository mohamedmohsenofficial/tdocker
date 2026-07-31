<div align="center">
  <img src="Images/Tdocker.png" alt="TDocker Logo" width="2000">

# 🐳 TDocker - Terminal Container Manager

</div>

![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=for-the-badge)
![Bash](https://img.shields.io/badge/Language-Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Supported-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Podman](https://img.shields.io/badge/Podman-Supported-892CA0?style=for-the-badge&logo=podman&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

**TDocker** is a lightweight terminal-based container management tool designed to simplify deployment, updates, HTTPS integration, cleanup, and day-to-day administration for both **Docker** and **Podman** without relying on heavy web dashboards.

It provides a single interactive interface for managing your containers, generating Compose configurations, enabling HTTPS with Caddy, and keeping your environments organized. Built for developers, homelab users, self-hosting enthusiasts, and anyone who prefers working directly from the terminal.

---

## ✨ Features

### 🚀 Deploy Containers
Create and launch new containers from a simple interactive menu. TDocker automatically generates the required Compose configuration (Docker or Podman) and starts the container for you.

### 🔒 Import Existing Containers
Already running a container? Import it into TDocker management without rebuilding everything from scratch. The tool automatically detects the image, internal/external ports, mounted volumes, and existing configuration, then generates a reusable Compose file.

### 🌐 HTTPS Integration (Docker Only)
Enable HTTPS access using Caddy Proxy. When encryption is enabled, TDocker automatically connects containers to the required network, configures routing labels, and creates HTTPS-enabled local domains (e.g., `https://myapp.localhost`), simplifying local development and testing.

### 🛠️ Container Management Dashboard
Manage containers directly from the terminal. Available actions include:
Start, Stop, Restart, Pause, Resume, Kill, Remove, Rename, Change image, Modify ports, and Recreate configuration—no manual Compose editing required.

### 🔄 Update All Containers
Update all managed services from a single menu option. TDocker pulls the latest images, recreates the containers, and applies updates automatically.

### 🧹 Space Recovery & Cleanup
Container environments accumulate unused resources over time. TDocker includes a cleanup mode that safely removes stopped containers, dangling/unused images, unused networks, build cache, and unused volumes. It displays a summary and estimated storage recovery before executing.

---

## ⚠️ Requirements

TDocker requires either Docker or Podman installed on your system.

**For Docker Users:**
```bash
# Debian / Ubuntu
sudo apt update && sudo apt install docker.io docker-compose-v2
sudo systemctl enable --now docker
```
```bash
# Fedora
sudo dnf install docker docker-compose
sudo systemctl enable --now docker

# Arch Linux
sudo pacman -S docker docker-compose
sudo systemctl enable --now docker

```

**For Podman Users:**
Install `podman` and `podman-compose` using your distribution's package manager.

*(Optional but recommended): Add your user to the docker group to run commands without sudo.*

```bash
sudo usermod -aG docker $USER
# Log out and back in for the change to take effect.

```

---

## 🚀 Installation & Updating

**Installation:**
Run this single command to download TDocker, make it executable, and move it to your system binaries:

```bash
sudo curl -L "[https://raw.githubusercontent.com/mohamedmohsenofficial/tdocker/main/tdocker](https://raw.githubusercontent.com/mohamedmohsenofficial/tdocker/main/tdocker)" -o /usr/local/bin/tdocker && sudo chmod +x /usr/local/bin/tdocker

```

**Updating:**
TDocker features a built-in auto-updater. Every time you run the script, it checks the repository in the background. If a new version is available, it applies the update automatically.

---

## 💻 How to Use

Simply launch the tool by typing:

```bash
tdocker

```

**On first launch:**

1. Select a working directory to store your configurations.
2. Choose an action from the interactive menu.
3. Follow the simple prompts to deploy or manage your containers.

---

## 🏆 Comparison

| Feature | TDocker | Portainer | Docker CLI |
| --- | --- | --- | --- |
| **Terminal Based** | ✅ | ❌ | ✅ |
| **Interactive UI** | ✅ | ✅ | ❌ |
| **Dual Engine (Docker/Podman)** | ✅ | Partial | ❌ |
| **Compose Generation** | ✅ | Partial | Manual |
| **Auto HTTPS Integration** | ✅ | Manual | Manual |
| **Bulk Updates** | ✅ | Partial | Manual |
| **Resource Usage** | Very Low | Higher | Very Low |

---

## 🤝 Contributing

This is a community-powered open-source project. Contributions are welcome for new management features, better workflows, documentation improvements, and bug fixes. Feel free to open an Issue or Pull Request.

---

## 📜 License

This project is released under the MIT License. You are free to use, modify, distribute, and fork for both personal and commercial projects.

---

## 💖 Support

If this tool simplifies your workflow, consider supporting its development. Every contribution helps improve features and maintain the project.

Built for my own needs, shared with the community. Thank you for using TDocker.
