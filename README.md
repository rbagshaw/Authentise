# Ansible playbook to install Docker and run an Nginx container on Ubuntu 22.04 hosts

## What the playbook does

This playbook installs Docker and runs an Nginx container on Ubuntu 22.04 hosts. The playbook performs the following tasks:

1. Installs the prerequisites for Docker, including ca-certificates, curl, gnupg-agent, and the Docker GPG key.
2. Adds the Docker repository to the Apt sources list.
3. Installs the Docker packages.
4. Starts the Docker service.
5. Logs in to Docker Hub using the provided username and password.
6. Pulls the Nginx image from Docker Hub.
7. Starts the Nginx container, exposing port 443.

## Expected arguments

The playbook will prompt you for the following arguments at runtime:

* `docker_username`: Your Docker Hub username.
* `docker_password`: Your Docker Hub password.


## Variables

The playbook uses the following variables:

* `ubuntu_version`: The version of Ubuntu to install Docker on.
* `ubuntu_image`: The Ubuntu image to use when installing Docker.
* `nginx_image`: The Nginx image to pull and run.
* `container_name`: The name of the Nginx container.

## Running the playbook

To run the playbook, simply type the following command:

```
ansible-playbook playbook.yml
```