# 🐳 Docker Homelab (Devuan + Compose)

A practical guide to running a **clean, reproducible Docker homelab** on bare metal using Devuan and Docker Compose.

This is the exact model used in RebelRx.

---

## 🔥 Why Docker (Not Proxmox)

You *can* use Proxmox. Many people do.

But for most homelabs, it introduces unnecessary complexity.

### ❌ Proxmox Challenges

- VM overhead (CPU + RAM waste)
- More layers to debug
- Backup complexity
- Networking becomes harder than it should be
- Encourages fragmentation (many small VMs instead of a unified system)

---

### ✅ Why Prefer Docker Bare Metal

- **Lightweight** → no virtualization overhead  
- **Simple** → one OS, one system to manage  
- **Fast deployments** → spin up services in seconds  
- **Reproducible** → everything defined in Compose  
- **Portable** → move your entire stack with Git  

> 💡 If you're not running enterprise multi-tenant workloads, you likely don’t need a hypervisor.

---

## ⚙️ Requirements

- PC or Laptop
- Internet access
- Devuan

If you don't have a dedicated PC, you can purchase one of these inexpensive mini PC boxes that includes RAM and SSD to get started right away: [Beelink Mini S12](https://www.amazon.com/gp/product/B0BW8JSQCH/ref=ox_sc_saved_image_1?smid=A2TEGSI85MTM6G)

If you don't have Devuan installed, see the [Devuan Linux Server Install Guide](../linux/devuan-server-install.md)

---

## 📦 Install Dependencies

```bash
sudo apt update
sudo apt install -y ca-certificates curl gnupg git
```

---

## 🔑 Add Docker Repository

```bash
sudo install -m 0755 -d /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/debian/gpg | \
  sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo $VERSION_CODENAME) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

---

## 🐳 Install Docker + Compose

```bash
sudo apt update

sudo apt install -y \
  docker-ce \
  docker-ce-cli \
  containerd.io \
  docker-buildx-plugin \
  docker-compose-plugin
```

---

## 🚀 Enable + Start Docker (SysVinit)

```bash
sudo service docker start
sudo update-rc.d docker defaults
```

Verify:

```bash
docker --version
docker compose version
```

---

## 🔐 Add User to Docker Group

```bash
sudo usermod -aG docker $USER
newgrp docker
```

Test:

```bash
docker run hello-world
```

---

## 📁 Directory Structure

This guide uses a **clean, predictable layout**:

```bash
~/docker/
├── compose/        # Docker Compose stacks (YAML)
└── apps/           # Persistent app data
    ├── plex/
    ├── nginx/
    ├── nextcloud/
    └── ...
```

### Why this matters

- Separation of **config vs data**
- Easier backups
- Cleaner Git repos
- Avoids Docker “sprawl”

---

## 🚀 Clone RebelRx Homelab Template

```bash
cd ~
git clone https://github.com/rebelrx/rebelrx-homelab.git docker
```

> This repo provides **real-world Compose templates** used in production.

---

## 📦 Template Structure

Inside the repo:

```bash
docker/
└── compose/
   ├── arr/
   ├── audiobooks/
   ├── authentik/
   └── ...
```

Each stack typically includes:

- `docker-compose.yml`
- `.env.example`
- README (usage notes)

---

## 🧠 Key Concepts (Read This First)

### 1. Compose-First Mindset

Everything is defined in YAML.

- No clicking around in GUIs
- No manual container creation
- Git = source of truth

---

### 2. `.env` Files

Each stack uses environment variables:

```env
PUID=1000
PGID=1000
TZ=America/New_York
```

**Why this matters:**

- Consistent permissions
- Portable configs
- Easy overrides

---

### 3. Volume Mapping

```yaml
volumes:
  - ~/docker/apps/plex:/config
```

This ensures:

- Data persists across container restarts
- Easy backups
- Full control over storage

---

### 4. Port Binding

```yaml
ports:
  - 127.0.0.1:8080:8080
```

**Best practice:**

- Bind to `127.0.0.1` for internal services
- Use a reverse proxy for external access

---

## 🌐 Reverse Proxy (Nginx Proxy Manager)

Recommended approach:

- Run **Nginx Proxy Manager (NPM)**
- Expose services via subdomains
- Handle SSL automatically

Example:

```text
https://plex.yourdomain.com
```

Benefits:

- No port juggling
- Clean URLs
- Centralized access control

---

## ▶️ Running Your First Stack

```bash
cd ~/docker/compose/proxy

cp .env.example .env
nano .env
```

Then:

```bash
docker compose up -d
```

---

## 🔄 Updating Containers

```bash
docker compose pull
docker compose up -d
```

---

## 🧼 Cleanup

Remove unused resources:

```bash
docker system prune -a
```

---

## ⚠️ Common Pitfalls

### ❌ Permission Issues

```bash
sudo chown -R $USER:$USER ~/docker
```

---

### ❌ Ports Already in Use

```bash
ss -tulnp | grep :PORT
```

---

### ❌ Containers Not Updating

```bash
docker compose pull
```

---

### ❌ Editing Running Containers

Don’t.

Edit the **Compose file**, then redeploy.

---

## 🧠 Final Thoughts

This setup is built around a few principles:

- **Keep it simple**
- **Define everything in code**
- **Own your infrastructure**
- **Avoid unnecessary layers**

Just Docker + Compose + discipline.

---

## 🔗 Suggested Next Steps

- Add more stacks from the RebelRx repo
- Set up reverse proxy with the "proxy" stack (NPM)
- Implement backups with the "backup" stack (Kopia)
- Use a Docker Compose stack manager with the "dockge" stack (Dockge)
- Add a file browser with the "filebrowser" stack (File Browser Quantum)

---

## ⚠️ Disclaimer

This guide is for educational purposes.

You are responsible for securing and maintaining your system.
