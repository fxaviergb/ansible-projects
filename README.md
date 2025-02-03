# Example Projects Repository with Ansible and Vagrant

This repository contains practical examples of using **Ansible** and **Vagrant** to create and automatically configure development and testing environments. Each example demonstrates how to set up common services and applications using automated provisioning.

## Included Examples

### 1. `ansible-vagrant-apache`
An environment that deploys an **Apache** web server using Ansible. This example shows how to configure a basic server with static pages and minimal customizations.

### 2. `ansible-vagrant-nginx`
This example deploys an **NGINX** server, illustrating common configurations such as reverse proxies and handling multiple virtual hosts.

### 3. `ansible-vagrant-wordpress`
An environment that installs and configures a **WordPress** site. Includes:
- Configuration of **NGINX** as a web server.
- Access restrictions for sensitive pages like `/wp-admin` and `/wp-login.php`.
- Redirecting traffic from port 80 to 8080.

## Requirements

Before using any of the examples, make sure you have the following software installed on your system:

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## How to Use the Examples

1. Clone this repository:
   ```sh
   git clone <REPOSITORY-URL>
   cd <repository-name>
   ```

2. Navigate to the directory of the example you want to try, for example:
   ```sh
   cd ansible-vagrant-wordpress
   ```

3. Start the virtual machine and provision it by running:
   ```sh
   vagrant up
   ```
   This command will start the virtual machine and apply the corresponding Ansible playbook.

4. Once finished, you can access the configured service according to the specific example instructions.

## Stopping and Destroying Environments

To stop the virtual machine without destroying its configuration:
```sh
vagrant halt
```

To completely remove the virtual machine and free up disk space:
```sh
vagrant destroy -f
```

## Contributions

If you want to add new examples or improve existing ones, feel free to submit **pull requests** or open **issues** in this repository.

## License

This repository is licensed under the **MIT** license.
