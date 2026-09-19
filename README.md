# LEMP-Stack-Deployment
Hands-on deployment and configuration of a LEMP stack on an Ubuntu EC2 instance, integrating Nginx, MySQL, and PHP to serve dynamic web content and manage database records.

# LEMP Stack Deployment on AWS EC2

> Hands-on deployment and configuration of a LEMP stack on an Ubuntu EC2 instance, integrating Nginx, MySQL, and PHP to serve dynamic web content and manage database records.

##  Project Overview

This project demonstrates the deployment of a LEMP stack environment on AWS EC2.

LEMP is a web application stack consisting of Linux, Nginx, MySQL, and PHP. The project involved provisioning a Linux server, configuring the web server, installing the database system, integrating PHP-FPM, and verifying database connectivity.

## Technologies Used

- **Amazon Web Services (AWS):** EC2
- **Operating System:** Ubuntu Server 24.04 LTS
- **Web Server:** Nginx
- **Database:** MySQL
- **Backend Processing:** PHP and PHP-FPM
- **PHP Database Integration:** php-mysql
- **Remote Access:** SSH
- **Testing:** cURL and web browser

## Architecture

The application components work together as follows:

1. Linux provides the server operating environment.
2. Nginx receives HTTP requests and serves web content.
3. PHP-FPM processes PHP scripts.
4. MySQL stores and manages application data.
5. PHP communicates with MySQL to retrieve and display database records.

## Implementation Steps

### 1. Provisioning the EC2 Instance

<img width="553" height="444" alt="image" src="https://github.com/user-attachments/assets/a53c079b-6c03-48d1-a4d0-546ebe9d0810" />


- Launched an EC2 instance using Ubuntu Server 24.04 LTS.
- Selected the t3.micro instance type.
- Created an SSH key pair for secure server access.
- Connected to the instance using SSH from Git Bash.

### 2. Installing and Configuring Nginx

<img width="553" height="450" alt="image" src="https://github.com/user-attachments/assets/666be861-842e-4c41-a6a2-2551e9b792e5" />


- Updated the Ubuntu package index.
- Installed Nginx and verified that the service was running.
- Created the project web directory:

  ```bash
  sudo mkdir /var/www/projectLEMP
  ```

- Configured the Nginx server block for the project.
- Enabled the site and tested the configuration.
- Verified that Nginx was listening on port 80.
- Tested the web server using a browser and cURL.

### 3. Installing and Securing MySQL

<img width="609" height="362" alt="image" src="https://github.com/user-attachments/assets/ab908735-7595-438d-82da-cf1f72d3ba02" />


- Installed the MySQL database server.
- Accessed the MySQL command-line interface.
- Configured database authentication and password validation.
- Created the `example_database` database.
- Created the `example_user` database account.
- Granted the user privileges on the project database.

### 4. Installing PHP and PHP-FPM

<img width="554" height="315" alt="image" src="https://github.com/user-attachments/assets/75cdf622-8669-423d-af0d-37a1914d2131" />


Installed PHP-FPM and the MySQL integration package:

```bash
sudo apt install php-fpm php-mysql
```

- Configured Nginx to process PHP requests through PHP-FPM.
- Created a temporary `info.php` file to test PHP processing.
- Verified PHP functionality through the browser.
- Removed the PHP information file after testing.

### 5. Database Integration

<img width="491" height="192" alt="image" src="https://github.com/user-attachments/assets/b8221ded-07e0-45bd-9c3c-31908461f20e" />

<img width="257" height="270" alt="image" src="https://github.com/user-attachments/assets/3d220e41-6bb5-4f8e-b0ee-5f2180825495" />


- Created a `todo_list` table in `example_database`.
- Inserted sample records into the table.
- Used SQL queries to verify stored records.
- Connected the PHP application to the MySQL database.
- Retrieved database records through PHP.

## Testing and Verification

The following checks were performed during the project:

| Component | Verification |
|---|---|
| EC2 | Instance launched and SSH connection established |
| Nginx | Service status and HTTP response checked |
| Nginx configuration | Configuration syntax tested using `nginx -t` |
| PHP-FPM | PHP test file accessed through the browser |
| MySQL | Database and user access verified |
| Database operations | Records inserted and retrieved using SQL |
| PHP and MySQL integration | Database data displayed through PHP |

## Troubleshooting and Learning

During implementation, I encountered and resolved command syntax errors, corrected Nginx symbolic-link configuration, and addressed a MySQL authentication plugin compatibility issue.

These troubleshooting activities helped me practise Linux command-line administration, service configuration, database access management, and application-layer integration.

##  Project Outcome

Successfully configured and tested a LEMP stack environment on AWS EC2.

The completed implementation demonstrated:

- Nginx serving web content.
- PHP scripts processed through PHP-FPM.
- MySQL database and user configuration.
- Database record insertion and retrieval.
- Integration of Nginx, PHP, and MySQL to serve dynamic content.

## Skills Demonstrated

- Linux server administration
- AWS EC2 provisioning
- SSH remote access
- Nginx configuration and troubleshooting
- MySQL database and user management
- PHP-FPM configuration
- SQL data manipulation
- Web server and database integration
- Technical troubleshooting and documentation

## Author

**Precious Samongoe**

GitHub: [@Pree2003](https://github.com/Pree2003)

Commit changes
