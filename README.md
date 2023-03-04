# <p align="center">👾 Octopus 👾</p>

<!-- PROJECT LOGO -->
<br />
<div align="center">
   <p align="center">
     Handy knowledge of a clean and efficient way of configuring machines
   </p>
</div>

## About The Project

Octopus provides a clean and efficient way to configure machines and deploy applications. The "poll" application demonstrates how to use Octopus to deploy a multi-tiered application on multiple machines using Ansible. We hope this repository serves as a helpful resource for anyone looking to learn about machine configuration and application deployment.

# 🚀 Getting Started

The poll application starts with a Python Flask web client that gathers the votes, and then pushes them into a Redis queue. Afterwards, the Java worker consumes the votes stored in the Redis queue, and pushes them into a PostgreSQL database. Finally, the Node.js web client fetches the votes from the PostgreSQL database and displays the results.

With Ansible, we deploy the application onto 5 different machines, without using containers.

## 🛠️ Deployment


To deploy the poll application on multiple machines, we use Ansible, an open-source tool for automating software provisioning, configuration management, and application deployment.

To deploy the application, follow these steps:

1. Configure your machines and set up the production inventory file.
2. Set the ANSIBLE_VAULT_PASSWORD_FILE environment variable to point to a file containing the Ansible vault password.
3. Run the Ansible playbook against the production inventory file.

Here's an example of how to run the Ansible playbook:

```
export ANSIBLE_VAULT_PASSWORD_FILE=/tmp/.vault_pass
echo verySecretPassword > /tmp/.vault_pass
ansible-playbook -i production playbook.yml
```      

## Author

- [@agahakan](https://www.github.com/agahakan)
