# Ansible Docker Apache WebApp Deployment

## 📌 Project Overview

This project demonstrates how to deploy a web application using **Ansible** and **Docker**.
The playbook automatically provisions a container running the Apache HTTP server and deploys a custom web page generated from an Ansible template.

The deployed page displays a message containing the hostname of the target machine.

---

## 🛠 Technologies Used

* Ansible
* Docker
* Apache HTTP Server (httpd image)
* YAML
* Jinja2 Templates
* Git / GitHub

---

## 📂 Project Structure

```
webapp/
│
├── deploy.yml
├── host.yml
├── ansible.cfg
│
├── templates/
│   └── index.html.j2
│
└── group_vars/
    └── prod
```

---

## ⚙️ Features

* Automated infrastructure configuration using Ansible
* Deployment of an Apache container using Docker
* Installation of required packages (`git`, `wget`) using Ansible loops
* Conditional installation based on the operating system
* Dynamic webpage generation using Jinja2 templates
* Volume mounting to serve a custom Apache web page
* Infrastructure-as-Code approach

---

## 🚀 Deployment

Run the playbook using:

```
ansible-playbook -i host.yml deploy.yml
```

This will:

1. Install required dependencies
2. Generate the web page from the template
3. Deploy an Apache container
4. Mount the generated HTML page into the container

---

## 🌐 Result

After deployment, the web page is accessible at:

```
http://<CLIENT_IP>:80
```

The page will display:

```
Bienvenue sur <hostname>
```

---

## 📚 Learning Objectives

This project was created as part of a DevOps training exercise to practice:

* Ansible automation
* Docker container deployment
* Infrastructure configuration management
* Template rendering with Jinja2
* Git version control

---

## 👤 Author

Ulrich Kouatang
