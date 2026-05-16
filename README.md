# Crypto Tax Tracker Backend

## Quick Start (Podman Recommended)

### 1. Download / Clone the Repository
```bash
git clone https://github.com/trubel/crypto-tax-tracker.git
cd crypto-tax-tracker

### 2. Start the Container
```bash
podman compose up --build -d
```

### 2. Create Persistent Volumes (One-time only)
```bash
podman volume create crypto-tax-tracker_config_data
podman volume create crypto-tax-tracker_postgres_data
```

### 3. Start the Container
podman compose up --build -d

### 4. Complete Setup via Guided Admin Page Wizard

**Immediately after the container starts**, open your browser and go to:

**http://localhost:7777/admin**

Follow the wizard to:
- Change the default PostgreSQL password
- Configure JWT secret and other backend settings
- Save all configuration

The backend will apply your settings and be ready for use.

**Pull the latest changes** to get the updated README:

```bash
git pull origin main

## Docker Alternative

The same steps work with Docker:
```bash
docker compose up --build -d
```

## Important Notes
- The only thing you need to do is set up the local volumes.
- All configuration (including database connection) is handled through the Guided Admin Page.
- OAuth secrets are **not** stored in .env files — they are encrypted in the DB.

Repo: https://github.com/trubel/crypto-tax-tracker
