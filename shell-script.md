# Change directory to 'scripts' folder
cd scripts/

# Check the path for bash and sh interpreters
which bash
which sh

# Clear the terminal screen
clear

# List files in the current directory
ls

# Open or create 'hello.sh' in vim (a text editor)
vim hello.sh

# Display the contents of 'hello.sh'
cat hello.sh

# List files in long format and include hidden files (-la)
ls -la

# List files in long format (-l)
ls -l

# Change permissions of 'hello.sh' to read/write/execute for owner, group, and read-only for others
chmod 774 hello.sh

# Execute the 'hello.sh' script
./hello.sh

# Open 'variables.sh' in vim
vim variables.sh

# Change permissions of 'variables.sh' to allow execution
chmod 774 variables.sh

# Execute 'variables.sh' script
./variables.sh

# Open 'install_ngnix.sh' in vim (to edit or create it)
vim install_ngnix.sh

# Set executable permissions for 'install_ngnix.sh'
chmod 774 install_ngnix.sh

# Run the 'install_ngnix.sh' script
./install_ngnix.sh

# Rename 'install_ngnix.sh' to 'install_package.sh'
mv install_ngnix.sh install_packge.sh
mv install_packge.sh install_package.sh

# Open 'install_package.sh' in vim
vim install_package.sh

# Run 'install_package.sh' with 'docker.io' as an argument
./install_package.sh docker.io

# Run 'install_package.sh' with 'ssh' as an argument
./install_package.sh ssh

# Run 'install_package.sh' with 'tree' as an argument
./install_package.sh tree

# Check directory structure in '/home/ubuntu'
tree /home/ubuntu

# Open or create 'demo.sh' in vim
vim demo.sh

# Change permissions of 'demo.sh' to make it executable
chmod 774 demo.sh

# Execute the 'demo.sh' script
./demo.sh

# Print working directory
pwd

# Change directory up one level
cd ..

# Create a zip archive named 'backup.zip' from '/home/ubuntu/scripts'
zip -r backup.zip /home/ubuntu/scripts

# Unzip 'backup.zip'
unzip backup.zip

# Display current date and time
date

# Open or create 'backup.sh' in vim
vim backup.sh

# Set executable permissions for 'backup.sh'
chmod 774 backup.sh

# Run 'backup.sh' script
./backup.sh

# Grant superuser executable permissions to 'backup.sh'
sudo chmod 774 backup.sh

# Run a Docker container named 'mysql' with MySQL image
docker run -d --name mysql -e MYSQL_ROOT_PASSWORD=root mysql:latest

# Initialize Docker (if needed)
docker init

# Install Docker using apt (commands corrected in next lines)
sudo apt-get install docker

# Create a backup directory
mkdir backup

# Remove 'backup' directory and any directories named 'backups'
rm -rf backup backups

# Move into the 'backup' directory
cd backup/

# Change back to previous directory
cd ..

# Execute 'backup.sh' in '/home/ubuntu/scripts' with bash
./bash backup.sh /home/ubuntu/scripts

# Display contents of 'demo.sh'
cat demo.sh
