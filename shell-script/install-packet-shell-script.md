#!/bin/bash
# ================================================================
# Script Name: setup_demo.sh
# Description: Demonstrates basic Linux operations, script creation,
#              permissions, backups, and Docker setup.
# Author: Sayujjata Malvade
# ================================================================

set -e  # Exit immediately if a command exits with a non-zero status

# ------------------------------
# 1. Change to scripts directory
# ------------------------------
cd ~/scripts || { echo "❌ scripts directory not found"; exit 1; }

# ------------------------------
# 2. Verify bash and sh interpreters
# ------------------------------
echo "👉 Checking interpreters..."
which bash
which sh

# ------------------------------
# 3. Create/Edit hello.sh
# ------------------------------
echo "👉 Creating hello.sh..."
cat > hello.sh <<'EOF'
#!/bin/bash
echo "Hello, World! 🎉"
EOF

chmod 774 hello.sh
./hello.sh

# ------------------------------
# 4. Create/Edit variables.sh
# ------------------------------
echo "👉 Creating variables.sh..."
cat > variables.sh <<'EOF'
#!/bin/bash
NAME="Sayujjata"
ROLE="DevOps Engineer"
echo "User: $NAME | Role: $ROLE"
EOF

chmod 774 variables.sh
./variables.sh

# ------------------------------
# 5. Create install_package.sh
# ------------------------------
echo "👉 Creating install_package.sh..."
cat > install_package.sh <<'EOF'
#!/bin/bash
# Usage: ./install_package.sh <package_name>
PKG=$1
if [ -z "$PKG" ]; then
  echo "❌ No package specified"
  exit 1
fi

echo "🔄 Installing package: $PKG"
sudo apt-get update -y
sudo apt-get install -y "$PKG"
EOF

chmod 774 install_package.sh

# Run for different packages
./install_package.sh docker.io
./install_package.sh ssh
./install_package.sh tree

# ------------------------------
# 6. Directory structure check
# ------------------------------
echo "👉 Checking directory structure..."
tree /home/ubuntu || echo "tree not installed"

# ------------------------------
# 7. Create demo.sh
# ------------------------------
echo "👉 Creating demo.sh..."
cat > demo.sh <<'EOF'
#!/bin/bash
echo "This is a demo script!"
EOF

chmod 774 demo.sh
./demo.sh

# ------------------------------
# 8. Create backup archive
# ------------------------------
echo "👉 Creating backup..."
cd ..
zip -r backup.zip ~/scripts
unzip -o backup.zip

# ------------------------------
# 9. Create backup.sh
# ------------------------------
cd ~/scripts
echo "👉 Creating backup.sh..."
cat > backup.sh <<'EOF'
#!/bin/bash
SRC_DIR=$1
DEST_DIR=~/backup

if [ -z "$SRC_DIR" ]; then
  echo "❌ Usage: ./backup.sh <source_directory>"
  exit 1
fi

mkdir -p "$DEST_DIR"
cp -r "$SRC_DIR" "$DEST_DIR"

echo "✅ Backup completed! Files copied to $DEST_DIR"
EOF

chmod 774 backup.sh
./backup.sh ~/scripts

# ------------------------------
# 10. Docker Setup
# ------------------------------
echo "👉 Setting up Docker..."
sudo apt-get update -y
sudo apt-get install -y docker.io

echo "👉 Running MySQL container..."
docker run -d --name mysql -e MYSQL_ROOT_PASSWORD=root mysql:latest

# ------------------------------
# Script Completed
# ------------------------------
echo "🎯 Script execution completed successfully!"
