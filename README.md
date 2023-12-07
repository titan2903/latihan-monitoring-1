# Set up Grafana using Ansible

## Build with

* [![Ansible][Ansible-image]][Ansible-url]

## Pre-requisites

* Set up six servers using [**Ubuntu Server 22.04.3 LTS**](https://ubuntu.com/download/server) for the Grafana, Loki, Prometheus, Tempo, Golang service and Nginx by deploying Virtual Machines (VMs) on a laptop, utilizing platforms such as [**VirtualBox**](https://www.virtualbox.org/) or a Cloud Provider
* Virtual Machine (VM) specifications are as follows:
  * [**Ubuntu Server 22.04.3 LTS**](https://ubuntu.com/download/server)
  * At least 2 vCPU
  * Minimum of 4GB RAM
  * Minimum storage capacity of 10GB

## What will do ?

* Configure the Prometheus server
* Configure the Loki server
* Install and configure the Golang server
* Install and configure the Nginx server
* Install and configure the Node Exporter agent on the Nginx server and integrate it with Prometheus
* Install and configure the Promtail agent on the Nginx server and integrate it with Loki
* Install and configure the Node Exporter agent on the Golang server and integrate it with Prometheus
* Install and configure the Promtail agent on the Golang server and integrate it with Loki
* Configure the Grafana Tempo server
* Configure Grafana Tempo on the Golang server
* Set up the Grafana server and establish integration with Prometheus, Loki and Tempo

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[Ansible-url]: https://www.ansible.com/
[Ansible-image]: https://img.shields.io/badge/ansible-FFFFF0?style=for-the-badge&logo=ansible&logoColor=black
