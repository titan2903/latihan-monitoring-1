<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>

# Set up Grafana using Ansible

## Build with

* [![Ansible][Ansible-image]][Ansible-url]

## Pre-requisites

* Install Ansible on your local computer
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

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Setup and Installation

1. Clone this repository

   ```sh
    git clone https://github.com/titan2903/latihan-monitoring-1.git
   ```

2. Install and configure Grafana Tempo
  
    ```sh
     ansible-playbook -i inventory.ini tempo-playbook.yaml
    ```

3. Install and configure Golang server and Golang service

    ```sh
     ansible-playbook -i inventory.ini goapp-playbook.yaml
    ```

4. Install and configure Nginx server

    ```sh
     ansible-playbook -i inventory.ini nginx-playbook.yaml
    ```

5. Install and configure Prometheus server

    ```sh
     ansible-playbook -i inventory.ini prometheus-playbook.yaml
    ```

6. Install and configure Loki server

    ```sh
     ansible-playbook -i inventory.ini loki-playbook.yaml
    ```

7. Install and configure Grafana server

    ```sh
     ansible-playbook -i inventory.ini grafana-playbook.yaml
    ```

8. Grafana running on port `3000`

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[Ansible-url]: https://www.ansible.com/
[Ansible-image]: https://img.shields.io/badge/ansible-FFFFF0?style=for-the-badge&logo=ansible&logoColor=black
