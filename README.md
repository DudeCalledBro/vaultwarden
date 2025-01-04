# Vaultwarden

[![CI](https://github.com/DudeCalledBro/vaultwarden/actions/workflows/ci.yml/badge.svg)](https://github.com/DudeCalledBro/vaultwarden/actions/workflows/ci.yml)

This repository contains Ansible playbooks and configurations for deploying Vaultwarden (an open-source password manager) along with a reverse proxy to manage incoming traffic and secure access.

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)
- Ensure Docker is installed (you may want to checkout my [ansible-docker-role](https://github.com/DudeCalledBro/ansible-role-docker))

## Setup

Before running the playbook, you'll need to configure the deployment by setting up the necessary inventory and configuration files.

1. Copy the example inventory file to `inventory.yml`:

    ```bash
    cp example.inventory.yml inventory.yml
    ```

2. Copy the example configuration file to config.yml. This file contains essential settings for your Vaultwarden deployment.

    ```bash
    cp example.config.yml config.yml
    ```

    > **Default Variables**: Take a moment to inspect the defaults directory within the roles to ensure that all variables are correctly set up according to your needs.

3. Once your configuration files are in place, you can deploy Vaultwarden by running the following Ansible playbook:

    ```bash
    ansible-playbook play-vaultwarden.yml
    ```

## Additional Resources

- [Vaultwarden Documentation](https://github.com/dani-garcia/vaultwarden/wiki/): For more detailed information on Vaultwarden, including setup, configuration, and usage, refer to the official documentation.

## License

Copyright © 2025 Niclas Spreng

Licensed under the [MIT license](LICENSE).
