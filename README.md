# Setting Up Ubuntu for Development

## Prerequisites

Before you begin, make sure you have the following:

- An Ubuntu system (16.04 LTS or later)
- An internet connection
- A GitHub account

## Step 1: Update and Upgrade Your System

First, update and upgrade your system packages to the latest versions.

```bash
sudo apt update
sudo apt upgrade -y
```

## Step 2: Install Git

Git is essential for cloning repositories and version control. Install Git using the following command:

```bash
sudo apt install git -y
```
Verify Installation
```bash
git --version

```

## Step 3: Configure Git

Set up your Git configuration with your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
## Step 4: Generate SSH Keys (Optional)

For secure authentication with GitHub, generate an SSH key:

```bash
ssh-keygen -t rsa -b 4096 -C "your.email@example.com"
```
Add your SSH key to the SSH agent:
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```
Copy the SSH key to your clipboard:
```
cat ~/.ssh/id_rsa.pub
```
## Step 5: Install Required Software

Depending on your project's requirements, install the necessary software. Common examples include:

### Python

If your project uses Python, install Python and pip:

```bash
sudo apt install python3 python3-pip -y
```
### Node.js

If your project uses Node.js, install Node.js and npm (Node Package Manager):

```bash
sudo apt install nodejs npm -y
```

### Docker

If your project uses Docker, install Docker:

```bash
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
```
Add your user to the Docker group:
```
sudo usermod -aG docker $USER
```
## Battery Optimization

Improving battery life on Ubuntu can be achieved through several optimizations:

### 1. Reduce Screen Brightness

Lowering screen brightness can significantly extend battery life. Adjust brightness using the system settings or function keys on your keyboard.

### 2. Use Power Saving Modes

Ubuntu offers power-saving modes that adjust system settings to conserve battery. Switch to a power-saving mode through the system settings.

### 3. Manage Startup Applications

Disable unnecessary startup applications to reduce system load and battery consumption. Use the "Startup Applications" utility to manage startup items.

### 4. Install TLP 

TLP is an advanced power management tool for Linux that can optimize battery life further. Install TLP with:

```bash
sudo apt install preload
sudo apt install tlp tlp-rdw
```
