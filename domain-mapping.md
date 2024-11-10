# Commands and Explanations

- `cat /etc/hosts`
  - Displays the content of the `/etc/hosts` file. This file is used to map hostnames to IP addresses on your system.

- `vim etc/hosts`
  - Opens the `etc/hosts` file in `vim`, a text editor. If `etc/hosts` doesn’t exist, this will create a new file in the current directory.

- `sudo vim /etc/hosts`
  - Opens the `/etc/hosts` file with `sudo` (superuser) privileges in `vim`. This allows you to edit the file, as it usually requires root permissions.

- `curl -l localhost:80`
  - Sends a `curl` request to `localhost` on port 80. `localhost` typically represents the local machine, and this command checks if there’s a web server running on port 80.
