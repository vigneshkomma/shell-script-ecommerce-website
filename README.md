# E-Commerce LAMP Stack Automated Deployment

This bash script completely automates the installation, configuration, and deployment of a multi-tier PHP e-commerce application on a RHEL/CentOS-stream (YUM-based) system.

## What It Does
* **Security:** Installs and configures `firewalld` (opens ports 80 and 3306).
* **Database:** Installs MariaDB, initializes the `ecomdb` database, and populates a dummy `products` table.
* **Web Server:** Installs Apache (`httpd`), PHP, and modules.
* **Deployment:** Clones the e-commerce source code from GitHub and sets up the application's environment configuration (`.env`).

## Prerequisites
* A clean RHEL, CentOS, or Rocky Linux instance.
* Sudo privileges.
* Internet access to download packages and clone the repository.

## How to Use

1. **Download or copy the script** to your server (e.g., save it as `deploy.sh`).
2. **Make the script executable:**
   ```bash
   chmod +x deploy.sh