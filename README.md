# 📖 Overview

This Ansible role automates the installation of Docker and Docker Compose on remote servers, authenticates with DockerHub, pulls container images, and deploys applications using Docker Compose. It supports environment variables via `.env` files and can automatically restart the stack when configuration changes.

---

# 🛠️ Features

- Installs Docker engine and Docker Compose plugin  
- Logs into DockerHub using username + password or personal access token  
- Pulls container images from DockerHub or other registries  
- Deploys services defined in `docker-compose.yml`  
- Supports `.env` files for environment variables  
- Includes handlers to restart the stack when configs change  

---

# 🚀 Requirements

- Ansible **2.12+**  
- Python **3.x**  
- Target hosts running **Debian/Ubuntu**  
- DockerHub account and token (recommended)  
- SSH access to target hosts  
- Sudo privileges on target hosts  
- Git installed (if pulling code before deployment)  
- Docker installed on control node (optional, for testing locally)  

---

# 📂 Role Variables

```yaml
dockerhub_username: "myuser"
dockerhub_token: "mytoken"
docker_image: "myorg/myapp:latest"
app_port: "3000"
# ▶️ Usage

### Run the Playbook

Use the following command to execute the playbook against your inventory:

```bash
ansible-playbook -i inventory.ini playbook.yaml


