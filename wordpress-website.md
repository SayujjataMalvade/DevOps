sudo apt-get update
This command updates the package list for Ubuntu or Debian, ensuring that the latest versions of packages and their dependencies are available for installation.

sudo apt install apache2
Installs Apache, a popular web server software. Apache2 is essential for hosting websites or web applications.

sudo apt install php libapache2-mod-php php-mysql
Installs PHP, along with the necessary modules for Apache to interpret PHP code (libapache2-mod-php) and a module for MySQL interaction (php-mysql). PHP is a server-side scripting language used to build dynamic web pages.

sudo apt install mysql-server
Installs MySQL Server, a relational database management system used to store data for web applications.

ls
Lists the contents of the current directory. This is often used to check files or directories in the current location.

ls -l
Lists the contents of the directory in a long format, showing permissions, owner, size, and modification time for each file and directory.

sudo mysql -u root
Opens the MySQL command-line interface as the root user, allowing administrative access to the MySQL database.

clear
Clears the terminal screen for easier readability.

cd /tem and cd /tmp
Navigates to the /tem and /tmp directories. /tmp is a temporary directory often used for temporary storage by system processes.

wget https://wordpress.org/latest.tar.gz
Downloads the latest WordPress package in compressed .tar.gz format from the official WordPress site.

tar -xvf latest.tar.gz
Extracts the downloaded WordPress package. The options mean:

x: extract
v: verbose output
f: specify the filename
sudo mv wordpress/ /var/www/html/
Moves the extracted WordPress folder to /var/www/html/, the default web directory for Apache. This makes WordPress accessible from the web server.

cd /var/www/html/
Changes the current directory to /var/www/html/, where WordPress files have been placed.

cd wordpress/
Navigates into the WordPress directory, preparing for configuration edits.

nano wp-config.php and vim wp-config.php
Opens the wp-config.php file (the main configuration file for WordPress) in editors (nano and vim) to configure database settings, security keys, etc.

cd /etc/apache2/sites-available/
Changes to the directory where Apache stores configuration files for different websites or virtual hosts.

vim 000-default.conf and sudo vim 000-default.conf
Opens the default Apache configuration file for editing. This file controls the default website settings, including the document root, logging, and more.

sudo systemctl restart apache2
Restarts the Apache service to apply configuration changes. This is necessary after any modification in the Apache configuration files.

cat /etc/hosts
Displays the content of the /etc/hosts file, which maps hostnames to IP addresses. This file can be edited to configure local DNS-like entries.
