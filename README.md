# Ubuntu Commands Cheat Sheet for DevOps Engineers
This guide covers essential Ubuntu commands tailored for DevOps engineers, from basic system navigation to advanced Docker and Kubernetes management. It's designed to help streamline your workflow and get you productive in a DevOps environment quickly.

# Table of Contents:
1. Basic Ubuntu Commands
2. File and Directory Management
3. User and Permission Management
4. Networking Commands
5. System Monitoring and Management
6. Package Management
7. Services and Daemon Management
8. Docker Commands
9. Kubernetes Commands
10. CI/CD Pipeline Commands



1. Basic Ubuntu Commands
bash
Copy code
# Update and upgrade the system packages
sudo apt update && sudo apt upgrade -y

# Display current directory path
pwd

# List files and directories (detailed view)
ls -al

# Create a new directory
mkdir <directory_name>

# Navigate to a directory
cd <directory_path>

# Check disk space usage
df -h

# Check free memory and swap
free -h

# Clear the terminal screen
clear
2. File and Directory Management
bash
Copy code
# Create a new file
touch <filename>

# View contents of a file
cat <filename>

# Edit a file with nano
nano <filename>

# Move or rename a file/directory
mv <source> <destination>

# Copy a file
cp <source> <destination>

# Delete a file
rm <filename>

# Recursively delete a directory
rm -r <directory_name>

# View the last 10 lines of a file
tail <filename>

# View the first 10 lines of a file
head <filename>
3. User and Permission Management
bash
Copy code
# Create a new user
sudo adduser <username>

# Delete a user
sudo deluser <username>

# Add user to sudo group
sudo usermod -aG sudo <username>

# Change file ownership
sudo chown <user>:<group> <file_or_directory>

# Modify file permissions
chmod 755 <file_or_directory>

# Switch to another user
su - <username>
4. Networking Commands
bash
Copy code
# Display current network configuration
ifconfig

# Check network connectivity
ping <hostname_or_ip>

# Show routing table
route -n

# Check open ports on the system
sudo netstat -tuln

# Display DNS information
nslookup <domain_name>

# Trace the route packets take to a network host
traceroute <hostname_or_ip>

# List open network connections
sudo lsof -i

# Test a specific port (e.g., 80)
telnet <hostname> 80
5. System Monitoring and Management
bash
Copy code
# Check system uptime
uptime

# View active processes
top

# View memory usage
htop

# List running processes (detailed)
ps aux

# Terminate a process by PID
kill <PID>

# Reboot the system
sudo reboot

# Shut down the system
sudo shutdown -h now

# Check system logs
sudo tail -f /var/log/syslog
6. Package Management
bash
Copy code
# Search for a package
sudo apt search <package_name>

# Install a package
sudo apt install <package_name>

# Remove a package
sudo apt remove <package_name>

# Purge (remove config files too)
sudo apt purge <package_name>

# List installed packages
dpkg -l

# Check details of a specific package
apt-cache show <package_name>
7. Services and Daemon Management
bash
Copy code
# Start a service
sudo systemctl start <service_name>

# Stop a service
sudo systemctl stop <service_name>

# Restart a service
sudo systemctl restart <service_name>

# Enable a service to start at boot
sudo systemctl enable <service_name>

# Disable a service from starting at boot
sudo systemctl disable <service_name>

# Check the status of a service
sudo systemctl status <service_name>
8. Docker Commands
bash
Copy code
# Install Docker (Ubuntu)
sudo apt install docker.io

# Check Docker version
docker --version

# Start Docker service
sudo systemctl start docker

# Run a container
docker run -d -p 8080:80 --name <container_name> <image_name>

# List running containers
docker ps

# Stop a running container
docker stop <container_name>

# Remove a container
docker rm <container_name>

# Pull an image from Docker Hub
docker pull <image_name>

# Push an image to a repository
docker push <repository_name>/<image_name>
9. Kubernetes Commands
bash
Copy code
# Install Minikube (local Kubernetes)
sudo apt install minikube

# Start Minikube
minikube start

# Display cluster information
kubectl cluster-info

# Get a list of running pods
kubectl get pods

# Create a deployment
kubectl create deployment <deployment_name> --image=<image_name>

# Expose deployment as a service
kubectl expose deployment <deployment_name> --port=80 --target-port=8080

# Scale a deployment
kubectl scale deployment <deployment_name> --replicas=3

# Delete a deployment
kubectl delete deployment <deployment_name>
10. CI/CD Pipeline Commands
Git Commands
bash
Copy code
# Clone a Git repository
git clone <repository_url>

# Check the status of the repository
git status

# Add changes to the staging area
git add <file_name_or_directory>

# Commit changes
git commit -m "commit message"

# Push changes to remote repository
git push origin <branch_name>

# Pull the latest changes from a remote repository
git pull origin <branch_name>
Jenkins Commands (CLI)
bash
Copy code
# Start Jenkins
sudo systemctl start jenkins

# Stop Jenkins
sudo systemctl stop jenkins

# List installed plugins
java -jar jenkins-cli.jar -s http://localhost:8080/ list-plugins

# Trigger a Jenkins job
java -jar jenkins-cli.jar -s http://localhost:8080/ build <job_name>
