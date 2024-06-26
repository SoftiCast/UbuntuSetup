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
