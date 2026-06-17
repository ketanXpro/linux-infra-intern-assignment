# Linux Infrastructure Intern Assignment

## Overview
This project demonstrates Linux infrastructure setup and management in a local Ubuntu Server VirtualBox VM.

## Project Structure

- scripts/
  - provision.sh
  - validate.sh
  - maintenance.sh

- systemd/
  - infra-demo.service
  - infra-maintenance.service
  - infra-maintenance.timer

- config/
  - infra-demo.env

- docs/
  - hardening-checklist.md
  - test-plan.md
  - troubleshooting.md
  - local-vm-reprovisioning.md

- evidence/
  - health_check.txt

## Setup

1. Clone the repository
2. Run:

```bash
chmod +x scripts/*.sh
./scripts/provision.sh
./scripts/validate.sh
