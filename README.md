# Static Website Deployment on Google Cloud Platform

A static web application developed using HTML, CSS, and JavaScript and deployed to a Google Cloud Platform (GCP) virtual machine using Nginx.

The project demonstrates how a locally developed website can be transferred to a cloud environment, hosted on a virtual machine, and made publicly accessible through an external IP address.

## 📌 Project Overview

This project focuses on deploying a simple static website to the cloud and learning the fundamentals of cloud-based web hosting.

The website consists of:

- `index.html`
- `bestseller.css`
- `bestseller.js`
- `contact.html`
- `contact.css`
- `contact.js`

Since the application does not require a backend server or database, it was suitable for demonstrating basic cloud deployment, server configuration, file management, and web accessibility.

## ☁️ Cloud Platform

The application was deployed using **Google Cloud Platform (GCP)**.

### GCP Services Used

- **Google Compute Engine** – Used to create and manage the virtual machine hosting the website.
- **Cloud Console SSH** – Used to connect to the virtual machine and configure the server.
- **External IP Address** – Used to make the website accessible from outside the cloud environment.

GCP was selected because it provides a straightforward interface for creating virtual machines and sufficient resources for hosting a small static website. 1

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Website structure |
| CSS3 | Website styling |
| JavaScript | Website functionality |
| Google Cloud Platform | Cloud hosting |
| Compute Engine | Virtual machine |
| Linux | Server operating system |
| Nginx | Web server |
| SSH | Remote server access |

The project used an E2 family virtual machine, specifically an `e2-micro` instance with 1 vCPU and 1 GB of memory, together with a 10 GB persistent disk. 2

## 🏗️ Deployment Architecture

```text
                    Internet
                       │
                       ▼
                External IP Address
                       │
                       ▼
             Google Cloud Platform
                       │
                       ▼
              Compute Engine VM
                       │
                       ▼
                    Nginx
                       │
                       ▼
              /var/www/html
                       │
          ┌────────────┴────────────┐
          │                         │
       HTML Files              CSS / JS Files
