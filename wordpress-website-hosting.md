# LAMP Stack and WordPress Installation Guide

This guide provides the commands to install and configure the LAMP stack (Linux, Apache, MySQL, PHP) and set up WordPress.

## 1. Update and Install Packages

- **`sudo apt-get update`**  
  Updates the package list to ensure that all software and dependencies are current.

- **`sudo apt install apache2`**  
  Installs Apache, a popular web server software necessary for hosting websites or web applications.

- **`sudo apt install php libapache2-mod-php php-mysql`**  
  Installs PHP, the Apache PHP module (`libapache2-mod-php`), and a module to connect PHP with MySQL databases (`php-mysql`).

- **`sudo apt install mysql-server`**  
  Installs MySQL Server, a relational database management system used to store website or application data.

## 2. Directory Navigation and Basic Commands

- **`ls`**  
  Lists the contents of the current directory, useful for checking files and folders.

- **`ls -l`**  
  Lists directory contents in a long, detailed format, showing permissions, owner, size, and modification time.

- **`clear`**  
  Clears the terminal screen for easier readability.

## 3. MySQL Setup

- **`sudo mysql -u root`**  
  Opens the MySQL command-line interface as the root user, granting administrative access to MySQL databases.

## 4. Download and Extract WordPress

- **`cd /tem`**  
  Changes the directory to `/tem`. This might be a typo; commonly, it would be `/tmp`.

- **`cd /tmp`**  
  Navigates to the `/tmp` directory, used for temporary file storage.

- **`wget https://wordpress.org/latest.tar.gz`**  
  Downloads the latest WordPress package in compressed format from the official WordPress website.

- **`tar -xvf latest.tar.gz`**  
  Extracts the downloaded WordPress archive. Options used:
  - `x`: extract
  - `v`: verbose output
  - `f`: specify filename

## 5. Move WordPress Files

- **`sudo mv wordpress/ /var/www/html/`**  
  Moves the extracted WordPress directory to Apache’s web root (`/var/www/html/`), making it accessible through the web server.

## 6. Navigate to WordPress Directory

- **`cd /var/www/html/`**  
  Changes the directory to the Apache root directory.

- **`cd wordpress/`**  
  Navigates into the WordPress directory for further setup.

## 7. Edit WordPress Configuration File

- **`nano wp-config.php`**  
  Opens the `wp-config.php` file in the Nano text editor to configure WordPress settings, such as database credentials and security keys.

- **`vim wp-config.php`**  
  Opens the same `wp-config.php` file in the Vim editor as an alternative.

## 8. Edit Apache Configuration for WordPress Site

- **`cd /etc/apache2/sites-available/`**  
  Changes to the directory where Apache stores configuration files for virtual hosts.

- **`vim 000-default.conf`**  
  Opens the default Apache configuration file, `000-default.conf`, for editing.

- **`sudo vim 000-default.conf`**  
  Opens the same file with root privileges, enabling modifications to Apache settings.

## 9. Restart Apache to Apply Changes

- **`sudo systemctl restart apache2`**  
  Restarts Apache to apply any configuration changes, making them effective immediately.

## 10. Verify Host Configurations

- **`cat /etc/hosts`**  
  Displays the contents of the `/etc/hosts` file, used to map hostnames to IP addresses locally.

---

By following these commands and instructions, you will have successfully installed and configured a LAMP stack and WordPress on your server.
