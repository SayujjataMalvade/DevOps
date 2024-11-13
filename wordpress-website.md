1. Update and Install Packages
sudo apt-get update
Updates the package list to ensure all software and dependencies are current.

sudo apt install apache2
Installs the Apache web server.

sudo apt install php libapache2-mod-php php-mysql
Installs PHP, along with the Apache module for PHP, and PHP-MySQL module to interact with MySQL.

sudo apt install mysql-server
Installs the MySQL database server.

2. Directory Navigation and Basic Commands
ls
Lists the contents of the current directory.

ls -l
Lists directory contents in long format, showing detailed file information.

clear
Clears the terminal screen.

3. MySQL Setup
sudo mysql -u root
Opens MySQL in the terminal as the root user, allowing direct access to the MySQL database.
4. Download and Extract WordPress
cd /tem
Changes directory to /tem.

cd /tmp
Changes directory to /tmp, commonly used for temporary files.

wget https://wordpress.org/latest.tar.gz
Downloads the latest WordPress version in a compressed format.

tar -xvf latest.tar.gz
Extracts the WordPress files from the downloaded archive.

5. Move WordPress Files
sudo mv wordpress/ /var/www/html/
Moves the extracted WordPress directory to Apache’s web root.
6. Navigate to WordPress Directory
cd /var/www/html/
Changes directory to the Apache root directory.

cd wordpress/
Navigates into the WordPress directory for further configuration.

7. Edit WordPress Configuration File
nano wp-config.php
Opens the wp-config.php file in the Nano text editor to configure WordPress settings.

vim wp-config.php
Opens wp-config.php in the Vim editor as an alternative.

8. Edit Apache Configuration for WordPress Site
cd /etc/apache2/sites-available/
Changes to the Apache directory where virtual host configurations are stored.

vim 000-default.conf
Opens the default Apache configuration file for editing.

sudo vim 000-default.conf
Opens 000-default.conf with sudo privileges to make necessary changes.

9. Restart Apache to Apply Changes
sudo systemctl restart apache2
Restarts Apache to apply the new configurations.
10. Verify Host Configurations
cat /etc/hosts
Displays the contents of the /etc/hosts file, used to map hostnames to IP addresses.
