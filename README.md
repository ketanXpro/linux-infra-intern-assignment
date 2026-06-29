Markdown

# Linux Server Provisioning & Automation Lab

## Overview

This project demonstrates automated Linux server provisioning, validation, maintenance automation, systemd service management, and basic security hardening using Ubuntu Server in a local VirtualBox environment. The project focuses on creating a reproducible deployment-ready server using Bash automation and Linux administration best practices.


---

## Environment

* Operating System: Ubuntu Server
* Virtualization Platform: VirtualBox
* Infrastructure Type: Local Virtual Machine
* Cloud Providers Used: None

All work was completed and tested on a local Ubuntu Server VM. No cloud VM, cloud provider, or external infrastructure service was used.

---

## Project Structure

```text
linux-server-provisioning-automation-lab/

├── app/
│   └── health server application

├── config/
│   └── infra-demo.env

├── docs/
│   ├── hardening-checklist.md
│   ├── test-plan.md
│   ├── troubleshooting.md
│   └── local-vm-reprovisioning.md

├── evidence/
│   └── health_check.txt

├── scripts/
│   ├── provision.sh
│   ├── validate.sh
│   └── maintenance.sh

├── systemd/
│   ├── infra-demo.service
│   ├── infra-maintenance.service
│   └── infra-maintenance.timer

└── README.md
```

---

## Components

### Python Health Server

Provides a simple health endpoint for validation and monitoring.

### Provision Script

Automates infrastructure setup and configuration.

### Validation Script

Verifies service availability and expected behavior.

### Maintenance Script

Performs maintenance-related operations.

### Environment Configuration

Stores application configuration values.

### Systemd Service Files

Used to manage application startup and automated maintenance tasks.

---

## Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/ketanXpro/linux-server-provisioning-automation-lab.git cd linux-server-provisioning-automation-lab
```

### 2. Make Scripts Executable

```bash
chmod +x scripts/*.sh
```

### 3. Run Provisioning

```bash
./scripts/provision.sh
```

### 4. Run Validation

```bash
./scripts/validate.sh
```

---

## Validation

Verify application availability:

```bash
curl http://localhost:8080
```

Expected Output:

```text
OK
```

Validation can also be executed using:

```bash
./scripts/validate.sh
```

---

## Systemd Services

Included service files:

### infra-demo.service

Responsible for managing the application service.

### infra-maintenance.service

Responsible for running maintenance tasks.

### infra-maintenance.timer

Schedules maintenance operations automatically.

Example usage:

```bash
sudo systemctl daemon-reload

sudo systemctl enable infra-demo.service
sudo systemctl start infra-demo.service

sudo systemctl enable infra-maintenance.timer
sudo systemctl start infra-maintenance.timer
```

---

## Documentation

The following documentation is included:

### Hardening Checklist

Location:

```text
docs/hardening-checklist.md
```

Contains security hardening measures that were implemented, along with explanations for configurations that were intentionally left unchanged.

### Test Plan

Location:

```text
docs/test-plan.md
```

Contains validation and testing procedures.

### Troubleshooting Guide

Location:

```text
docs/troubleshooting.md
```

Contains troubleshooting steps and common fixes.

### Reprovisioning Guide

Location:

```text
docs/local-vm-reprovisioning.md
```

Contains instructions for rebuilding the local environment.

---

## Evidence

Evidence files are available in:

```text
evidence/
```

Example:

```text
evidence/health_check.txt
```

These files demonstrate successful validation and testing of the environment.

---

## Security Considerations

* No private keys committed
* No passwords committed
* No tokens committed
* No API credentials committed
* No personal secrets committed
* No cloud infrastructure used
* Work performed entirely within a local VM

---

## Hardening

Security-related checks and hardening recommendations are documented in:

```text
docs/hardening-checklist.md
```

---

## Demo Video

Demo Video

Google Drive:

https://drive.google.com/drive/folders/1gk4jQnRSMcqs40xzZqegpAjsiDT3cJ7N

---

## Features

- Automated Linux server provisioning using Bash scripts
- Systemd service and timer configuration for service management
- Python-based HTTP health monitoring service
- Automated infrastructure validation and health checks
- Environment-based configuration using `.env` files
- Basic Linux security hardening with documented practices
- Maintenance automation for periodic system tasks
- Local VirtualBox VM deployment and reproducible setup
- Comprehensive documentation and troubleshooting guides
- Validation and reboot-survival testing

---

## Technologies Used

- **Operating System:** Ubuntu Server
- **Virtualization:** Oracle VirtualBox
- **Scripting:** Bash
- **Programming Language:** Python
- **Service Manager:** systemd
- **Version Control:** Git & GitHub
- **Command-Line Tools:** Linux CLI

---

## Author

Ketan Kumbhar

B.Tech Information Technology

