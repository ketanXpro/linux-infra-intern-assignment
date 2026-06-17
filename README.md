Markdown

# Linux Infrastructure Intern Assignment

## Overview

This project demonstrates Linux infrastructure provisioning, validation, maintenance automation, service management, and documentation using Ubuntu Server running in a local VirtualBox virtual machine.

The assignment includes provisioning scripts, validation scripts, maintenance automation, systemd services, documentation, and evidence generated during testing.

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
linux-infra-intern-assignment/

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
git clone <repository-url>
cd linux-infra-intern-assignment
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

Contains security and hardening recommendations applied during the assignment.

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

Demo Video Link:

```text
N/A
```

(Add your demo video URL here if available.)

---

## AI Assistance Notes

AI tools (ChatGPT) were used for:

* Linux command explanation
* VirtualBox shared folder troubleshooting
* Shell scripting guidance
* Documentation structure guidance
* GitHub workflow assistance
* General Linux administration learning

Manual verification performed:

* All commands executed manually inside Ubuntu Server
* Provisioning process tested manually
* Validation process tested manually
* Systemd configuration verified manually
* Shared folder configuration verified manually
* Archive generation verified manually
* Repository accessibility verified manually
* Final submission package verified manually

All submitted work was executed, tested, and verified within the local Ubuntu VirtualBox environment.

---

## Author

Ketan Kumbhar

B.Tech Information Technology

Ubuntu Server Infrastructure Assignment


