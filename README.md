# Documenso (YunoHost custom app)

This app runs Documenso in Docker with a path-based reverse proxy.

## Notes
- Install path e.g. `/sign` (or install at root `/` on its own subdomain)
- Optional SMTP (config panel). Hinweis: bei Docker muss SMTP **über den Host** erreichbar sein → `host.docker.internal:25` (mit extra_hosts gesetzt). `127.0.0.1` funktioniert im Container nicht.
- Postgres is bundled via Docker (no external DB needed)
- SSO disabled on the app's domain (required for public access on some setups)

## Install (terminal)
### 1) Install Docker on the VPS (if not already installed)
```bash
sudo apt update
sudo apt install -y docker.io docker-compose-plugin
sudo systemctl enable --now docker
```

### 2) Install the app from the repo
```bash
sudo yunohost app install https://github.com/WhiteCrispStudios/documenso_ynh
```

### 3) Configure SMTP (optional)
In YunoHost Web UI → Apps → Documenso → Configuration.

## Install (Web UI)
YunoHost Web UI → Apps → Install → From a repository
Repo URL:
```
https://github.com/WhiteCrispStudios/documenso_ynh
```
