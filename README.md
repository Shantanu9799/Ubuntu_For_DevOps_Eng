# Ubuntu Commands Cheat Sheet for DevOps Engineers
This guide covers essential Ubuntu commands tailored for DevOps engineers, from basic system navigation to advanced Docker and Kubernetes management. It's designed to help streamline your workflow and get you productive in a DevOps environment quickly.

## Table of Contents:
1. [Basic Ubuntu Commands](#basic-ubuntu-commands)
2. [File and Directory Management](#file-and-directory-management)
3. [User and Permission Management](#user-and-permission-management)
4. [Networking Commands](#networking-commands)
5. [System Monitoring and Management](#system-monitoring-and-management)
6. [Package Management](#package-management)
7. [Services and Daemon Management](#services-and-daemon-management)
8. [Docker Commands](#docker-commands)
9. [Kubernetes Commands](#kubernetes-commands)
10. [CI/CD Pipeline Commands](#cicd-pipeline-commands)



## 1. Basic Ubuntu Commands

### Update and upgrade the system packages
```bash
sudo apt update && sudo apt upgrade -y
```

### Display current directory path
```bash
pwd

### List files and directories (detailed view)
```bash
ls -al

Create a new directory
```bash
mkdir <directory_name>

Navigate to a directory
```bash
cd <directory_path>

Check disk space usage
```bash
df -h

Check free memory and swap
```bash
free -h

Clear the terminal screen
```bash
clear



## 2. File and Directory Management

Create a new file
```bash
touch <filename>

View contents of a file
```bash
cat <filename>

Edit a file with nano
```bash
nano <filename>

Move or rename a file/directory
```bash
mv <source> <destination>

Copy a file
```bash
cp <source> <destination>

Delete a file
```bash
rm <filename>

Recursively delete a directory
```bash
rm -r <directory_name>

View the last 10 lines of a file
```bash
tail <filename>

View the first 10 lines of a file
```bash
head <filename>



## 3. User and Permission Management

Create a new user
```bash
sudo adduser <username>

Delete a user
```bash
sudo deluser <username>

Add user to sudo group
```bash
sudo usermod -aG sudo <username>

Change file ownership
```bash
sudo chown <user>:<group> <file_or_directory>

Modify file permissions
```bash
chmod 755 <file_or_directory>

Switch to another user
```bash
su - <username>



# 4. Networking Commands

Display current network configuration
```bash
ifconfig

Check network connectivity
```bash
ping <hostname_or_ip>

Show routing table
```bash
route -n

Check open ports on the system
```bash
sudo netstat -tuln

Display DNS information
```bash
nslookup <domain_name>

Trace the route packets take to a network host
```bash
traceroute <hostname_or_ip>

List open network connections
```bash
sudo lsof -i

Test a specific port (e.g., 80)
```bash
telnet <hostname> 80



# 5. System Monitoring and Management

Check system uptime
```bash
uptime

View active processes
```bash
top

View memory usage
```bash
htop

List running processes (detailed)
```bash
ps aux

Terminate a process by PID
```bash
kill <PID>

Reboot the system
```bash
sudo reboot

Shut down the system
```bash
sudo shutdown -h now

Check system logs
```bash
sudo tail -f /var/log/syslog



## 6. Package Management

Search for a package
```bash
sudo apt search <package_name>

Install a package
```bash
sudo apt install <package_name>

Remove a package
```bash
sudo apt remove <package_name>

Purge (remove config files too)
```bash
sudo apt purge <package_name>

List installed packages
```bash
dpkg -l

Check details of a specific package
```bash
apt-cache show <package_name>



# 7. Services and Daemon Management

Start a service
```bash
sudo systemctl start <service_name>

Stop a service
```bash
sudo systemctl stop <service_name>

Restart a service
```bash
sudo systemctl restart <service_name>

Enable a service to start at boot
```bash
sudo systemctl enable <service_name>

Disable a service from starting at boot
```bash
sudo systemctl disable <service_name>

Check the status of a service
```bash
sudo systemctl status <service_name>



## 8. Docker Commands

Install Docker (Ubuntu)
```bash
sudo apt install docker.io

Check Docker version
```bash
docker --version

Start Docker service
```bash
sudo systemctl start docker

Run a container
```bash
docker run -d -p 8080:80 --name <container_name> <image_name>

List running containers
```bash
docker ps

Stop a running container
```bash
docker stop <container_name>

Remove a container
```bash
docker rm <container_name>

Pull an image from Docker Hub
```bash
docker pull <image_name>

Push an image to a repository
```bash
docker push <repository_name>/<image_name>
```


## 9. Kubernetes Commands

### Install Minikube (local Kubernetes)
```bash
sudo apt install minikube
```
### Start Minikube
```bash
minikube start
```
### Display cluster information
```bash
kubectl cluster-info
```
### Get a list of running pods
```bash
kubectl get pods
```
### Create a deployment
```bash
kubectl create deployment <deployment_name> --image=<image_name>
```
### Expose deployment as a service
```bash
kubectl expose deployment <deployment_name> --port=80 --target-port=8080
```
### Scale a deployment
```bash
kubectl scale deployment <deployment_name> --replicas=3
```
### Delete a deployment
```bash
kubectl delete deployment <deployment_name>
```


## 10. CI/CD Pipeline Commands
    
## Git Commands
### Clone a Git repository
```bash
git clone <repository_url>
```
### Check the status of the repository
```bash
git status
```
### Add changes to the staging area
```bash
git add <file_name_or_directory>
```
C### ommit changes
```bash
git commit -m "commit message"
```
### Push changes to remote repository
```bash
git push origin <branch_name>
```
### Pull the latest changes from a remote repository
```bash
git pull origin <branch_name>
```
## Jenkins Commands (CLI)
### Start Jenkins
```bash
sudo systemctl start jenkins
```
### Stop Jenkins
```bash
sudo systemctl stop jenkins
```
### List installed plugins
```bash
java -jar jenkins-cli.jar -s http://localhost:8080/ list-plugins
```
### Trigger a Jenkins job
```bash
java -jar jenkins-cli.jar -s http://localhost:8080/ build <job_name>
```
