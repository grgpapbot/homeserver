# Homeserver

This repository contains the configuration for a Raspberry Pi homeserver using Docker and Ansible.

## Services

- Jellyfin (Media Server)
- Prometheus (Monitoring)
- Grafana (Monitoring Dashboard)

## Setup

1. Clone this repository
2. Run the initial setup:
   ```bash
   ansible-playbook -i ansible/inventory.yml ansible/playbooks/setup.yml
   ```
3. Deploy services:
   ```bash
   cd docker
   docker-compose up -d
   ```

## Directory Structure

- `/opt/homeserver/`
  - `jellyfin/` - Jellyfin configuration and cache
  - `media/` - Media files for Jellyfin
  - `prometheus/` - Prometheus data and configuration
  - `grafana/` - Grafana configuration and data

## Monitoring

- Grafana: http://your-pi-ip:3000
- Prometheus: http://your-pi-ip:9090
- Jellyfin: http://your-pi-ip:8096