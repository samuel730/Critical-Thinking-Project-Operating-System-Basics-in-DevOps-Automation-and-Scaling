# Operating System Basics for DevOps Automation and Scaling

## Project Overview

This lab introduces foundational operating system concepts required for DevOps engineering. It focuses on comparing Linux and Windows, mastering essential Linux command-line operations, and implementing user management and file permissions for secure system administration.

You will simulate real-world DevOps tasks such as server navigation, automation preparation, and access control configuration in a Linux environment.

---

## Author

**Name:** Samuel Adesanya

**Course:** Linux Administration 

**Environment:** Ubuntu Linux / Windows Subsystem for Linux (WSL)

---

# Task 1: Linux vs Windows for DevOps Automation

## Objective

Evaluate Linux and Windows in terms of scripting, automation, package management, and container support, and recommend the best OS for DevOps workflows.

## Comparison Table

| Feature            | Linux                                            | Windows                                         |
| ------------------ | ------------------------------------------------ | ----------------------------------------------- |
| Scripting          | Bash scripting (highly efficient for automation) | PowerShell (powerful but less common in DevOps) |
| Package Management | apt, yum, dnf (fast and simple)                  | winget, Chocolatey (less standardized)          |
| Container Support  | Native Docker and Kubernetes support             | Requires WSL2 or Hyper-V                        |
| Performance        | Lightweight and efficient                        | Heavier resource usage                          |
| Server Usage       | Industry standard for servers                    | Mostly enterprise desktop/server hybrid         |

## Analysis

Linux provides a highly flexible environment for DevOps tasks. Its strong shell scripting capabilities allow automation of repetitive tasks, while its package managers simplify software installation and updates. Additionally, Linux is the preferred OS for containerized applications and orchestration tools like Docker and Kubernetes.

Windows, while powerful in enterprise environments, relies heavily on GUI tools and has less native support for containerized workloads.

## Conclusion

Linux is the most suitable operating system for DevOps automation due to its lightweight nature, scripting efficiency, and strong ecosystem support for containers and server-side applications.

---

# Task 2: Linux Command-Line Guide

## Objective

Learn and document essential Linux commands used in system navigation, file management, and DevOps automation.

---

## 1. ls Command

**Purpose:** Lists files and directories
**Why it is useful:** Helps view contents of a directory
**DevOps use case:** Checking deployed application files on servers

```bash
ls -l
```

---

## 2. cd Command

**Purpose:** Changes directory
**Why it is useful:** Allows navigation through the file system
**DevOps use case:** Moving into project or deployment folders

```bash
cd /var/www/html
```

---

## 3. mkdir Command

**Purpose:** Creates a new directory
**Why it is useful:** Organizes files and projects
**DevOps use case:** Creating deployment or project folders

```bash
mkdir devops-project
```

---

## 4. cat Command

**Purpose:** Displays file contents
**Why it is useful:** Reads configuration or log files
**DevOps use case:** Viewing server logs or config files

```bash
cat config.txt
```

---

## 5. rm Command

**Purpose:** Deletes files or directories
**Why it is useful:** Removes unwanted files
**DevOps use case:** Cleaning up old builds or logs

```bash
rm oldfile.txt
```

**Warning:** Use with caution as deleted files may not be recoverable.

---

# Task 3: User Management and Permissions

## Objective

Understand Linux user management and file permissions for improving system security in DevOps environments.

---

## 👤 Step 1: Create a New User

```bash
sudo adduser devopsuser
```

Creates a new user called `devopsuser`.

---

## Step 2: Switch User (Optional)

```bash
su - devopsuser
```

Used to log in as the newly created user.

---

## Step 3: Create a File

```bash
touch file1.txt
```

Creates a new empty file.

---

## Step 4: Check File Permissions

```bash
ls -l file1.txt
```

Example output:

```
-rw-r--r-- 1 devopsuser devopsuser 0 May 25 10:00 file1.txt
```

---

## Step 5: Modify Permissions

```bash
chmod 700 file1.txt
```

### Permission Meaning:

* Owner: read, write, execute
* Group: no access
* Others: no access

---

## Step 6: Understand Ownership

```bash
ls -l
```

Shows:

* File owner
* Group owner
* Permission settings

---

## Security Explanation

User management and file permissions are critical in DevOps environments. They ensure only authorized users can access or modify sensitive files such as configuration files, deployment scripts, and logs. This improves system security and prevents unauthorized changes.

---

# Final Notes

This lab demonstrates core Linux skills essential for DevOps automation, including OS selection, command-line usage, and access control. These skills form the foundation for CI/CD, configuration management, and infrastructure automation.

