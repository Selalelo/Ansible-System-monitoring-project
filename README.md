# Ansible-System-monitoring-project

Automated Ansible project for setting up system monitoring with Prometheus and Grafana on multiple servers.

![Prometheus Logo](https://prometheus.io/assets/icon-120.png) ![Grafana Logo](https://grafana.com/static/assets/img/grafana_icon.svg)

## Overview

This Ansible project automates the deployment of Prometheus and Grafana for system monitoring on multiple servers. Prometheus is responsible for scraping metrics, and Grafana provides a visual interface for monitoring and analysis.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Setup](#setup)
- [Configuration](#configuration)
- [Usage](#usage)
- [Customization](#customization)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

- Ansible installed on your local machine.
- Target servers (e.g., AWS EC2 instances) with SSH key authentication.
- Internet access from target servers for package installation.

## Project Structure

- `inventory/`: Ansible inventory file specifying target server details.
- `roles/`: Roles for Prometheus, Node Exporter, and Grafana.
- `playbook.yml`: Main Ansible playbook orchestrating the deployment.

## Setup

1. Update the `inventory/hosts` file with the IP addresses or hostnames of your target servers.
2. Run the Ansible playbook:

   ```bash
   ansible-playbook -i inventory/hosts playbook.yml
Configuration

    Edit inventory/hosts to specify the IP addresses or hostnames of your target servers.
    Customize role variables in roles/*/defaults/main.yml for specific configurations.

Usage

    Access Prometheus web interface at http://<prometheus-server-ip>:9090.
    Access Grafana web interface at http://<grafana-server-ip>:3000 (default credentials: admin/admin).

Customization

Feel free to customize the playbook and roles to suit your environment. Explore individual role tasks and templates for further adjustments.
Troubleshooting

    Check Ansible output for error messages during playbook execution.
    Inspect log files on target servers (e.g., /var/log/*) for specific role-related errors.

Contributing

Contributions are welcome! If you have improvements or additional features to suggest, open an issue or submit a pull request.
License

This project is licensed under the MIT License.
